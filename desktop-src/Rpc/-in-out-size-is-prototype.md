---
title: " in, out, size_is Prototype"
description: '\ in, out, size is\ prototype usa una matrice di caratteri a conteggio singolo che viene passata da client a server e \_ da server a client.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a623dc39e9bd18fdd0c7bc02f008ccc1c16919362fd2a52e373abdde762eb726
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073641"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, size \_ è \] Prototype

Il prototipo di funzione seguente usa una matrice di caratteri a conteggio singolo che viene passata in entrambi i modi: da client a server e da server a client:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Come parametro \[ [**in,**](/windows/desktop/Midl/in) \] *achInOut* deve puntare a una memoria valida sul lato client. Lo sviluppatore alloca la memoria associata alla matrice sul lato client prima di effettuare la chiamata di procedura remota.

Gli stub usano il parametro \[ [**\_ size**](/windows/desktop/Midl/size-is) \] *strsize* per allocare memoria nel server \[ [**\_**](/windows/desktop/Midl/length-is) e quindi usano il parametro length \] *pcbSize* per trasmettere gli elementi della matrice in questa memoria. Lo sviluppatore deve assicurarsi che il codice client imposta la **\[ lunghezza \_ sia \]** variabile prima di chiamare la procedura remota.

In alcune situazioni, l'uso di parametri separati anziché di una singola stringa per l'input e l'output è più efficiente e offre flessibilità. Questa operazione viene illustrata nell'esempio seguente:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

Nell'esempio precedente viene usata anche la matrice di caratteri achInOut come \[ [**parametro out.**](/windows/desktop/Midl/out-idl) \] In C il nome della matrice è equivalente all'uso di un puntatore . Per impostazione predefinita, tutti i puntatori di primo livello sono puntatori di riferimento, che non cambiano valore e puntano alla stessa area di memoria nel client prima e dopo la chiamata. Tutta la memoria a cui accede la procedura remota deve corrispondere alle dimensioni specificate dal client prima della chiamata, in caso contrario gli stub genereranno un'eccezione.

Prima della restituzione, la funzione Analyze nel server deve reimpostare il parametro *pcbSize* per indicare il numero di elementi che il server trasmetterà al client come illustrato:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 