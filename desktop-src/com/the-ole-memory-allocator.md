---
title: Allocatore di memoria OLE
description: Allocatore di memoria OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118507"
---
# <a name="the-ole-memory-allocator"></a>Allocatore di memoria OLE

La libreria COM fornisce un'implementazione di un allocatore di memoria thread-safe. Ovvero non può causare problemi nelle situazioni multithread. Ogni volta che la proprietà di un blocco allocato di memoria viene passata attraverso un'interfaccia COM o tra un client e la libreria COM, è necessario usare questo allocatore COM per allocare la memoria. L'allocazione interna a un oggetto può utilizzare qualsiasi schema di allocazione desiderato, ma l'allocatore di memoria COM è un allocatore pratico, efficiente e thread-safe.

Una chiamata alla funzione API [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) fornisce un puntatore all'allocatore OLE, che è un'implementazione dell'interfaccia [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) . Tuttavia, è più efficiente chiamare le funzioni di supporto [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)e [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), che eseguono il wrapping di un puntatore all'allocatore di memoria delle attività, chiamando il metodo **IMalloc** corrispondente e quindi rilasciando il puntatore all'allocatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'allocazione di memoria](managing-memory-allocation.md)
</dt> <dt>

[Libreria COM](the-com-library.md)
</dt> </dl>

 

 