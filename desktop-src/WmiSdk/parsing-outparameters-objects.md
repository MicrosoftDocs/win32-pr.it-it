---
description: Un oggetto SWbemMethod.OutParameters viene creato e fornito con dati dal metodo del provider in esecuzione.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analisi di oggetti OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69c13e7d4d6b74f1c404c77e1ae0cc26d62ad698684ca1c864ebf31871dc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923249"
---
# <a name="parsing-outparameters-objects"></a>Analisi di oggetti OutParameters

Un [**oggetto SWbemMethod.OutParameters**](swbemmethod-outparameters.md) viene creato e fornito con dati dal metodo del provider in esecuzione. Le proprietà **dell'oggetto OutParameters** sono specifiche del metodo chiamato. Ad esempio, nello script *seguente, SD* (contenuto in *outParam*) è il parametro di output definito per il **\_ \_ metodo SystemSecurity.GetSD.** La **proprietà ReturnValue** è una proprietà generica disponibile per tutti **gli oggetti OutParameters** che contengono il risultato dell'operazione.

L'esempio di codice seguente illustra come ottenere parametri di output dall'esecuzione del [**metodo GetSD**](--systemsecurity-getsd.md) nella [**\_ \_ classe SystemSecurity**](--systemsecurity.md) per il sistema locale.


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



Per altre informazioni, vedere [**SWbemMethod.InParameters.**](swbemmethod-inparameters.md)

 

 



