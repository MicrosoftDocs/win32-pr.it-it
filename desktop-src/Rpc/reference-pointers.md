---
title: Puntatori di riferimento
description: I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047244"
---
# <a name="reference-pointers"></a>Puntatori di riferimento

I puntatori di riferimento sono i puntatori più semplici e richiedono la quantità minima di elaborazione da parte dello stub client. Quando un programma client passa un puntatore di riferimento a una procedura remota, il puntatore di riferimento contiene sempre l'indirizzo di un blocco di memoria valido. Il puntatore verrà ancora posizionato allo stesso blocco di memoria al termine della procedura remota. Questi puntatori vengono utilizzati principalmente per implementare la semantica di riferimento e per consentire \[ parametri [**out**](/windows/desktop/Midl/out-idl) \] in C.

Nell'esempio seguente, il valore del puntatore non cambia durante la chiamata, sebbene il contenuto dei dati all'indirizzo indicato dal puntatore possa cambiare.

![modifica dei dati in corrispondenza di un indirizzo puntatore di riferimento statico](images/prog-a07.png)

Un puntatore di riferimento presenta le seguenti caratteristiche:

-   Punta sempre a una risorsa di archiviazione valida e non ha mai il valore **null**.
-   Non viene mai modificato durante una chiamata e punta sempre alla stessa risorsa di archiviazione prima e dopo la chiamata.
-   I dati restituiti dalla procedura remota vengono scritti nella risorsa di archiviazione esistente.
-   Non è possibile accedere allo spazio di archiviazione a cui punta un puntatore di riferimento per nessun altro puntatore o altro nome nella funzione.

Usare l' \[ attributo [**ref**](/windows/desktop/Midl/ref) \] per specificare i puntatori di riferimento nelle definizioni di interfaccia, come illustrato nell'esempio seguente.

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

Questo esempio definisce il parametro *PChar* come puntatore a un singolo carattere, non a una matrice di caratteri. Si tratta \[  \] di un parametro out e di un puntatore di riferimento che punta alla memoria che la routine del server RemoteFn riempirà con i dati.

 

 