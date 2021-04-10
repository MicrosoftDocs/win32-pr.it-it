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
# <a name="in-out-string-prototype"></a>\[in, out, \] prototipo di stringa

Il prototipo di funzione seguente usa un singolo \[ parametro [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**stringa**](/windows/desktop/Midl/string) \] per le stringhe di input e di output. La stringa contiene prima di tutto l'input del paziente e viene quindi sovrascritta con la risposta Doctor, come illustrato:

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Questo esempio è simile a quello che ha utilizzato una stringa con un solo conteggio sia per l'input che per l'output. Come per l'esempio, l' \[ attributo [**size \_ è**](/windows/desktop/Midl/size-is) \] determinato dal numero di elementi allocati nel server. L' \[ [](/windows/desktop/Midl/string) \] attributo stringa indirizza lo stub alla chiamata di **strlen** per determinare il numero di elementi trasmessi.

Il client alloca tutta la memoria prima della chiamata a:

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Si noti che la funzione ANALYZE non è più in grado di calcolare la lunghezza della stringa restituita come nell'esempio di stringa calcolata in cui l'attributo **\[ stringa \]** non è stato usato. Ora gli stub calcolano la lunghezza come illustrato:

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 