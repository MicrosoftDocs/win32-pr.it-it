---
title: Metodo WSMan. SessionFlagUseNoAuthentication (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseNoAuthentication per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: 22a8107a-8e5e-4636-bf7d-a261f885e074
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUseNoAuthentication
- Metodo SessionFlagUseNoAuthentication Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUseNoAuthentication
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseNoAuthentication
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9676d3baa9a18ae8a3feb5eb4092c63586a94b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478778"
---
# <a name="wsmansessionflagusenoauthentication-method"></a><span data-ttu-id="eaadb-106">WSMan. SessionFlagUseNoAuthentication, metodo</span><span class="sxs-lookup"><span data-stu-id="eaadb-106">WSMan.SessionFlagUseNoAuthentication method</span></span>

<span data-ttu-id="eaadb-107">Il metodo **WSMan. SessionFlagUseNoAuthentication** restituisce il valore del flag di autenticazione **WSManFlagUseNoAuthentication** da usare nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="eaadb-107">The **WSMan.SessionFlagUseNoAuthentication** method returns the value of the **WSManFlagUseNoAuthentication** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="eaadb-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="eaadb-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="eaadb-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="eaadb-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="eaadb-110">**WSManFlagUseNoAuthentication** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="eaadb-110">**WSManFlagUseNoAuthentication** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="eaadb-111">Per ulteriori informazioni, vedere//[costanti di autenticazione](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="eaadb-111">For more information, see //[Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eaadb-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eaadb-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseNoAuthentication( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="eaadb-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaadb-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaadb-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eaadb-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaadb-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="eaadb-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaadb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaadb-116">Return value</span></span>

<span data-ttu-id="eaadb-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eaadb-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eaadb-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eaadb-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaadb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaadb-119">Requirements</span></span>



| <span data-ttu-id="eaadb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaadb-120">Requirement</span></span> | <span data-ttu-id="eaadb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="eaadb-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaadb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaadb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eaadb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eaadb-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="eaadb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaadb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eaadb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eaadb-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="eaadb-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaadb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaadb-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaadb-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaadb-128">IDL</span><span class="sxs-lookup"><span data-stu-id="eaadb-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eaadb-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eaadb-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="eaadb-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="eaadb-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="eaadb-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eaadb-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eaadb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="eaadb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaadb-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaadb-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eaadb-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaadb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaadb-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="eaadb-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="eaadb-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="eaadb-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





