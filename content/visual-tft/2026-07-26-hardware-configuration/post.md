# Visual TFT 하드웨어 구성

> [!Note]
> 본 문서는 [원본 문서](https://github.com/gitgunny/gitgunny.github.io/blob/main/content/visual-tft/2026-07-26-hardware-configuration/post.md)를 기준으로 작성되었습니다.

## 하드웨어 선정

본 문서는 아래와 같은 기준으로 작성되었습니다.

```
- 디스플레이: DC80600EW070 TFT
- 하드웨어(펌웨어) 버전: 7.0.1011.0
- 소프트웨어 버전: 3.0.0.1253
```

> [!Note]
> 버전은 Visual TFT 우측 하단 화면에서 볼 수 있습니다.

### DC80600EW070 앞면

![image-1](https://cdn.jsdelivr.net/gh/gitgunny/gitgunny.github.io@main/content/visual-tft/2026-07-26-hardware-configuration/images/image-1.jpg)

### DC80600EW070 뒷면

![image-2](https://cdn.jsdelivr.net/gh/gitgunny/gitgunny.github.io@main/content/visual-tft/2026-07-26-hardware-configuration/images/image-2.jpg)

## 통신 방식 선택

DC80600EW070 TFT는 RS232와 TTL 통신 방식을 지원하며 J5 점퍼를 통해 통신 방식을 선택할 수 있습니다.

### J5 ON(Close): TTL

![image-3](https://cdn.jsdelivr.net/gh/gitgunny/gitgunny.github.io@main/content/visual-tft/2026-07-26-hardware-configuration/images/image-3.jpg)

## PC TFT 간 연결

펌웨어 다운로드와 디버깅을 위해 USB to TTL 컨버터로 PC와 연결합니다.

### USB 컨버터가 최소 3.3W 전원 공급이 가능한 경우

|PC   |USB 컨버터 핀|TFT 핀|
|:---:|:----------:|:----:|
|`USB`|`VCC`       |`VCC` |
|`USB`|`GND`       |`GND` |
|`USB`|`RX`        |`DOUT`|
|`USB`|`TX`        |`DIN` |

### USB 컨버터가 최소 3.3W 전원 공급이 불가능한 경우 별도 전원 공급

|PC   |USB 컨버터 핀|TFT 핀|
|:---:|:----------:|:----:|
|`USB`|`GND`       |`GND` |
|`USB`|`RX`        |`DOUT`|
|`USB`|`TX`        |`DIN` |

|전원 |전원 컨버터 핀|TFT 핀|
|:---:|:-----------:|:----:|
|`L/N`|`VCC`        |`VCC` |
|`GND`|`GND`        |`GND` |

> [!Note]
> 본 문서에서는 별도 전원 공급 방식으로 진행합니다.

![image-4](https://cdn.jsdelivr.net/gh/gitgunny/gitgunny.github.io@main/content/visual-tft/2026-07-26-hardware-configuration/images/image-4.jpg)