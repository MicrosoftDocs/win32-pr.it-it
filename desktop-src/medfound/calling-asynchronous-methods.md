---
description: Chiamata di metodi asincroni
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Chiamata di metodi asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524642"
---
# <a name="calling-asynchronous-methods"></a>Chiamata di metodi asincroni

In Media Foundation, molte operazioni vengono eseguite in modo asincrono. Le operazioni asincrone possono migliorare le prestazioni, perché non bloccano il thread chiamante. Un'operazione asincrona in Media Foundation viene definita da una coppia di metodi con la convenzione di denominazione **Begin..** . e **end..**... Insieme, questi due metodi definiscono un'operazione di lettura asincrona sul flusso.

Per avviare un'operazione asincrona, chiamare il metodo **Begin** . Il metodo **Begin** contiene sempre almeno due parametri:

-   Puntatore all'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . L'applicazione deve implementare questa interfaccia.
-   Puntatore a un oggetto di stato facoltativo.

L'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) invia una notifica all'applicazione quando l'operazione è stata completata. Per un esempio di come implementare questa interfaccia, vedere [implementazione del callback asincrono](implementing-the-asynchronous-callback.md). L'oggetto di stato è facoltativo. Se specificato, deve implementare l'interfaccia **IUnknown** . È possibile usare l'oggetto state per archiviare le informazioni sullo stato necessarie per il callback. Se non sono necessarie informazioni sullo stato, è possibile impostare questo parametro su **null**. Il metodo **Begin** può contenere parametri aggiuntivi specifici di tale metodo.

Se il metodo **Begin** restituisce un codice di errore, significa che l'operazione non è riuscita immediatamente e il callback non viene richiamato. Se il metodo **Begin** ha esito positivo, significa che l'operazione è in sospeso e il callback verrà richiamato al completamento dell'operazione.

Ad esempio, il metodo [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) avvia un'operazione di lettura asincrona su un flusso di byte:


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



Il metodo di callback è [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Ha un solo parametro, *pAsyncResult*, che è un puntatore all'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Per completare l'operazione asincrona, chiamare il metodo **end** che corrisponde al metodo **Begin** asincrono. Il metodo **end** accetta sempre un puntatore **IMFAsyncResult** . Passare sempre lo stesso puntatore ricevuto nel metodo **Invoke** . L'operazione asincrona non è completa fino a quando non si chiama il metodo **end** . È possibile chiamare il metodo **end** dall'interno del metodo **Invoke** oppure è possibile chiamarlo da un altro thread.

Per completare, ad esempio, [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) in un flusso di byte, chiamare [**IMFByteStream:: indread**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



Il valore restituito del metodo **end** indica lo stato dell'operazione asincrona. Nella maggior parte dei casi, l'applicazione eseguirà alcune operazioni dopo il completamento dell'operazione asincrona, indipendentemente dal fatto che venga completata correttamente. Sono disponibili diverse opzioni:

-   Eseguire l'operazione all'interno del metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Questo approccio è accettabile purché l'applicazione non blocchi mai il thread chiamante o attenda qualsiasi elemento all'interno del metodo **Invoke** . Se si blocca il thread chiamante, è possibile bloccare la pipeline di streaming. Ad esempio, è possibile aggiornare alcune variabili di stato, ma non eseguire un'operazione di lettura sincrona o attendere un oggetto mutex.
-   Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) impostare un evento e restituire immediatamente un risultato. Il thread chiamante dell'applicazione attende l'evento ed esegue l'operazione quando viene segnalato l'evento.
-   Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , inviare un messaggio di finestra privata alla finestra dell'applicazione e restituire immediatamente un messaggio. L'applicazione esegue il lavoro nel relativo ciclo di messaggi. (Assicurarsi di pubblicare il messaggio chiamando **PostMessage**, non **SendMessage**, perché **SendMessage** può bloccare il thread di callback).

È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un altro thread. L'applicazione è responsabile di garantire che qualsiasi lavoro eseguito all'interno di **Invoke** sia thread-safe.

Per impostazione predefinita, il thread che chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) non fa presupposto del comportamento dell'oggetto callback. Facoltativamente, è possibile implementare il metodo [**IMFAsyncCallback:: GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) per restituire informazioni sull'implementazione del callback. In caso contrario, questo metodo può restituire **E \_ NOTIMPL**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Se è stato specificato un oggetto stato nel metodo **Begin** , è possibile recuperarlo dall'interno del metodo di callback chiamando [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> </dl>

 

 



