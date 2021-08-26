---
title: buffer Application-Allocated
description: L'attributo ACF \ byte count\ indica agli stub di usare un buffer preallocato non allocato o liberato dalle \_ routine di supporto client.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb87390637cba57cbdf4021a43f4ec98ea64c3828c67dfdb615ffcd62dc8c16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024181"
---
# <a name="application-allocated-buffer"></a>buffer Application-Allocated

Il conteggio dei byte dell'attributo ACF indica agli stub di usare un buffer preallocato non allocato o liberato dalle routine di supporto \[ [**\_**](/windows/desktop/Midl/byte-count) \] client. \[ **L'attributo byte \_ count** \] viene applicato a un puntatore o a un parametro di matrice che punta al buffer. Richiede un parametro che specifica le dimensioni del buffer in byte.

L'area di memoria allocata dal client può contenere strutture di dati complesse con più puntatori. Poiché l'area di memoria è contigua, l'applicazione non deve effettuare diverse chiamate per liberare singolarmente ogni puntatore e struttura. Come quando si usa l'attributo \[ [**allocate(all \_ nodes),**](/windows/desktop/Midl/allocate) l'area di memoria può essere allocata o liberata con una chiamata alla routine di allocazione di memoria o \] alla routine free. Tuttavia, a differenza dell'uso dell'attributo \[ **allocate(all \_ nodes),** il parametro buffer non è gestito dallo \] stub client ma dall'applicazione client.

Il buffer deve essere un \[ [**parametro**](/windows/desktop/Midl/out-idl) \] out-only e la lunghezza del buffer in byte deve essere un \[ [**parametro in**](/windows/desktop/Midl/in) \] -only. \[ [**L'attributo byte \_ count**](/windows/desktop/Midl/byte-count) \] può essere applicato solo ai tipi puntatore. L'attributo ACF per il conteggio dei byte è un'estensione Microsoft di DCE IDL e, di conseguenza, non è disponibile se si esegue la compilazione usando l'opzione \[ **\_** \] MIDL [**/osf.**](/windows/desktop/Midl/-osf)

Nell'esempio seguente il parametro *pRoot usa* il numero di byte:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

\[ [**L'attributo byte \_ count**](/windows/desktop/Midl/byte-count) \] viene visualizzato in ACF come:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

Lo stub client generato da questi file IDL e ACF non alloca né libera la memoria per questo buffer. Lo stub del server alloca e libera il buffer in una singola chiamata usando il parametro size fornito. Se i dati sono troppo grandi per le dimensioni del buffer specificate, viene generata un'eccezione.

 

 