---
description: I sottotipi seguenti definiscono formati RGB non compressi senza canale alfa.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Sottotipi video RGB non compressi (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f149786c32c0734492179e2d3e75e5a7d7df969
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119246"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Sottotipi video RGB non compressi

I sottotipi seguenti definiscono formati RGB non compressi senza canale alfa.



| Costante                                                                                                                                                                        | Descrizione                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**MEDIASUBTYPE \_ RGB1**</dt> </dl>       | RGB, 1 bit per pixel (bpp), satittizzato<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**MEDIASUBTYPE \_ RGB4**</dt> </dl>       | RGB, 4 bpp, satittizzato<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**MEDIASUBTYPE \_ RGB8**</dt> </dl>       | RGB, 8 bpp, in modalità bttized<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**MEDIASUBTYPE \_ RGB555**</dt> </dl> | RGB 555, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**MEDIASUBTYPE \_ RGB565**</dt> </dl> | RGB 565, 16 bpp<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**MEDIASUBTYPE \_ RGB24**</dt> </dl>    | RGB, 24 bpp<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**MEDIASUBTYPE \_ RGB32**</dt> </dl>    | RGB, 32 bpp<br/>                            |



I sottotipi seguenti definiscono formati RGB non compressi con canale alfa.



| Costante                                                                                                                                                                                       | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB1555**</dt> </dl>          | RGB 555 con canale alfa<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB32**</dt> </dl>                | RGB 32 con canale alfa<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**MEDIASUBTYPE \_ ARGB4444**</dt> </dl>          | RGB a 16 bit con canale alfa; 4 bit per canale<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**MEDIASUBTYPE \_ A2R10G10B10**</dt> </dl> | RGB a 32 bit con canale alfa; 10 bit per canale RGB più 2 bit per alfa.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**MEDIASUBTYPE \_ A2B10G10R10**</dt> </dl> | BGR a 32 bit con canale alfa; 10 bit per canale BGR più 2 bit per alfa.<br/> |



## <a name="remarks"></a>Commenti

Per i formati svasati, il colore di ogni pixel viene specificato come indice in una tavolozza. La tavolozza deve essere inclusa nel blocco di formato, in base alla [**struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Per i formati non svasati, il colore di ogni pixel viene specificato direttamente. Il layout della memoria dipende dalla profondità in bit:

-   RGB 555 usa il layout di memoria seguente:
    ```C++
    High-order byte:    Low-order byte: 
    X R R R R R G G     G G G B B B B B 

    X = Don't care, R = Red, G = Green, B = Blue
    ```

    

-   RGB 565 usa il layout di memoria seguente:
    ```C++
    High-order byte:    Low-order byte: 
    R R R R R G G G     G G G B B B B B 
    ```

    

-   Per RGB 24, ogni pixel è un [**RGBTRIPLE.**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) Ogni colore è di un byte, con un valore compreso tra 0 e 255 inclusi. Il layout della memoria è:

    |       | Layout     | Layout      | Layout     |
    |-------|------|-------|-----|
    | **Byte**  | 0    | 1     | 2   |
    | **Valore** | Blu | Green | Red |

    

     

-   Per RGB 32, ogni pixel è un **RGBQUAD.** Ogni colore è di un byte, con un valore compreso tra 0 e 255 inclusi. Il layout della memoria è: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|------|-------|-----|---------------------|
    | **Byte**  | 0    | 1     | 2   | 3                   |
    | **Valore** | Blu | Green | Red | Alfa o non importa |

    

     

    Se il sottotipo è MEDIASUBTYPE \_ ARGB32, il byte 3 contiene un valore per il canale alfa. Se il sottotipo è MEDIASUBTYPE \_ RGB32, il byte 3 deve essere ignorato.

-   A2R10G10B10 usa il layout seguente: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **pezzo**   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | **Valore** | Blu  | Green   | Red     | Alfa   |

    

     

-   A2B10G10R10 usa il layout seguente: 

    |       | Layout     | Layout      | Layout     | Layout |
    |-------|-------|---------|---------|---------|
    | **pezzo**   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | **Valore** | Red   | Green   | Blu    | Alfa   |

    

     

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Sottotipi video](video-subtypes.md)
</dt> <dt>

[Uso dei fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 
