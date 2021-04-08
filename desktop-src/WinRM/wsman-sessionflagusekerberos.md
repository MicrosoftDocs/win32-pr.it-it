---
title: Metodo WSMan. SessionFlagUseKerberos (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseKerberos per l'utilizzo nel parametro Flags di WSMan. CreateSession.
ms.assetid: be005312-1e87-4371-9791-709a9be46f7c
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUseKerberos
- Metodo SessionFlagUseKerberos Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUseKerberos
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseKerberos
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e7436a5b79480b39c093545a0b579da3d13082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741618"
---
# <a name="wsmansessionflagusekerberos-method"></a><span data-ttu-id="e7de6-106">WSMan. SessionFlagUseKerberos, metodo</span><span class="sxs-lookup"><span data-stu-id="e7de6-106">WSMan.SessionFlagUseKerberos method</span></span>

<span data-ttu-id="e7de6-107">Il metodo **WSMan. SessionFlagUseKerberos** restituisce il valore del flag di autenticazione **WSManFlagUseKerberos** da usare nel parametro *Flags* di [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="e7de6-107">The **WSMan.SessionFlagUseKerberos** method returns the value of the **WSManFlagUseKerberos** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="e7de6-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="e7de6-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="e7de6-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e7de6-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="e7de6-110">**WSManFlagUseKerberos** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="e7de6-110">**WSManFlagUseKerberos** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="e7de6-111">Per altre informazioni, vedere [costanti di autenticazione](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e7de6-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e7de6-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7de6-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseKerberos( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="e7de6-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7de6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7de6-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e7de6-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7de6-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="e7de6-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7de6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7de6-116">Return value</span></span>

<span data-ttu-id="e7de6-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7de6-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7de6-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7de6-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7de6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7de6-119">Requirements</span></span>



| <span data-ttu-id="e7de6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7de6-120">Requirement</span></span> | <span data-ttu-id="e7de6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e7de6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7de6-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7de6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7de6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7de6-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e7de6-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7de6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7de6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7de6-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e7de6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7de6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7de6-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7de6-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7de6-128">IDL</span><span class="sxs-lookup"><span data-stu-id="e7de6-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e7de6-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e7de6-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="e7de6-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7de6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7de6-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e7de6-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e7de6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e7de6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7de6-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7de6-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e7de6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7de6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7de6-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="e7de6-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="e7de6-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="e7de6-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





