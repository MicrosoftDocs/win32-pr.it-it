---
description: Richiama l'operazione Chkdsk sul disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Metodo CHKDSK della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 662fc8739f90eea15295b762edc446ac16677aef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127223"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="7cd24-103">Metodo CHKDSK della classe Win32 \_ disco logico</span><span class="sxs-lookup"><span data-stu-id="7cd24-103">Chkdsk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="7cd24-104">Il metodo dell'istanza **chkdsk** richiama l'operazione **chkdsk** sul disco.</span><span class="sxs-lookup"><span data-stu-id="7cd24-104">The **Chkdsk** instance method invokes the **chkdsk** operation on the disk.</span></span>

<span data-ttu-id="7cd24-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7cd24-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7cd24-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7cd24-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd24-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cd24-107">Syntax</span></span>


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a><span data-ttu-id="7cd24-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cd24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd24-109">*FixErrors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-109">*FixErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-110">Indica cosa fare per gli errori rilevati nel disco.</span><span class="sxs-lookup"><span data-stu-id="7cd24-110">Indicates what should be done to errors found on the disk.</span></span> <span data-ttu-id="7cd24-111">Se **true**, gli errori sono corretti.</span><span class="sxs-lookup"><span data-stu-id="7cd24-111">If **true**, then errors are fixed.</span></span> <span data-ttu-id="7cd24-112">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-112">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-113">*VigorousIndexCheck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-113">*VigorousIndexCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-114">Se **true**, deve essere eseguita una verifica meno vigorosa delle voci di indice.</span><span class="sxs-lookup"><span data-stu-id="7cd24-114">If **true**, a less vigorous check of index entries should be performed.</span></span> <span data-ttu-id="7cd24-115">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-115">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-116">*SkipFolderCycle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-116">*SkipFolderCycle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-117">Se **true**, il controllo del ciclo di cartelle deve essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="7cd24-117">If **true**, the folder cycle checking should be skipped.</span></span> <span data-ttu-id="7cd24-118">Il valore predefinito è **True**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-118">The default is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-119">*ForceDismount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-119">*ForceDismount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-120">Se **true**, l'unità deve essere disinstallata prima del controllo.</span><span class="sxs-lookup"><span data-stu-id="7cd24-120">If **true**, the drive should be forced to dismount before checking.</span></span> <span data-ttu-id="7cd24-121">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-121">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-122">*RecoverBadSectors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-122">*RecoverBadSectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-123">Se **true**, i settori danneggiati devono essere individuati e le informazioni leggibili devono essere recuperate da questi settori.</span><span class="sxs-lookup"><span data-stu-id="7cd24-123">If **true**, the bad sectors should be located and the readable information should be recovered from these sectors.</span></span> <span data-ttu-id="7cd24-124">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-124">The default is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-125">*OKToRunAtBootUp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7cd24-125">*OKToRunAtBootUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-126">Se **true**, l'operazione **chkdsk** deve essere eseguita al momento dell'avvio successivo, nel caso in cui non sia stato possibile eseguire l'operazione perché il disco è bloccato al momento della chiamata di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="7cd24-126">If **true**, the **chkdsk** operation should be performed at next boot up time, in case the operation could not be performed because the disk is locked at time this method is called.</span></span> <span data-ttu-id="7cd24-127">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7cd24-127">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd24-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cd24-128">Return value</span></span>

<span data-ttu-id="7cd24-129">Restituisce un valore pari a 0 (zero) se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7cd24-129">Returns a value of 0 (zero) if successful.</span></span> <span data-ttu-id="7cd24-130">Gli altri valori sono elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="7cd24-130">Other values are listed in the following list.</span></span> <span data-ttu-id="7cd24-131">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7cd24-131">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7cd24-132">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7cd24-132">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7cd24-133">**Operazione riuscita-Chkdsk completata**</span><span class="sxs-lookup"><span data-stu-id="7cd24-133">**Success - Chkdsk completed**</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-134">0</span><span class="sxs-lookup"><span data-stu-id="7cd24-134">0</span></span>

