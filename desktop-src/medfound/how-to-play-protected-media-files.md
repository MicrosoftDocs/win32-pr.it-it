---
description: Come riprodurre file che contengono supporti protetti da DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Come riprodurre file multimediali protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20a2b525f8acc3a602bcaae2630726d01269881beec07ac214f4d0bd02ee1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942341"
---
# <a name="how-to-play-protected-media-files"></a>Come riprodurre file multimediali protetti

Un file multimediale protetto è qualsiasi file multimediale a cui sono associate regole per l'uso del contenuto. In alcuni casi, un file multimediale protetto viene crittografato usando una qualche forma di crittografia DRM (Digital Rights Management). Per riprodurre un file multimediale protetto, la riproduzione deve avvenire all'interno del percorso del supporto protetto (PMP). Inoltre, l'utente potrebbe dover acquisire diritti per il contenuto.

Il termine acquisizione dei diritti si riferisce a qualsiasi azione che l'applicazione deve eseguire prima che l'utente possa riprodurre il contenuto. L'esempio più comune è ottenere una licenza DRM, ma Media Foundation un meccanismo generico in grado di supportare altri tipi di acquisizione dei diritti. [**L'interfaccia IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) definisce questo meccanismo generico.

L'acquisizione dei diritti deve essere eseguita al di fuori del PMP, dal processo dell'applicazione. La sessione multimediale invia una notifica all'applicazione tramite [**l'interfaccia IMFContentProtectionManager,**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) implementata dall'applicazione. La sessione multimediale usa **l'interfaccia IMFContentProtectionManager** per inoltrare un oggetto content enabler all'applicazione. Gli abilitatori di contenuto implementano [**l'interfaccia IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) L'applicazione usa questa interfaccia per acquisire i diritti necessari.

Un abilitazione del contenuto potrebbe supportare l'acquisizione automatica dei diritti, nel qual caso l'abilitazione del contenuto implementa l'intero processo e l'applicazione monitora semplicemente lo stato. In caso contrario, l'applicazione deve usare l'acquisizione di diritti non invisibile all'utente, ovvero un processo in cui l'applicazione invia i dati HTTP POST a un URL fornito dall'abilitazione del contenuto.

Per riprodurre file multimediali protetti, un'applicazione segue gli stessi passaggi indicati nell'argomento [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md), con i passaggi aggiuntivi seguenti:

1.  Eseguire una query se l'origine multimediale contiene contenuto protetto. Facoltativo.
2.  Creare la sessione multimediale nel processo PMP, anziché nel processo dell'applicazione.
3.  Eseguire l'acquisizione dei diritti, se viene notificata dalla sessione multimediale. Questa operazione viene eseguita in modo asincrono dall'applicazione.
4.  Completare l'operazione asincrona.

## <a name="query-for-protected-content"></a>Eseguire query per il contenuto protetto

Per eseguire una query se un'origine multimediale contiene contenuto protetto, chiamare la [**funzione MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) nel descrittore di presentazione dell'origine multimediale. Se la funzione restituisce S \_ OK, è necessario usare PMP per riprodurre il contenuto. Se la funzione restituisce S FALSE, il PMP non è necessario ed è possibile creare la sessione multimediale \_ nel processo dell'applicazione. In alternativa, è possibile usare PMP per riprodurre entrambi i tipi di contenuto, protetti e non protetti. In questo caso, non è necessario chiamare **MFRequireProtectedEnvironment**.

