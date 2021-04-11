---
description: La \_ proprietà Path dell'oggetto SWbemObject restituisce un oggetto SWbemObjectPath che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Proprietà SWbemObject.Path_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232206"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="5ab1e-104">Proprietà SWbemObject. Path \_</span><span class="sxs-lookup"><span data-stu-id="5ab1e-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="5ab1e-105">La **proprietà \_ path** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="5ab1e-106">Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="5ab1e-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5ab1e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5ab1e-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab1e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ab1e-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="5ab1e-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5ab1e-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab1e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ab1e-111">Remarks</span></span>

<span data-ttu-id="5ab1e-112">È possibile modificare solo la proprietà [**Class**](swbemobjectpath-class.md) dell'istanza [**SWbemObjectPath**](swbemobjectpath.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="5ab1e-113">Se si tenta di modificare qualsiasi altra proprietà o si tenta di chiamare i metodi [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md), si otterrà un errore **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="5ab1e-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="5ab1e-114">Per questo motivo, non è possibile modificare l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che corrisponde al valore della proprietà [**Keys**](swbemobjectpath-keys.md) dell'istanza di [**SWbemObjectPath**](swbemobjectpath.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="5ab1e-115">Se si tenta di chiamare i metodi [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) su questo valore, si otterrà un errore wbemErrReadOnly.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="5ab1e-116">Non è inoltre possibile modificare i [**SWbemNamedValue**](swbemnamedvalue.md) ottenuti da questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="5ab1e-117">I tentativi di modificare la proprietà **value** restituiscono lo stesso codice di errore.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="5ab1e-118">Tuttavia, se si chiama [**SWbemObject. Clone \_**](swbemobject-clone-.md) per creare una copia, la proprietà [**SWbemObjectPath. Path**](swbemobjectpath-path.md) della copia è completamente modificabile.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="5ab1e-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5ab1e-119">Examples</span></span>

<span data-ttu-id="5ab1e-120">Nell'esempio di codice seguente, tratto da un [elenco di tutte le classi WMI cimV2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) nella raccolta TechNet, viene utilizzata la \_ proprietà Path per elencare tutte le classi cimV2 di WMI.</span><span class="sxs-lookup"><span data-stu-id="5ab1e-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="5ab1e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ab1e-121">Requirements</span></span>



| <span data-ttu-id="5ab1e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab1e-122">Requirement</span></span> | <span data-ttu-id="5ab1e-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5ab1e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab1e-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ab1e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab1e-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ab1e-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ab1e-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ab1e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab1e-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ab1e-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ab1e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ab1e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab1e-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab1e-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ab1e-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5ab1e-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ab1e-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ab1e-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ab1e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5ab1e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ab1e-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ab1e-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ab1e-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="5ab1e-134">CLSID</span></span><br/>                    | <span data-ttu-id="5ab1e-135">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="5ab1e-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="5ab1e-136">IID</span><span class="sxs-lookup"><span data-stu-id="5ab1e-136">IID</span></span><br/>                      | <span data-ttu-id="5ab1e-137">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="5ab1e-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




