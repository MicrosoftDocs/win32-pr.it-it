---
title: " in, out, size_is prototipo"
description: '\ in, out, Size \_ is \ Prototype usa una matrice di caratteri a valore singolo che viene passata da client a server e da server a client.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337791"
---
# <a name="in-out-size_is-prototype"></a>\[in, out, dimensioni \_ è un \] prototipo

Il prototipo di funzione seguente usa una matrice di caratteri a conteggio singolo che viene passata in entrambi i modi: da client a server e da server a client:

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

Come parametro \[ [**in**](/windows/desktop/Midl/in) \] , *achInOut* deve puntare a un archivio valido sul lato client. Prima di eseguire la chiamata di procedura remota, lo sviluppatore alloca memoria associata alla matrice sul lato client.

Gli stub utilizzano le \[ [**dimensioni \_**](/windows/desktop/Midl/size-is) del \] parametro *strsize* per allocare la memoria sul server e quindi utilizzano la \[ [**lunghezza \_ è**](/windows/desktop/Midl/length-is) il \] parametro *pcbSize* per trasmettere gli elementi della matrice in questa memoria. Lo sviluppatore deve assicurarsi che il codice client imposti la **\[ lunghezza \_ sia \]** variabile prima di chiamare la procedura remota.

In alcune situazioni, l'uso di parametri distinti anziché di una singola stringa per l'input e l'output è più efficiente e garantisce flessibilità. Questa operazione è illustrata nell'esempio seguente:

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

Nell'esempio precedente, la matrice di caratteri achInOut viene usata anche come parametro \[ [**out**](/windows/desktop/Midl/out-idl) \] . In C, il nome della matrice è equivalente all'utilizzo di un puntatore. Per impostazione predefinita, tutti i puntatori di primo livello sono puntatori di riferimento, ma non cambiano nel valore e puntano alla stessa area di memoria sul client prima e dopo la chiamata. Tutta la memoria a cui accede la procedura remota deve adattarsi alla dimensione specificata dal client prima della chiamata. in alternativa, gli stub genereranno un'eccezione.

Prima di restituire, la funzione Analyze sul server deve reimpostare il parametro *pcbSize* per indicare il numero di elementi che il server trasmetterà al client, come illustrato di seguito:

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 