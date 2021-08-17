---
description: Funzioni per video e immagini
ms.assetid: 02401edc-362b-4f6c-b10b-c46b30b3ebe7
title: Funzioni per video e immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab4b57f804c1da1e4a6da0ca4625e3503ed9987077a80f1f98dde91cf2e27f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432121"
---
# <a name="video-and-image-functions"></a>Funzioni per video e immagini

Queste funzioni e macro modificano le strutture DirectShow formato video.



| Funzione                                                             | Descrizione                                                                                                                                                       |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CORRISPONDENZE \_ DI MASCHERE \_ DI BIT**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bit_masks_match)                         | Confronta le maschere di colore per due [**strutture VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                       |
| [**MASCHERA DI BIT**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-bitmasks)                                         | Recupera le maschere di colore da una [**struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                         |
| [**CheckVideoInfoType**](checkvideoinfotype.md)                     | Controlla un tipo di supporto che contiene una [**struttura di formato VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) per verificare la presenza di errori che possono causare sovraccarichi del buffer o overflow di interi.   |
| [**CheckVideoInfo2Type**](checkvideoinfo2type.md)                   | Controlla un tipo di supporto che contiene una struttura di [**formato VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) per verificare la presenza di errori che possono causare sovraccarichi del buffer o overflow di interi. |
| [**Colori**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-colors)                                             | Recupera le voci della tavolozza da una [**struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                                     |
| [**ContainsPalette**](containspalette.md)                           | Determina se una struttura [**VIDEOINFOHEADER specificata**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contiene una tavolozza.                                                           |
| [**ConvertVideoInfoToVideoInfo2**](convertvideoinfotovideoinfo2.md) | Converte un tipo di supporto che usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in uno che usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)                          |
| [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)                                           | Calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB).                                                                                     |
| [**GetBitCount**](getbitcount.md)                                   | Restituisce il numero di bit per pixel utilizzati da un sottotipo video specificato.                                                                                           |
| [**GetBitmapFormatSize**](getbitmapformatsize.md)                   | Calcola le dimensioni necessarie per una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che può contenere una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) specificata.       |
| [**GetBitmapPalette**](getbitmappalette.md)                         | Restituisce la prima voce del riquadro in una [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                        |
| [**GetBitmapSize**](getbitmapsize.md)                               | Calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB).                                                                                     |
| [**GetBitmapSubtype**](getbitmapsubtype.md)                         | Restituisce il GUID del sottotipo **multimediale** per la bitmap specificata.                                                                                                      |
| [**GetSubtypeName**](getsubtypename.md)                             | Recupera il nome leggibile di un sottotipo video.                                                                                                             |
| [**GetTrueColorType**](gettruecolortype.md)                         | Restituisce il GUID del sottotipo **multimediale** per una bitmap RGB non compressa a 16 bit.                                                                                          |
| [**Intestazione**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header)                                             | Restituisce l'indirizzo di [**BITMAPINFOHEADER all'interno**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) di [**un oggetto VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                      |
| [**INFORMAZIONI SULLA SEQUENZA MPEG1 \_ \_**](/previous-versions/windows/desktop/api/amvideo/nf-amvideo-mpeg1_sequence_info)                 | Restituisce l'indirizzo dell'intestazione della sequenza all'interno [**di una struttura MPEG1VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo)                                                          |
| [**PALETTISED**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palettised)                                     | Controlla se una bitmap ha una profondità del colore di 8 bit o inferiore.                                                                                                      |
| [**VOCI \_ DELLA TAVOLOZZA**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-palette_entries)                          | Recupera il numero massimo di colori nella tavolozza di una bitmap specificata.                                                                                      |
| [**REIMPOSTARE \_ LE MASCHERE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_masks)                                  | Riempie i campi della maschera colore in una [**struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con zeri.                                                                            |
| [**REIMPOSTA \_ INTESTAZIONE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_header)                                | Riempie un [**OGGETTO VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con zeri.                                                                                                   |
| [**REIMPOSTA \_ RIQUADRO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-reset_palette)                              | Riempie le voci della tavolozza in una [**struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) con zeri.                                                                              |
| [**RIQUADRO \_ DIMENSIONI EGA \_**](/previous-versions/windows/desktop/legacy/dd377602(v=vs.85))                       | Calcola le dimensioni necessarie per le voci del riquadro in una bitmap RGB a 4 bit.                                                                                         |
| [**MASCHERE \_ DI DIMENSIONI**](/previous-versions/windows/desktop/legacy/dd377603(v=vs.85))                                    | Calcola le dimensioni delle maschere di colore in una [**struttura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                             |
| [**DIMENSIONI \_ MPEG1VIDEOINFO**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-size_mpeg1videoinfo)                  | Calcola le dimensioni di una struttura [**MPEG1VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo) inclusa l'intestazione della sequenza.                                                      |
| [**RIQUADRO \_ DIMENSIONI**](/previous-versions/windows/desktop/legacy/dd377605(v=vs.85))                                | calcola le dimensioni delle voci della tavolozza in una [**struttura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                                                         |
| [**PREHEADER \_ DI DIMENSIONI**](/previous-versions/windows/desktop/legacy/dd377606(v=vs.85))                            | Calcola l'offset in byte del **campo bmiHeader** all'interno di una [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                              |
| [**DIMENSIONI \_ VIDEOHEADER**](/previous-versions/windows/desktop/legacy/dd377607(v=vs.85))                        | Calcola le dimensioni della struttura [**VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)                                                                                  |
| [**Truecolor**](/previous-versions/windows/desktop/legacy/dd407230(v=vs.85))                                   | Restituisce la [**struttura TRUECOLORINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo) da una [**struttura VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)                                            |
| [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md)         | Controlla la presenza di errori in una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che possono causare sovraccarichi del buffer o overflow di interi.                                   |



 

## <a name="remarks"></a>Commenti

La maggior parte delle macro e delle funzioni descritte nella sezione è progettata per la modifica delle strutture **VIDEOINFOHEADER** e **VIDEOINFO** per le bitmap RGB. Usare queste macro con cautela: la maggior parte di esse presuppone che la struttura specificata sia stata inizializzata correttamente. Molti di essi presuppongono anche che la **struttura BITMAPINFOHEADER** sia di dimensioni standard. cio, `biSize == sizeof(BITMAPINFOHEADER)` .

La DirectShow di classi di base fornisce anche le costanti globali seguenti, che definiscono le maschere di colore standard per le bitmap di colore reale.



| Dati globali | Descrizione                                                   |
|-------------|---------------------------------------------------------------|
| **bits555** | Matrice di maschere di colore per una bitmap RGB a 16 bit in formato 5-5-5. |
| **bits565** | Matrice di maschere di colore per una bitmap RGB a 16 bit in formato 5-6-5. |
| **bits888** | Matrice di maschere di colore per una bitmap RGB a 24 bit.                 |



 

Ognuna di queste costanti in una matrice di tre **DWORD,** contenenti le maschere rosse, verdi e blu, nell'ordine indicato.

 

 
