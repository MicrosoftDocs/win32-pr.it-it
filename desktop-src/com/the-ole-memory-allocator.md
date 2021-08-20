---
title: Allocatore di memoria OLE
description: Allocatore di memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0be9cb16459787aa1fd56a691c8475f4d81ba359ecec690f2178e4f5e83cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103648"
---
# <a name="the-ole-memory-allocator"></a>Allocatore di memoria OLE

La libreria COM fornisce un'implementazione di un allocatore di memoria thread-safe. Ciò significa che non può causare problemi in situazioni con multithreading. Ogni volta che la proprietà di un blocco di memoria allocato viene passata tramite un'interfaccia COM o tra un client e la libreria COM, è necessario utilizzare questo allocatore COM per allocare la memoria. L'allocazione interna a un oggetto può usare qualsiasi schema di allocazione desiderato, ma l'allocatore di memoria COM è un allocatore pratico, efficiente e thread-safe.

Una chiamata alla funzione API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fornisce un puntatore all'allocatore OLE, che è un'implementazione [**dell'interfaccia IMalloc.**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) Tuttavia, è più efficiente chiamare le funzioni helper [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)e [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), che esegono il wrapping di un puntatore all'allocatore di memoria dell'attività, chiamano il metodo **IMalloc** corrispondente e quindi rilasciano il puntatore all'allocatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'allocazione di memoria](managing-memory-allocation.md)
</dt> <dt>

[Libreria COM](the-com-library.md)
</dt> </dl>

 

 