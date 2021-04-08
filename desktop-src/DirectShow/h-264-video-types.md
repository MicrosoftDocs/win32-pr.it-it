---
description: Tipi di video H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipi di video H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965456"
---
# <a name="h264-video-types"></a>Tipi di video H. 264

I sottotipi di supporto seguenti sono definiti per il video H. 264.



| Subtype                | FOURCC | Descrizione                                                    |
|------------------------|--------|----------------------------------------------------------------|
| **\_AVC1 MEDIASUBTYPE** | 'AVC1' | Bitstream H. 264 senza codici iniziali.                           |
| **MEDIASUBTYPE \_ H264** | H264 | Bitstream H. 264 con codici iniziali.                              |
| **MEDIASUBTYPE \_ H264** | H264 | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso. |
| **MEDIASUBTYPE \_ x264** | X264 | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso. |
| **MEDIASUBTYPE \_ x264** | x264 | Equivalente a **MEDIASUBTYPE \_ H264**, con un FourCC diverso. |



 

Questi GUID del sottotipo sono dichiarati in wmcodecdsp. h.

La differenza principale tra questi tipi di supporti è la presenza di codici iniziali nel bitstream. Se il sottotipo è **MEDIASUBTYPE \_ AVC1**, il Bitstream non contiene i codici iniziali.

### <a name="h264-bitstream-with-start-codes"></a>Bitstream H. 264 con codici iniziali

I Bitstream H. 264 trasmessi in aria o contenuti in flussi di programmi o di trasporto MPEG-2 o registrati in HD-DVD sono formattati come descritto nell'allegato B di ITU-T REC. H. 264. In base a questa specifica, il Bitstream è costituito da una sequenza di NALUs (Network Abstraction Layer Unit), ognuno dei quali è preceduto da un codice di inizio uguale a 0x000001 o 0x00000001.

Quando i codici iniziali sono presenti in Bitstream, viene usato il seguente tipo di supporto:



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| Tipo principale  | **Video di MEDIATYPE \_**                                                                              |
| Sottotipi    | **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** o **MEDIASUBTYPE \_ x264** |
| Tipo di formato | **Formato \_ VideoInfo**, **Format \_ VideoInfo2**, **Format \_ mpeg2video** o **GUID \_ null**          |



 

Se il tipo di formato **è \_ null GUID**, non è presente alcuna struttura di formato.

Quando il Bitstream contiene i codici iniziali, i tipi di formato elencati di seguito sono sufficienti, perché il decodificatore non richiede informazioni aggiuntive per analizzare il flusso. Il Bitstream contiene già tutte le informazioni necessarie per il decodificatore e i codici iniziali consentono al decodificatore di individuare l'inizio di ogni NALU.

I sottotipi seguenti sono equivalenti:

### <a name="h264-bitstream-without-start-codes"></a>Bitstream H. 264 senza codici iniziali

Il formato contenitore MP4 archivia i dati H. 264 senza codici iniziali. Al contrario, ogni NALU è preceduto da un campo Length, che restituisce la lunghezza di NALU in byte. Le dimensioni del campo Length possono variare, ma sono in genere pari a 1, 2 o 4 byte.

Quando i codici di avvio non sono presenti nel bitstream, viene usato il seguente tipo di supporto.



|             |                        |
|-------------|------------------------|
| Tipo principale  | **Video di MEDIATYPE \_**   |
| Subtype     | **\_AVC1 MEDIASUBTYPE** |
| Tipo di formato | **FORMATO \_ mpeg2video** |



 

Il blocco di formato è una struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) . Questa struttura deve essere compilata come indicato di seguito:

-   **HDR**: struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) che descrive il Bitstream. Non è presente alcuna tabella dei colori dopo la parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) della struttura e **biClrUsed** deve essere zero.
-   **dwStartTimeCode**: non utilizzato. Imposta su zero.
-   **cbSequenceHeader**: lunghezza della matrice **dwSequenceHeader** in byte.
-   **dwProfile**: specifica il profilo H. 264.
-   **dwLevel**: specifica il livello H. 264.
-   **dwFlags**: numero di byte utilizzati per il campo Length visualizzato prima di ogni **Nalu**. Il campo lunghezza indica le dimensioni dei seguenti NALU in byte. Ad esempio, se **dwFlags** è 4, ogni Nalu è preceduto da un campo di lunghezza di 4 byte. I valori validi sono 1, 2 e 4.
-   **dwSequenceHeader**: matrice di byte che può contenere set di parametri di sequenza (SPS) e set di parametri immagine (PPS) NALUs.

Il contenitore MP4 potrebbe contenere set di parametri di sequenza (SPS) o set di parametri immagine (PPS) come unità NAL speciali nelle intestazioni di file o in un flusso separato (distinto dal flusso video). Quando viene stabilito il formato, il tipo di supporto può specificare unità SPS e PPS NAL nella matrice **dwSequenceHeader** . Se **cbSequenceHeader** è maggiore di zero, **dwSequenceHeader** è l'inizio di una matrice di byte che contiene i NALUs SPS e PPS, delimitati da campi di lunghezza 2 byte, tutti nell'ordine dei byte di rete (big-endian). È possibile avere sia SPS che PPS, solo uno di questi tipi o nessuno. Il tipo effettivo di ogni NALU può essere determinato esaminando il campo **del \_ \_ tipo di unità NAL** del Nalu stesso.

Quando si usa questo tipo di supporto, ogni esempio di supporto viene avviato all'inizio di una NALU e le unità NAL non si estendono sugli esempi. In questo modo, il decodificatore è in grado di ripristinare i dati o gli esempi eliminati.

 

 



