---
title: Metodo WSMan. SessionFlagCredUsernamePassword (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagCredUsernamePassword per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: 70d12df4-f0ac-499a-8b2f-6ba83b77869e
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagCredUsernamePassword
- Metodo SessionFlagCredUsernamePassword Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagCredUsernamePassword
topic_type:
- apiref
api_name:
- WSMan.SessionFlagCredUsernamePassword
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84827f342f70b13f1a2f0192289b34e347f26045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048533"
---
# <a name="wsmansessionflagcredusernamepassword-method"></a><span data-ttu-id="38f5d-106">WSMan. SessionFlagCredUsernamePassword, metodo</span><span class="sxs-lookup"><span data-stu-id="38f5d-106">WSMan.SessionFlagCredUsernamePassword method</span></span>

<span data-ttu-id="38f5d-107">Il metodo **WSMan. SessionFlagCredUsernamePassword** restituisce il valore del flag di autenticazione **WSManFlagCredUsernamePassword** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="38f5d-107">The **WSMan.SessionFlagCredUsernamePassword** method returns the value of the authentication flag **WSManFlagCredUsernamePassword** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="38f5d-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="38f5d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="38f5d-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="38f5d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="38f5d-110">**WSManFlagCredUsernamePassword** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="38f5d-110">**WSManFlagCredUsernamePassword** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="38f5d-111">Per altre informazioni, vedere [costanti di autenticazione](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="38f5d-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="38f5d-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38f5d-112">Syntax</span></span>


```VB
WSMan.SessionFlagCredUsernamePassword( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="38f5d-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="38f5d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f5d-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38f5d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f5d-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="38f5d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f5d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38f5d-116">Return value</span></span>

<span data-ttu-id="38f5d-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="38f5d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38f5d-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="38f5d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f5d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38f5d-119">Requirements</span></span>



| <span data-ttu-id="38f5d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f5d-120">Requirement</span></span> | <span data-ttu-id="38f5d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="38f5d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="38f5d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38f5d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="38f5d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38f5d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="38f5d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="38f5d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="38f5d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38f5d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="38f5d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38f5d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f5d-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f5d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="38f5d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="38f5d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38f5d-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38f5d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="38f5d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="38f5d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="38f5d-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="38f5d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="38f5d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="38f5d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f5d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f5d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38f5d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38f5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f5d-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="38f5d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="38f5d-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="38f5d-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





