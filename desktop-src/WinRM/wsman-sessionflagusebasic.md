---
title: Metodo WSMan. SessionFlagUseBasic (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseBasic per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: 789ecef9-7871-43af-9d63-018f1d99bd09
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUseBasic
- Metodo SessionFlagUseBasic Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUseBasic
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseBasic
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41641e0398791ab46c81f71f967f2d43700a2984
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048012"
---
# <a name="wsmansessionflagusebasic-method"></a><span data-ttu-id="f8bb9-106">WSMan. SessionFlagUseBasic, metodo</span><span class="sxs-lookup"><span data-stu-id="f8bb9-106">WSMan.SessionFlagUseBasic method</span></span>

<span data-ttu-id="f8bb9-107">Il metodo **WSMan. SessionFlagUseBasic** restituisce il valore del flag di autenticazione **WSManFlagUseBasic** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="f8bb9-107">The **WSMan.SessionFlagUseBasic** method returns the value of the authentication flag **WSManFlagUseBasic** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="f8bb9-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="f8bb9-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="f8bb9-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb9-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="f8bb9-110">**WSManFlagUseBasic** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="f8bb9-110">**WSManFlagUseBasic** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="f8bb9-111">Per altre informazioni, vedere [**costanti di autenticazione**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f8bb9-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f8bb9-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8bb9-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseBasic( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f8bb9-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8bb9-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8bb9-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f8bb9-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8bb9-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="f8bb9-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8bb9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8bb9-116">Return value</span></span>

<span data-ttu-id="f8bb9-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8bb9-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8bb9-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8bb9-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8bb9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8bb9-119">Requirements</span></span>



| <span data-ttu-id="f8bb9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8bb9-120">Requirement</span></span> | <span data-ttu-id="f8bb9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f8bb9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8bb9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8bb9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f8bb9-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8bb9-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="f8bb9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8bb9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f8bb9-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8bb9-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f8bb9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8bb9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8bb9-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8bb9-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8bb9-128">IDL</span><span class="sxs-lookup"><span data-stu-id="f8bb9-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8bb9-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8bb9-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="f8bb9-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="f8bb9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8bb9-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f8bb9-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f8bb9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f8bb9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8bb9-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8bb9-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8bb9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8bb9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8bb9-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="f8bb9-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="f8bb9-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="f8bb9-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





