---
title: " in, size_is e out, size_is Prototipo"
description: Il prototipo di funzione seguente usa due stringhe contate. Lo sviluppatore deve scrivere codice sia nel client che nel server per tenere traccia delle lunghezze delle matrici di caratteri e passare parametri che indicano agli stub il numero di elementi della matrice da trasmettere.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75075ccabe4a29ca1765a189c371c407c791cb868d2980386488879415e8f60d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073631"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[in, size \_ è \] e \[ out, size è \_ \] Prototype

Il prototipo di funzione seguente usa due stringhe contate. Lo sviluppatore deve scrivere codice sia nel client che nel server per tenere traccia delle lunghezze delle matrici di caratteri e passare parametri che indicano agli stub il numero di elementi della matrice da trasmettere.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Si noti che i parametri che descrivono la lunghezza della matrice vengono trasmessi nella stessa direzione delle matrici: *cbIn* e *achIn* sono nei parametri mentre \[ [](/windows/desktop/Midl/in) \] *pcbOut* e *achOut* sono \[ [**parametri**](/windows/desktop/Midl/out-idl) \] out. Come parametro **\[ out, \]** il parametro *pcbOut* deve seguire la convenzione C ed essere dichiarato come puntatore.

Il codice client conta il numero di caratteri nella stringa, incluso lo zero finale, prima di chiamare la procedura remota, come illustrato di seguito:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

La procedura remota nel server specifica la lunghezza del buffer restituito in *cbOut,* come illustrato di seguito:

``` syntax
/* server */
void Analyze(char *pchIn,
             long cbIn,
             char *pchOut,
             long *pcbOut)
{
   ...
   *pcbOut = strlen(pchOut) + 1; // transmitted elements
   return;
}
```

\[ **L'attributo** \] stringa può essere utilizzato quando un parametro è noto come stringa. Questo attributo indica allo stub di calcolare le dimensioni della stringa, eliminando così il sovraccarico associato alla \[ [**lunghezza dei**](/windows/desktop/Midl/size-is) \] parametri. Inoltre, invierà lo stub per verificare che la stringa sia **NULL** terminata prima di passare il parametro all'applicazione.

 

 