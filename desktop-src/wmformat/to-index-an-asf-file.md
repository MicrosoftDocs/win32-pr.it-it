---
title: Per indicizzare un file ASF
description: Per indicizzare un file ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indicizzazione di file ASF
- Advanced Systems Format (ASF), file di indicizzazione
- ASF (Advanced Systems Format),indicizzazione di file
- indici, indicizzazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845579"
---
# <a name="to-index-an-asf-file"></a>Per indicizzare un file ASF

Il processo di indicizzazione di un file ASF è molto semplice. Effettuare una chiamata a [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passare il nome del file. L'indicizzatore esegue il resto. La chiamata a **StartIndexing è** asincrona, quindi lo stato deve essere monitorato usando il callback **OnStatus.**

Il codice seguente illustra come indicizzare un file ASF. Se si vuole configurare l'indicizzatore prima di indicizzare il file, è necessario includere il codice dell'esempio incluso in Per configurare [l'indicizzatore](to-configure-the-indexer.md).

Per questo esempio, l'handle che punta all'evento deve essere creato come variabile globale in modo che sia accessibile dal callback. La dichiarazione seguente deve essere visualizzata in un ambito globale.


```C++
HANDLE g_hEvent = NULL;

```



In uno scenario più realistico, l'handle dell'evento deve essere un membro dati della classe che contiene sia il callback che la logica per avviare l'indicizzatore.

L'indicizzatore invia diversi eventi al callback **OnStatus** dopo la chiamata a **IWMIndexer::StartIndexing.** È possibile intercettarli in base alle esigenze per l'applicazione. Come minimo, è necessario intercettare WMT \_ CLOSED, che viene inviato al termine dell'indicizzazione. Usare la logica seguente all'interno dell'opzione message nell'implementazione del callback **OnStatus.**


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Per questo esempio si presuppone che l'implementazione del callback **OnStatus** sia accessibile tramite un oggetto denominato MyCallback. Per altre informazioni sull'uso di eventi e callback con questo SDK, vedere [Uso dei metodi di callback.](using-the-callback-methods.md)


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Per configurare l'indicizzatore**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




