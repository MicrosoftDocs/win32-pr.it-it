---
description: Chiamata di metodi asincroni
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Chiamata di metodi asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a53f5f0a3062ad6af955fbbfdd8cd05c82b30271cf680d6434bc652d567325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959201"
---
# <a name="calling-asynchronous-methods"></a>Chiamata di metodi asincroni

In Media Foundation, molte operazioni vengono eseguite in modo asincrono. Le operazioni asincrone possono migliorare le prestazioni, perché non bloccano il thread chiamante. Un'operazione asincrona Media Foundation definita da una coppia di metodi con la convenzione di denominazione **Begin...** ed **End....**. Insieme, questi due metodi definiscono un'operazione di lettura asincrona nel flusso.

Per avviare un'operazione asincrona, chiamare il **metodo Begin.** Il **metodo Begin** contiene sempre almeno due parametri:

-   Puntatore [**all'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) L'applicazione deve implementare questa interfaccia.
-   Puntatore a un oggetto stato facoltativo.

[**L'interfaccia IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) invia una notifica all'applicazione al termine dell'operazione. Per un esempio di implementazione di questa interfaccia, vedere [Implementazione del callback asincrono](implementing-the-asynchronous-callback.md). L'oggetto stato è facoltativo. Se specificato, deve implementare **l'interfaccia IUnknown.** È possibile usare l'oggetto state per archiviare le informazioni sullo stato necessarie per il callback. Se non sono necessarie informazioni sullo stato, è possibile impostare questo parametro su **NULL.** Il **metodo Begin** può contenere parametri aggiuntivi specifici di tale metodo.

Se il **metodo Begin** restituisce un codice di errore, significa che l'operazione non è riuscita immediatamente e il callback non verrà richiamato. Se il **metodo Begin** ha esito positivo, significa che l'operazione è in sospeso e il callback verrà richiamato al termine dell'operazione.

Ad esempio, il [**metodo IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) avvia un'operazione di lettura asincrona su un flusso di byte:


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



Il metodo di callback è [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Ha un singolo parametro, *pAsyncResult*, che è un puntatore [**all'interfaccia IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) Per completare l'operazione asincrona, chiamare **il metodo End** corrispondente al metodo **Begin** asincrono. Il **metodo End** accetta sempre un **puntatore IMFAsyncResult.** Passare sempre lo stesso puntatore ricevuto nel **metodo Invoke.** L'operazione asincrona non viene completata fino a quando non si chiama **il metodo End.** È possibile chiamare il **metodo End** dall'interno del **metodo Invoke** oppure da un altro thread.

Ad esempio, per completare [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) in un flusso di byte, chiamare [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



Il valore restituito del **metodo End** indica lo stato dell'operazione asincrona. Nella maggior parte dei casi, l'applicazione eseguirà alcune operazioni al termine dell'operazione asincrona, indipendentemente dal fatto che l'operazione sia stata completata correttamente o meno. Sono disponibili diverse opzioni:

-   Eseguire le operazioni all'interno [**del metodo Invoke.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Questo approccio è accettabile purché l'applicazione non blocchi mai il thread chiamante o attenda qualsiasi elemento all'interno **del metodo Invoke.** Se si blocca il thread chiamante, è possibile bloccare la pipeline di streaming. Ad esempio, è possibile aggiornare alcune variabili di stato, ma non eseguire un'operazione di lettura sincrona o attendere un oggetto mutex.
-   Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) impostare un evento e restituire immediatamente . Il thread chiamante dell'applicazione attende l'evento ed esegue il lavoro quando l'evento viene segnalato.
-   Nel metodo [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) pubblicare un messaggio di finestra privata nella finestra dell'applicazione e restituire immediatamente . L'applicazione esegue il lavoro sul ciclo di messaggi. Assicurarsi di pubblicare il messaggio chiamando **PostMessage**, non **SendMessage**, perché **SendMessage** può bloccare il thread di callback.

È importante ricordare che [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) viene chiamato da un altro thread. L'applicazione è responsabile della verifica che qualsiasi lavoro eseguito all'interno **di Invoke** sia thread-safe.

Per impostazione predefinita, il thread che chiama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) non presuppone il comportamento dell'oggetto callback. Facoltativamente, è possibile implementare il [**metodo IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) per restituire informazioni sull'implementazione del callback. In caso contrario, questo metodo può restituire **E \_ NOTIMPL**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Se è stato specificato un oggetto stato nel **metodo Begin,** è possibile recuperarlo dall'interno del metodo di callback chiamando [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Metodi di callback asincroni](asynchronous-callback-methods.md)
</dt> </dl>

 

 



