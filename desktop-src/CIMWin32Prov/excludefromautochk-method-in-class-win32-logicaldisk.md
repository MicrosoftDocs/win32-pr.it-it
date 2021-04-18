---
description: Esclude i dischi dall'operazione Autochk da eseguire al riavvio successivo.
ms.assetid: 5df2bc3b-e149-4853-aa02-af4cb8af6da0
ms.tgt_platform: multiple
title: Metodo ExcludeFromAutochk della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ExcludeFromAutochk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c41d93111742e975490d97169c7e9147ba5fb1ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304692"
---
# <a name="excludefromautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="f9ca0-103">Metodo ExcludeFromAutochk della \_ classe disco logico Win32</span><span class="sxs-lookup"><span data-stu-id="f9ca0-103">ExcludeFromAutochk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="f9ca0-104">Il metodo **ExcludeFromAutochk** esclude i dischi dall'operazione **Autochk** da eseguire al riavvio successivo.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-104">The **ExcludeFromAutochk** method excludes disks from the **autochk** operation to be run at the next reboot.</span></span>

<span data-ttu-id="f9ca0-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="f9ca0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f9ca0-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f9ca0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ca0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9ca0-107">Syntax</span></span>


```mof
uint32 ExcludeFromAutochk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="f9ca0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9ca0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ca0-109">*Disco logico* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9ca0-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9ca0-110">Elenco di unità che devono essere escluse da **Autochk** al riavvio successivo.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-110">List of drives that should be excluded from **autochk** at the next reboot.</span></span> <span data-ttu-id="f9ca0-111">La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-111">The string syntax consists of the drive letter followed by a colon for the logical disk.</span></span>

<span data-ttu-id="f9ca0-112">Esempio: "C:"</span><span class="sxs-lookup"><span data-stu-id="f9ca0-112">Example: "C:"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ca0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9ca0-113">Return value</span></span>

<span data-ttu-id="f9ca0-114">Restituisce un valore pari a 0 (zero) quando non si verifica alcun errore.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-114">Returns a value of 0 (zero) when no error occurs.</span></span> <span data-ttu-id="f9ca0-115">I valori sono elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-115">Values are listed in the following list.</span></span> <span data-ttu-id="f9ca0-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f9ca0-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f9ca0-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f9ca0-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f9ca0-118">**Operazione riuscita** (0)</span><span class="sxs-lookup"><span data-stu-id="f9ca0-118">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f9ca0-119">**Errore-unità remota** (1)</span><span class="sxs-lookup"><span data-stu-id="f9ca0-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f9ca0-120">**Errore-unità rimovibile** (2)</span><span class="sxs-lookup"><span data-stu-id="f9ca0-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f9ca0-121">**Errore-unità non directory radice** (3)</span><span class="sxs-lookup"><span data-stu-id="f9ca0-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f9ca0-122">**Errore-unità sconosciuta** (4)</span><span class="sxs-lookup"><span data-stu-id="f9ca0-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f9ca0-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9ca0-123">Remarks</span></span>

<span data-ttu-id="f9ca0-124">Se non viene escluso, **Autochk** viene eseguito sul disco quando è impostato il bit dirty per il disco.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-124">If not excluded, **autochk** is performed on the disk when the dirty bit is set for the disk.</span></span> <span data-ttu-id="f9ca0-125">Si noti che le chiamate per escludere dischi non sono cumulative.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-125">Note that the calls to exclude disks are not cumulative.</span></span> <span data-ttu-id="f9ca0-126">Se viene effettuata una chiamata per escludere alcuni dischi, il nuovo elenco non viene aggiunto all'elenco di dischi già contrassegnati per l'esclusione.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-126">If a call is made to exclude some disks, then the new list is not added to the list of disks that are already marked for exclusion.</span></span> <span data-ttu-id="f9ca0-127">Il nuovo elenco di dischi sovrascrive l'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-127">The new list of disks overwrites the previous list.</span></span> <span data-ttu-id="f9ca0-128">Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-128">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="f9ca0-129">Non è applicabile alle unità logiche mappate.</span><span class="sxs-lookup"><span data-stu-id="f9ca0-129">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="f9ca0-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9ca0-130">Examples</span></span>

<span data-ttu-id="f9ca0-131">Nell'esempio di codice VBScript seguente si garantisce che Autochk.exe non venga eseguito sull'unità C alla successiva riavvio del computer, anche se l'unità C è stata impostata sul "bit dirty".</span><span class="sxs-lookup"><span data-stu-id="f9ca0-131">The following VBScript code sample ensures that Autochk.exe will not run against drive C the next time the computer reboots, even if the "dirty bit" has been set on drive C.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ExcludeFromAutoChk(Array("C:")) 
```



## <a name="requirements"></a><span data-ttu-id="f9ca0-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9ca0-132">Requirements</span></span>



| <span data-ttu-id="f9ca0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9ca0-133">Requirement</span></span> | <span data-ttu-id="f9ca0-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f9ca0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ca0-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9ca0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ca0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9ca0-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9ca0-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9ca0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ca0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9ca0-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9ca0-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9ca0-139">Namespace</span></span><br/>                | <span data-ttu-id="f9ca0-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f9ca0-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f9ca0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f9ca0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9ca0-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9ca0-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9ca0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f9ca0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9ca0-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ca0-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ca0-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9ca0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ca0-146">**\_Disco logico Win32**</span><span class="sxs-lookup"><span data-stu-id="f9ca0-146">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="f9ca0-147">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="f9ca0-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

