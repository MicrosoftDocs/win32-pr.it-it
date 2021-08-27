---
description: Tipi di video H.264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipi di video H.264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973df2825b0824256e2eb7a1a7f580c5f13bf5cdbb390602175e1319305756b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102764"
---
# <a name="h264-video-types"></a>Tipi di video H.264

Per il video H.264 sono definiti i sottotipi multimediali seguenti.



| Subtype                | FOURCC | Descrizione                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **MEDIASUBTYPE \_ AVC1** | 'AVC1' | Flusso di bit H.264 senza codici di avvio.                           |
| **MEDIASUBTYPE \_ H264** | 'H264' | Flusso di bit H.264 con codici di avvio.                              |
| **MEDIASUBTYPE \_ h264** | 'h264' | Equivalente a **MEDIASUBTYPE \_ H264,** con un'istruzione FOURCC diversa. |
| **MEDIASUBTYPE \_ X264** | 'X264' | Equivalente a **MEDIASUBTYPE \_ H264,** con un'istruzione FOURCC diversa. |
| **MEDIASUBTYPE \_ x264** | 'x264' | Equivalente a **MEDIASUBTYPE \_ H264,** con un'istruzione FOURCC diversa. |



 

Questi GUID del sottotipo vengono dichiarati in wmcodecdsp.h.

La differenza principale tra questi tipi di supporti è la presenza di codici di avvio nel flusso di bit. Se il sottotipo **è MEDIASUBTYPE \_ AVC1,** il flusso di bit non contiene codici di avvio.

### <a name="h264-bitstream-with-start-codes"></a>H.264 Bitstream con codici di avvio

I flussi di bit H.264 trasmessi in aria o contenuti in flussi di trasporto o programma MPEG-2 o registrati su HD-DVD sono formattati come descritto nell'allegato B di ITU-T Rec. H.264. In base a questa specifica, il flusso di bit è costituito da una sequenza di unità del livello di astrazione di rete (NALU), ognuna delle quali è preceduta da un codice iniziale uguale a 0x000001 o 0x00000001.

Quando nel flusso di bit sono presenti codici di avvio, viene usato il tipo di supporto seguente:



| Etichetta | Valore |
|-------------|---------------------------------------------------------------------------------------------------|
| Tipo principale  | **MEDIATYPE \_ Video**                                                                              |
| Sottotipi    | **MEDIASUBTYPE \_ H264,** **MEDIASUBTYPE \_ h264,** **MEDIASUBTYPE \_ X264** o **MEDIASUBTYPE \_ x264** |
| Tipo di formato | **FORMAT \_ VideoInfo**, **FORMAT \_ VideoInfo2**, **FORMAT \_ MPEG2Video** o **GUID \_ NULL**          |



 

Se il tipo di formato è **GUID \_ NULL,** non è presente alcuna struttura di formato.

Quando il flusso di bit contiene codici di avvio, è sufficiente uno dei tipi di formato elencati di seguito, perché il decodificatore non richiede informazioni aggiuntive per analizzare il flusso. Il flusso di bit contiene già tutte le informazioni necessarie per il decodificatore e i codici di avvio consentono al decodificatore di individuare l'inizio di ogni NALU.

I sottotipi seguenti sono equivalenti:

### <a name="h264-bitstream-without-start-codes"></a>H.264 Bitstream senza codici di avvio

Il formato del contenitore MP4 archivia i dati H.264 senza codici di avvio. Al contrario, ogni NALU è preceduto da un campo di lunghezza, che fornisce la lunghezza del NALU in byte. Le dimensioni del campo length possono variare, ma in genere sono 1, 2 o 4 byte.

Quando i codici di avvio non sono presenti nel flusso di bit, viene utilizzato il tipo di supporto seguente.



| Etichetta | Valore |
|-------------|------------------------|
| Tipo principale  | **MEDIATYPE \_ Video**   |
| Subtype     | **MEDIASUBTYPE \_ AVC1** |
| Tipo di formato | **FORMAT \_ MPEG2Video** |



 

Il blocco di formato è [**una struttura MPEG2VIDEOINFO.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) Questa struttura deve essere compilata come segue:

-   **hdr:** struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) che descrive il flusso di bit. Non è presente alcuna tabella dei colori dopo [**la parte BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) della struttura e **biClrUsed** deve essere zero.
-   **dwStartTimeCode:** non usato. Imposta su zero.
-   **cbSequenceHeader:** lunghezza della matrice **dwSequenceHeader** in byte.
-   **dwProfile:** specifica il profilo H.264.
-   **dwLevel:** specifica il livello H.264.
-   **dwFlags:** numero di byte usato per il campo di lunghezza visualizzato prima di ogni **NALU.** Il campo length indica le dimensioni in byte dell'oggetto NALU seguente. Ad esempio, se **dwFlags** è 4, ogni NALU è preceduto da un campo di lunghezza di 4 byte. I valori validi sono 1, 2 e 4.
-   **dwSequenceHeader:** matrice di byte che può contenere set di parametri di sequenza (SPS) e NALU del set di parametri immagine (PPS).

Il contenitore MP4 può contenere set di parametri di sequenza (SPS) o set di parametri immagine (PPS) come unità NAL speciali nelle intestazioni dei file o in un flusso separato (distinto dal flusso video). Quando viene stabilito il formato, il tipo di supporto può specificare unità SPS e PPS NAL nella matrice **dwSequenceHeader.** Se **cbSequenceHeader** è maggiore di zero, **dwSequenceHeader** è l'inizio di una matrice di byte contenente SPS e NALU PPS, delimitati da campi di lunghezza di 2 byte, il tutto in ordine di byte di rete (big-endian). È possibile avere sia SPS che PPS, solo uno di questi tipi o nessuno. Il tipo effettivo di ogni NALU può essere determinato esaminando il campo del tipo di **\_ unità \_ nal** dell'unità NALU stessa.

Quando si usa questo tipo di supporto, ogni campione di supporti inizia all'inizio di un NALU e le unità NAL non si estendono sui campioni. In questo modo il decodificatore può eseguire il ripristino dal danneggiamento dei dati o da campioni eliminati.

 

 



