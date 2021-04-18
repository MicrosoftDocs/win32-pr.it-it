---
description: In questo argomento viene descritto quando e come usare un remux MFT e un sink MP4 H. 264/AVC.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quando e come usare H. 264/AVC remux MFT e MP4 sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132c582fa16eae56c4fec8809caa4bd501469e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310842"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Quando e come usare H. 264/AVC remux MFT e MP4 sink

In questo argomento viene descritto quando e come usare un remux MFT e un sink MP4 H. 264/AVC.

## <a name="when-to-use-h264avc-remux-mft"></a>Quando usare H. 264/AVC remux MFT

Il formato di file MPEG-4 richiede che ogni esempio compresso contenga un'immagine principale con unità NAL nell'ordine corretto. (Fare riferimento alla definizione dell'immagine principale e dell'ordine di unità NAL obbligatorie nella sezione 7.4.1.2.3, **ordine di unità NAL e immagini codificate e associazione alle unità di accesso**, della specifica AVC H. 264). Richiede anche che ogni campione compresso sia associato a un timestamp di presentazione, alla decodifica del timestamp e alla durata del campione.

In molti scenari in cui le applicazioni devono registrare video H. 264/AVC in un contenitore di file MPEG-4, l'esempio compresso potrebbe non soddisfare i requisiti precedenti. Un esempio compresso, ad esempio, potrebbe non contenere un'immagine principale completa o potrebbe non essere associato a un timestamp di presentazione appropriato. Alcuni esempi di applicazioni sono:

-   Scrivere il video elementare di streaming H. 264/AVC nel contenitore di file MPEG-4.
-   Registrare il video elementare H. 264/AVC della fotocamera nel contenitore di file MPEG-4.
-   Registrare la conferenza video H. 264/AVC nel contenitore di file MPEG-4.
-   Concatenare due video H. 264/AVC in MPEG-2 TS o MP4 e scrivere nel contenitore di file MPEG-4 con timestamp corretti.
-   Video remux H. 264/AVC dal formato di file AVCHD, MPEG-2 TS/PS al formato di file MPEG-4.
-   Tagliare il file video H. 264/AVC senza transcodifica.

In questa situazione, l'applicazione deve usare una remux MFT H. 264/AVC per convertire gli esempi compressi che non contengono un'immagine principale completa prima che vengano scritti nel contenitore di file MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Come usare H. 264/AVC remux MFT e MP4 sink

Impostare il tipo di supporto di output di origine su **MFVideoFormat \_ H264 \_ es**, che indica che ogni campione potrebbe non contenere un'immagine principale completa. Impostare il tipo di supporto di input MP4 sink su **MFVideoFormat \_ H264**. Il tipo di supporto di input di H. 264/AVC remux MFT è quindi **MFVideoFormat \_ H264 \_ es** e il tipo di supporto di output di h. 264/AVC remux MFT è **MFVideoFormat \_ H264**, che verrà inserito automaticamente nel resolver della topologia.

La durata del campione viene ignorata dal remux H. 264/AVC, perché la durata del campione per un campione che non contiene un'immagine primaria completa non ha un significato chiaro. La durata del campione viene invece calcolata dalla frequenza dei fotogrammi. La frequenza dei fotogrammi viene calcolata dal parametro Sequence. Se le informazioni non sono presenti nel parametro Sequence, la frequenza dei fotogrammi viene calcolata in base ai parametri nel tipo di supporto di input. Se non sono disponibili informazioni sulla frequenza dei fotogrammi, viene utilizzata la frequenza dei fotogrammi predefinita 29,97 fps.

H. 264/AVC remux MFT esegue l'interpolazione lineare dei timestamp di decodifica (DTS) per ogni immagine compressa in base alla frequenza dei fotogrammi. H. 264/AVC remux MFT rispetta i timestamp di presentazione dell'input (PTS) negli esempi di input e li passa all'output se esistono. Esegue l'interpolazione PTS in base alla frequenza dei fotogrammi, ai punti precedenti e all'ordine di output dell'immagine tramite il processo di ingrandimento del buffering delle immagini decodificato (DBP), come specificato nel processo di ingrandimento **4.5.3** della specifica H. 264 AVC. Ogni esempio di output di H. 264/AVC remux MFT deve avere PTS, DTS e la durata del campione. H. 264/AVC remux MFT identifica anche le immagini IDR nel bitstream e le imposta come punto di pulizia con l'attributo MF di [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Attualmente il remux MFT di H. 264/AVC può gestire un massimo di 64 di frame riordinato. Se il numero di fotogrammi riordinati supera 64 con un frame di riferimento a lungo termine, l'remux MFT di H. 264/AVC eseguirà l'interpolazione di un PTS errato per quel frame e l'output del frame in un momento errato.

Per creare un'istanza di un remux MFT H. 264/AVC, impostare i tipi di supporti di input e di output corretti nella MFT remux H. 264/AVC, impostare il tipo di supporto di input per il sink MP4 e risolvere la topologia.

Il codice di esempio seguente illustra come inizializzare le remux MFT e MP4 del sink H. 264/AVC.

Per la remux MFT H. 264/AVC,


```C++
hr = CoCreateInstance(
            CLSID_CMSH264RemuxMFT,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IMFTransform,
            (void**) &pIMFTransform
            );
```



Non è richiesta alcuna configurazione aggiuntiva.

Per il sink MP4,


```C++
IMFByteStream*  pMFBSOutputFile = NULL;
hr = MFCreateFile(
    MF_ACCESSMODE_READWRITE,
    MF_OPENMODE_DELETE_IF_EXIST,
    MF_FILEFLAGS_NONE,
    m_pszOutputFile,
    &pMFBSOutputFile);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create output file for MP4 Sink (hr=0x%x)", hr);
    break;
}

hr = MFCreateMPEG4MediaSink(
    pMFBSOutputFile,
    (guidMajorType == MFMediaType_Video) ? pMediaType : NULL,  // pMediaType comes from the output type of the remux MFT
    (guidMajorType == MFMediaType_Audio) ? pMediaType : NULL,
    &m_pMediaSink);
if(FAILED(hr))
{
    Log(L"ERROR>> Failed to create MP4 Sink (hr=0x%x)", hr);
    break;
}
hr = m_pMediaSink->GetStreamSinkByIndex(0, &pStream);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 



