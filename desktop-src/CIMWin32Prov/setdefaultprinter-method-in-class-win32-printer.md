---
description: Il metodo della classe WMI SetDefaultPrinter imposta la stampante di sistema predefinita per l'utente che chiama il metodo.
ms.assetid: 7e896961-363d-4b8b-9d22-bbfc9681e97b
ms.tgt_platform: multiple
title: Metodo SetDefaultPrinter della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetDefaultPrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a18c6d7771eb0e95d86142f41262d721509eb6f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878382"
---
# <a name="setdefaultprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="e15bd-103">Metodo SetDefaultPrinter della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="e15bd-103">SetDefaultPrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="e15bd-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultPrinter** imposta la stampante di sistema predefinita per l'utente che chiama il metodo.</span><span class="sxs-lookup"><span data-stu-id="e15bd-104">The **SetDefaultPrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the default system printer for the user calling the method.</span></span>

<span data-ttu-id="e15bd-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="e15bd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e15bd-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e15bd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e15bd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e15bd-107">Syntax</span></span>


```mof
uint32 SetDefaultPrinter();
```



## <a name="parameters"></a><span data-ttu-id="e15bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e15bd-108">Parameters</span></span>

<span data-ttu-id="e15bd-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="e15bd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e15bd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e15bd-110">Return value</span></span>

<span data-ttu-id="e15bd-111">Restituisce 0 (zero) se ha esito positivo e un altro valore se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="e15bd-111">Returns 0 (zero) if successful, and some other value if an error occurs.</span></span> <span data-ttu-id="e15bd-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="e15bd-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="e15bd-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="e15bd-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

## <a name="examples"></a><span data-ttu-id="e15bd-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="e15bd-114">Examples</span></span>

<span data-ttu-id="e15bd-115">L'esempio [Install an TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript installa una porta stampante TCP/IP, installa una stampante e quindi imposta la stampante come predefinita.</span><span class="sxs-lookup"><span data-stu-id="e15bd-115">The [Install a TCP/IP Printer Port and Printer](https://Gallery.TechNet.Microsoft.Com/41a4c996-b7f7-4d58-808d-2acac20ddbf7) VBScript sample installs a TCP/IP printer port, installs a printer, and then sets the printer to be default.</span></span>

<span data-ttu-id="e15bd-116">Nell'esempio di codice VBScript riportato di seguito viene impostata la stampante predefinita in un computer.</span><span class="sxs-lookup"><span data-stu-id="e15bd-116">The following VBScript code sample sets the default printer on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where Name = 'ScriptedPrinter'") 
 
For Each objPrinter in colInstalledPrinters 
    objPrinter.SetDefaultPrinter() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="e15bd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e15bd-117">Requirements</span></span>



| <span data-ttu-id="e15bd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e15bd-118">Requirement</span></span> | <span data-ttu-id="e15bd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e15bd-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15bd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e15bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e15bd-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e15bd-121">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e15bd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e15bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e15bd-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e15bd-123">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e15bd-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e15bd-124">Namespace</span></span><br/>                | <span data-ttu-id="e15bd-125">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e15bd-125">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="e15bd-126">MOF</span><span class="sxs-lookup"><span data-stu-id="e15bd-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e15bd-127"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e15bd-127"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="e15bd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e15bd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e15bd-129"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e15bd-129"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e15bd-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e15bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e15bd-131">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="e15bd-131">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="e15bd-132">Attività WMI: stampanti e stampa</span><span class="sxs-lookup"><span data-stu-id="e15bd-132">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="e15bd-133">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="e15bd-133">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

