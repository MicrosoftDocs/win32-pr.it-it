---
description: Usare il \_ Metodo SpawnDerivedClass dell'oggetto SWbemObject per creare un oggetto classe derivata dall'oggetto corrente. L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Metodo SWbemObject.SpawnDerivedClass_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226814"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="993b7-104">SWbemObject. SpawnDerivedClass, \_ Metodo</span><span class="sxs-lookup"><span data-stu-id="993b7-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="993b7-105">Usare il **metodo \_ SpawnDerivedClass** dell'oggetto [**SWbemObject**](swbemobject.md) per creare un oggetto classe derivata dall'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="993b7-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="993b7-106">L'oggetto deve essere una definizione di classe che diventa la classe padre dell'oggetto generato.</span><span class="sxs-lookup"><span data-stu-id="993b7-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="993b7-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="993b7-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="993b7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="993b7-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="993b7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="993b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="993b7-110">*iFlags* \[ opzionale\]</span><span class="sxs-lookup"><span data-stu-id="993b7-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="993b7-111">Riservato e deve essere 0 (zero) se specificato.</span><span class="sxs-lookup"><span data-stu-id="993b7-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="993b7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="993b7-112">Return value</span></span>

<span data-ttu-id="993b7-113">Se la chiamata ha esito positivo, l'oggetto [**SWbemObject**](swbemobject.md) contiene il nuovo oggetto definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="993b7-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="993b7-114">Non viene restituito alcun oggetto quando si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="993b7-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="993b7-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="993b7-115">Error codes</span></span>

<span data-ttu-id="993b7-116">Dopo il completamento del metodo **SpawnDerivedClass \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="993b7-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="993b7-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="993b7-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="993b7-118">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="993b7-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="993b7-119">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="993b7-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="993b7-120">L'utente ha richiesto un'operazione non valida, ad esempio la generazione di una classe da un'istanza.</span><span class="sxs-lookup"><span data-stu-id="993b7-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="993b7-121">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="993b7-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="993b7-122">La classe di origine non è stata completamente definita o è stata registrata con WMI, pertanto non è consentita una nuova classe derivata.</span><span class="sxs-lookup"><span data-stu-id="993b7-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="993b7-123">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="993b7-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="993b7-124">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="993b7-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="993b7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="993b7-125">Remarks</span></span>

<span data-ttu-id="993b7-126">L'oggetto restituito diventa automaticamente una sottoclasse dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="993b7-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="993b7-127">Non è possibile eseguire l'override di questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="993b7-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="993b7-128">Non esiste un altro metodo tramite il quale è possibile creare classi derivate.</span><span class="sxs-lookup"><span data-stu-id="993b7-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="993b7-129">Non è possibile creare una classe derivata da una classe locale per il proprio processo client.</span><span class="sxs-lookup"><span data-stu-id="993b7-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="993b7-130">Prima di usare questo metodo per creare una classe derivata, è necessario creare la classe di base.</span><span class="sxs-lookup"><span data-stu-id="993b7-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="993b7-131">Per creare la classe di base, chiamare [**SWbemObject. \_ put**](swbemobject-put-.md)e recuperare la classe di base utilizzando [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="993b7-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="993b7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="993b7-132">Requirements</span></span>



| <span data-ttu-id="993b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="993b7-133">Requirement</span></span> | <span data-ttu-id="993b7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="993b7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="993b7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="993b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="993b7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="993b7-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="993b7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="993b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="993b7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="993b7-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="993b7-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="993b7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="993b7-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="993b7-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="993b7-141">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="993b7-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="993b7-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="993b7-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="993b7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="993b7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="993b7-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="993b7-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="993b7-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="993b7-145">CLSID</span></span><br/>                    | <span data-ttu-id="993b7-146">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="993b7-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="993b7-147">IID</span><span class="sxs-lookup"><span data-stu-id="993b7-147">IID</span></span><br/>                      | <span data-ttu-id="993b7-148">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="993b7-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




