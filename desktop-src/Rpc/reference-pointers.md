---
title: Puntatori di riferimento
description: I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6338b1017f05bdf004fee2b288c4eae1ee9775eaa2ad225d5f4b6afa3e74d8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927037"
---
# <a name="reference-pointers"></a>Puntatori di riferimento

I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client. Quando un programma client passa un puntatore di riferimento a una procedura remota, il puntatore di riferimento contiene sempre l'indirizzo di un blocco di memoria valido. La procedura remota continuerà a puntare allo stesso blocco di memoria al termine della procedura remota. Questi puntatori vengono usati principalmente per implementare la semantica dei riferimenti e per consentire i \[ [**parametri out**](/windows/desktop/Midl/out-idl) \] in C.

Nell'esempio seguente il valore del puntatore non cambia durante la chiamata, anche se il contenuto dei dati all'indirizzo indicato dal puntatore può cambiare.

![modifica dei dati in corrispondenza di un indirizzo puntatore di riferimento statico](images/prog-a07.png)

Un puntatore di riferimento presenta le caratteristiche seguenti:

-   Punta sempre a un'archiviazione valida e non ha mai il valore **NULL.**
-   Non cambia mai durante una chiamata e punta sempre alla stessa archiviazione prima e dopo la chiamata.
-   I dati restituiti dalla procedura remota vengono scritti nell'archiviazione esistente.
-   L'archiviazione a cui punta un puntatore di riferimento non è accessibile a nessun altro puntatore o a qualsiasi altro nome nella funzione.

Usare \[ [**l'attributo ref**](/windows/desktop/Midl/ref) \] per specificare puntatori di riferimento nelle definizioni di interfaccia, come illustrato nell'esempio seguente.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

Questo esempio definisce il parametro *pChar* come puntatore a un singolo carattere, non a una matrice di caratteri. Si tratta di un parametro out e di un puntatore di riferimento che punta alla memoria che la \[  \] routine del server RemoteFn riempirà con i dati.

 

 