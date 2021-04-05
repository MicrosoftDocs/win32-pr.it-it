---
title: Recupero di messaggi di errore da un sink
description: Recupero di messaggi di errore da un sink
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- ASF (Advanced Systems Format), messaggi di errore dai sink
- ASF (Advanced Systems Format), messaggi di errore dai sink
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, messaggi di errore
- messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117375"
---
# <a name="getting-error-messages-from-a-sink"></a>Recupero di messaggi di errore da un sink

L'oggetto writer non invia messaggi al metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback. Tuttavia, è possibile impostare i sink del writer per inviare messaggi a OnStatus. Ogni sink deve essere impostato in modo da recapitare lo stato separatamente, ma tutti i sink possono indicare lo stesso callback.

Per impostare un sink per recapitare i messaggi di stato a **OnStatus**, chiamare il metodo [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .

Nell'esempio di codice seguente viene illustrato come impostare tutti i sink per recapitare i messaggi di stato a un callback **OnStatus** . In questo esempio, l'indice di ogni sink verrà usato come parametro di contesto in modo che il metodo **OnStatus** possa distinguere tra i messaggi dei diversi sink. Per ulteriori informazioni sull'utilizzo di questo codice, vedere [utilizzo degli esempi di codice](using-the-code-examples.md).


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

[**Utilizzo dei sink di writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




