---
title: " in, out, prototipo di stringa"
description: Il prototipo di funzione seguente usa un singolo parametro \ in, out, String \ per entrambe le stringhe di input e di output.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963188"
---
# <a name="in-out-string-prototype"></a><span data-ttu-id="125bb-103">\[in, out, \] prototipo di stringa</span><span class="sxs-lookup"><span data-stu-id="125bb-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="125bb-104">Il prototipo di funzione seguente usa un singolo \[ parametro [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**stringa**](/windows/desktop/Midl/string) \] per le stringhe di input e di output.</span><span class="sxs-lookup"><span data-stu-id="125bb-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="125bb-105">La stringa contiene prima di tutto l'input del paziente e viene quindi sovrascritta con la risposta Doctor, come illustrato:</span><span class="sxs-lookup"><span data-stu-id="125bb-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="125bb-106">Questo esempio è simile a quello che ha utilizzato una stringa con un solo conteggio sia per l'input che per l'output.</span><span class="sxs-lookup"><span data-stu-id="125bb-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="125bb-107">Come per l'esempio, l' \[ attributo [**size \_ è**](/windows/desktop/Midl/size-is) \] determinato dal numero di elementi allocati nel server.</span><span class="sxs-lookup"><span data-stu-id="125bb-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="125bb-108">L' \[ [](/windows/desktop/Midl/string) \] attributo stringa indirizza lo stub alla chiamata di **strlen** per determinare il numero di elementi trasmessi.</span><span class="sxs-lookup"><span data-stu-id="125bb-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="125bb-109">Il client alloca tutta la memoria prima della chiamata a:</span><span class="sxs-lookup"><span data-stu-id="125bb-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="125bb-110">Si noti che la funzione ANALYZE non è più in grado di calcolare la lunghezza della stringa restituita come nell'esempio di stringa calcolata in cui l'attributo **\[ stringa \]** non è stato usato.</span><span class="sxs-lookup"><span data-stu-id="125bb-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="125bb-111">Ora gli stub calcolano la lunghezza come illustrato:</span><span class="sxs-lookup"><span data-stu-id="125bb-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 