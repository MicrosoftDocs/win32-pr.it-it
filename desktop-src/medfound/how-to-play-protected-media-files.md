---
description: Come riprodurre file che contengono supporti protetti da DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Come riprodurre file multimediali protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320647"
---
# <a name="how-to-play-protected-media-files"></a>Come riprodurre file multimediali protetti

Un file multimediale protetto è un file multimediale con regole associate per l'utilizzo del contenuto. In alcuni casi, un file multimediale protetto viene crittografato con una forma di crittografia Digital Rights Management (DRM). Per riprodurre un file multimediale protetto, la riproduzione deve essere eseguita all'interno del percorso del supporto protetto (PMP). Inoltre, l'utente potrebbe dover acquisire i diritti per il contenuto.

Il termine acquisizione dei diritti si riferisce a qualsiasi azione che l'applicazione deve eseguire prima che l'utente possa riprodurre il contenuto. L'esempio più comune è ottenere una licenza DRM, ma Media Foundation definisce un meccanismo generico che può supportare altri tipi di acquisizione dei diritti. L'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) definisce questo meccanismo generico.

L'acquisizione dei diritti deve essere eseguita all'esterno del PMP, dal processo dell'applicazione. La sessione multimediale invia una notifica all'applicazione tramite l'interfaccia [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , implementata dall'applicazione. La sessione multimediale usa l'interfaccia **IMFContentProtectionManager** per l'invio di un oggetto Enabler contenuto all'applicazione. Gli attivatori del contenuto implementano l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . L'applicazione usa questa interfaccia per acquisire i diritti necessari.

Un abilitatore del contenuto potrebbe supportare l'acquisizione automatica dei diritti, nel qual caso l'attivatore del contenuto implementa l'intero processo e l'applicazione monitora semplicemente lo stato. In caso contrario, l'applicazione deve usare l'acquisizione di diritti non invisibile all'utente, che è un processo in cui l'applicazione invia i dati HTTP POST a un URL fornito da Content Enabler.

Per riprodurre supporti protetti, un'applicazione segue gli stessi passaggi illustrati nell'argomento [come riprodurre file multimediali con Media Foundation](how-to-play-unprotected-media-files.md), con i seguenti passaggi aggiuntivi:

1.  Eseguire una query per verificare se l'origine del supporto contiene contenuto protetto. Facoltativo.
2.  Creare la sessione multimediale nel processo PMP invece che nel processo dell'applicazione.
3.  Eseguire l'acquisizione dei diritti, se notificata a tale scopo dalla sessione multimediale. Questa operazione viene eseguita in modo asincrono dall'applicazione.
4.  Completare l'operazione asincrona.

## <a name="query-for-protected-content"></a>Query per contenuto protetto

Per eseguire una query sull'origine del supporto che contiene contenuto protetto, chiamare la funzione [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) sul descrittore di presentazione dell'origine multimediale. Se la funzione restituisce S \_ OK, è necessario usare il PMP per riprodurre il contenuto. Se la funzione restituisce \_ false, il file PMP non è obbligatorio ed è possibile creare la sessione multimediale nel processo dell'applicazione. In alternativa, è possibile usare il file PMP per riprodurre entrambi i tipi di contenuto, protetto e non protetto. In tal caso, non è necessario chiamare **MFRequireProtectedEnvironment**.

