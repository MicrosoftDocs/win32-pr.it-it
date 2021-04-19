---
description: Un oggetto SWbemPropertySet è una raccolta di oggetti SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Oggetto SWbemPropertySet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318498"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="6d537-103">Oggetto SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="6d537-103">SWbemPropertySet object</span></span>

<span data-ttu-id="6d537-104">Un oggetto **SWbemPropertySet** è una raccolta di oggetti [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="6d537-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="6d537-105">È possibile aggiungere elementi alla raccolta usando il metodo [**Add**](swbempropertyset-add.md) , recuperare gli elementi dalla raccolta usando il metodo [**Item**](swbempropertyset-item.md) e rimuovere gli elementi dalla raccolta usando il metodo [**Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="6d537-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="6d537-106">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="6d537-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="6d537-107">Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="6d537-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="6d537-108">Gli oggetti [**SWbemProperty**](swbemproperty.md) che costituiscono una raccolta **SWbemPropertySet** vengono utilizzati per descrivere le proprietà di una singola istanza o classe WMI.</span><span class="sxs-lookup"><span data-stu-id="6d537-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="6d537-109">Membri</span><span class="sxs-lookup"><span data-stu-id="6d537-109">Members</span></span>

<span data-ttu-id="6d537-110">L'oggetto **SWbemPropertySet** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6d537-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="6d537-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d537-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d537-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d537-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d537-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="6d537-113">Methods</span></span>

<span data-ttu-id="6d537-114">L'oggetto **SWbemPropertySet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6d537-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="6d537-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="6d537-115">Method</span></span>                                    | <span data-ttu-id="6d537-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d537-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d537-117">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="6d537-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="6d537-118">Aggiunge un oggetto [**SWbemProperty**](swbemproperty.md) alla raccolta **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="6d537-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="6d537-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6d537-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="6d537-120">Ottiene un oggetto denominato [**SWbemProperty**](swbemproperty.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6d537-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="6d537-121">Questo è il metodo predefinito per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6d537-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="6d537-122">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="6d537-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="6d537-123">Elimina un oggetto [**SWbemProperty**](swbemproperty.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6d537-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="6d537-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d537-124">Properties</span></span>

<span data-ttu-id="6d537-125">L'oggetto **SWbemPropertySet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6d537-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="6d537-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6d537-126">Property</span></span>                                           | <span data-ttu-id="6d537-127">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="6d537-127">Access type</span></span>          | <span data-ttu-id="6d537-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d537-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="6d537-129">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="6d537-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="6d537-130">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6d537-130">Read-only</span></span><br/> | <span data-ttu-id="6d537-131">Numero di elementi nella raccolta **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="6d537-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="6d537-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="6d537-132">Examples</span></span>

<span data-ttu-id="6d537-133">Nell'esempio VBScript seguente viene illustrato come [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) può restituire **wbemErrResetToDefault** se la proprietà viene sottoposta a override.</span><span class="sxs-lookup"><span data-stu-id="6d537-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="6d537-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d537-134">Requirements</span></span>



| <span data-ttu-id="6d537-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d537-135">Requirement</span></span> | <span data-ttu-id="6d537-136">Valore</span><span class="sxs-lookup"><span data-stu-id="6d537-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d537-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d537-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6d537-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6d537-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6d537-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d537-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6d537-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d537-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d537-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d537-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d537-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d537-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d537-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6d537-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="6d537-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6d537-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6d537-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6d537-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d537-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d537-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6d537-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="6d537-147">CLSID</span></span><br/>                    | <span data-ttu-id="6d537-148">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="6d537-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="6d537-149">IID</span><span class="sxs-lookup"><span data-stu-id="6d537-149">IID</span></span><br/>                      | <span data-ttu-id="6d537-150">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="6d537-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="6d537-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d537-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d537-152">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="6d537-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




