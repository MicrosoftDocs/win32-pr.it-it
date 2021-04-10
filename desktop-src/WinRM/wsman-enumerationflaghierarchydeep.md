---
title: Metodo WSMan. EnumerationFlagHierarchyDeep (WSManDisp. h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagHierarchyDeep per l'utilizzo nel parametro Flags di Session. enumerate.
ms.assetid: b84b82fa-0b2e-418e-850f-6d7a4749fdc1
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo EnumerationFlagHierarchyDeep
- Metodo EnumerationFlagHierarchyDeep Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo EnumerationFlagHierarchyDeep
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyDeep
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61982c6117d0a91ec253af35657f0cbbf5af12c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964801"
---
# <a name="wsmanenumerationflaghierarchydeep-method"></a><span data-ttu-id="bdbe7-106">WSMan. EnumerationFlagHierarchyDeep, metodo</span><span class="sxs-lookup"><span data-stu-id="bdbe7-106">WSMan.EnumerationFlagHierarchyDeep method</span></span>

<span data-ttu-id="bdbe7-107">Il metodo **EnumerationFlagHierarchyDeep** restituisce il valore del flag di enumerazione **EnumerationFlagHierarchyDeep** per l'utilizzo nel parametro *Flags* di [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="bdbe7-107">The **EnumerationFlagHierarchyDeep** method returns the value of the enumeration flag **EnumerationFlagHierarchyDeep** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="bdbe7-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="bdbe7-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="bdbe7-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bdbe7-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="bdbe7-110">**EnumerationFlagHierarchyDeep** è una costante nell'enumerazione **\_ WSManEnumFlags** ed è descritta in [**costanti di enumerazione**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="bdbe7-110">**EnumerationFlagHierarchyDeep** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbe7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdbe7-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyDeep( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="bdbe7-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdbe7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbe7-113">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bdbe7-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbe7-114">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="bdbe7-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbe7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdbe7-115">Return value</span></span>

<span data-ttu-id="bdbe7-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bdbe7-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bdbe7-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdbe7-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdbe7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdbe7-118">Requirements</span></span>



| <span data-ttu-id="bdbe7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdbe7-119">Requirement</span></span> | <span data-ttu-id="bdbe7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="bdbe7-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbe7-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdbe7-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbe7-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bdbe7-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="bdbe7-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdbe7-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbe7-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bdbe7-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="bdbe7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdbe7-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdbe7-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbe7-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdbe7-127">IDL</span><span class="sxs-lookup"><span data-stu-id="bdbe7-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdbe7-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdbe7-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="bdbe7-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdbe7-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdbe7-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bdbe7-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bdbe7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bdbe7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdbe7-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdbe7-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bdbe7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdbe7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbe7-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="bdbe7-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="bdbe7-135">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="bdbe7-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





