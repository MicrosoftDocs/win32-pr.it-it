---
description: Il metodo Item dell'oggetto SWbemObjectSet ottiene un SWbemObject dalla raccolta.
ms.assetid: da91683c-9895-4110-9f51-c340a0c52aec
ms.tgt_platform: multiple
title: Metodo SWbemObjectSet. Item (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Item
- ISWbemObjectSet.Item
- ISWbemObjectSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 69267b86a45cc1b95160e1400440b868426b7cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309801"
---
# <a name="swbemobjectsetitem-method"></a><span data-ttu-id="ac282-103">Metodo SWbemObjectSet. Item</span><span class="sxs-lookup"><span data-stu-id="ac282-103">SWbemObjectSet.Item method</span></span>

<span data-ttu-id="ac282-104">Il metodo **Item** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) ottiene un [**SWbemObject**](swbemobject.md) dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="ac282-104">The **Item** method of the [**SWbemObjectSet**](swbemobjectset.md) object gets an [**SWbemObject**](swbemobject.md) from the collection.</span></span>

<span data-ttu-id="ac282-105">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ac282-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ac282-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac282-106">Syntax</span></span>


```VB
objWbemObject = .Item( _
  ByVal strObjectPath _
)
```



## <a name="parameters"></a><span data-ttu-id="ac282-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac282-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac282-108">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="ac282-108">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="ac282-109">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac282-109">Required.</span></span> <span data-ttu-id="ac282-110">Percorso relativo dell'oggetto da recuperare dall'insieme.</span><span class="sxs-lookup"><span data-stu-id="ac282-110">Relative path of the object to retrieve from the collection.</span></span> <span data-ttu-id="ac282-111">Esempio: Win32 \_ disco logico = "C:"</span><span class="sxs-lookup"><span data-stu-id="ac282-111">Example: Win32\_LogicalDisk="C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac282-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac282-112">Return value</span></span>

<span data-ttu-id="ac282-113">In caso di esito positivo, l'oggetto [**SWbemObject**](swbemobject.md) richiesto restituisce.</span><span class="sxs-lookup"><span data-stu-id="ac282-113">If successful, the requested [**SWbemObject**](swbemobject.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ac282-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ac282-114">Error codes</span></span>

<span data-ttu-id="ac282-115">Al termine del metodo **Item** , l'oggetto **Err** può contenere uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ac282-115">Upon completion of the **Item** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="ac282-116">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ac282-116">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ac282-117">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="ac282-117">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ac282-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ac282-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ac282-119">È stato specificato un parametro non valido.</span><span class="sxs-lookup"><span data-stu-id="ac282-119">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="ac282-120">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ac282-120">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ac282-121">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ac282-121">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ac282-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="ac282-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="ac282-123">L'elemento richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="ac282-123">Requested item was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ac282-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac282-124">Remarks</span></span>

<span data-ttu-id="ac282-125">Il metodo **Item** può richiedere molto tempo del processore perché per restituire il risultato è necessaria un'enumerazione completa da parte del provider degli elementi del set.</span><span class="sxs-lookup"><span data-stu-id="ac282-125">The **Item** method can require a lot of processor time because complete enumeration by the provider of the elements of the set is required to return the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac282-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac282-126">Requirements</span></span>



| <span data-ttu-id="ac282-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac282-127">Requirement</span></span> | <span data-ttu-id="ac282-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ac282-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac282-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac282-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ac282-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ac282-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ac282-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac282-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ac282-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ac282-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ac282-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac282-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac282-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac282-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac282-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ac282-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ac282-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ac282-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ac282-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ac282-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac282-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac282-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ac282-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="ac282-139">CLSID</span></span><br/>                    | <span data-ttu-id="ac282-140">\_SWBEMOBJECTSET CLSID</span><span class="sxs-lookup"><span data-stu-id="ac282-140">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="ac282-141">IID</span><span class="sxs-lookup"><span data-stu-id="ac282-141">IID</span></span><br/>                      | <span data-ttu-id="ac282-142">\_ISWBEMOBJECTSET IID</span><span class="sxs-lookup"><span data-stu-id="ac282-142">IID\_ISWbemObjectSet</span></span><br/>                                                         |



 

 




