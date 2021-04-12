---
title: Metodo Disable della classe SystemRestore
description: Disabilita il monitoraggio in un'unità specifica.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Disabilitare il ripristino del sistema del metodo
- Disable System Restore Method, classe SystemRestore
- SystemRestore classe di ripristino di sistema, Disable (metodo)
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120026"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="3aec9-106">Metodo Disable della classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="3aec9-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="3aec9-107">Disabilita il monitoraggio in un'unità specifica.</span><span class="sxs-lookup"><span data-stu-id="3aec9-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aec9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3aec9-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="3aec9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3aec9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aec9-110">*Unità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3aec9-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aec9-111">Unità da disabilitare.</span><span class="sxs-lookup"><span data-stu-id="3aec9-111">The drive to be disabled.</span></span> <span data-ttu-id="3aec9-112">Il formato della stringa dell'unità deve essere "C: \\ ".</span><span class="sxs-lookup"><span data-stu-id="3aec9-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="3aec9-113">Se questo parametro è l'unità di sistema o una stringa vuota (""), non vengono monitorate unità.</span><span class="sxs-lookup"><span data-stu-id="3aec9-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aec9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3aec9-114">Return value</span></span>

<span data-ttu-id="3aec9-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3aec9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3aec9-116">In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.</span><span class="sxs-lookup"><span data-stu-id="3aec9-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="3aec9-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="3aec9-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="3aec9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3aec9-118">Requirements</span></span>



| <span data-ttu-id="3aec9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aec9-119">Requirement</span></span> | <span data-ttu-id="3aec9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3aec9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3aec9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aec9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3aec9-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3aec9-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3aec9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3aec9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3aec9-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3aec9-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="3aec9-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3aec9-125">Namespace</span></span><br/>                | <span data-ttu-id="3aec9-126">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="3aec9-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="3aec9-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3aec9-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aec9-128"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3aec9-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aec9-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3aec9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aec9-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="3aec9-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





