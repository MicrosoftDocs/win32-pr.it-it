---
title: Buffer Stub-Allocated
description: Anziché forzare una chiamata distinta per ogni nodo dell'albero o del grafo, è possibile indirizzare gli stub per calcolare le dimensioni dei dati e allocare e liberare memoria effettuando una singola chiamata a MIDL \_ User \_ allocate o MIDL \_ User \_ free.
ms.assetid: 9911649d-00e8-47d8-b512-7d9b185d1e09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956acf6452c1a4e7d04afcd1da263439436e3bad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047088"
---
# <a name="stub-allocated-buffers"></a>Buffer Stub-Allocated

Anziché forzare una chiamata distinta per ogni nodo dell'albero o del grafo, è possibile indirizzare gli stub per calcolare le dimensioni dei dati e allocare e liberare memoria effettuando una singola chiamata a [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1) o [MIDL \_ User \_ Free](/windows/desktop/Midl/midl-user-free-1). L'attributo ACF **\[ allocate (tutti i \_ nodi) \]** indica agli stub di allocare o liberare tutti i nodi in una singola chiamata all'utente fornito: funzioni di gestione della memoria.

Ad esempio, un'applicazione RPC può utilizzare la struttura dei dati dell'albero binario seguente:

``` syntax
/* IDL file fragment */
typedef struct _TREE_TYPE 
{
    short sNumber;
    struct _TREE_TYPE * pLeft;
    struct _TREE_TYPE * pRight;
} TREE_TYPE;

typedef TREE_TYPE * P_TREE_TYPE;
```

L'attributo ACF **\[ allocate (tutti i \_ nodi) \]** applicato a questo tipo di dati viene visualizzato nella Dichiarazione **typedef** in ACF come:

``` syntax
/* ACF file fragment */
typedef [allocate(all_nodes)] P_TREE_TYPE;
```

L'attributo **\[ allocate \]** può essere applicato solo ai tipi di puntatore. L'attributo **\[ \] allocate** ACF è un'estensione Microsoft per DCE IDL e, di conseguenza, non è disponibile se si compila con l'opzione MIDL **/OSF** . Quando **\[ allocate (tutti i \_ nodi) \]** viene applicato a un tipo di puntatore, gli stub generati dal compilatore MIDL attraversano la struttura dei dati specificata per determinare le dimensioni di allocazione. Gli stub effettuano quindi una singola chiamata per allocare l'intera quantità di memoria necessaria per il grafico o l'albero. Un'applicazione client può liberare memoria in modo molto più efficiente effettuando una singola chiamata a **MIDL \_ User \_ Free**. Tuttavia, le prestazioni dello stub server vengono in genere aumentate quando si usa l'allocazione di memoria nodo per nodo perché gli stub del server possono spesso usare la memoria privata che non richiede allocazioni.

Per ulteriori informazioni, vedere allocazione [e deallocazione di nodi per nodo](node-by-node-allocation-and-deallocation.md).

 

 