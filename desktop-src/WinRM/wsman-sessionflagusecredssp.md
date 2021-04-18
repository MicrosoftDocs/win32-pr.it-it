---
title: Metodo WSMan. SessionFlagUseCredSsp (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUseCredSsp per l'utilizzo nel parametro Flags del metodo WSMan. CreateSession.
ms.assetid: bb167445-91d6-4e06-a976-bf869320784a
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUseCredSsp
- Metodo SessionFlagUseCredSsp Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUseCredSsp
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUseCredSsp
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed5dfbaba3e705f100cdd373e194174f4654a7d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476864"
---
# <a name="wsmansessionflagusecredssp-method"></a><span data-ttu-id="a5287-106">WSMan. SessionFlagUseCredSsp, metodo</span><span class="sxs-lookup"><span data-stu-id="a5287-106">WSMan.SessionFlagUseCredSsp method</span></span>

<span data-ttu-id="a5287-107">Restituisce il valore del flag di autenticazione **WSManFlagUseCredSsp** per l'utilizzo nel parametro *Flags* del metodo [**WSMan. CreateSession**](wsman-createsession.md) .</span><span class="sxs-lookup"><span data-stu-id="a5287-107">Returns the value of the **WSManFlagUseCredSsp** authentication flag for use in the *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) method.</span></span> <span data-ttu-id="a5287-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="a5287-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="a5287-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a5287-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="a5287-110">**WSManFlagUseCredSsp** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="a5287-110">**WSManFlagUseCredSsp** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="a5287-111">Per altre informazioni, vedere [costanti di autenticazione](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="a5287-111">For more information, see [Authentication Constants](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5287-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5287-112">Syntax</span></span>


```VB
WSMan.SessionFlagUseCredSsp( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="a5287-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5287-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5287-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a5287-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5287-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="a5287-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5287-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5287-116">Return value</span></span>

<span data-ttu-id="a5287-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a5287-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a5287-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a5287-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5287-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5287-119">Requirements</span></span>



| <span data-ttu-id="a5287-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5287-120">Requirement</span></span> | <span data-ttu-id="a5287-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a5287-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5287-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5287-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a5287-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5287-123">Windows 7</span></span><br/>                                                                                                        |
| <span data-ttu-id="a5287-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5287-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a5287-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a5287-125">Windows Server 2008 R2</span></span><br/>                                                                                           |
| <span data-ttu-id="a5287-126">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a5287-126">Redistributable</span></span><br/>          | <span data-ttu-id="a5287-127">Windows Management Framework in Windows Server 2008 con SP2, Windows Vista con SP1 e Windows Vista con SP2</span><span class="sxs-lookup"><span data-stu-id="a5287-127">Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2</span></span><br/> |
| <span data-ttu-id="a5287-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5287-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5287-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5287-129"><dt>WSManDisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="a5287-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a5287-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a5287-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a5287-131"><dt>WSManDisp.idl</dt></span></span> </dl>                                    |
| <span data-ttu-id="a5287-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5287-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5287-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a5287-133"><dt>WSManDisp.tlb</dt></span></span> </dl>                                    |
| <span data-ttu-id="a5287-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a5287-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5287-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5287-135"><dt>WSMAuto.dll</dt></span></span> </dl>                                      |



## <a name="see-also"></a><span data-ttu-id="a5287-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5287-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5287-137">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="a5287-137">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="a5287-138">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="a5287-138">**Session**</span></span>](session.md)
</dt> </dl>

 

 





