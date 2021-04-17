---
description: Il metodo Add dell'oggetto SWbemNamedValueSet aggiunge un oggetto SWbemNamedValue alla raccolta. Se un elemento esiste già nella raccolta con lo stesso nome, il nuovo elemento lo sostituisce.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Metodo SWbemNamedValueSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528482"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="c84c8-104">SWbemNamedValueSet. Add, metodo</span><span class="sxs-lookup"><span data-stu-id="c84c8-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="c84c8-105">Il metodo **Add** dell'oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) aggiunge un oggetto [**SWbemNamedValue**](swbemnamedvalue.md) alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="c84c8-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="c84c8-106">Se un elemento esiste già nella raccolta con lo stesso nome, il nuovo elemento lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="c84c8-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="c84c8-107">Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c84c8-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c84c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c84c8-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c84c8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c84c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84c8-110">*strName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c84c8-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84c8-111">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c84c8-111">Required.</span></span> <span data-ttu-id="c84c8-112">Nome del nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="c84c8-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="c84c8-113">*varVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c84c8-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c84c8-114">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c84c8-114">Required.</span></span> <span data-ttu-id="c84c8-115">Variante che rappresenta il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="c84c8-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="c84c8-116">*iFlags* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="c84c8-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c84c8-117">Riservato e deve essere impostato su zero se specificato.</span><span class="sxs-lookup"><span data-stu-id="c84c8-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84c8-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c84c8-118">Return value</span></span>

<span data-ttu-id="c84c8-119">Se ha esito positivo, questo metodo restituisce l'oggetto [**SWbemNamedValue**](swbemnamedvalue.md) appena modificato o appena creato.</span><span class="sxs-lookup"><span data-stu-id="c84c8-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84c8-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c84c8-120">Remarks</span></span>

<span data-ttu-id="c84c8-121">Per esempi relativi all'aggiunta e al recupero di valori denominati, vedere [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="c84c8-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c84c8-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c84c8-122">Requirements</span></span>



| <span data-ttu-id="c84c8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84c8-123">Requirement</span></span> | <span data-ttu-id="c84c8-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c84c8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c84c8-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c84c8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c84c8-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c84c8-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c84c8-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c84c8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c84c8-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c84c8-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c84c8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c84c8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84c8-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c84c8-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c84c8-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="c84c8-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="c84c8-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c84c8-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c84c8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c84c8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84c8-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84c8-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c84c8-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="c84c8-135">CLSID</span></span><br/>                    | <span data-ttu-id="c84c8-136">\_SWBEMNAMEDVALUESET CLSID</span><span class="sxs-lookup"><span data-stu-id="c84c8-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="c84c8-137">IID</span><span class="sxs-lookup"><span data-stu-id="c84c8-137">IID</span></span><br/>                      | <span data-ttu-id="c84c8-138">\_ISWBEMNAMEDVALUESET IID</span><span class="sxs-lookup"><span data-stu-id="c84c8-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="c84c8-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c84c8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84c8-140">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="c84c8-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




