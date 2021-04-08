---
title: Metodo WSMan. SessionFlagUTF8 (WSManDisp. h)
description: Restituisce il valore del flag di autenticazione WSManFlagUTF8 per l'utilizzo nel parametro Flags di WSMan. CreateSession.
ms.assetid: a79e292a-364b-4bf3-ae66-6a15ad51524f
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows del metodo SessionFlagUTF8
- Metodo SessionFlagUTF8 Gestione remota Windows, oggetto WSMan
- Gestione remota Windows oggetto WSMan, metodo SessionFlagUTF8
topic_type:
- apiref
api_name:
- WSMan.SessionFlagUTF8
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 985763131c2f3d4227f1a24af612ea3141237832
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743215"
---
# <a name="wsmansessionflagutf8-method"></a><span data-ttu-id="ea19d-106">WSMan. SessionFlagUTF8, metodo</span><span class="sxs-lookup"><span data-stu-id="ea19d-106">WSMan.SessionFlagUTF8 method</span></span>

<span data-ttu-id="ea19d-107">Il metodo **WSMan. SessionFlagUTF8** restituisce il valore del flag di autenticazione **WSManFlagUTF8** da usare nel parametro *Flags* di [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="ea19d-107">The **WSMan.SessionFlagUTF8** method returns the value of the **WSManFlagUTF8** authentication flag for use in the *flags* parameter of [**WSMan.CreateSession**](wsman-createsession.md).</span></span> <span data-ttu-id="ea19d-108">Questo metodo fornisce una sintassi più efficiente per l'utilizzo della costante, in modo che gli script non siano necessari per impostare un valore costante.</span><span class="sxs-lookup"><span data-stu-id="ea19d-108">This method provides a more efficient syntax for using the constant so that scripts are not required to set a constant value.</span></span> <span data-ttu-id="ea19d-109">Per ulteriori informazioni su come chiamare questo metodo, vedere [costanti di sessione](session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ea19d-109">For more information about how to call this method, see [Session Constants](session-constants.md).</span></span>

<span data-ttu-id="ea19d-110">**WSManFlagUTF8** è una costante nell'enumerazione **\_ \_ WSManSessionFlags** .</span><span class="sxs-lookup"><span data-stu-id="ea19d-110">**WSManFlagUTF8** is a constant in the **\_\_WSManSessionFlags** enumeration.</span></span> <span data-ttu-id="ea19d-111">Per ulteriori informazioni, vedere [altre costanti della sessione](other-session-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ea19d-111">For more information, see [Other Session Constants](other-session-constants.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ea19d-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea19d-112">Syntax</span></span>


```VB
WSMan.SessionFlagUTF8( _
  ByRef flags _
)
```



## <a name="parameters"></a><span data-ttu-id="ea19d-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea19d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea19d-114">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea19d-114">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea19d-115">Valore della costante.</span><span class="sxs-lookup"><span data-stu-id="ea19d-115">The value of the constant.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea19d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea19d-116">Return value</span></span>

<span data-ttu-id="ea19d-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ea19d-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ea19d-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ea19d-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea19d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea19d-119">Requirements</span></span>



| <span data-ttu-id="ea19d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea19d-120">Requirement</span></span> | <span data-ttu-id="ea19d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ea19d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea19d-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea19d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea19d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea19d-123">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ea19d-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea19d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea19d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea19d-125">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ea19d-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea19d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea19d-127"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea19d-127"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea19d-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ea19d-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea19d-129"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea19d-129"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ea19d-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea19d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea19d-131"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea19d-131"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea19d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ea19d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea19d-133"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea19d-133"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea19d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea19d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea19d-135">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="ea19d-135">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="ea19d-136">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="ea19d-136">**Session**</span></span>](session.md)
</dt> </dl>

 

 





