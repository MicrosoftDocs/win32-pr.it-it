---
description: Usare il \_ metodo SpawnInstance dell'oggetto SWbemObject per creare una nuova istanza di una classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Metodo SWbemObject.SpawnInstance_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233804"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="a8a9f-103">SWbemObject. SpawnInstance, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="a8a9f-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="a8a9f-104">Usare il **metodo \_ SpawnInstance** dell'oggetto [**SWbemObject**](swbemobject.md) per creare una nuova istanza di una classe.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="a8a9f-105">L'oggetto corrente deve essere una definizione di classe ottenuta da WMI tramite un metodo, ad esempio [**SWbemServices. Get**](swbemservices-get.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="a8a9f-106">Usare quindi questa definizione di classe per creare nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="a8a9f-107">Creare ogni nuova istanza in locale all'interno del processo e quindi chiamare [**SWbemObject. \_ put**](swbemobject-put-.md) per creare effettivamente l'istanza in WMI.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="a8a9f-108">La generazione di un'istanza da un'istanza è supportata, ma l'istanza restituita è vuota.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="a8a9f-109">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a9f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8a9f-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a8a9f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8a9f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a9f-112">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a8a9f-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-113">Riservato e deve essere zero se specificato.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a9f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8a9f-114">Return value</span></span>

<span data-ttu-id="a8a9f-115">Se ha esito positivo, questa chiamata restituisce un oggetto [**SWbemObject**](swbemobject.md) che contiene una nuova istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8a9f-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a8a9f-116">Error codes</span></span>

<span data-ttu-id="a8a9f-117">Dopo il completamento del metodo **SpawnInstance \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="a8a9f-118">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="a8a9f-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-119">L'oggetto corrente non è una definizione di classe valida e non può generare nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="a8a9f-120">Il valore è incompleto o non è stato registrato con WMI mediante [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="a8a9f-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8a9f-121">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="a8a9f-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-122">Restituito se questo metodo viene utilizzato in un'istanza di anziché in una classe.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="a8a9f-123">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="a8a9f-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-124">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="a8a9f-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="a8a9f-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-126">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8a9f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8a9f-127">Requirements</span></span>



| <span data-ttu-id="a8a9f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a9f-128">Requirement</span></span> | <span data-ttu-id="a8a9f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a9f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a9f-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8a9f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a8a9f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8a9f-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8a9f-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8a9f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a8a9f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8a9f-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8a9f-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a8a9f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8a9f-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8a9f-136">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a8a9f-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8a9f-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a8a9f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="a8a9f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8a9f-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="a8a9f-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="a8a9f-140">CLSID</span></span><br/>                    | <span data-ttu-id="a8a9f-141">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="a8a9f-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="a8a9f-142">IID</span><span class="sxs-lookup"><span data-stu-id="a8a9f-142">IID</span></span><br/>                      | <span data-ttu-id="a8a9f-143">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="a8a9f-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="a8a9f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8a9f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a9f-145">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-146">**SWbemObject. Put\_**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="a8a9f-147">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




