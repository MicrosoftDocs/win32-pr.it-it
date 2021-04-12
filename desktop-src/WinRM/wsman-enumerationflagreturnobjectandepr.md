---
title: Metodo WSMan. EnumerationFlagReturnObjectAndEPR (WSManDisp. h)
description: Restituisce il valore del flag di enumerazione EnumerationFlagReturnObjectAndEPR per l'utilizzo nel parametro Flags di Session. enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo EnumerationFlagReturnObjectAndEPR
- Metodo EnumerationFlagReturnObjectAndEPR Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo EnumerationFlagReturnObjectAndEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478658"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a><span data-ttu-id="01aa8-106">WSMan. EnumerationFlagReturnObjectAndEPR, metodo</span><span class="sxs-lookup"><span data-stu-id="01aa8-106">WSMan.EnumerationFlagReturnObjectAndEPR method</span></span>

<span data-ttu-id="01aa8-107">Il metodo **EnumerationFlagReturnObjectAndEPR** restituisce il valore del flag di enumerazione **EnumerationFlagReturnObjectAndEPR** per l'utilizzo nel parametro *Flags* di [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="01aa8-107">The **EnumerationFlagReturnObjectAndEPR** method returns the value of the enumeration flag **EnumerationFlagReturnObjectAndEPR** for use in the *flags* parameter of [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="01aa8-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="01aa8-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="01aa8-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="01aa8-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="01aa8-110">**EnumerationFlagReturnObjectAndEPR** è una costante nell'enumerazione **\_ WSManEnumFlags** ed è descritta in [**costanti di enumerazione**](enumeration-constants.md).</span><span class="sxs-lookup"><span data-stu-id="01aa8-110">**EnumerationFlagReturnObjectAndEPR** is a constant in the **\_WSManEnumFlags** enumeration and is described in [**Enumeration Constants**](enumeration-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01aa8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01aa8-111">Syntax</span></span>


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="01aa8-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="01aa8-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01aa8-113">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="01aa8-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="01aa8-114">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="01aa8-114">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01aa8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01aa8-115">Return value</span></span>

<span data-ttu-id="01aa8-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="01aa8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="01aa8-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01aa8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="01aa8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01aa8-118">Requirements</span></span>



| <span data-ttu-id="01aa8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="01aa8-119">Requirement</span></span> | <span data-ttu-id="01aa8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="01aa8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="01aa8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01aa8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="01aa8-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01aa8-122">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="01aa8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01aa8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="01aa8-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01aa8-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="01aa8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01aa8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="01aa8-126"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01aa8-126"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01aa8-127">IDL</span><span class="sxs-lookup"><span data-stu-id="01aa8-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="01aa8-128"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="01aa8-128"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="01aa8-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="01aa8-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="01aa8-130"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01aa8-130"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01aa8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="01aa8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01aa8-132"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01aa8-132"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01aa8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01aa8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01aa8-134">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="01aa8-134">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="01aa8-135">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="01aa8-135">**Session**</span></span>](session.md)
</dt> </dl>

 

 





