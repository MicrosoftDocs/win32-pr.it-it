---
description: Se si usa l'API di scripting per WMI per recuperare o archiviare informazioni sulla classe localizzata, specificare le impostazioni locali come parte di un moniker.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Recupero di classi modificate tramite l'API di scripting per WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47d01af2515b26ca308a1b258aa40508f227a0c1d0eaa5b2b332c1e7b3200420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130883"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Recupero di classi modificate tramite l'API di scripting per WMI

Se si usa l'API di scripting per WMI per recuperare o archiviare informazioni sulla classe localizzata, specificare le impostazioni locali come parte di un moniker. In caso contrario, è possibile fornire il nome delle impostazioni locali nel *parametro strLocale* al [**metodo SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md) Durante la lettura o la scrittura di classi modificate, indicare che si vogliono usare definizioni di classe localizzate specificando [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) come flag per il *parametro iFlags* del metodo chiamato. Per PowerShell, è possibile usare il *parametro -locale* in [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) per specificare le impostazioni locali.

Nell'esempio di codice seguente viene illustrato come recuperare una classe localizzata utilizzando un moniker di scripting WMI o il parametro -locale.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





Nell'esempio di codice seguente viene illustrato come impostare il parametro delle impostazioni locali e usare il flag [wbemFlagUseAmendedQualifiers.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrono anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

Nella tabella seguente sono elencati i metodi che accettano il flag [wbemFlagUseAmendedQualifiers.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)



| Metodo sincrono                                                 | Metodo asincrono                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)   | [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject.Subclasses\_**](swbemobject-subclasses-.md)        | [**SWbemObject.SubclassesAsync\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)     | [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)     |
| [**SWbemObject.Instances\_**](swbemobject-instances-.md)          | [**SWbemObject.InstancesAsync\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExecQuery**](swbemservices-execquery.md)         | [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)         |
| [**SWbemServices.Get**](swbemservices-get.md)                     | [**SWbemServices.GetAsync**](swbemservices-getasync.md)                     |
| [**SWbemObject.Put\_**](swbemobject-put-.md)                      | [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)   | [**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)   |
| [**SWbemObject.References\_**](swbemobject-references-.md)        | [**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md) | [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md) |
| [**SWbemObject.Associators\_**](swbemobject-associators-.md)      | [**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)      |



 

 

 
