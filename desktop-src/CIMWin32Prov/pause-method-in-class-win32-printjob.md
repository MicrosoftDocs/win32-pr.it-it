---
description: Il metodo Sospendi classe WMI sospende un processo di stampa.
ms.assetid: f1e3906f-1ca2-45c0-9863-5762e4e2119a
ms.tgt_platform: multiple
title: Metodo pause della classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob.Pause
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 785ba54b56c65fd298b6ef763ec2d7eca0d8f61a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878393"
---
# <a name="pause-method-of-the-win32_printjob-class"></a><span data-ttu-id="a11fb-103">Metodo pause della classe Win32 \_ PrintJob</span><span class="sxs-lookup"><span data-stu-id="a11fb-103">Pause method of the Win32\_PrintJob class</span></span>

<span data-ttu-id="a11fb-104">Il metodo **Sospendi** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) sospende un processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="a11fb-104">The **Pause** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method suspends a print job.</span></span>

<span data-ttu-id="a11fb-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="a11fb-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a11fb-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a11fb-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a11fb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a11fb-107">Syntax</span></span>


```mof
uint32 Pause();
```



## <a name="parameters"></a><span data-ttu-id="a11fb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a11fb-108">Parameters</span></span>

<span data-ttu-id="a11fb-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a11fb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a11fb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a11fb-110">Return value</span></span>

<span data-ttu-id="a11fb-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="a11fb-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="a11fb-112">**0**</span><span class="sxs-lookup"><span data-stu-id="a11fb-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a11fb-113">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="a11fb-113">Success</span></span>

</dd> <dt>

<span data-ttu-id="a11fb-114">**5**</span><span class="sxs-lookup"><span data-stu-id="a11fb-114">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a11fb-115">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="a11fb-115">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a11fb-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="a11fb-116">Examples</span></span>

<span data-ttu-id="a11fb-117">L'esempio [Sospendi tutte le stampanti con code di stampa vuote di](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) codice VBScript sospende tutte le stampanti che non dispongono di processi di stampa in sospeso.</span><span class="sxs-lookup"><span data-stu-id="a11fb-117">The [Pause All Printers with Empty Print Queues](https://Gallery.TechNet.Microsoft.Com/cf2b6b61-8ffe-444b-857b-e3a205bc693c) VBScript code sample pauses any printers that have no pending print jobs.</span></span>

<span data-ttu-id="a11fb-118">Nell'esempio di codice VBScript seguente vengono sospesi tutti i processi di stampa in un server di stampa.</span><span class="sxs-lookup"><span data-stu-id="a11fb-118">The following VBScript code sample pauses all the print jobs on a print server.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrintJobs =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrintJob") 
 
For Each objPrintJob in colPrintJobs  
    objPrintJob.Pause 
Next 
```



## <a name="requirements"></a><span data-ttu-id="a11fb-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a11fb-119">Requirements</span></span>



| <span data-ttu-id="a11fb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a11fb-120">Requirement</span></span> | <span data-ttu-id="a11fb-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a11fb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a11fb-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a11fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a11fb-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a11fb-123">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="a11fb-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a11fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a11fb-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a11fb-125">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="a11fb-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a11fb-126">Namespace</span></span><br/>                | <span data-ttu-id="a11fb-127">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a11fb-127">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="a11fb-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a11fb-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a11fb-129"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a11fb-129"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="a11fb-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a11fb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a11fb-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a11fb-131"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a11fb-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a11fb-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11fb-133">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="a11fb-133">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a11fb-134">**\_PrintJob Win32**</span><span class="sxs-lookup"><span data-stu-id="a11fb-134">**Win32\_PrintJob**</span></span>](win32-printjob.md)
</dt> </dl>

 

