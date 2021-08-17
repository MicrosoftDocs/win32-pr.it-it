---
description: Questo argomento descrive quando e come usare un sink H.264/AVC Remux MFT e MP4.
ms.assetid: 1DD236D9-775B-4417-BC49-BF52A6B3C8AD
title: Quando e come usare il sink H.264/AVC Remux MFT e MP4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ce5b6d63a21e7a9d6b75acd29690cdeaeba5b0105dcf8d45fe0c93e6b768f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119357951"
---
# <a name="when-and-how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Quando e come usare il sink H.264/AVC Remux MFT e MP4

Questo argomento descrive quando e come usare un sink H.264/AVC Remux MFT e MP4.

## <a name="when-to-use-h264avc-remux-mft"></a>Quando usare H.264/AVC Remux MFT

Il formato di file MPEG-4 richiede che ogni esempio compresso contenga un'immagine primaria con unità NAL nell'ordine corretto. Vedere la definizione dell'immagine primaria e dell'ordine delle unità NAL obbligatorie nella sezione 7.4.1.2.3, Ordine delle unità **NAL** e immagini codificate e associazione per accedere alle unità , della specifica H.264 AVC. Richiede anche che ogni esempio compresso sia associato a un timestamp di presentazione, a un timestamp di decodifica e a una durata del campione.

In molti scenari in cui le applicazioni devono registrare video H.264/AVC in un contenitore di file MPEG-4, l'esempio compresso potrebbe non soddisfare i requisiti precedenti. Ad esempio, un esempio compresso potrebbe non contenere un'immagine primaria completa o non avere un timestamp di presentazione corretto associato. Di seguito sono riportati alcuni esempi di applicazioni:

-   Scrivere video elementare di streaming H.264/AVC nel contenitore di file MPEG-4.
-   Registrare il video elementare H.264/AVC acquisito dalla fotocamera nel contenitore di file MPEG-4.
-   Registrare la videoconferenza H.264/AVC nel contenitore di file MPEG-4.
-   Concatenare due video H.264/AVC in MPEG-2 TS o MP4 e scrivere nel contenitore di file MPEG-4 con timestamp corretti.
-   Remux video H.264/AVC dal formato di file AVCHD, MPEG-2 TS/PS al formato di file MPEG-4.
-   Tagliare il file video H.264/AVC senza transcodico.

In questo caso, l'applicazione deve usare un MFT remux H.264/AVC per convertire gli esempi compressi che non contengono un'immagine primaria completa prima che siano scritti nel contenitore di file MPEG-4.

## <a name="how-to-use-h264avc-remux-mft-and-mp4-sink"></a>Come usare il sink H.264/AVC Remux MFT e MP4

Impostare il tipo di supporto di output di origine su **MFVideoFormat \_ H264 \_ ES,** che indica che ogni esempio potrebbe non contenere un'immagine primaria completa. Impostare il tipo di supporto di input del sink MP4 su **MFVideoFormat \_ H264**. Il tipo di supporto di input del MFT remux H.264/AVC è **MFVideoFormat \_ H264 \_ ES** e il tipo di supporto di output del MFT remux H.264/AVC è **MFVideoFormat \_ H264,** che verrà inserito automaticamente nel sistema di risoluzione della topologia.

La durata del campione viene ignorata dal remux H.264/AVC, perché la durata del campione per un campione che non contiene un'immagine primaria completa non ha un significato chiaro. Al contrario, la durata del campione viene calcolata dalla frequenza dei fotogrammi. La frequenza dei fotogrammi viene calcolata dal parametro sequence. Se le informazioni non esistono nel parametro sequence, la frequenza dei fotogrammi viene calcolata dai parametri nel tipo di supporto di input. Se le informazioni sulla frequenza dei fotogrammi non sono disponibili, viene usata la frequenza fotogrammi predefinita di 29,97 fps.

H.264/AVC remux MFT interpola in modo lineare i timestamp di decodifica (DTS) per ogni immagine compressa in base alla frequenza dei fotogrammi. H.264/AVC remux MFT rispetta i timestamp di presentazione di input (PTS) negli esempi di input e li passa all'output, se presenti. Esegue l'interpolazione PTS in base alla frequenza dei fotogrammi, al PTS precedente e all'ordine di output dell'immagine tramite il processo di bumping DBP (Decoded Picture Buffering), come specificato nell'allegato **C.4.5.3 Bumping process** della specifica H.264 AVC. Ogni esempio di output della MFT remux H.264/AVC deve avere durata PTS, DTS e campione. H.264/AVC remux MFT identifica anche le immagini IDR nel flusso di bit e le imposta come punto pulito con l'attributo MF di [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md).

Attualmente il remux MFT H.264/AVC può gestire un massimo di 64 fotogrammi riordinati. Se il numero di fotogrammi riordinati supera 64 con un frame di riferimento a lungo termine presente, la MFT remux H.264/AVC interpolerà un PTS errato per tale frame e restituisce tale frame in un momento errato.

Per creare un'istanza di H.264/AVC remux MFT, impostare i tipi di supporti di input e output corretti in H.264/AVC remux MFT, impostare il tipo di supporto di input per il sink MP4 e risolvere la topologia.

Il codice di esempio seguente illustra come inizializzare il sink H.264/AVC remux MFT e MP4.

Per H.264/AVC remux MFT,


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

 

 



