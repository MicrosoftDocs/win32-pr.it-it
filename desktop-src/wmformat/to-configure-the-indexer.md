---
title: Per configurare l'indicizzatore
description: Per configurare l'indicizzatore
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK, configurazione di indicizzatori
- Advanced Systems Format (ASF), configurazione degli indicizzatori
- ASF (Advanced Systems Format), configurazione degli indicizzatori
- indici, configurazione di indicizzatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a624a4ed9ae749559a1908e3809500bf8aece2b29b8ad406769c5f639e547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845626"
---
# <a name="to-configure-the-indexer"></a>Per configurare l'indicizzatore

È possibile configurare l'indicizzatore prima di usarlo per indicizzare un file ASF. Ogni flusso nel file può essere configurato separatamente oppure è possibile impostare la stessa configurazione per tutti i flussi.

Se si configurano più elementi per l'indicizzazione in un file, è necessario configurarli tutti e quindi iniziare l'indicizzazione. Se si configura e indicizza un flusso e quindi si configura un altro flusso nello stesso file, avviando nuovamente l'indicizzatore verrà eliminato il primo indice. Questo è conforme al formato di file ASF.

Il codice seguente illustra come configurare l'indicizzatore. Il codice presuppone che il file da indicizzare abbia due flussi: il primo è un flusso audio che non deve essere indicizzato e il secondo è un flusso video. Questo codice illustra solo come configurare l'indicizzatore. Per indicizzare un file, è necessario seguire i passaggi presentati in [Per indicizzare un file ASF.](to-index-an-asf-file.md)


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> Il tipo di indice predefinito è WMT \_ IT \_ NEAREST CLEAN \_ \_ POINT. Anche se è possibile impostare il tipo di indice su altri valori, questa operazione riduce le prestazioni di ricerca.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMIndexer2::Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Per indicizzare un file ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




