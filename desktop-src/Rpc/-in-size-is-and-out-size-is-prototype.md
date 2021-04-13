---
title: " in, size_is e out size_is Prototype"
description: Il prototipo di funzione seguente usa due stringhe calcolate. Lo sviluppatore deve scrivere il codice sia sul client che sul server per tenere traccia delle lunghezze delle matrici di caratteri e passare i parametri che indicano agli stub il numero di elementi della matrice da trasmettere.
ms.assetid: 334c5e0f-b1fb-41ca-8157-d92525e78b3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d03dbb4dd65d44122bea7ff086013295e0bf616d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399604"
---
# <a name="in-size_is-and-out-size_is-prototype"></a>\[in, Size \_ is \] e \[ out, Size \_ è \] Prototype

Il prototipo di funzione seguente usa due stringhe calcolate. Lo sviluppatore deve scrivere il codice sia sul client che sul server per tenere traccia delle lunghezze delle matrici di caratteri e passare i parametri che indicano agli stub il numero di elementi della matrice da trasmettere.

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

Si noti che i parametri che descrivono la lunghezza della matrice vengono trasmessi nella stessa direzione delle matrici: *cbIn* e *achIn* sono \[ [**nei**](/windows/desktop/Midl/in) \] parametri mentre *pcbOut* e *achOut* sono \[ parametri [**out**](/windows/desktop/Midl/out-idl) \] . Come parametro **\[ out \]** , il parametro *PcbOut* deve seguire la convenzione C ed essere dichiarato come puntatore.

Il codice client conta il numero di caratteri nella stringa, incluso lo zero finale, prima di chiamare la procedura remota come illustrato:

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

La procedura remota nel server fornisce la lunghezza del buffer restituito in *cbOut* , come illustrato:

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

L' \[ attributo **stringa** \] può essere utilizzato quando un parametro è noto come una stringa. Questo attributo indirizza lo stub per calcolare le dimensioni della stringa, eliminando in tal modo l'overhead associato alla \[ [**lunghezza sono**](/windows/desktop/Midl/size-is) i \] parametri. Consente inoltre di indirizzare lo stub per verificare che la stringa sia terminata con **null** prima di passare il parametro all'applicazione.

 

 