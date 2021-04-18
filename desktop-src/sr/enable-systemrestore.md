---
title: Metodo Enable della classe SystemRestore
description: Abilita il monitoraggio in un'unità specifica.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Abilita ripristino del sistema del metodo
- Enable Method System Restore, classe SystemRestore
- Ripristino del sistema della classe SystemRestore, metodo Enable
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301766"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="85a00-106">Metodo Enable della classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="85a00-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="85a00-107">Abilita il monitoraggio in un'unità specifica.</span><span class="sxs-lookup"><span data-stu-id="85a00-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a00-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85a00-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="85a00-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="85a00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a00-110">*Unità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="85a00-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a00-111">Unità da abilitare.</span><span class="sxs-lookup"><span data-stu-id="85a00-111">The drive to be enabled.</span></span> <span data-ttu-id="85a00-112">Il formato della stringa dell'unità deve essere "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="85a00-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="85a00-113">Se questo parametro è l'unità di sistema o una stringa vuota (""), vengono monitorate tutte le unità.</span><span class="sxs-lookup"><span data-stu-id="85a00-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a00-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85a00-114">Return value</span></span>

<span data-ttu-id="85a00-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85a00-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="85a00-116">In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.</span><span class="sxs-lookup"><span data-stu-id="85a00-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a00-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="85a00-117">Remarks</span></span>

<span data-ttu-id="85a00-118">Il metodo **Enable** non attende che il monitoraggio venga abilitato completamente prima della restituzione, perché l'operazione potrebbe richiedere alcuni minuti.</span><span class="sxs-lookup"><span data-stu-id="85a00-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="85a00-119">Viene invece restituito immediatamente dopo l'avvio del servizio Ripristino configurazione di sistema e del driver del filtro.</span><span class="sxs-lookup"><span data-stu-id="85a00-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="85a00-120">Per abilitare ripristino configurazione di sistema in un'unità non di sistema, è necessario innanzitutto abilitare ripristino configurazione di sistema nell'unità di sistema.</span><span class="sxs-lookup"><span data-stu-id="85a00-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="85a00-121">Questo metodo ha esito negativo in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="85a00-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="85a00-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="85a00-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="85a00-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85a00-123">Requirements</span></span>



| <span data-ttu-id="85a00-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a00-124">Requirement</span></span> | <span data-ttu-id="85a00-125">Valore</span><span class="sxs-lookup"><span data-stu-id="85a00-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="85a00-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85a00-126">Minimum supported client</span></span><br/> | <span data-ttu-id="85a00-127">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="85a00-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="85a00-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85a00-128">Minimum supported server</span></span><br/> | <span data-ttu-id="85a00-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85a00-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="85a00-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85a00-130">Namespace</span></span><br/>                | <span data-ttu-id="85a00-131">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="85a00-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="85a00-132">MOF</span><span class="sxs-lookup"><span data-stu-id="85a00-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85a00-133"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85a00-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a00-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85a00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a00-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="85a00-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





