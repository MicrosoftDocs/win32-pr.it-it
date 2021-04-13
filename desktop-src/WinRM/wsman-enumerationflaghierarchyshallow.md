---
title: Metodo WSMan. EnumerationFlagHierarchyShallow (WSManDisp. h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagHierarchyShallow per l'utilizzo nel parametro Flags di Session. enumerate.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo EnumerationFlagHierarchyShallow
- Metodo EnumerationFlagHierarchyShallow Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo EnumerationFlagHierarchyShallow
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b74552fd88ac370ad4a3f8b885a7f61e65a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518141"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a><span data-ttu-id="15fe0-106">WSMan. EnumerationFlagHierarchyShallow, metodo</span><span class="sxs-lookup"><span data-stu-id="15fe0-106">WSMan.EnumerationFlagHierarchyShallow method</span></span>

<span data-ttu-id="15fe0-107">Il metodo **EnumerationFlagHierarchyShallow** restituisce il valore del flag di enumerazione **EnumerationFlagHierarchyShallow** per l'utilizzo nel parametro *Flags* di [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="15fe0-107">The **EnumerationFlagHierarchyShallow** method returns the value of the enumeration flag **EnumerationFlagHierarchyShallow** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="15fe0-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="15fe0-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="15fe0-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="15fe0-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="15fe0-110">**EnumerationFlagHierarchyShallow** è una costante nell'enumerazione **\_ WSManEnumFlags** ed è descritta in [**costanti di enumerazione**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="15fe0-110">**EnumerationFlagHierarchyShallow** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15fe0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15fe0-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagHierarchyShallow( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="15fe0-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="15fe0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fe0-113">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="15fe0-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15fe0-114">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="15fe0-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fe0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15fe0-115">Return value</span></span>

<span data-ttu-id="15fe0-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="15fe0-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="15fe0-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="15fe0-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fe0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15fe0-118">Requirements</span></span>



| <span data-ttu-id="15fe0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15fe0-119">Requirement</span></span> | <span data-ttu-id="15fe0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="15fe0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fe0-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15fe0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="15fe0-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15fe0-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="15fe0-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15fe0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="15fe0-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15fe0-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="15fe0-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15fe0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="15fe0-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="15fe0-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15fe0-127">IDL</span><span class="sxs-lookup"><span data-stu-id="15fe0-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15fe0-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15fe0-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="15fe0-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="15fe0-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="15fe0-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15fe0-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15fe0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="15fe0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15fe0-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15fe0-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15fe0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15fe0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fe0-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="15fe0-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="15fe0-135">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="15fe0-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





