---
description: Questo argomento descrive come riprodurre una sequenza di file audio/video usando MFPlay.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Come riprodurre una sequenza di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf9cfc6fe48caf5eb185a19ec98ac119fcfbbb78d5e2363bd2db9607a4875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828161"
---
# <a name="how-to-play-a-sequence-of-files"></a>Come riprodurre una sequenza di file

\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. È possibile che in versioni successive sia stata modificata o non sia più disponibile. \]

Questo argomento descrive come riprodurre una sequenza di file audio/video usando MFPlay.


[L'Attività iniziali con MFPlay](getting-started-with-mfplay.md) illustra come riprodurre un singolo file multimediale. È anche possibile usare MFPlay per riprodurre una sequenza di file.

### <a name="synchronous-blocking-method"></a>Metodo sincrono (blocco)

1.  Chiamare il [**metodo IMFPMediaPlayer::CreateMediaItemFromURL.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) Il metodo crea un elemento multimediale.
2.  Chiamare [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per accodare l'elemento multimediale per la riproduzione.
3.  Chiamare [**IMFPMediaPlayer::P per**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) avviare la riproduzione.

Il codice riportato di seguito illustra i diversi passaggi.


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



Il [**metodo CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) accetta i parametri seguenti:

-   Il primo parametro è l'URL del file.
-   Il secondo parametro specifica se il metodo si blocca. Se si specifica il valore **TRUE,** come illustrato di seguito, il metodo si blocca fino a quando non viene creato l'elemento multimediale.
-   Il terzo parametro associa un valore **\_ PTR DWORD arbitrario** all'elemento multimediale. È possibile ottenere questo valore in un secondo momento chiamando [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).
-   Il quarto parametro riceve un puntatore [**all'interfaccia IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) dell'elemento multimediale.

### <a name="asynchronous-non-blocking-method"></a>Metodo asincrono (non bloccante)

Evitare l'opzione di blocco se si chiama [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) dal thread dell'interfaccia utente, perché il completamento può richiedere una notevole quantità di tempo. Il metodo in genere apre una connessione di file o di rete e legge dati sufficienti per analizzare le intestazioni del file, il che può richiedere tempo. Pertanto, in genere è consigliabile impostare il secondo parametro su **FALSE.** Questa opzione determina l'esecuzione asincrona del metodo . Quando si usa l'opzione asincrona, l'ultimo parametro deve essere **NULL:**


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Quando viene creato l'elemento multimediale, l'applicazione riceve un evento **MFP \_ EVENT \_ TYPE \_ MEDIAITEM \_ CREATED.** La struttura dei dati per questo evento contiene un puntatore all'elemento multimediale. Passare questo puntatore al [**metodo SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) per accodare l'elemento per la riproduzione.


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a>Requisiti

MFPlay richiede Windows 7.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di MFPlay per la riproduzione audio/video](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



