---
title: Metodo WSMan. SessionFlagNoEncryption (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagNoEncryption per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: 15c76f0e-85ae-4ee3-bf9f-ba32195d9adc
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagNoEncryption
- Metodo SessionFlagNoEncryption Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagNoEncryption
topic_type:
- apiref
api_name:
- WSMan.SessionFlagNoEncryption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4c7a85e97afd67ab6b1114248a9c4b3ee3ebbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300982"
---
# <a name="wsmansessionflagnoencryption-method"></a><span data-ttu-id="69bb2-106">WSMan. SessionFlagNoEncryption, metodo</span><span class="sxs-lookup"><span data-stu-id="69bb2-106">WSMan.SessionFlagNoEncryption method</span></span>

<span data-ttu-id="69bb2-107">Il metodo **WSMan. SessionFlagNoEncryption** restituisce il valore del flag di autenticazione **WSManFlagNoEncryption** da usare nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="69bb2-107">The **WSMan.SessionFlagNoEncryption** method returns the value of the **WSManFlagNoEncryption** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="69bb2-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="69bb2-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="69bb2-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="69bb2-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="69bb2-110">**WSManFlagNoEncryption** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="69bb2-110">**WSManFlagNoEncryption** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="69bb2-111">Per ulteriori informazioni, vedere [altre costanti della sessione](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="69bb2-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="69bb2-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69bb2-112">Syntax</span></span>


```VB
WSMan.SessionFlagNoEncryption( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="69bb2-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="69bb2-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bb2-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="69bb2-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69bb2-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="69bb2-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bb2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69bb2-116">Return value</span></span>

<span data-ttu-id="69bb2-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="69bb2-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="69bb2-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="69bb2-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bb2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69bb2-119">Requirements</span></span>



| <span data-ttu-id="69bb2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="69bb2-120">Requirement</span></span> | <span data-ttu-id="69bb2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="69bb2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bb2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69bb2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="69bb2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69bb2-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="69bb2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="69bb2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="69bb2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69bb2-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="69bb2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69bb2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="69bb2-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bb2-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="69bb2-128">IDL</span><span class="sxs-lookup"><span data-stu-id="69bb2-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69bb2-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69bb2-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="69bb2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="69bb2-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="69bb2-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="69bb2-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="69bb2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="69bb2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69bb2-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69bb2-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="69bb2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69bb2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bb2-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="69bb2-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="69bb2-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="69bb2-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





