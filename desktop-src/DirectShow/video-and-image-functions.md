---
description: Funzioni video e immagine
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funzioni video e immagine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55e439a17dd570b6e939d1cb84d836f9100eaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308963"
---
# <a name="video-and-image-functions"></a>Funzioni video e immagine

Queste funzioni e macro modificano le strutture del formato video DirectShow.



| Funzione                                                             | Descrizione                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_corrispondenza maschere di bit \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Confronta le maschere dei colori per due strutture [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                                       |
| [**MASCHERE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera le maschere dei colori da una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per gli errori che possono causare sovraccarichi del buffer o overflow di Integer.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Controlla un tipo di supporto che contiene una struttura di formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) per gli errori che possono causare sovraccarichi del buffer o overflow di Integer. |
| [**COLORI**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera le voci della tavolozza da una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina se una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) specificata contiene una tavolozza.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Converte un tipo di supporto che usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in uno che usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Restituisce il numero di bit per pixel utilizzato da un sottotipo video specificato.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcola la dimensione necessaria per una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che può ospitare una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) specificata.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Restituisce la prima voce della tavolozza in una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Restituisce il **GUID** del sottotipo di supporto per la bitmap specificata.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera il nome leggibile di un sottotipo video.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Restituisce il **GUID** del sottotipo di supporto per una bitmap RGB non compressa a 16 bit.                                                                                          |
| [**INTESTAZIONE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Restituisce l'indirizzo di [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) all'interno di un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader).                                      |
| [**\_Informazioni sequenza \_ MPEG1**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Restituisce l'indirizzo dell'intestazione della sequenza all'interno di una struttura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) .                                                          |
| [**PALETTISED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Verifica se una bitmap ha una profondità di colore pari o inferiore a 8 bit.                                                                                                      |
| [**voci TAVOLOzza \_**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera il numero massimo di colori nella tavolozza di una bitmap specificata.                                                                                      |
| [**Reimposta \_ maschere**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Riempie i campi della maschera dei colori in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con zeri.                                                                            |
| [**Reimposta \_ intestazione**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Riempie un [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con zeri.                                                                                                   |
| [**Reimposta \_ tavolozza**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Riempie le voci della tavolozza in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con zeri.                                                                              |
| [**Ridimensiona \_ la \_ tavolozza EGA**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcola le dimensioni necessarie per le voci della tavolozza in una bitmap RGB a 4 bit.                                                                                         |
| [**\_maschere dimensioni**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcola la dimensione delle maschere dei colori in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                             |
| [**DIMENSIONI \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcola la dimensione di una struttura [**MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) , inclusa l'intestazione della sequenza.                                                      |
| [**\_tavolozza dimensioni**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | Calcola la dimensione delle voci della tavolozza in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                                                         |
| [**DIMENSIONI \_ PREheader**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcola l'offset di byte del campo **bmiHeader** all'interno di una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                              |
| [**DIMENSIONI \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcola la dimensione della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .                                                                                  |
| [**TRUECOLOR**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Restituisce la struttura [**TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) da una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Verifica una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) per individuare eventuali errori che possono causare sovraccarichi del buffer o overflow di Integer.                                   |



 

## <a name="remarks"></a>Commenti

La maggior parte delle macro e delle funzioni descritte nella sezione è progettata per la modifica delle strutture **VIDEOINFOHEADER** e **VIDEOINFO** per le bitmap RGB. Usare queste macro con cautela: la maggior parte di essi presuppone che la struttura specificata sia stata inizializzata correttamente. Molti di essi presuppongono anche che la struttura **BITMAPINFOHEADER** sia la dimensione standard; ovvero `biSize == sizeof(BITMAPINFOHEADER)` .

La libreria di classi base DirectShow fornisce anche le costanti globali seguenti, che definiscono le maschere dei colori standard per le bitmap con colori reali.



| Dati globali | Descrizione                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matrice di maschere colori per una bitmap RGB a 16 bit in formato 5-5-5. |
| **bits565** | Matrice di maschere colori per una bitmap RGB a 16 bit in formato 5-6-5. |
| **bits888** | Matrice di maschere colori per una bitmap RGB a 24 bit.                 |



 

Ognuna di queste costanti in una matrice di tre **DWORD**, che contiene le maschere rosso, verde e blu, in questo ordine.

 

 
