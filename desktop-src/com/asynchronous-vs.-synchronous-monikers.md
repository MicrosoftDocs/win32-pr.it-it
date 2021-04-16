---
title: Moniker asincroni e sincroni
description: Moniker asincroni e sincroni
ms.assetid: 79c7894d-956a-4c86-8806-2c6c7faa6034
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d54ee1b5f31941774944463baad893058fd15ad
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104553647"
---
# <a name="asynchronous-and-synchronous-monikers"></a>Moniker asincroni e sincroni

Un client di un moniker OLE standard e sincrono in genere crea e include un riferimento al moniker, nonché il contesto di binding da utilizzare durante l'associazione. Il diagramma seguente illustra i componenti interessati dall'utilizzo dei moniker tradizionali.

![Diagramma che mostra il client connesso al contesto di associazione o a qualsiasi moniker per l'oggetto fornito dal sistema.](images/1b29d6fe-f6e7-4eec-91e7-5043c09ca4dc.png)

I client in genere creano moniker standard chiamando funzioni quali [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker), [**CreateItemMoniker**](/windows/desktop/api/Objbase/nf-objbase-createitemmoniker)o [**CreatePointerMoniker**](/windows/desktop/api/Objbase/nf-objbase-createpointermoniker) o, perché possono essere salvati nell'archivio permanente, tramite [**OleSaveToStream**](/windows/desktop/api/ole/nf-ole-olesavetostream) e [**OleLoadFromStream**](/windows/desktop/api/ole/nf-ole-oleloadfromstream). I moniker possono anche essere ottenuti da un oggetto contenitore chiamando il metodo [**IBindHost:: CreateMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) . I client creano contesti di binding chiamando la funzione [**CreateBindCtx**](/windows/desktop/api/Objbase/nf-objbase-createbindctx) e quindi passano il contesto di associazione al moniker con le chiamate a [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).

Come illustrato nel diagramma seguente, un client di un moniker asincrono crea e include anche un riferimento al moniker e al contesto di associazione da utilizzare durante l'associazione.

![Diagramma che mostra le connessioni tra il client specificato, il Monker fornito e il sistema fornito.](images/86872be9-bcbb-4ce8-b69a-38ae5bd7ba41.png)

Per ottenere il comportamento asincrono, il client implementa l'interfaccia [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) su un oggetto Bind-status-callback e chiama la funzione [**RegisterBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775115(v=vs.85)) o la funzione [**CreateAsyncBindCtx**](/windows/desktop/api/Urlmon/nf-urlmon-createasyncbindctx) per registrare questa interfaccia con il contesto di associazione. Il moniker passa un puntatore alla relativa interfaccia [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) in una chiamata al metodo [**IBindStatusCallback:: OnStart**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775065(v=vs.85)) . Il client indica al moniker asincrono come si desidera eseguire l'associazione al ritorno dalla chiamata del moniker al metodo [**IBindStatusCallback:: GetBindInfo.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Moniker asincroni](asynchronous-monikers.md)
</dt> </dl>

 

 