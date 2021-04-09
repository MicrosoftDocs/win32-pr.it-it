---
description: L'oggetto SWbemRefresher è un oggetto contenitore in grado di aggiornare i dati per tutti gli oggetti aggiunti. Il set di oggetti aggiunti, ogni elemento rappresentato da un'istanza di SWbemRefreshableItem può essere considerato come una raccolta ed enumerata.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Oggetto SWbemRefresher (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968929"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="6323d-104">Oggetto SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="6323d-104">SWbemRefresher object</span></span>

<span data-ttu-id="6323d-105">L'oggetto **SWbemRefresher** è un oggetto contenitore in grado di aggiornare i dati per tutti gli oggetti aggiunti.</span><span class="sxs-lookup"><span data-stu-id="6323d-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="6323d-106">Le istanze singole e gli enumeratori di istanza possono essere aggiunti o rimossi dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="6323d-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="6323d-107">Il set di oggetti aggiunti, ogni elemento rappresentato da un'istanza di [**SWbemRefreshableItem**](swbemrefreshableitem.md) , può essere considerato come una raccolta ed enumerata.</span><span class="sxs-lookup"><span data-stu-id="6323d-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="6323d-108">Le istanze WMI di qualsiasi classe possono essere aggiunte all'oggetto **SWbemRefresher** .</span><span class="sxs-lookup"><span data-stu-id="6323d-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="6323d-109">Anche se il provider per i dati dell'istanza non è un provider a prestazioni elevate, l'oggetto di aggiornamento può comunque aggiornare i dati nella chiamata di [**aggiornamento**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="6323d-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="6323d-110">Se i dati vengono forniti tramite un provider a prestazioni elevate e la proprietà [**AutoReconnect**](swbemrefresher-autoreconnect.md) è **true**, l'oggetto **SWbemRefresher** tenta di ristabilire una connessione interruppe al provider di dati.</span><span class="sxs-lookup"><span data-stu-id="6323d-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="6323d-111">Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="6323d-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="6323d-112">È possibile eseguire l'operazione di aggiornamento chiamando il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) o [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="6323d-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="6323d-113">Membri</span><span class="sxs-lookup"><span data-stu-id="6323d-113">Members</span></span>

<span data-ttu-id="6323d-114">L'oggetto **SWbemRefresher** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6323d-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="6323d-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="6323d-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="6323d-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6323d-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6323d-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="6323d-117">Methods</span></span>

<span data-ttu-id="6323d-118">L'oggetto **SWbemRefresher** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6323d-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="6323d-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="6323d-119">Method</span></span>                                        | <span data-ttu-id="6323d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6323d-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6323d-121">**Aggiungere**</span><span class="sxs-lookup"><span data-stu-id="6323d-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="6323d-122">Aggiunge un nuovo oggetto aggiornabile alla raccolta nell'oggetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6323d-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="6323d-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="6323d-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="6323d-124">Aggiunge un nuovo enumeratore all'oggetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6323d-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="6323d-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="6323d-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="6323d-126">Rimuove tutti gli elementi dalla raccolta nell'oggetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6323d-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="6323d-127">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6323d-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="6323d-128">Restituisce un elemento di aggiornamento specificato dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6323d-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="6323d-129">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="6323d-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="6323d-130">Aggiorna tutti gli elementi contenuti nell'oggetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6323d-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="6323d-131">**Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="6323d-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="6323d-132">Rimuove dall'aggiornamento l'oggetto o il set di oggetti dell'elemento di aggiornamento con un indice specificato.</span><span class="sxs-lookup"><span data-stu-id="6323d-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6323d-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6323d-133">Properties</span></span>

<span data-ttu-id="6323d-134">L'oggetto **SWbemRefresher** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6323d-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="6323d-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6323d-135">Property</span></span>                                                         | <span data-ttu-id="6323d-136">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="6323d-136">Access type</span></span>          | <span data-ttu-id="6323d-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6323d-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6323d-138">**AutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="6323d-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="6323d-139">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6323d-139">Read-only</span></span><br/> | <span data-ttu-id="6323d-140">Indica se l'aggiornamento viene riconnesso automaticamente a un provider remoto se la connessione è interruppe.</span><span class="sxs-lookup"><span data-stu-id="6323d-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="6323d-141">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="6323d-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="6323d-142">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6323d-142">Read-only</span></span><br/> | <span data-ttu-id="6323d-143">Contiene il numero di elementi nell'oggetto di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="6323d-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="6323d-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="6323d-144">Examples</span></span>

<span data-ttu-id="6323d-145">Nell'esempio seguente viene illustrata la creazione di un oggetto **SWbemRefresher** , l'utilizzo dei metodi [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) per archiviare una singola istanza e un'istanza di enumerazione, l'aggiornamento dei dati e l'utilizzo della proprietà Item per ottenere gli oggetti [**SWbemRefreshableItem**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="6323d-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="6323d-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6323d-146">Requirements</span></span>



| <span data-ttu-id="6323d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="6323d-147">Requirement</span></span> | <span data-ttu-id="6323d-148">Valore</span><span class="sxs-lookup"><span data-stu-id="6323d-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6323d-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6323d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6323d-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6323d-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6323d-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6323d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6323d-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6323d-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6323d-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6323d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="6323d-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6323d-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6323d-155">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6323d-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="6323d-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6323d-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6323d-157">DLL</span><span class="sxs-lookup"><span data-stu-id="6323d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6323d-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6323d-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6323d-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="6323d-159">CLSID</span></span><br/>                    | <span data-ttu-id="6323d-160">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="6323d-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="6323d-161">IID</span><span class="sxs-lookup"><span data-stu-id="6323d-161">IID</span></span><br/>                      | <span data-ttu-id="6323d-162">\_ISWBEMREFRESHER IID</span><span class="sxs-lookup"><span data-stu-id="6323d-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="6323d-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6323d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6323d-164">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="6323d-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="6323d-165">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="6323d-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="6323d-166">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="6323d-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




