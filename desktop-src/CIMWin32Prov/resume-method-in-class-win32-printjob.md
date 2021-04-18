---
description: Il metodo Resume WMI class continua un processo di stampa in pausa.
ms.assetid: acfbca2b-19af-4339-bbca-834db50c3d8d
ms.tgt_platform: multiple
title: Metodo Resume della classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Resume
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f8ca1602eb29e1e18d83d2e8b79760d13f63e101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304515"
---
# <a name="resume-method-of-the-win32_printjob-class"></a><span data-ttu-id="ca1b2-103">Metodo Resume della classe Win32 \_ PrintJob</span><span class="sxs-lookup"><span data-stu-id="ca1b2-103">Resume method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="ca1b2-104">Il metodo **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) continua un processo di stampa in pausa.</span><span class="sxs-lookup"><span data-stu-id="ca1b2-104">The **Resume** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method continues a paused print job.</span></span>

<span data-ttu-id="ca1b2-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ca1b2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ca1b2-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ca1b2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca1b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca1b2-107">Syntax</span></span>


```mof
uint32 Resume();
```



## <a name="parameters"></a><span data-ttu-id="ca1b2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca1b2-108">Parameters</span></span>

<span data-ttu-id="ca1b2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="ca1b2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca1b2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca1b2-110">Return value</span></span>

<span data-ttu-id="ca1b2-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="ca1b2-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca1b2-112">**0**</span><span class="sxs-lookup"><span data-stu-id="ca1b2-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ca1b2-113">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="ca1b2-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="ca1b2-114">**5**</span><span class="sxs-lookup"><span data-stu-id="ca1b2-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ca1b2-115">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="ca1b2-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ca1b2-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="ca1b2-116">Examples</span></span>

<span data-ttu-id="ca1b2-117">Nell'esempio di codice VBScript seguente vengono ripresi tutti i processi di stampa in un computer.</span><span class="sxs-lookup"><span data-stu-id="ca1b2-117">The following VBScript code sample resumes all the print jobs on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Resume 
Next 
```



## <a name="requirements"></a><span data-ttu-id="ca1b2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca1b2-118">Requirements</span></span>



| <span data-ttu-id="ca1b2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca1b2-119">Requirement</span></span> | <span data-ttu-id="ca1b2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ca1b2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1b2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca1b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1b2-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca1b2-122">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ca1b2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca1b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1b2-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca1b2-124">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ca1b2-125">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca1b2-125">Namespace</span></span><br/>                | <span data-ttu-id="ca1b2-126">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ca1b2-126">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="ca1b2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ca1b2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca1b2-128"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca1b2-128"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca1b2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ca1b2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca1b2-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca1b2-130"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ca1b2-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca1b2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca1b2-132">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ca1b2-132">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ca1b2-133">**\_PrintJob Win32**</span><span class="sxs-lookup"><span data-stu-id="ca1b2-133">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

