---
title: Metodo Restore della classe SystemRestore
description: Avvia un ripristino di sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Ripristino del sistema del metodo Restore
- Ripristino del sistema del metodo Restore, classe SystemRestore
- SystemRestore classe di ripristino del sistema, metodo Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740311"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="16361-106">Metodo Restore della classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="16361-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="16361-107">Avvia un ripristino di sistema.</span><span class="sxs-lookup"><span data-stu-id="16361-107">Initiates a system restore.</span></span> <span data-ttu-id="16361-108">Il chiamante deve forzare il riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="16361-108">The caller must force a system reboot.</span></span> <span data-ttu-id="16361-109">Il ripristino effettivo si verifica durante il riavvio.</span><span class="sxs-lookup"><span data-stu-id="16361-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="16361-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16361-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="16361-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="16361-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16361-112">*SequenceNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16361-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16361-113">Numero di sequenza del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="16361-113">The sequence number of the restore point.</span></span> <span data-ttu-id="16361-114">Per determinare il numero di sequenza di un punto di ripristino specifico, enumerare tutti i punti di ripristino nel sistema.</span><span class="sxs-lookup"><span data-stu-id="16361-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16361-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16361-115">Return value</span></span>

<span data-ttu-id="16361-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="16361-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="16361-117">In caso contrario, il metodo restituisce uno dei codici di errore COM definiti in WinError. h.</span><span class="sxs-lookup"><span data-stu-id="16361-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="16361-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="16361-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="16361-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16361-119">Requirements</span></span>



| <span data-ttu-id="16361-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="16361-120">Requirement</span></span> | <span data-ttu-id="16361-121">Valore</span><span class="sxs-lookup"><span data-stu-id="16361-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="16361-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16361-122">Minimum supported client</span></span><br/> | <span data-ttu-id="16361-123">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="16361-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="16361-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16361-124">Minimum supported server</span></span><br/> | <span data-ttu-id="16361-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="16361-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="16361-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16361-126">Namespace</span></span><br/>                | <span data-ttu-id="16361-127">\\ \\ Impostazioni predefinite radice</span><span class="sxs-lookup"><span data-stu-id="16361-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="16361-128">MOF</span><span class="sxs-lookup"><span data-stu-id="16361-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16361-129"><dt>Sr. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16361-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16361-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16361-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16361-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="16361-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





