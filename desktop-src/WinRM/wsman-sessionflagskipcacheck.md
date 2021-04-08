---
title: Metodo WSMan. SessionFlagSkipCACheck (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagSkipCACheck per l'utilizzo nel parametro Flags di WSMan. CreateSession.
ms.assetid: a67cadb3-c20a-4a58-a13b-5bbd23c547d1
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagSkipCACheck
- Metodo SessionFlagSkipCACheck Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagSkipCACheck
topic_type:
- apiref
api_name:
- WSMan.SessionFlagSkipCACheck
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e536112b16ad8cbab3cebb2de582a2e0ea8aec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047872"
---
# <a name="wsmansessionflagskipcacheck-method"></a><span data-ttu-id="ed9c7-106">WSMan. SessionFlagSkipCACheck, metodo</span><span class="sxs-lookup"><span data-stu-id="ed9c7-106">WSMan.SessionFlagSkipCACheck method</span></span>

<span data-ttu-id="ed9c7-107">Il metodo **WSMan. SessionFlagSkipCACheck** restituisce il valore del flag di autenticazione **WSManFlagSkipCACheck** da usare nel parametro *Flags* di [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="ed9c7-107">The **WSMan.SessionFlagSkipCACheck** method returns the value of the **WSManFlagSkipCACheck** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="ed9c7-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="ed9c7-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="ed9c7-109">Per ulteriori informazioni su come chiamare questo metodo ed esempi di codice, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ed9c7-109">For more information about how to call this method and code examples, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="ed9c7-110">**WSManFlagSkipCACheck** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="ed9c7-110">**WSManFlagSkipCACheck** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="ed9c7-111">Per altre informazioni, vedere [**costanti di autenticazione**](authentication-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ed9c7-111">For more information, see [**Authentication Constants**](authentication-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9c7-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed9c7-112">Syntax</span></span>


```VB
WSMan.SessionFlagSkipCACheck( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="ed9c7-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed9c7-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed9c7-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed9c7-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9c7-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="ed9c7-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed9c7-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed9c7-116">Return value</span></span>

<span data-ttu-id="ed9c7-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ed9c7-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed9c7-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ed9c7-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9c7-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed9c7-119">Requirements</span></span>



| <span data-ttu-id="ed9c7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9c7-120">Requirement</span></span> | <span data-ttu-id="ed9c7-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ed9c7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9c7-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed9c7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ed9c7-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed9c7-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ed9c7-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed9c7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ed9c7-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed9c7-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ed9c7-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed9c7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed9c7-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c7-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed9c7-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ed9c7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed9c7-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c7-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ed9c7-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed9c7-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed9c7-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c7-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ed9c7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ed9c7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed9c7-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed9c7-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ed9c7-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed9c7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9c7-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="ed9c7-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="ed9c7-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="ed9c7-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





