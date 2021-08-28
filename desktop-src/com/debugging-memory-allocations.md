---
title: Debug delle allocazioni di memoria
description: Debug delle allocazioni di memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b3376b2ffee17ce747197eb57fecbdae18e086d5252dd5f4721975181885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993451"
---
# <a name="debugging-memory-allocations"></a>Debug delle allocazioni di memoria

COM fornisce [**l'interfaccia IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) che gli sviluppatori possono usare per eseguire il debug delle allocazioni di memoria. Per ogni metodo in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)sono disponibili due metodi in **IMallocSpy,** un metodo "pre" e un metodo "post". Dopo che uno sviluppatore lo implementa e lo pubblica nel sistema, il sistema chiama il metodo "pre" **IMallocSpy** subito prima del metodo **IMalloc** corrispondente, consentendo in modo efficace al codice di debug di "spiare" l'operazione di allocazione e chiama il metodo "post" per rilasciare la spy.

Ad esempio, quando COM rileva che la chiamata successiva è una chiamata a [**IMalloc::Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), chiama [**IMallocSpy::P reAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), eseguendo le operazioni di debug che lo sviluppatore vuole durante l'esecuzione **di Alloc** e quindi, quando la chiamata **Alloc** viene restituita, chiama [**IMallocSpy::P ostAlloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) per rilasciare la spy e restituire il controllo al codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'allocazione di memoria](managing-memory-allocation.md)
</dt> </dl>

 

 