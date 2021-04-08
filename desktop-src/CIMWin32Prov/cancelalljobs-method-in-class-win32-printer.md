---
description: Rimuove tutti i processi, incluso quello attualmente stampato dalla coda.
ms.assetid: d7466513-b123-43af-ab17-b3213ba80284
ms.tgt_platform: multiple
title: Metodo CancelAllJobs della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.CancelAllJobs
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d2d816dab837aafd7b6e9c6beff75c4e62b19b2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877410"
---
# <a name="cancelalljobs-method-of-the-win32_printer-class"></a><span data-ttu-id="d2d4b-103">Metodo CancelAllJobs della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="d2d4b-103">CancelAllJobs method of the Win32\_Printer class</span></span>

<span data-ttu-id="d2d4b-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CancelAllJobs** rimuove tutti i processi, incluso quello attualmente stampato dalla coda.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-104">The **CancelAllJobs** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method removes all jobs, including the one currently printing from the queue.</span></span>

<span data-ttu-id="d2d4b-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d2d4b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2d4b-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2d4b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d4b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2d4b-107">Syntax</span></span>


```mof
uint32 CancelAllJobs();
```



## <a name="parameters"></a><span data-ttu-id="d2d4b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2d4b-108">Parameters</span></span>

<span data-ttu-id="d2d4b-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2d4b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2d4b-110">Return value</span></span>

<span data-ttu-id="d2d4b-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="d2d4b-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d2d4b-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d2d4b-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="d2d4b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d2d4b-114">**0**</span><span class="sxs-lookup"><span data-stu-id="d2d4b-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d2d4b-115">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="d2d4b-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="d2d4b-116">**5**</span><span class="sxs-lookup"><span data-stu-id="d2d4b-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="d2d4b-117">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="d2d4b-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d2d4b-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="d2d4b-118">Examples</span></span>

<span data-ttu-id="d2d4b-119">La [notifica agli utenti quando viene eliminata una coda di stampa](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) USA Msg.exe per inviare un avviso di rete a tutti gli utenti che dispongono di documenti in una coda di stampa che stanno per essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-119">The [Notify Users When a Print Queue is Purged](https://Gallery.TechNet.Microsoft.Com/9f8ad84e-239d-45bf-a14f-ad8f3fc4988a) uses Msg.exe to send a network alert to any users who had documents in a print queue about to be purged.</span></span> <span data-ttu-id="d2d4b-120">Dopo aver inviato gli avvisi, lo script Elimina la coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-120">After sending the alerts, the script purges the print queue.</span></span>

<span data-ttu-id="d2d4b-121">L'esempio di codice [Elimina tutti i processi di stampa](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript Elimina tutti i processi di stampa nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-121">The [Delete all print jobs](https://Gallery.TechNet.Microsoft.Com/0e89fa7c-a837-4607-b421-c870142e7323) VBScript code sample deletes all print jobs on the local computer.</span></span>

<span data-ttu-id="d2d4b-122">L'esempio VBScript seguente elimina tutti i processi di stampa per una stampante denominata HP QuietJet.</span><span class="sxs-lookup"><span data-stu-id="d2d4b-122">The following VBScript sample deletes all the print jobs for a printer named HP QuietJet.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'HP QuietJet'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.CancelAllJobs() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d2d4b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2d4b-123">Requirements</span></span>



| <span data-ttu-id="d2d4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d4b-124">Requirement</span></span> | <span data-ttu-id="d2d4b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d2d4b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d4b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d4b-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2d4b-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d2d4b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d4b-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2d4b-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d2d4b-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2d4b-130">Namespace</span></span><br/>                | <span data-ttu-id="d2d4b-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d2d4b-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d2d4b-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d2d4b-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2d4b-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2d4b-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2d4b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d4b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d4b-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2d4b-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d2d4b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2d4b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d4b-137">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d2d4b-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d2d4b-138">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="d2d4b-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

