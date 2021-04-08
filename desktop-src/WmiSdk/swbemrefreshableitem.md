---
description: Rappresenta un singolo elemento in un oggetto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Oggetto SWbemRefreshableItem (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761411"
---
# <a name="swbemrefreshableitem-object"></a><span data-ttu-id="ad921-103">Oggetto SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="ad921-103">SWbemRefreshableItem object</span></span>

<span data-ttu-id="ad921-104">L'oggetto **SWbemRefreshableItem** rappresenta un singolo elemento in un oggetto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="ad921-104">The **SWbemRefreshableItem** object represents a single item in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="ad921-105">Un oggetto **SWbemRefreshableItem** viene ottenuto tramite i metodi [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) di [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="ad921-105">An **SWbemRefreshableItem** object is obtained through the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods of [**SWbemRefresher**](swbemrefresher.md).</span></span> <span data-ttu-id="ad921-106">Questo oggetto non può essere creato dalla chiamata [CreateObject](creating-an-object-using-vbscript.md) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="ad921-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="ad921-107">Membri</span><span class="sxs-lookup"><span data-stu-id="ad921-107">Members</span></span>

<span data-ttu-id="ad921-108">L'oggetto **SWbemRefreshableItem** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ad921-108">The **SWbemRefreshableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="ad921-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ad921-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad921-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad921-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad921-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ad921-111">Methods</span></span>

<span data-ttu-id="ad921-112">L'oggetto **SWbemRefreshableItem** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ad921-112">The **SWbemRefreshableItem** object has these methods.</span></span>



| <span data-ttu-id="ad921-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="ad921-113">Method</span></span>                                        | <span data-ttu-id="ad921-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad921-114">Description</span></span>                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad921-115">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="ad921-115">**Remove**</span></span>](swbemrefreshableitem-remove.md) | <span data-ttu-id="ad921-116">Rimuove l'oggetto **SWbemRefreshableItem** dall'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.</span><span class="sxs-lookup"><span data-stu-id="ad921-116">Removes the **SWbemRefreshableItem** object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ad921-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad921-117">Properties</span></span>

<span data-ttu-id="ad921-118">L'oggetto **SWbemRefreshableItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ad921-118">The **SWbemRefreshableItem** object has these properties.</span></span>



| <span data-ttu-id="ad921-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ad921-119">Property</span></span>                                                       | <span data-ttu-id="ad921-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ad921-120">Access type</span></span>           | <span data-ttu-id="ad921-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad921-121">Description</span></span>                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad921-122">**Indice**</span><span class="sxs-lookup"><span data-stu-id="ad921-122">**Index**</span></span>](swbemrefreshableitem-index.md)<br/>         | <span data-ttu-id="ad921-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ad921-123">Read/write</span></span><br/> | <span data-ttu-id="ad921-124">Indice dell'elemento nell'oggetto [**SWbemRefresher**](swbemrefresher.md) padre.</span><span class="sxs-lookup"><span data-stu-id="ad921-124">Index of the item in its parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/>                                          |
| [<span data-ttu-id="ad921-125">**IsSet**</span><span class="sxs-lookup"><span data-stu-id="ad921-125">**IsSet**</span></span>](swbemrefreshableitem-isset.md)<br/>         | <span data-ttu-id="ad921-126">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ad921-126">Read/write</span></span><br/> | <span data-ttu-id="ad921-127">Indica se l'oggetto **SWbemRefreshableItem** rappresenta un singolo oggetto o un set di oggetti.</span><span class="sxs-lookup"><span data-stu-id="ad921-127">Indicates whether the **SWbemRefreshableItem** object represents a single object or an object set.</span></span><br/>                        |
| [<span data-ttu-id="ad921-128">**Oggetto**</span><span class="sxs-lookup"><span data-stu-id="ad921-128">**Object**</span></span>](swbemrefreshableitem-object.md)<br/>       | <span data-ttu-id="ad921-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ad921-129">Read/write</span></span><br/> | <span data-ttu-id="ad921-130">Rappresenta un singolo oggetto [**SWbemObject**](swbemobject.md) che viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ad921-130">Represents a single [**SWbemObject**](swbemobject.md) object that is refreshed.</span></span><br/>                                          |
| [<span data-ttu-id="ad921-131">**ObjectSet**</span><span class="sxs-lookup"><span data-stu-id="ad921-131">**ObjectSet**</span></span>](swbemrefreshableitem-objectset.md)<br/> | <span data-ttu-id="ad921-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ad921-132">Read/write</span></span><br/> | <span data-ttu-id="ad921-133">Rappresenta il set di oggetti da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="ad921-133">Represents the object set to be refreshed.</span></span><br/>                                                                                |
| [<span data-ttu-id="ad921-134">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="ad921-134">**Refresher**</span></span>](swbemrefreshableitem-refresher.md)<br/> | <span data-ttu-id="ad921-135">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="ad921-135">Read-only</span></span><br/>  | <span data-ttu-id="ad921-136">Rappresenta l'oggetto [**SWbemRefresher**](swbemrefresher.md) padre che contiene l'oggetto **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="ad921-136">Represents the parent [**SWbemRefresher**](swbemrefresher.md) object which contains the **SWbemRefreshableItem** object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad921-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad921-137">Remarks</span></span>

<span data-ttu-id="ad921-138">Non è possibile usare il metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) per creare direttamente oggetti **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="ad921-138">The VBScript method [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) cannot be used to create **SWbemRefreshableItem** objects directly.</span></span>

## <a name="examples"></a><span data-ttu-id="ad921-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad921-139">Examples</span></span>

<span data-ttu-id="ad921-140">Nello script seguente viene illustrata la creazione di un oggetto [**SWbemRefresher**](swbemrefresher.md) e l'aggiunta di un singolo oggetto e di un enumeratore **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="ad921-140">The following script illustrates the creation of an [**SWbemRefresher**](swbemrefresher.md) object and the addition of single object and enumerator **SWbemRefreshableItem** to it.</span></span>


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a><span data-ttu-id="ad921-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad921-141">Requirements</span></span>



| <span data-ttu-id="ad921-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad921-142">Requirement</span></span> | <span data-ttu-id="ad921-143">Valore</span><span class="sxs-lookup"><span data-stu-id="ad921-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad921-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad921-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ad921-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad921-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad921-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad921-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ad921-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad921-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad921-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad921-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad921-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad921-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad921-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ad921-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="ad921-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ad921-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ad921-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ad921-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad921-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad921-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ad921-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="ad921-154">CLSID</span></span><br/>                    | <span data-ttu-id="ad921-155">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="ad921-155">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="ad921-156">IID</span><span class="sxs-lookup"><span data-stu-id="ad921-156">IID</span></span><br/>                      | <span data-ttu-id="ad921-157">\_ISWBEMREFRESHABLEITEM IID</span><span class="sxs-lookup"><span data-stu-id="ad921-157">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="ad921-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad921-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad921-159">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="ad921-159">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




