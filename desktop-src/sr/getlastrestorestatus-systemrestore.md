---
title: Metodo GetLastRestoreStatus della classe SystemRestore
description: Recupera lo stato dell'ultimo ripristino di sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Ripristino del sistema del metodo GetLastRestoreStatus
- Ripristino del sistema del metodo GetLastRestoreStatus, classe SystemRestore
- SystemRestore Class System Restore, metodo GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300978"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a><span data-ttu-id="503d6-106">Metodo GetLastRestoreStatus della classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="503d6-106">GetLastRestoreStatus method of the SystemRestore class</span></span>

<span data-ttu-id="503d6-107">Recupera lo stato dell'ultimo ripristino di sistema.</span><span class="sxs-lookup"><span data-stu-id="503d6-107">Retrieves the status of the last system restore.</span></span>

## <a name="syntax"></a><span data-ttu-id="503d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="503d6-108">Syntax</span></span>


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a><span data-ttu-id="503d6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="503d6-109">Parameters</span></span>

<span data-ttu-id="503d6-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="503d6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="503d6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="503d6-111">Return value</span></span>

<span data-ttu-id="503d6-112">Il metodo restituisce uno dei valori di stato seguenti.</span><span class="sxs-lookup"><span data-stu-id="503d6-112">The method returns one of the following status values.</span></span>



| <span data-ttu-id="503d6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="503d6-113">Return value</span></span>                                                                 | <span data-ttu-id="503d6-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="503d6-114">Description</span></span>                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="503d6-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="503d6-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="503d6-116">L'ultimo ripristino non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="503d6-116">The last restore failed.</span></span><br/>          |
| <dl> <span data-ttu-id="503d6-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="503d6-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="503d6-118">L'ultimo ripristino è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="503d6-118">The last restore was successful.</span></span><br/>  |
| <dl> <span data-ttu-id="503d6-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="503d6-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="503d6-120">L'ultimo ripristino è stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="503d6-120">The last restore was interrupted.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="503d6-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="503d6-121">Examples</span></span>


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
End If
```



## <a name="requirements"></a><span data-ttu-id="503d6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="503d6-122">Requirements</span></span>



| <span data-ttu-id="503d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="503d6-123">Requirement</span></span> | <span data-ttu-id="503d6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="503d6-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="503d6-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="503d6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="503d6-126">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="503d6-126">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="503d6-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="503d6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="503d6-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="503d6-128">None supported</span></span><br/>                                                         |
| <span data-ttu-id="503d6-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="503d6-129">Namespace</span></span><br/>                | <span data-ttu-id="503d6-130">\\Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="503d6-130">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="503d6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="503d6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="503d6-132"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="503d6-132"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="503d6-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="503d6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503d6-134">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="503d6-134">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





