---
description: Il metodo Remove dell'oggetto SWbemPropertySet Elimina una proprietà dalla raccolta SWbemPropertySet.
ms.assetid: 2a1005db-033c-48f9-8ea0-0bd43b8c989f
ms.tgt_platform: multiple
title: Metodo SWbemPropertySet. Remove (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Remove
- ISWbemPropertySet.Remove
- ISWbemPropertySet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5b6903ae05c801d5903754ef8df0bb02cad51204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130979"
---
# <a name="swbempropertysetremove-method"></a><span data-ttu-id="5c4c5-103">Metodo SWbemPropertySet. Remove</span><span class="sxs-lookup"><span data-stu-id="5c4c5-103">SWbemPropertySet.Remove method</span></span>

<span data-ttu-id="5c4c5-104">Il metodo **Remove** dell'oggetto [**SWbemPropertySet**](swbempropertyset.md) Elimina una proprietà dalla raccolta **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="5c4c5-104">The **Remove** method of the [**SWbemPropertySet**](swbempropertyset.md) object deletes a property from the **SWbemPropertySet** collection.</span></span>

<span data-ttu-id="5c4c5-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5c4c5-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4c5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c4c5-106">Syntax</span></span>


```VB
SWbemPropertySet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5c4c5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c4c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4c5-108">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4c5-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-109">Required.</span></span> <span data-ttu-id="5c4c5-110">Nome dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-110">Name of the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-111">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5c4c5-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-112">Reserved.</span></span> <span data-ttu-id="5c4c5-113">Se specificato, questo valore deve essere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5c4c5-113">This value must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4c5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c4c5-114">Return value</span></span>

<span data-ttu-id="5c4c5-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c4c5-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5c4c5-116">Error codes</span></span>

<span data-ttu-id="5c4c5-117">Dopo il completamento del metodo **Remove** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="5c4c5-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-119">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-119">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-120">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-120">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-121">L'utente ha tentato di eliminare una proprietà che non può essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-121">User attempted to delete a property that cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-123">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-125">La proprietà specificata non esiste.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-125">Specified property does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-126">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-126">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-127">Memoria insufficiente per l'esecuzione di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-127">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-128">**wbemErrPropagatedProperty** -142927303552 (0x2147219380)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-128">**wbemErrPropagatedProperty** - 142927303552 (0x2147219380)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-129">L'utente ha tentato di eliminare una proprietà che non possedeva.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-129">User attempted to delete a property that was not owned.</span></span> <span data-ttu-id="5c4c5-130">La proprietà è stata ereditata da una classe padre.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-130">The property was inherited from a parent class.</span></span>

</dd> <dt>

<span data-ttu-id="5c4c5-131">**wbemErrResetToDefault** -2147758082 (0x80043002)</span><span class="sxs-lookup"><span data-stu-id="5c4c5-131">**wbemErrResetToDefault** - 2147758082 (0x80043002)</span></span>
</dt> <dd>

<span data-ttu-id="5c4c5-132">L'utente ha eliminato un valore predefinito di sostituzione per la classe corrente.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-132">User deleted an override default value for the current class.</span></span> <span data-ttu-id="5c4c5-133">Il valore predefinito per questa proprietà nella classe padre è stato riattivato.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-133">The default value for this property in the parent class has been reactivated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c4c5-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c4c5-134">Remarks</span></span>

<span data-ttu-id="5c4c5-135">Non è possibile rimuovere le proprietà dalle istanze della classe o dalle classi derivate con proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-135">Properties cannot be removed from class instances or derived classes with inherited properties.</span></span> <span data-ttu-id="5c4c5-136">Tali tentativi di eliminazione generano un errore e la proprietà non viene rimossa. la proprietà viene reimpostata sul valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-136">Such deletion attempts raise an error and the property is not removed; the property is reset to its default value.</span></span>

<span data-ttu-id="5c4c5-137">Non è possibile eseguire l'iterazione di una raccolta durante la rimozione degli elementi perché quando si rimuove un elemento da una raccolta, il puntatore alla raccolta viene spostato nell'elemento successivo.</span><span class="sxs-lookup"><span data-stu-id="5c4c5-137">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="5c4c5-138">Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="5c4c5-138">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c4c5-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c4c5-139">Examples</span></span>

<span data-ttu-id="5c4c5-140">Per un esempio di codice che usa questo metodo, vedere l'argomento [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="5c4c5-140">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4c5-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c4c5-141">Requirements</span></span>



| <span data-ttu-id="5c4c5-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c4c5-142">Requirement</span></span> | <span data-ttu-id="5c4c5-143">Valore</span><span class="sxs-lookup"><span data-stu-id="5c4c5-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4c5-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c4c5-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5c4c5-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c4c5-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c4c5-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c4c5-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5c4c5-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c4c5-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c4c5-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c4c5-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c4c5-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c4c5-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c4c5-150">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5c4c5-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c4c5-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c4c5-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c4c5-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5c4c5-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c4c5-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c4c5-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c4c5-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c4c5-154">CLSID</span></span><br/>                    | <span data-ttu-id="5c4c5-155">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="5c4c5-155">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="5c4c5-156">IID</span><span class="sxs-lookup"><span data-stu-id="5c4c5-156">IID</span></span><br/>                      | <span data-ttu-id="5c4c5-157">\_ISWBEMPROPERTYSET IID</span><span class="sxs-lookup"><span data-stu-id="5c4c5-157">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="5c4c5-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c4c5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4c5-159">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="5c4c5-159">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="5c4c5-160">**SWbemPropertySet. Add**</span><span class="sxs-lookup"><span data-stu-id="5c4c5-160">**SWbemPropertySet.Add**</span></span>](swbempropertyset-add.md)
</dt> </dl>

 

 




