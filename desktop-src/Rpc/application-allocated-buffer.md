---
title: Buffer Application-Allocated
description: L'attributo ACF \ byte \_ count \ indica agli stub di usare un buffer preallocato non allocato o liberato dalle routine di supporto client.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473915"
---
# <a name="application-allocated-buffer"></a>Buffer Application-Allocated

Il \[ [**\_ numero di byte**](/windows/desktop/Midl/byte-count) dell'attributo ACF \] indica agli stub di usare un buffer preallocato non allocato o liberato dalle routine di supporto client. L' \[ **attributo \_ conteggio byte** \] viene applicato a un puntatore o a un parametro di matrice che punta al buffer. Richiede un parametro che specifica la dimensione del buffer in byte.

L'area di memoria allocata dal client può contenere strutture di dati complesse con più puntatori. Poiché l'area di memoria è contigua, l'applicazione non deve effettuare diverse chiamate per liberare singolarmente ogni puntatore e struttura. Come quando si usa l' \[ attributo [**allocate (tutti i \_ nodi)**](/windows/desktop/Midl/allocate) \] , l'area di memoria può essere allocata o liberata con una sola chiamata alla routine di allocazione della memoria o alla routine gratuita. Tuttavia, a differenza dell'attributo \[ **allocate (tutti i \_ nodi)** \] , il parametro buffer non viene gestito dallo stub client ma dall'applicazione client.

Il buffer deve essere un \[ [](/windows/desktop/Midl/out-idl) \] parametro di sola uscita e la lunghezza del buffer in byte deve essere un \[ [](/windows/desktop/Midl/in) \] parametro solo in. L' \[ [**attributo \_ conteggio byte**](/windows/desktop/Midl/byte-count) \] può essere applicato solo ai tipi di puntatore. L' \[ attributo ACF **\_ count bytes** \] è un'estensione Microsoft per DCE IDL e, di conseguenza, non è disponibile se si esegue la compilazione con l'opzione MIDL [**/OSF**](/windows/desktop/Midl/-osf) .

Nell'esempio seguente il parametro *pRoot* usa il numero di byte:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

L' \[ [**attributo \_ conteggio byte**](/windows/desktop/Midl/byte-count) \] viene visualizzato in ACF come:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

Lo stub client generato da questi file IDL e ACF non alloca o libera la memoria per questo buffer. Lo stub del server alloca e libera il buffer in una singola chiamata utilizzando il parametro di dimensione fornito. Se i dati sono troppo grandi per le dimensioni del buffer specificate, viene generata un'eccezione.

 

 