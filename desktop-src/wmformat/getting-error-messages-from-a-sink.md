---
title: Recupero di messaggi di errore da un sink
description: Recupero di messaggi di errore da un sink
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Advanced Systems Format (ASF), messaggi di errore dai sink
- ASF (Advanced Systems Format), messaggi di errore dai sink
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- sink, messaggi di errore
- messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e432f805b5e33de0e830a2f319713bccec328d429f8eb04064d87edc56bf375c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930871"
---
# <a name="getting-error-messages-from-a-sink"></a>Recupero di messaggi di errore da un sink

L'oggetto writer non invia messaggi al metodo di callback [**IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) Tuttavia, è possibile impostare i sink del writer per inviare messaggi a OnStatus. Ogni sink deve essere impostato per recapitare lo stato separatamente, ma tutti i sink possono segnalare allo stesso callback.

Per impostare un sink per recapitare i messaggi di stato su **OnStatus,** chiamare il [**metodo IWMRegisterCallback::Advise.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise)

Il codice di esempio seguente illustra come impostare tutti i sink per recapitare i messaggi di stato a un callback **OnStatus.** In questo esempio l'indice di ogni sink verrà usato come parametro di contesto in modo che il **metodo OnStatus** possa distinguere i messaggi dai diversi sink. Per altre informazioni sull'uso di questo codice, vedere [Uso degli esempi di codice](using-the-code-examples.md).


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Uso dei sink del writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