Per altre informazioni sui descrittori di presentazione, vedere [Descrittori di presentazione](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Creare la sessione del supporto PMP

Per creare la sessione multimediale nel PMP, chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Questa funzione è simile a [**MFCreateMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)ma invece di creare la sessione multimediale nel processo dell'applicazione, crea la sessione multimediale nel processo PMP. L'applicazione riceve un puntatore a un oggetto proxy per la sessione multimediale. L'applicazione [**chiama i metodi IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) sull'oggetto proxy, esattamente come nella sessione multimediale. L'oggetto proxy inoltra le chiamate alla sessione multimediale attraverso il limite del processo.

Creare la sessione del supporto PMP come indicato di seguito:

1.  Creare un nuovo archivio attributi chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Impostare [**l'attributo MF \_ SESSION \_ CONTENT PROTECTION \_ \_ MANAGER**](mf-session-content-protection-manager-attribute.md) nell'archivio attributi. Il valore di questo attributo è un puntatore all'implementazione dell'applicazione [**di IMFContentProtectionManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) Chiamare [**IMFAttributes::SetUnknown per**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) impostare l'attributo.
3.  Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la sessione multimediale nel processo PMP. Il *parametro pConfiguration* è un puntatore [**all'interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dell'archivio attributi.


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



Creare quindi una topologia di riproduzione e accodarla nella sessione multimediale, come descritto in [Creazione di topologie di riproduzione](creating-playback-topologies.md).

## <a name="perform-rights-acquisition"></a>Eseguire l'acquisizione dei diritti

Se la riproduzione richiede l'acquisizione dei diritti, la sessione multimediale chiama [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Il *parametro pEnablerActivate* di questo metodo è un puntatore [**all'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Usare questa interfaccia per creare l'oggetto content enabler, che espone [**l'interfaccia IMFContentEnabler.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) Usare quindi l'abilitazione del contenuto per eseguire il passaggio di acquisizione dei diritti.

Per creare l'abilitazione del contenuto, chiamare [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Eseguire una query [**sul puntatore IMFContentEnabler restituito**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) per [**l'interfaccia IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) Usare questa interfaccia per ottenere eventi dall'oggetto content enabler. Per altre informazioni sugli eventi, vedere [Generatori di eventi multimediali](media-event-generators.md).

Per determinare se l'abilitazione del contenuto supporta l'acquisizione automatica, chiamare [**IMFContentEnabler::IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Se questo metodo restituisce il valore **TRUE,** l'applicazione deve usare l'acquisizione automatica. In caso contrario, usare l'acquisizione non invisibile all'utente.

Il [**metodo BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) è asincrono. L'applicazione deve eseguire il passaggio di acquisizione nel thread dell'applicazione. Un approccio consiste nel pubblicare un messaggio di finestra privata nella finestra principale dell'applicazione, notificando al thread dell'applicazione di eseguire l'acquisizione. Mentre l'operazione è in sospeso, l'applicazione deve archiviare il puntatore di callback e l'oggetto stato ricevuto nei parametri *pCallback* e *punkState* di **BeginEnableContent**. Verranno usati per completare l'operazione asincrona.

### <a name="automatic-acquisition"></a>Acquisizione automatica

Per eseguire l'acquisizione automatica, [**chiamare IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Questo metodo è asincrono. Al termine dell'operazione, l'abilitazione del contenuto invia un [evento MEEnablerCompleted.](meenablercompleted.md) Il codice di stato dell'evento indica se l'operazione ha avuto esito positivo. Se il codice di stato dell'evento MEEnablerCompleted è NS \_ E \_ DRM LICENSE NOTACQUIRED, l'applicazione deve provare a usare \_ l'acquisizione non \_ invisibile all'utente.

Mentre l'operazione di acquisizione è in corso, l'oggetto enabler potrebbe inviare [l'evento MEEnablerProgress](meenablerprogress.md) per indicare lo stato dell'operazione. Per annullare l'operazione, chiamare [**IMFContentEnabler::Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Acquisizione non invisibile all'utente

Se il metodo [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) restituisce **FALSE** o il [**metodo AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) ha esito negativo con il codice di errore NS \_ E \_ DRM LICENSE \_ NOTACQUIRED, l'applicazione deve eseguire l'acquisizione non invisibile all'utente come descritto nei \_ passaggi seguenti:

1.  Chiamare [**IMFContentEnabler::GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) per ottenere l'URL per l'acquisizione dei diritti. Questo metodo restituisce anche un flag che indica se l'URL è attendibile.
2.  Chiamare [**IMFContentEnabler::GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) per ottenere i dati HTTP POST.
3.  Chiamare [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Questo metodo fa in modo che l'abilitazione del contenuto monitori lo stato di avanzamento dell'azione di acquisizione dei diritti.

4.  Inviare i dati all'URL di acquisizione dei diritti usando un'azione HTTP POST. È possibile usare il Internet Explorer o le API Windows Internet (WinINet).

Il codice seguente illustra i passaggi da 1 a 3. Il passaggio 4 dipende dai requisiti specifici dell'applicazione.


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



Al termine dell'operazione, l'abilitazione del contenuto invia un [evento MEEnablerCompleted.](meenablercompleted.md)

## <a name="complete-the-asynchronous-operation"></a>Completare l'operazione asincrona

Al termine dell'acquisizione dei diritti, l'applicazione deve inviare una notifica alla sessione multimediale richiamando il puntatore di callback specificato nel [**metodo BeginEnableContent.**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent)

1.  Creare un oggetto risultato asincrono chiamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Richiamare il callback della sessione multimediale chiamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  La sessione multimediale chiamerà [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). Nell'implementazione di questo metodo rilasciare tutti i puntatori o le risorse allocati all'interno [**di BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Restituisce un **HRESULT** che indica l'esito positivo complessivo dell'operazione. Se l'acquisizione dei diritti non è riuscita o l'utente è stato annullato prima del completamento, restituire un codice di errore.

Il codice seguente illustra come creare il risultato asincrono e richiamare il callback.


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sessione multimediale](media-session.md)
</dt> <dt>

[Riproduzione di audio/video](audio-video-playback.md)
</dt> </dl>

 

 



