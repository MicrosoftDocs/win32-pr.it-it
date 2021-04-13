---
title: Configurazione di flussi di immagini
description: Configurazione di flussi di immagini
ms.assetid: 29325834-8766-47f4-8b33-b5fcbcc494c1
keywords:
- flussi, configurazione di flussi di immagini
- codec, configurazione di flussi di immagini
- flussi di immagini, configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b05a21474143e227257dad240ff4d4464732ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395838"
---
# <a name="configuring-image-streams"></a>Configurazione di flussi di immagini

I flussi di immagini contengono ancora immagini in formato JPEG. Anche se i flussi di immagini sono simili ai flussi video perché accettano immagini non compresse come input, richiedono una configurazione leggermente diversa. Per configurare un flusso di immagini, è necessario impostare i valori per i membri delle strutture di configurazione video, come illustrato nella tabella seguente.



| Impostazione                                                           | Descrizione                                                                                                                                                                      |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Tipo di supporto WM \_ . majortype**                                     | Impostare su WMMEDIATYPE \_ Image.                                                                                                                                                       |
| **\_Tipo di supporto WM \_ . sottotipo**                                       | Impostare su WMMEDIASUBTYPE \_ Rgb24.                                                                                                                                                    |
| **\_Tipo di supporto WM \_ . bFixedSizeSamples**                             | Impostare su **false**.                                                                                                                                                                |
| **\_Tipo di supporto WM \_ . bTemporalCompression**                          | Impostare su **false**.                                                                                                                                                                |
| **\_Tipo di supporto WM \_ . lSampleSize**                                   | Impostare su 0.                                                                                                                                                                        |
| **\_Tipo di supporto WM \_ . formatType**                                    | Impostare su WMFORMAT \_ videoinfo.                                                                                                                                                      |
| **\_Tipo di supporto WM \_ . punk**                                          | Impostare su **null**.                                                                                                                                                                 |
| **\_Tipo di supporto WM \_ . cbFormat**                                      | Impostare su `sizeof(WMVIDEOINFOHEADER)`.                                                                                                                                              |
| **\_Tipo di supporto WM \_ . pbFormat**                                      | Impostare sull'indirizzo di una struttura **WMVIDEOINFOHEADER** correttamente configurata.                                                                                                     |
| **WMVIDEOINFOHEADER. rcSource** e **WMVIDEOINFOHEADER. rcTarget** | Impostare entrambi i rettangoli in modo che gli angoli superiore sinistro siano coordinate (0, 0) e gli angoli inferiori destro siano le coordinate (x, y) dove x è la larghezza dell'immagine e y è l'altezza dell'immagine. |
| **WMVIDEOINFOHEADER.dwBitRate**                                   | Impostare sulla velocità in bit del flusso.                                                                                                                                               |
| **WMVIDEOINFOHEADER.dwErrorRate**                                 | Impostare su 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER.dwBitErrorRate**                              | Impostare su 0.                                                                                                                                                                        |
| **WMVIDEOINFOHEADER. AvgTimePerFrame**                             | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biWidth**                                      | Impostare sulla larghezza dell'immagine.                                                                                                                                                   |
| **BITMAPINFOHEADER. biHeight**                                     | Impostare sull'altezza dell'immagine.                                                                                                                                                  |
| **BITMAPINFOHEADER. Biplanes**                                     | impostare su 1.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biBitCount**                                   | Impostare su 24.                                                                                                                                                                       |
| **BITMAPINFOHEADER. biCompression**                                | Impostare su BI \_ RGB.                                                                                                                                                                  |
| **BITMAPINFOHEADER. biSizeImage**                                  | Impostare su ((x \* y \* c)/8), dove x è la larghezza dell'immagine, y è l'altezza dell'immagine e c è la profondità di colore dell'immagine (in questo caso sempre 24).                     |
| **BITMAPINFOHEADER. biXPelsPerMeter**                              | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biYPelsPerMeter**                              | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biClrUsed**                                    | Impostare su 0.                                                                                                                                                                        |
| **BITMAPINFOHEADER. biClrImportant**                               | Impostare su 0.                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Ottenere risultati soddisfacenti con il codec della schermata Windows Media Video 9**](getting-good-results-with-the-windows-media-video-9-screen-codec.md)
</dt> <dt>

[**Flussi di immagini**](image-streams.md)
</dt> </dl>

 

 




