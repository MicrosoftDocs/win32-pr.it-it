---
title: Per configurare l'indicizzatore
description: Per configurare l'indicizzatore
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Media Format SDK, configurazione degli indicizzatori
- Formato di sistemi avanzati (ASF), configurazione degli indicizzatori
- ASF (formato avanzato dei sistemi), configurazione degli indicizzatori
- indici, configurazione degli indicizzatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398606"
---
# <a name="to-configure-the-indexer"></a>Per configurare l'indicizzatore

È possibile configurare l'indicizzatore prima di utilizzarlo per indicizzare un file ASF. Ogni flusso del file può essere configurato separatamente oppure è possibile impostare la stessa configurazione per tutti i flussi.

Se si configurano più Vapor per l'indicizzazione in un file, è necessario configurarli tutti e quindi avviare l'indicizzazione. Se si configura e indicizza un flusso e quindi si configura un altro flusso nello stesso file, l'avvio dell'indicizzatore eliminerà nuovamente il primo indice. Questa operazione deve essere conforme al formato di file ASF.

Il codice seguente illustra come configurare l'indicizzatore. Il codice presuppone che il file da indicizzare abbia due flussi: il primo è un flusso audio che non deve essere indicizzato e il secondo è un flusso video. Questo codice Mostra solo come configurare l'indicizzatore. Per indicizzare un file, è necessario seguire la procedura illustrata in [per indicizzare un file ASF](to-index-an-asf-file.md).


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
> Il tipo di indice predefinito è \_ WMT \_ punto di pulizia più vicino \_ \_ . Sebbene sia possibile impostare il tipo di indice su altri valori, in questo modo si riduce la ricerca delle prestazioni.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Per indicizzare un file ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Operazioni con gli indici**](working-with-indexes.md)
</dt> </dl>

 

 




