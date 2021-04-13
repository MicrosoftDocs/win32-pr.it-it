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
# <a name="in-size_is-and-out-size_is-prototype"></a><span data-ttu-id="062bc-104">\[in, Size \_ is \] e \[ out, Size \_ è \] Prototype</span><span class="sxs-lookup"><span data-stu-id="062bc-104">\[in, size\_is\] and \[out, size\_is\] Prototype</span></span>

<span data-ttu-id="062bc-105">Il prototipo di funzione seguente usa due stringhe calcolate.</span><span class="sxs-lookup"><span data-stu-id="062bc-105">The following function prototype uses two counted strings.</span></span> <span data-ttu-id="062bc-106">Lo sviluppatore deve scrivere il codice sia sul client che sul server per tenere traccia delle lunghezze delle matrici di caratteri e passare i parametri che indicano agli stub il numero di elementi della matrice da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="062bc-106">The developer must write code on both client and server to keep track of the character array lengths and pass parameters that tell the stubs how many array elements to transmit.</span></span>

``` syntax
void Analyze(
    [in,  length_is(cbIn), size_is(STRSIZE)]    char  achIn[],
    [in]                                        long  cbIn,
    [out, length_is(*pcbOut), size_is(STRSIZE)] char  achOut[],
    [out]                                       long *pcbOut);
```

<span data-ttu-id="062bc-107">Si noti che i parametri che descrivono la lunghezza della matrice vengono trasmessi nella stessa direzione delle matrici: *cbIn* e *achIn* sono \[ [**nei**](/windows/desktop/Midl/in) \] parametri mentre *pcbOut* e *achOut* sono \[ parametri [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="062bc-107">Note the parameters that describe the array length are transmitted in the same direction as the arrays: *cbIn* and *achIn* are \[[**in**](/windows/desktop/Midl/in)\] parameters while *pcbOut* and *achOut* are \[[**out**](/windows/desktop/Midl/out-idl)\] parameters.</span></span> <span data-ttu-id="062bc-108">Come parametro **\[ out \]** , il parametro *PcbOut* deve seguire la convenzione C ed essere dichiarato come puntatore.</span><span class="sxs-lookup"><span data-stu-id="062bc-108">As an **\[out\]** parameter, the parameter *pcbOut* must follow C convention and be declared as a pointer.</span></span>

<span data-ttu-id="062bc-109">Il codice client conta il numero di caratteri nella stringa, incluso lo zero finale, prima di chiamare la procedura remota come illustrato:</span><span class="sxs-lookup"><span data-stu-id="062bc-109">The client code counts the number of characters in the string, including the trailing zero, before calling the remote procedure as shown:</span></span>

``` syntax
/* client */
char achIn[STRSIZE], achOut[STRSIZE];
long cbIn, cbOut;
...
gets_s(achIn, STRSIZE);                   // get patient input
cbIn = strlen(achIn) + 1;      // transmitted elements
Analyze(achIn, cbIn, achOut, &cbOut);
```

<span data-ttu-id="062bc-110">La procedura remota nel server fornisce la lunghezza del buffer restituito in *cbOut* , come illustrato:</span><span class="sxs-lookup"><span data-stu-id="062bc-110">The remote procedure on the server supplies the length of the return buffer in *cbOut* as shown:</span></span>

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

<span data-ttu-id="062bc-111">L' \[ attributo **stringa** \] può essere utilizzato quando un parametro è noto come una stringa.</span><span class="sxs-lookup"><span data-stu-id="062bc-111">The \[**string**\] attribute can be utilized when a parameter is known to be a string.</span></span> <span data-ttu-id="062bc-112">Questo attributo indirizza lo stub per calcolare le dimensioni della stringa, eliminando in tal modo l'overhead associato alla \[ [**lunghezza sono**](/windows/desktop/Midl/size-is) i \] parametri.</span><span class="sxs-lookup"><span data-stu-id="062bc-112">This attribute directs the stub to calculate the string size, thus eliminating the overhead associated with the \[[**length is**](/windows/desktop/Midl/size-is)\] parameters.</span></span> <span data-ttu-id="062bc-113">Consente inoltre di indirizzare lo stub per verificare che la stringa sia terminata con **null** prima di passare il parametro all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="062bc-113">Additionally, it will direct the stub to verify the string is **NULL** terminated before passing the parameter to the application.</span></span>

 

 