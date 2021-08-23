---
description: Informazioni sui tipi di supporti in DirectShow. Il tipo di supporto è un modo universale ed estendibile per descrivere i formati multimediali digitali.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informazioni sui tipi di supporti (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fa3034581e443472f1b73c0bc42ca7b8b532a18120df3e067b02ad16f37930e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074895"
---
# <a name="about-media-types-directshow"></a>Informazioni sui tipi di supporti (DirectShow)

Poiché DirectShow è modulare, è necessario un modo per descrivere il formato dei dati in ogni punto del grafico dei filtri. Si consideri ad esempio la riproduzione AVI. I dati vengono immessi nel grafico come flusso di blocchi RIFF. Questi vengono analizzati in flussi video e audio. Il flusso video è costituito da fotogrammi video, che sono probabilmente compressi. Dopo la decodifica, il flusso video è una serie di bitmap non compresse. Il flusso audio passa attraverso un processo simile.

Tipi di supporti: come DirectShow rappresenta i formati

Il *tipo di supporto* è un modo universale ed estendibile per descrivere i formati multimediali digitali. Quando due filtri si connettono, accettano un tipo di supporto. Il tipo di supporto identifica il tipo di dati che il filtro upstream consegnerà al filtro downstream e il layout fisico dei dati. Se due filtri non sono d'accordo su un tipo di supporto, non si connetteranno.

Per alcune applicazioni, non sarà mai necessario preoccuparsi dei tipi di supporti. Nella riproduzione di file, ad esempio, DirectShow gestisce tutti i dettagli. Altri tipi di applicazioni potrebbero dover lavorare direttamente con i tipi di supporti.

I tipi di supporti vengono definiti usando la [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Questa struttura contiene le informazioni seguenti:

-   **Tipo principale:** il tipo principale è un GUID che definisce la categoria complessiva dei dati. I tipi principali includono video, audio, flusso di byte non analizzato, dati MIDI e così via.
-   **Sottotipo:** il sottotipo è un altro GUID, che definisce ulteriormente il formato. Ad esempio, all'interno del tipo principale video, sono presenti sottotipi per RGB-24, RGB-32, UYVY e così via. All'interno dell'audio sono presenti audio PCM, payload MPEG-1 e altri. Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutto il formato. Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi. Questi sono definiti dal blocco di formato, descritto di seguito.
-   **Blocco di formato:** il blocco di formato è un blocco di dati che descrive in dettaglio il formato. Il blocco di formato viene allocato separatamente dalla [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type) Il **membro pbFormat** della struttura **AM MEDIA \_ \_ TYPE** punta al blocco di formato.

    Il **membro pbFormat** è tipiato **\* void* _ perché il layout del blocco di formato cambia a seconda del tipo di supporto. Ad esempio, l'audio PCM usa [una struttura _ *WAVEFORMATEX.* *](/previous-versions/dd757713(v=vs.85)) Video usa varie strutture, tra cui [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Il **membro formattype** della [**struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) è un GUID che specifica la struttura contenuta nel blocco di formato. A ogni struttura di formato viene assegnato un GUID. Il **membro cbFormat** specifica le dimensioni del blocco di formato. Controllare sempre questi valori prima di dereferenziare il **puntatore pbFormat.**

Se il blocco di formato viene compilato, il tipo principale e il sottotipo contengono informazioni ridondanti. Il tipo principale e il sottotipo, tuttavia, forniscono un modo pratico per identificare i formati senza un blocco di formato completo. Ad esempio, è possibile specificare un formato RGB generico a 24 bit (MEDIASUBTYPE RGB24), senza conoscere tutte le informazioni richieste dalla struttura VIDEOINFOHEADER, ad esempio le dimensioni dell'immagine e la frequenza dei \_ fotogrammi. [](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

Ad esempio, un filtro potrebbe usare il codice seguente per controllare un tipo di supporto:


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



La [**struttura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) contiene anche alcuni campi facoltativi. Questi possono essere usati per fornire informazioni aggiuntive, ma i filtri non sono necessari per usarli:

-   **lSampleSize**. Se questo campo è diverso da zero, definisce le dimensioni di ogni campione. Se è zero, indica che le dimensioni del campione possono cambiare da campione a campione.
-   **bFixedSizeSamples**. Se questo flag booleano **è TRUE,** significa che il valore in **lSampleSize** è valido. In caso contrario, è necessario ignorare **lSampleSize**.
-   **bTemporalCompression**. Se questo flag booleano è **FALSE,** significa che tutti i fotogrammi sono fotogrammi chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Il filtro Graph e i relativi componenti](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
