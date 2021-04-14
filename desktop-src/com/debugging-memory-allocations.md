---
title: Debug delle allocazioni di memoria
description: Debug delle allocazioni di memoria
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339327"
---
# <a name="debugging-memory-allocations"></a>Debug delle allocazioni di memoria

COM fornisce l'interfaccia [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) che gli sviluppatori possono utilizzare per eseguire il debug delle allocazioni di memoria. Per ogni metodo in [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)sono disponibili due metodi in **IMallocSpy**, un metodo "pre" e un metodo "post". Quando uno sviluppatore lo implementa e lo pubblica nel sistema, il sistema chiama il metodo **IMallocSpy** "pre" immediatamente prima del metodo **IMalloc** corrispondente, consentendo in modo efficace al codice di debug di "Spy" nell'operazione di allocazione e chiama il metodo "post" per rilasciare la spia.

Ad esempio, quando COM rileva che la chiamata successiva è una chiamata a [**IMalloc:: Alloc**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc), chiama [**IMallocSpy::P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc), eseguendo tutte le operazioni di debug desiderate dallo sviluppatore durante l'esecuzione dell' **allocazione** e, quando la chiamata di **Alloc** restituisce, chiama [**IMallocSpy::P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) per rilasciare la spia e restituire il controllo al codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dell'allocazione di memoria](managing-memory-allocation.md)
</dt> </dl>

 

 