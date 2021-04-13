---
description: Un oggetto SWbemMethod. OutParameters viene creato e fornito con i dati dal metodo del provider in esecuzione.
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: Analisi di oggetti OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348896"
---
# <a name="parsing-outparameters-objects"></a>Analisi di oggetti OutParameters

Un oggetto [**SWbemMethod. OutParameters**](swbemmethod-outparameters.md) viene creato e fornito con i dati dal metodo del provider in esecuzione. Le proprietà dell'oggetto **OutParameters** sono specifiche del metodo chiamato. Nello script seguente, ad esempio, *SD* (contenuto in *outParam*) è il parametro di output definito per il metodo **\_ \_ SystemSecurity. getsd** . La proprietà **returnValue** è una proprietà generica disponibile per tutti gli oggetti **OutParameters** che contengono il risultato dell'operazione.

Nell'esempio di codice seguente viene illustrato come ottenere parametri di output dall'esecuzione del metodo [**ottenuto**](--systemsecurity-getsd.md) nella classe [**\_ \_ SystemSecurity**](--systemsecurity.md) per il sistema locale.


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



Per ulteriori informazioni, vedere [**SWbemMethod. InParameters**](swbemmethod-inparameters.md).

 

 



