---
description: Pianifica Autochk da eseguire sull'unità disco rappresentata dal \_ disco logico Win32 al riavvio successivo se è impostato il bit modificato.
ms.assetid: 34f4c26b-6bfb-45d9-9d6c-0a9b735355f3
ms.tgt_platform: multiple
title: Metodo ScheduleAutoChk della classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.ScheduleAutoChk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2707810d919c119aff35f2313e9aa5218f7948f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966019"
---
# <a name="scheduleautochk-method-of-the-win32_logicaldisk-class"></a><span data-ttu-id="29385-103">Metodo ScheduleAutoChk della \_ classe disco logico Win32</span><span class="sxs-lookup"><span data-stu-id="29385-103">ScheduleAutoChk method of the Win32\_LogicalDisk class</span></span>

<span data-ttu-id="29385-104">Il metodo della classe **ScheduleAutoChk** pianifica l'esecuzione di Autochk sull'unità disco rappresentata dal [**\_ disco logico Win32**](win32-logicaldisk.md) al riavvio successivo se è impostato il bit dirty.</span><span class="sxs-lookup"><span data-stu-id="29385-104">The **ScheduleAutoChk** class method schedules Autochk to be run on the disk drive represented by the [**Win32\_LogicalDisk**](win32-logicaldisk.md) at the next reboot if the dirty bit is set.</span></span>

<span data-ttu-id="29385-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="29385-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="29385-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="29385-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="29385-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29385-107">Syntax</span></span>


```mof
uint32 ScheduleAutoChk(
  [in] string LogicalDisk[]
);
```



## <a name="parameters"></a><span data-ttu-id="29385-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29385-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29385-109">*Disco logico* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29385-109">*LogicalDisk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29385-110">Specifica l'elenco di unità da pianificare per Autochk al riavvio successivo.</span><span class="sxs-lookup"><span data-stu-id="29385-110">Specifies the list of drives to schedule for Autochk at the next reboot.</span></span> <span data-ttu-id="29385-111">La sintassi della stringa è costituita dalla lettera di unità seguita da due punti per il disco logico, ad esempio: "C:"</span><span class="sxs-lookup"><span data-stu-id="29385-111">The string syntax consists of the drive letter followed by a colon for the logical disk, for example: "C:"</span></span>

> [!Note]  
> <span data-ttu-id="29385-112">Controllare sempre la validità delle lettere di unità nella matrice *disco logico* quando i dati provengono da un'origine sconosciuta o da un'origine non attendibile.</span><span class="sxs-lookup"><span data-stu-id="29385-112">Always check the validity of the drive letters in the *LogicalDisk* array when the data comes from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29385-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29385-113">Return value</span></span>

<span data-ttu-id="29385-114">Restituisce un valore pari a 0 (zero) se ha esito positivo e un altro valore se si verifica un altro errore.</span><span class="sxs-lookup"><span data-stu-id="29385-114">Returns a value of 0 (zero) if successful, and some other value if any other error occurs.</span></span> <span data-ttu-id="29385-115">I valori sono elencati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="29385-115">Values are listed in the following list.</span></span> <span data-ttu-id="29385-116">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="29385-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="29385-117">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="29385-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="29385-118">**Nessun errore** (0)</span><span class="sxs-lookup"><span data-stu-id="29385-118">**No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="29385-119">**Errore-unità remota** (1)</span><span class="sxs-lookup"><span data-stu-id="29385-119">**Error - Remote Drive** (1)</span></span>
</dt> <dt>

<span data-ttu-id="29385-120">**Errore-unità rimovibile** (2)</span><span class="sxs-lookup"><span data-stu-id="29385-120">**Error - Removable Drive** (2)</span></span>
</dt> <dt>

<span data-ttu-id="29385-121">**Errore-unità non directory radice** (3)</span><span class="sxs-lookup"><span data-stu-id="29385-121">**Error - Drive Not Root Directory** (3)</span></span>
</dt> <dt>

<span data-ttu-id="29385-122">**Errore-unità sconosciuta** (4)</span><span class="sxs-lookup"><span data-stu-id="29385-122">**Error - Unknown Drive** (4)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="29385-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="29385-123">Remarks</span></span>

<span data-ttu-id="29385-124">Questo metodo è applicabile solo alle istanze del disco logico che rappresentano un disco fisico nel computer.</span><span class="sxs-lookup"><span data-stu-id="29385-124">This method is only applicable to those instances of logical disk that represent a physical disk in the machine.</span></span> <span data-ttu-id="29385-125">Questo metodo non è applicabile alle unità logiche mappate.</span><span class="sxs-lookup"><span data-stu-id="29385-125">This method is not applicable to mapped logical drives.</span></span>

## <a name="examples"></a><span data-ttu-id="29385-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="29385-126">Examples</span></span>

<span data-ttu-id="29385-127">Gli esempi VBScript e PowerShell seguenti pianificano Autochk.exe per l'esecuzione sull'unità C alla successiva riavvio del computer.</span><span class="sxs-lookup"><span data-stu-id="29385-127">The following VBScript and PowerShell samples schedule Autochk.exe to run against drive C the next time the computer reboots.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk") 
 
errReturn = objDisk.ScheduleAutoChk(Array("C:")) 
```


```PowerShell

Invoke-WmiMethod -path win32_logicaldisk -Name ScheduleAutoChk -ArgumentList @(&quot;C:&quot;)
```





## <a name="requirements"></a><span data-ttu-id="29385-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29385-128">Requirements</span></span>



| <span data-ttu-id="29385-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="29385-129">Requirement</span></span> | <span data-ttu-id="29385-130">Valore</span><span class="sxs-lookup"><span data-stu-id="29385-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29385-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29385-131">Minimum supported client</span></span><br/> | <span data-ttu-id="29385-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29385-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="29385-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29385-133">Minimum supported server</span></span><br/> | <span data-ttu-id="29385-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29385-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="29385-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="29385-135">Namespace</span></span><br/>                | <span data-ttu-id="29385-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="29385-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="29385-137">MOF</span><span class="sxs-lookup"><span data-stu-id="29385-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29385-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="29385-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="29385-139">DLL</span><span class="sxs-lookup"><span data-stu-id="29385-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29385-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29385-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29385-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29385-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29385-142">**\_Disco logico Win32**</span><span class="sxs-lookup"><span data-stu-id="29385-142">**Win32\_LogicalDisk**</span></span>](win32-logicaldisk.md)
</dt> </dl>

 

