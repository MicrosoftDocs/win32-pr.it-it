---
title: Metodo WSMan. SessionFlagEnableSPNServerPort (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagEnableSPNServerPort per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: a18a87e6-dcee-4e9f-8e8c-262fef36ab1a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagEnableSPNServerPort
- Metodo SessionFlagEnableSPNServerPort Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagEnableSPNServerPort
topic_type:
- apiref
api_name:
- WSMan.SessionFlagEnableSPNServerPort
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4153f088079b58b3b0e048f2cd8f38b3524754a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518136"
---
# <a name="wsmansessionflagenablespnserverport-method"></a><span data-ttu-id="2ebcc-106">WSMan. SessionFlagEnableSPNServerPort, metodo</span><span class="sxs-lookup"><span data-stu-id="2ebcc-106">WSMan.SessionFlagEnableSPNServerPort method</span></span>

<span data-ttu-id="2ebcc-107">Il metodo **WSMan. SessionFlagEnableSPNServerPort** restituisce il valore del flag di autenticazione **WSManFlagEnableSPNServerPort** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="2ebcc-107">The **WSMan.SessionFlagEnableSPNServerPort** method returns the value of the authentication flag **WSManFlagEnableSPNServerPort** for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="2ebcc-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="2ebcc-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ebcc-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="2ebcc-110">**WSManFlagEnableSPNServerPort** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="2ebcc-110">**WSManFlagEnableSPNServerPort** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="2ebcc-111">Per ulteriori informazioni, vedere [**altre costanti della sessione**](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2ebcc-111">For more information, see [**Other Session Constants**](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebcc-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ebcc-112">Syntax</span></span>


```VB
WSMan.SessionFlagEnableSPNServerPort( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="2ebcc-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ebcc-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebcc-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ebcc-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ebcc-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ebcc-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ebcc-116">Return value</span></span>

<span data-ttu-id="2ebcc-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2ebcc-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2ebcc-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2ebcc-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ebcc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ebcc-119">Requirements</span></span>



| <span data-ttu-id="2ebcc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebcc-120">Requirement</span></span> | <span data-ttu-id="2ebcc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2ebcc-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebcc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ebcc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebcc-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ebcc-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2ebcc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ebcc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebcc-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ebcc-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2ebcc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ebcc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ebcc-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ebcc-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ebcc-128">IDL</span><span class="sxs-lookup"><span data-stu-id="2ebcc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ebcc-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ebcc-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2ebcc-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ebcc-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="2ebcc-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2ebcc-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2ebcc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ebcc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebcc-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ebcc-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ebcc-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ebcc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebcc-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="2ebcc-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="2ebcc-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="2ebcc-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





