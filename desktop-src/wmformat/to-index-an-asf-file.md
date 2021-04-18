---
title: Per indicizzare un file ASF
description: Per indicizzare un file ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indicizzazione di file ASF
- ASF (Advanced Systems Format), indicizzazione di file
- ASF (Advanced Systems Format), indicizzazione di file
- indici, indicizzazione di file ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299400"
---
# <a name="to-index-an-asf-file"></a>Per indicizzare un file ASF

Il processo di indicizzazione di un file ASF è molto semplice. Effettuare una chiamata a [**IWMIndexer:: startindexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) e passare il nome del file. L'indicizzatore esegue il resto. La chiamata a **startIndex** è asincrona, pertanto lo stato deve essere monitorato tramite il callback **OnStatus** .

Nel codice seguente viene illustrato come indicizzare un file ASF. Se si vuole configurare l'indicizzatore prima di indicizzare il file, sarà necessario includere il codice dell'esempio incluso in [per configurare l'indicizzatore](to-configure-the-indexer.md).

Per questo esempio, è necessario creare l'handle che punta all'evento come variabile globale in modo che sia accessibile dal callback. La dichiarazione seguente dovrebbe essere visualizzata in un ambito globale.


```C++
HANDLE g_hEvent = NULL;

```



In uno scenario più realistico, l'handle di evento deve essere un membro dati della classe che contiene sia il callback che la logica per l'avvio dell'indicizzatore.

L'indicizzatore invia diversi eventi al callback **OnStatus** dopo la chiamata a **IWMIndexer:: startindexing**. È possibile intercettarli in base alle esigenze dell'applicazione. Come minimo, è necessario intercettare la chiusura di WMT \_ , che viene inviata al termine dell'indicizzazione. Utilizzare la seguente logica all'interno dell'opzione Message nell'implementazione del callback **OnStatus** .


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Per questo esempio si presuppone che l'implementazione del callback **OnStatus** sia accessibile tramite un oggetto denominato callback. Per altre informazioni sull'uso di eventi e callback con questo SDK, vedere [uso dei metodi di callback](using-the-callback-methods.md).


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

 

 




