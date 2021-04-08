---
description: La \_ proprietà Path dell'oggetto SWbemLastError restituisce un oggetto SWbemObjectPath che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente. Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: Proprietà SWbemLastError.Path_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050230"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="f6397-104">Proprietà SWbemLastError. Path \_</span><span class="sxs-lookup"><span data-stu-id="f6397-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="f6397-105">La **proprietà \_ path** dell'oggetto [**SWbemLastError**](swbemlasterror.md) restituisce un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="f6397-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="f6397-106">Questa proprietà può essere passata come parametro ai metodi che richiedono un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f6397-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="f6397-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f6397-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f6397-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f6397-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6397-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6397-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="f6397-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f6397-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f6397-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6397-111">Remarks</span></span>

<span data-ttu-id="f6397-112">È possibile modificare solo la proprietà [**Class**](swbemobjectpath-class.md) dell'istanza [**SWbemObjectPath**](swbemobjectpath.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="f6397-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="f6397-113">Se si tenta di modificare qualsiasi altra proprietà o si tenta di chiamare i metodi [**SetAsClass**](swbemobjectpath-setasclass.md) o [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , si ottiene un errore di **wbemErrReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="f6397-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="f6397-114">Per questo motivo, non è possibile modificare l'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che corrisponde al valore della proprietà [**Keys**](swbemobjectpath-keys.md) dell'istanza di [**SWbemObjectPath**](swbemobjectpath.md) restituita.</span><span class="sxs-lookup"><span data-stu-id="f6397-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="f6397-115">Se si tenta di chiamare i metodi [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)o [**DeleteAll**](swbemnamedvalueset-deleteall.md) su questo valore, si ottiene un errore **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="f6397-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="f6397-116">Non è inoltre possibile modificare i [**SWbemNamedValue**](swbemnamedvalue.md) ottenuti da questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="f6397-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="f6397-117">I tentativi di modificare la proprietà [**value**](swbemnamedvalue-value.md) restituiscono lo stesso codice di errore.</span><span class="sxs-lookup"><span data-stu-id="f6397-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="f6397-118">Tuttavia, se si chiama [**SWbemObject. Clone \_**](swbemobject-clone-.md) per creare una copia, la [**proprietà \_ path**](swbemobject-path-.md) della copia è completamente modificabile.</span><span class="sxs-lookup"><span data-stu-id="f6397-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6397-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6397-119">Requirements</span></span>



| <span data-ttu-id="f6397-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6397-120">Requirement</span></span> | <span data-ttu-id="f6397-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f6397-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6397-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6397-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6397-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6397-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f6397-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6397-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6397-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6397-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f6397-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6397-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6397-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6397-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6397-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f6397-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6397-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f6397-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f6397-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f6397-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6397-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6397-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f6397-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="f6397-132">CLSID</span></span><br/>                    | <span data-ttu-id="f6397-133">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="f6397-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="f6397-134">IID</span><span class="sxs-lookup"><span data-stu-id="f6397-134">IID</span></span><br/>                      | <span data-ttu-id="f6397-135">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="f6397-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