Per ulteriori informazioni sui descrittori di presentazione, vedere [descrittori di presentazione](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Creare la sessione multimediale PMP

Per creare la sessione multimediale in PMP, chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Questa funzione è simile a [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), ma anziché creare la sessione multimediale nel processo dell'applicazione, crea la sessione multimediale nel processo PMP. L'applicazione riceve un puntatore a un oggetto proxy per la sessione multimediale. L'applicazione chiama i metodi [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) sull'oggetto proxy, esattamente come si farebbe per la sessione multimediale. L'oggetto proxy esegue il inoltro delle chiamate alla sessione multimediale attraverso il limite di processo.

Creare la sessione multimediale PMP come segue:

1.  Creare un nuovo archivio di attributi chiamando [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Impostare l'attributo [**MF \_ Session \_ Content \_ Protection \_ Manager**](mf-session-content-protection-manager-attribute.md) nell'archivio di attributi. Il valore di questo attributo è un puntatore all'implementazione dell'applicazione di [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager). Chiamare [**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) per impostare l'attributo.
3.  Chiamare [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) per creare la sessione multimediale nel processo PMP. Il parametro *pConfiguration* è un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) dell'archivio di attributi.


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



Successivamente, creare una topologia di riproduzione e accodarla nella sessione multimediale, come descritto in [creazione di topologie di riproduzione](creating-playback-topologies.md).

## <a name="perform-rights-acquisition"></a>Eseguire l'acquisizione dei diritti

Se la riproduzione richiede l'acquisizione dei diritti, la sessione multimediale chiama [**IMFContentProtectionManager:: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Il parametro *pEnablerActivate* di questo metodo è un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Usare questa interfaccia per creare l'oggetto Enabler contenuto, che espone l'interfaccia [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Usare quindi il Content Enabler per eseguire il passaggio di acquisizione dei diritti.

Per creare l'Enabler del contenuto, chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Eseguire una query sul puntatore [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) restituito per l'interfaccia [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Usare questa interfaccia per ottenere gli eventi dall'oggetto Enabler del contenuto. Per ulteriori informazioni sugli eventi, vedere [generatori di eventi multimediali](media-event-generators.md).

Per sapere se l'Enabler del contenuto supporta l'acquisizione automatica, chiamare [**IMFContentEnabler:: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Se questo metodo restituisce il valore **true**, l'applicazione deve usare l'acquisizione automatica. In caso contrario, usare l'acquisizione non invisibile all'utente.

Il metodo [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) è asincrono. L'applicazione deve eseguire il passaggio di acquisizione nel thread dell'applicazione. Un approccio consiste nell'inviare un messaggio di finestra privata alla finestra principale dell'applicazione, inviando una notifica al thread dell'applicazione per eseguire l'acquisizione. Mentre l'operazione è in sospeso, l'applicazione deve archiviare il puntatore di callback e l'oggetto di stato ricevuti nei parametri *pCallback* e *punkState* di **BeginEnableContent**. Questi verranno usati per completare l'operazione asincrona.

### <a name="automatic-acquisition"></a>Acquisizione automatica

Per eseguire l'acquisizione automatica, chiamare [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Questo metodo è asincrono. Al termine dell'operazione, l'attivatore di contenuto invia un evento [MEEnablerCompleted](meenablercompleted.md) . Il codice di stato dell'evento indica se l'operazione è stata completata correttamente. Se il codice di stato dell'evento MEEnablerCompleted è NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l'applicazione dovrebbe provare a usare l'acquisizione non invisibile all'utente.

Mentre è in corso l'operazione di acquisizione, l'oggetto Enabler potrebbe inviare l'evento [MEEnablerProgress](meenablerprogress.md) per indicare lo stato di avanzamento dell'operazione. Per annullare l'operazione, chiamare [**IMFContentEnabler:: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Acquisizione non invisibile all'utente

Se il metodo [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) restituisce **false** o il metodo [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) ha esito negativo con il codice di errore NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l'applicazione deve eseguire un'acquisizione non invisibile all'utente, come descritto nei passaggi seguenti:

1.  Chiamare [**IMFContentEnabler:: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) per ottenere l'URL per l'acquisizione dei diritti. Questo metodo restituisce anche un flag che indica se l'URL è attendibile.
2.  Chiamare [**IMFContentEnabler:: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) per ottenere i dati http post.
3.  Chiamare [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Questo metodo fa in modo che l'attivatore del contenuto monitori lo stato di avanzamento dell'azione di acquisizione dei diritti.

4.  Inviare i dati all'URL di acquisizione dei diritti usando un'azione HTTP POST. È possibile utilizzare il controllo Internet Explorer o le API di Windows Internet (WinINet).

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



Al termine dell'operazione, l'attivatore di contenuto invia un evento [MEEnablerCompleted](meenablercompleted.md) .

## <a name="complete-the-asynchronous-operation"></a>Completa l'operazione asincrona

Quando l'acquisizione dei diritti viene completata correttamente o in caso contrario, l'applicazione deve inviare una notifica alla sessione multimediale richiamando il puntatore di callback fornito nel metodo [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .

1.  Creare un oggetto risultato asincrono chiamando [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Richiamare il callback della sessione multimediale chiamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  La sessione multimediale chiamerà [**IMFContentProtectionManager:: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). Nell'implementazione di questo metodo rilasciare tutti i puntatori o le risorse allocati all'interno di [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Restituisce un valore **HRESULT** che indica l'esito positivo complessivo dell'operazione. Se l'acquisizione dei diritti ha avuto esito negativo o l'utente ha annullato prima del completamento, restituire un codice di errore.

Nel codice seguente viene illustrato come creare il risultato asincrono e richiamare il callback.


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

 

 



