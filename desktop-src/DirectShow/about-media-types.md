---
description: Informazioni sui tipi di supporto
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Informazioni sui tipi di supporto (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351231"
---
# <a name="about-media-types-directshow"></a>Informazioni sui tipi di supporto (DirectShow)

Poiché DirectShow è modulare, richiede un modo per descrivere il formato dei dati in ogni punto del grafico del filtro. Ad esempio, si consideri la riproduzione AVI. I dati entrano nel grafico come un flusso di blocchi RIFF. Questi vengono analizzati in flussi video e audio. Il flusso video è costituito da fotogrammi video, probabilmente compressi. Dopo la decodifica, il flusso video è una serie di bitmap non compresse. Il flusso audio passa attraverso un processo simile.

Tipi di supporto: come DirectShow rappresenta i formati

Il *tipo di supporto* è un modo universale ed estendibile per descrivere i formati multimediali digitali. Quando due filtri si connettono, accettano un tipo di supporto. Il tipo di supporto identifica il tipo di dati che il filtro upstream fornirà al filtro downstream e il layout fisico dei dati. Se due filtri non sono in grado di accettare un tipo di supporto, non verranno connessi.

Per alcune applicazioni, non sarà mai necessario preoccuparsi dei tipi di supporto. Nella riproduzione dei file, ad esempio, DirectShow gestisce tutti i dettagli. È possibile che altri tipi di applicazioni debbano funzionare direttamente con i tipi di supporto.

I tipi di supporto vengono definiti utilizzando la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Questa struttura contiene le informazioni seguenti:

-   **Tipo principale**: il tipo principale è un GUID che definisce la categoria complessiva dei dati. I tipi principali includono video, audio, flusso di byte non analizzato, dati MIDI e così via.
-   **Sottotipo**: il sottotipo è un altro GUID, che definisce ulteriormente il formato. Ad esempio, all'interno del tipo principale video sono presenti sottotipi per RGB-24, RGB-32, UYVY e così via. All'interno di audio, sono presenti audio PCM, payload MPEG-1 e altri. Il sottotipo fornisce più informazioni rispetto al tipo principale, ma non definisce tutti gli elementi del formato. Ad esempio, i sottotipi video non definiscono le dimensioni dell'immagine o la frequenza dei fotogrammi. Questi vengono definiti dal blocco di formato, descritto di seguito.
-   **Format Block**: il blocco di formato è un blocco di dati che descrive in dettaglio il formato. Il blocco di formato viene allocato separatamente dalla struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Il membro **pbFormat** della struttura **del \_ \_ tipo di supporto am** punta al blocco di formato.

    Il membro **pbFormat** è tipizzato ** \* void* _ perché il layout del blocco di formato cambia a seconda del tipo di supporto. Ad esempio, l'audio PCM usa una struttura [_ *WAVEFORMATEX* *](/previous-versions/dd757713(v=vs.85)) . Il video usa varie strutture, tra cui [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Il membro **formatType** della struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) è un GUID che specifica la struttura contenuta nel blocco di formato. A ogni struttura di formato viene assegnato un GUID. Il membro **cbFormat** specifica le dimensioni del blocco di formato. Controllare sempre questi valori prima di dereferenziare il puntatore **pbFormat** .

Se il blocco di formato è compilato, il tipo e il sottotipo principale contengono informazioni ridondanti. Il tipo e il sottotipo principale, tuttavia, costituiscono un modo pratico per identificare i formati senza un blocco di formato completo. Ad esempio, è possibile specificare un formato RGB a 24 bit generico (MEDIASUBTYPE \_ RGB24), senza conoscere tutte le informazioni necessarie per la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , ad esempio le dimensioni dell'immagine e la frequenza dei fotogrammi.

Ad esempio, un filtro può utilizzare il codice seguente per controllare un tipo di supporto:


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



La struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) contiene anche alcuni campi facoltativi. Questi possono essere usati per fornire informazioni aggiuntive, ma i filtri non sono necessari per utilizzarli:

-   **lSampleSize**. Se questo campo è diverso da zero, definisce la dimensione di ogni campione. Se è zero, indica che la dimensione del campione può variare da campione a campione.
-   **bFixedSizeSamples**. Se questo flag booleano è **true**, significa che il valore in **lSampleSize** è valido. In caso contrario, è consigliabile ignorare **lSampleSize**.
-   **bTemporalCompression**. Se questo flag booleano è **false**, significa che tutti i frame sono fotogrammi chiave.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Il grafico del filtro e i relativi componenti](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
