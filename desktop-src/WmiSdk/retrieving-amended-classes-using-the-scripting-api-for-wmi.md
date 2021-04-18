---
description: Se si utilizza l'API di scripting per WMI per recuperare o archiviare informazioni sulle classi localizzate, specificare le impostazioni locali come parte di un moniker.
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
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309903"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="966d6-103">Recupero di classi modificate tramite l'API di scripting per WMI</span><span class="sxs-lookup"><span data-stu-id="966d6-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="966d6-104">Se si utilizza l'API di scripting per WMI per recuperare o archiviare informazioni sulle classi localizzate, specificare le impostazioni locali come parte di un moniker.</span><span class="sxs-lookup"><span data-stu-id="966d6-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="966d6-105">In alternativa, è possibile specificare il nome delle impostazioni locali nel parametro *strLocale* per il metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .</span><span class="sxs-lookup"><span data-stu-id="966d6-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="966d6-106">Durante la lettura o la scrittura di classi modificate, indicare di voler usare le definizioni di classe localizzate specificando [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) come flag per il parametro *iFlags* del metodo chiamato.</span><span class="sxs-lookup"><span data-stu-id="966d6-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="966d6-107">Per PowerShell, è possibile usare il parametro *-locale* su [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) per specificare le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="966d6-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="966d6-108">Nell'esempio di codice seguente viene illustrato come recuperare una classe localizzata utilizzando un moniker di scripting WMI o il parametro-locale.</span><span class="sxs-lookup"><span data-stu-id="966d6-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="966d6-109">Nell'esempio di codice seguente viene illustrato come impostare il parametro delle impostazioni locali e utilizzare il flag [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="966d6-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="966d6-110">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="966d6-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="966d6-111">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="966d6-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="966d6-112">Nella tabella seguente sono elencati i metodi che accettano il flag [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .</span><span class="sxs-lookup"><span data-stu-id="966d6-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="966d6-113">Metodo sincrono</span><span class="sxs-lookup"><span data-stu-id="966d6-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="966d6-114">Metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="966d6-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="966d6-115">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="966d6-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="966d6-116">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="966d6-117">**SWbemObject. sottoclassi\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="966d6-118">**SWbemObject. SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="966d6-119">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="966d6-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="966d6-120">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="966d6-121">**SWbemObject. Instances\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="966d6-122">**SWbemObject. InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="966d6-123">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="966d6-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="966d6-124">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="966d6-125">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="966d6-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="966d6-126">**SWbemServices. GetAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="966d6-127">**SWbemObject. Put\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="966d6-128">**SWbemObject. PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="966d6-129">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="966d6-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="966d6-130">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="966d6-131">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="966d6-132">**SWbemObject. ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="966d6-133">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="966d6-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="966d6-134">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="966d6-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="966d6-135">**SWbemObject. Associator\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="966d6-136">**SWbemObject. AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="966d6-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