<span data-ttu-id="7cd24-135">Operazione riuscita- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) completata</span><span class="sxs-lookup"><span data-stu-id="7cd24-135">Success - [**Chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) Completed</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-136">**Operazione riuscita-bloccato e CHKDSK pianificati al riavvio**</span><span class="sxs-lookup"><span data-stu-id="7cd24-136">**Success - Locked and chkdsk scheduled on reboot**</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-137">1</span><span class="sxs-lookup"><span data-stu-id="7cd24-137">1</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-138">**Errore-file system sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7cd24-138">**Failure - Unknown file system**</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-139">2</span><span class="sxs-lookup"><span data-stu-id="7cd24-139">2</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-140">**Errore-errore sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="7cd24-140">**Failure - Unknown error**</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-141">3</span><span class="sxs-lookup"><span data-stu-id="7cd24-141">3</span></span>

</dd> <dt>

<span data-ttu-id="7cd24-142">**Errore-file System non supportato**</span><span class="sxs-lookup"><span data-stu-id="7cd24-142">**Failure - Unsupported File System**</span></span>
</dt> <dd>

<span data-ttu-id="7cd24-143">4</span><span class="sxs-lookup"><span data-stu-id="7cd24-143">4</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cd24-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cd24-144">Remarks</span></span>

<span data-ttu-id="7cd24-145">Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer.</span><span class="sxs-lookup"><span data-stu-id="7cd24-145">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="7cd24-146">Non è applicabile alle unità logiche mappate.</span><span class="sxs-lookup"><span data-stu-id="7cd24-146">It is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="7cd24-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="7cd24-147">Examples</span></span>

<span data-ttu-id="7cd24-148">Il[valore del bit dirty CHKDSK impostato in un](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) esempio di codice PowerShell del server esamina il sistema remoto e restituisce true o false se è stato impostato il flag chkdsk/f.</span><span class="sxs-lookup"><span data-stu-id="7cd24-148">The[Is CHKDSK Dirty Bit Set on a server](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) PowerShell code sample examines the remote system and returns a true or false if the chkdsk /f flag was set.</span></span>

<span data-ttu-id="7cd24-149">L'esempio di codice PowerShell per l' [analisi remota del disco](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) avvia in modalità remota o Pianifica il disco di analisi.</span><span class="sxs-lookup"><span data-stu-id="7cd24-149">The [Remotely scan disk](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) PowerShell code sample remotely starts or schedules Scan Disk.</span></span>

<span data-ttu-id="7cd24-150">Nell'esempio di codice VBScript seguente viene eseguito ChkDsk.exe sull'unità D in un computer.</span><span class="sxs-lookup"><span data-stu-id="7cd24-150">The following VBScript code sample Runs ChkDsk.exe against drive D on a computer.</span></span>


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
```



## <a name="requirements"></a><span data-ttu-id="7cd24-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cd24-151">Requirements</span></span>



| <span data-ttu-id="7cd24-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd24-152">Requirement</span></span> | <span data-ttu-id="7cd24-153">Valore</span><span class="sxs-lookup"><span data-stu-id="7cd24-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd24-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cd24-154">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd24-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cd24-155">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cd24-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cd24-156">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd24-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cd24-157">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cd24-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7cd24-158">Namespace</span></span><br/>                | <span data-ttu-id="7cd24-159">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7cd24-159">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7cd24-160">MOF</span><span class="sxs-lookup"><span data-stu-id="7cd24-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cd24-161"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cd24-161"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cd24-162">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd24-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd24-163"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cd24-163"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd24-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cd24-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd24-165">**\_Disco logico Win32**</span><span class="sxs-lookup"><span data-stu-id="7cd24-165">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> <dt>

[<span data-ttu-id="7cd24-166">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="7cd24-166">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

