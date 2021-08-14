---
title: Configurazione delle immagini Flussi
description: Configurazione delle immagini Flussi
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- flussi, configurazione di flussi di immagini
- codec, configurazione di flussi di immagini
- flussi di immagini, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ce58fe3da709772b08d0956f3f5540713f7960742338f73c9d9807ad1a1e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848966"
---
# <a name="configuring-image-streams"></a>Configurazione delle immagini Flussi

I flussi di immagini contengono immagini fisse in formato JPEG. Anche se i flussi di immagini sono simili ai flussi video in quanto accettano immagini non compresse come input, richiedono una configurazione leggermente diversa. Per configurare un flusso di immagini, è necessario impostare i valori per i membri delle strutture di configurazione video, come illustrato nella tabella seguente.



| Impostazione                                                           | Descrizione                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WM \_ MEDIA \_ TYPE.majortype**                                     | Impostare su IMMAGINE \_ WMMEDIATYPE.                                                                                                                                                       |
| **WM \_ MEDIA \_ TYPE.subtype**                                       | Impostare su WMMEDIASUBTYPE \_ RGB24.                                                                                                                                                    |
| **WM \_ MEDIA \_ TYPE.bFixedSizeSamples**                             | Impostare su **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.bTemporalCompression**                          | Impostare su **FALSE.**                                                                                                                                                                |
| **WM \_ MEDIA \_ TYPE.lSampleSize**                                   | Impostare su 0.                                                                                                                                                                        |
| **WM \_ MEDIA \_ TYPE.formattype**                                    | Impostare su WMFORMAT \_ VideoInfo.                                                                                                                                                      |
| **WM \_ MEDIA \_ TYPE.pUnk**                                          | Impostare su **NULL.**                                                                                                                                                                 |
| **WM \_ MEDIA \_ TYPE.cbFormat**                                      | Impostare su `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **WM \_ MEDIA \_ TYPE.pbFormat**                                      | Impostare sull'indirizzo di una struttura **WMVIDEOINFOHEADER configurata** correttamente.                                                                                                     |
| **WMVIDEOINFOHEADER.rcSource** e **WMVIDEOINFOHEADER.rcTarget** | Impostare entrambi i rettangoli in modo che gli angoli superiori a sinistra siano coordinate (0, 0) e gli angoli inferiori a destra siano coordinate(x, y), dove x è la larghezza dell'immagine e y è l'altezza dell'immagine. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Impostare sulla velocità in bit del flusso.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Impostare su 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Impostare su 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biWidth**                                      | Impostare sulla larghezza dell'immagine.                                                                                                                                                   |
| **BITMAPINFOHEADER.biHeight**                                     | Impostare sull'altezza dell'immagine.                                                                                                                                                  |
| **BITMAPINFOHEADER.biPlanes**                                     | impostare su 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biBitCount**                                   | Impostare su 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER.biCompression**                                | Impostare su BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER.biSizeImage**                                  | Impostare su ((x y c) / 8), dove x è la larghezza dell'immagine, y è l'altezza dell'immagine e c è la profondità del colore dell'immagine (in questo caso \* \* sempre 24).                     |
| **BITMAPINFOHEADER.biXPelsPerMeter**                              | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biYPelsPerMeter**                              | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrUsed**                                    | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER.biClrImportant**                               | Impostare su 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Ottenere buoni risultati con il codec Windows media video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Immagine Flussi**](image-streams.md)
</dt> </dl>

 

 




