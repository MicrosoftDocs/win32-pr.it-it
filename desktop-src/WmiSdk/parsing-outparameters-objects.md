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
# <a name="parsing-outparameters-objects"></a><span data-ttu-id="8e70a-103">Analisi di oggetti OutParameters</span><span class="sxs-lookup"><span data-stu-id="8e70a-103">Parsing OutParameters Objects</span></span>

<span data-ttu-id="8e70a-104">Un oggetto [**SWbemMethod. OutParameters**](swbemmethod-outparameters.md) viene creato e fornito con i dati dal metodo del provider in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8e70a-104">A [**SWbemMethod.OutParameters**](swbemmethod-outparameters.md) object is created and supplied with data by the provider method that is executing.</span></span> <span data-ttu-id="8e70a-105">Le proprietà dell'oggetto **OutParameters** sono specifiche del metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="8e70a-105">Properties of the **OutParameters** object are specific to the method called.</span></span> <span data-ttu-id="8e70a-106">Nello script seguente, ad esempio, *SD* (contenuto in *outParam*) è il parametro di output definito per il metodo **\_ \_ SystemSecurity. getsd** .</span><span class="sxs-lookup"><span data-stu-id="8e70a-106">For example, in the script below, *SD* (contained in *outParam*) is the output parameter defined for the **\_\_SystemSecurity.GetSD** method.</span></span> <span data-ttu-id="8e70a-107">La proprietà **returnValue** è una proprietà generica disponibile per tutti gli oggetti **OutParameters** che contengono il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8e70a-107">The **ReturnValue** property is a generic property available for all **OutParameters** objects which contain the result of the operation.</span></span>

<span data-ttu-id="8e70a-108">Nell'esempio di codice seguente viene illustrato come ottenere parametri di output dall'esecuzione del metodo [**ottenuto**](--systemsecurity-getsd.md) nella classe [**\_ \_ SystemSecurity**](--systemsecurity.md) per il sistema locale.</span><span class="sxs-lookup"><span data-stu-id="8e70a-108">The following code example illustrates obtaining output parameters from executing the [**GetSD**](--systemsecurity-getsd.md) method in class [**\_\_SystemSecurity**](--systemsecurity.md) for the local system.</span></span>


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



<span data-ttu-id="8e70a-109">Per ulteriori informazioni, vedere [**SWbemMethod. InParameters**](swbemmethod-inparameters.md).</span><span class="sxs-lookup"><span data-stu-id="8e70a-109">For more information, see [**SWbemMethod.InParameters**](swbemmethod-inparameters.md).</span></span>

 

 



