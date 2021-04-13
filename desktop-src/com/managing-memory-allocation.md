---
title: Gestione dell'allocazione di memoria
description: Gestione dell'allocazione di memoria
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399798"
---
# <a name="managing-memory-allocation"></a>Gestione dell'allocazione di memoria

In COM, molti, se non più, i metodi di interfaccia vengono chiamati dal codice scritto da un'organizzazione di programmazione e implementati dal codice scritto da un altro. Molti dei parametri e i valori restituiti di queste funzioni sono di tipo che può essere passato in base al valore. In alcuni casi, tuttavia, è necessario passare strutture di dati per le quali questo non è il caso, pertanto è necessario sia per il chiamante che per chiamare per avere un criterio di allocazione e deallocazione compatibile. COM definisce una convenzione universale per l'allocazione di memoria, perché è più ragionevole rispetto alla definizione di regole maiuscole/minuscole e in modo che l'implementazione della chiamata di procedura remota COM possa gestire correttamente la memoria.

I metodi di un'interfaccia COM forniscono sempre la gestione della memoria dei puntatori all'interfaccia chiamando le funzioni [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) disponibili nell'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , da cui derivano tutte le altre interfacce com. Per ulteriori informazioni, vedere [regole per la gestione dei conteggi dei riferimenti](rules-for-managing-reference-counts.md) .

In questa sezione viene descritto solo come allocare memoria per i parametri che non vengono passati per valore, non per i puntatori alle interfacce, ma più banali come le stringhe, i puntatori alle strutture e così via.

Per altre informazioni, vedere i seguenti argomenti:

-   [Allocatore di memoria OLE](the-ole-memory-allocator.md)
-   [Regole di gestione della memoria](memory-management-rules.md)
-   [Debug delle allocazioni di memoria](debugging-memory-allocations.md)

 

 