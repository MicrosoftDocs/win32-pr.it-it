---
description: Le costanti seguenti, definite in Gdipluspixelformats. h, specificano vari formati pixel utilizzati nelle bitmap.
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: Costanti di formato pixel immagine (Gdipluspixelformats. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62abc8b0ed606b958764e27171f8b45e619d23b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982883"
---
# <a name="image-pixel-format-constants"></a>Costanti formato pixel immagine

Le costanti seguenti, definite in Gdipluspixelformats. h, specificano vari formati pixel utilizzati nelle bitmap.



| Costante                                                                                                                                                                                                                                     | Descrizione                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | Specifica che il formato è 1 bit per pixel, indicizzato.<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | Specifica che il formato è di 4 bit per pixel indicizzati.<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | Specifica che il formato è 8 bit per pixel, indicizzati.<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | Specifica che il formato è di 16 bit per pixel; 1 bit viene utilizzato per il componente alfa e 5 bit vengono utilizzati per i componenti rosso, verde e blu.<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | Specifica che il formato è di 16 bit per pixel, di scala di grigi.<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | Specifica che il formato è di 16 bit per pixel; 5 bit per i componenti rosso, verde e blu. L'altro bit non viene utilizzato.<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | Specifica che il formato è di 16 bit per pixel: 5 bit sono utilizzati per il componente rosso, 6 bit per il componente verde e 5 per il componente blu.<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | Specifica che il formato è 24 bit per pixel, 8 bit per ogni componente, rosso, verde e blu.<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | Specifica che il formato è di 32 bit per pixel; per i componenti alfa, rosso, verde e blu sono utilizzati 8 bit ciascuno.<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | Specifica che il formato è di 32 bit per pixel; per i componenti alfa, rosso, verde e blu sono utilizzati 8 bit ciascuno. I componenti rosso, verde e blu vengono premoltiplicati in base al componente alfa.<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | Specifica che il formato è 32 bit per pixel, 8 bit per ogni componente, rosso, verde e blu. I rimanenti 8 bit non vengono utilizzati.<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | Specifica che il formato è 48 bit per pixel, 16 bit per ogni componente, rosso, verde e blu.<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | Specifica che il formato è 64 bit per pixel, 16 bit per ogni componente, alfa, rosso, verde e blu.<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | Specifica che il formato è 64 bit per pixel, 16 bit per ogni componente, alfa, rosso, verde e blu. I componenti rosso, verde e blu vengono premoltiplicati in base al componente alfa. <br/> |



## <a name="remarks"></a>Commenti

**PixelFormat48bppRGB**, **PixelFormat64bppARGB** e **PixelFormat64bppPARGB** utilizzano 16 bit per ogni componente colore (canale). Windows GDI+ versione 1,0 è in grado di leggere immagini a 16 bit per canale, ma tali immagini vengono convertite in un formato a 8 bit per canale per l'elaborazione, la visualizzazione e il salvataggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Gdipluspixelformats. h</dt> </dl> |



 

 




