---
description: I sottotipi seguenti definiscono formati RGB non compressi senza canale alfa.
ms.assetid: 49c91c8c-6889-48c6-8fa5-84929c03d951
title: Sottotipi video RGB non compressi (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e04237a61fa91f4fe648dcb7743c893604adbe7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331429"
---
# <a name="uncompressed-rgb-video-subtypes"></a>Sottotipi video RGB non compressi

I sottotipi seguenti definiscono formati RGB non compressi senza canale alfa.



| Costante                                                                                                                                                                        | Descrizione                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------|
| <span id="MEDIASUBTYPE_RGB1"></span><span id="mediasubtype_rgb1"></span><dl> <dt>**\_RGB1 MEDIASUBTYPE**</dt> </dl>       | RGB, 1 bit per pixel (BPP), pallettizzati<br/> |
| <span id="MEDIASUBTYPE_RGB4"></span><span id="mediasubtype_rgb4"></span><dl> <dt>**\_RGB4 MEDIASUBTYPE**</dt> </dl>       | RGB, 4 BPP, pallettizzati<br/>                 |
| <span id="MEDIASUBTYPE_RGB8"></span><span id="mediasubtype_rgb8"></span><dl> <dt>**\_RGB8 MEDIASUBTYPE**</dt> </dl>       | RGB, 8 BPP, pallettizzati<br/>                 |
| <span id="MEDIASUBTYPE_RGB555"></span><span id="mediasubtype_rgb555"></span><dl> <dt>**\_RGB555 MEDIASUBTYPE**</dt> </dl> | RGB 555, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB565"></span><span id="mediasubtype_rgb565"></span><dl> <dt>**\_RGB565 MEDIASUBTYPE**</dt> </dl> | RGB 565, 16 BPP<br/>                        |
| <span id="MEDIASUBTYPE_RGB24"></span><span id="mediasubtype_rgb24"></span><dl> <dt>**\_RGB24 MEDIASUBTYPE**</dt> </dl>    | RGB, 24 BPP<br/>                            |
| <span id="MEDIASUBTYPE_RGB32"></span><span id="mediasubtype_rgb32"></span><dl> <dt>**\_Rgb32 MEDIASUBTYPE**</dt> </dl>    | RGB, 32 BPP<br/>                            |



I sottotipi seguenti definiscono formati RGB non compressi con canale alfa.



| Costante                                                                                                                                                                                       | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| <span id="MEDIASUBTYPE_ARGB1555"></span><span id="mediasubtype_argb1555"></span><dl> <dt>**\_ARGB1555 MEDIASUBTYPE**</dt> </dl>          | RGB 555 con canale alfa<br/>                                                    |
| <span id="MEDIASUBTYPE_ARGB32"></span><span id="mediasubtype_argb32"></span><dl> <dt>**\_ARGB32 MEDIASUBTYPE**</dt> </dl>                | RGB 32 con canale alfa<br/>                                                     |
| <span id="MEDIASUBTYPE_ARGB4444"></span><span id="mediasubtype_argb4444"></span><dl> <dt>**\_ARGB4444 MEDIASUBTYPE**</dt> </dl>          | RGB a 16 bit con canale alfa; 4 bit per canale<br/>                             |
| <span id="MEDIASUBTYPE_A2R10G10B10"></span><span id="mediasubtype_a2r10g10b10"></span><dl> <dt>**\_A2R10G10B10 MEDIASUBTYPE**</dt> </dl> | RGB a 32 bit con canale alfa; 10 bit per canale RGB più 2 bit per Alpha.<br/> |
| <span id="MEDIASUBTYPE_A2B10G10R10"></span><span id="mediasubtype_a2b10g10r10"></span><dl> <dt>**\_A2B10G10R10 MEDIASUBTYPE**</dt> </dl> | BGR a 32 bit con canale alfa; 10 bit per canale BGR più 2 bit per Alpha.<br/> |



## <a name="remarks"></a>Commenti

Per i formati pallettizzati, il colore di ogni pixel viene specificato come indice in una tavolozza. La tavolozza deve essere inclusa nel blocco di formato, dopo la struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Per i formati non pallettizzati, il colore di ogni pixel viene specificato direttamente; il layout della memoria dipende dalla profondità dei bit:

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

    

-   Per RGB 24, ogni pixel è un [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple). Ogni colore è un byte, con un valore compreso tra 0 e 255, inclusi. Il layout della memoria è: 

    |       |      |       |     |
    |-------|------|-------|-----|
    | Byte  | 0    | 1     | 2   |
    | Valore | Blu | Green | Red |

    

     

-   Per RGB 32, ogni pixel è un **RGBQUAD**. Ogni colore è un byte, con un valore compreso tra 0 e 255, inclusi. Il layout della memoria è: 

    |       |      |       |     |                     |
    |-------|------|-------|-----|---------------------|
    | Byte  | 0    | 1     | 2   | 3                   |
    | Valore | Blu | Green | Red | Alpha o non importa |

    

     

    Se il sottotipo è MEDIASUBTYPE \_ ARGB32, byte 3 contiene un valore per il canale alfa. Se il sottotipo è MEDIASUBTYPE \_ rgb32, byte 3 deve essere ignorato.

-   A2R10G10B10 usa il layout seguente: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Valore | Blu  | Green   | Red     | Alfa   |

    

     

-   A2B10G10R10 usa il layout seguente: 

    |       |       |         |         |         |
    |-------|-------|---------|---------|---------|
    | bit   | 0 - 9 | 10 - 19 | 20 - 29 | 30 - 31 |
    | Valore | Red   | Green   | Blu    | Alfa   |

    

     

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sottotipi video](video-subtypes.md)
</dt> <dt>

[Utilizzo di fotogrammi video](working-with-video-frames.md)
</dt> </dl>

 

 
