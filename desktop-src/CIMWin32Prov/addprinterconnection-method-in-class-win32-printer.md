---
description: Fornisce una connessione a una stampante esistente sulla rete e la aggiunge all'elenco delle stampanti disponibili.
ms.assetid: 44149051-4abf-4428-8999-355dd0b0ce69
ms.tgt_platform: multiple
title: Metodo AddPrinterConnection della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.AddPrinterConnection
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2ad9e225a60e33fdf51d5f677dd4342acd148b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877417"
---
# <a name="addprinterconnection-method-of-the-win32_printer-class"></a><span data-ttu-id="87b85-103">Metodo AddPrinterConnection della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="87b85-103">AddPrinterConnection method of the Win32\_Printer class</span></span>

<span data-ttu-id="87b85-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **AddPrinterConnection** fornisce una connessione a una stampante esistente sulla rete e la aggiunge all'elenco delle stampanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="87b85-104">The **AddPrinterConnection** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method provides a connection to an existing printer on the network, and adds it to the list of available printers.</span></span>

<span data-ttu-id="87b85-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="87b85-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="87b85-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="87b85-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="87b85-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87b85-107">Syntax</span></span>


```mof
uint32 AddPrinterConnection(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="87b85-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87b85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87b85-109">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87b85-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87b85-110">Nome descrittivo per la stampante.</span><span class="sxs-lookup"><span data-stu-id="87b85-110">Friendly name for the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87b85-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87b85-111">Return value</span></span>

<span data-ttu-id="87b85-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="87b85-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="87b85-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="87b85-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="87b85-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="87b85-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="87b85-115">**0**</span><span class="sxs-lookup"><span data-stu-id="87b85-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="87b85-116">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="87b85-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="87b85-117">**5**</span><span class="sxs-lookup"><span data-stu-id="87b85-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="87b85-118">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="87b85-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="87b85-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="87b85-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="87b85-120">Nome stampante non valido</span><span class="sxs-lookup"><span data-stu-id="87b85-120">Invalid Printer Name</span></span>

</dd> <dt>

<span data-ttu-id="87b85-121">**1930**</span><span class="sxs-lookup"><span data-stu-id="87b85-121">**1930**</span></span>
</dt> <dd>

<span data-ttu-id="87b85-122">Driver della stampante incompatibile</span><span class="sxs-lookup"><span data-stu-id="87b85-122">Incompatible Printer Driver</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="87b85-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="87b85-123">Examples</span></span>

<span data-ttu-id="87b85-124">L'esempio [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) di PowerShell installa tutti i driver della stampante da un server di stampa specificato.</span><span class="sxs-lookup"><span data-stu-id="87b85-124">The [Add-PrinterDriver](https://Gallery.TechNet.Microsoft.Com/1c8f4c0d-9439-4af0-8840-59686d9b4bc1) PowerShell sample installs all printer drivers from a specified print server.</span></span>

<span data-ttu-id="87b85-125">L'esempio [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell elenca le stampanti condivise in un computer remoto e consente di aggiungere una connessione alla stampante dal computer remoto al computer.</span><span class="sxs-lookup"><span data-stu-id="87b85-125">The [ListSharedPrintersAddPrintConnection.ps1](https://Gallery.TechNet.Microsoft.Com/b7f74333-e78b-49d8-b23a-f1307d5b1ee6) PowerShell sample lists shared printers on a remote comptuer, and gives you the ability to add a printer connection from the remote computer to your computer.</span></span>

<span data-ttu-id="87b85-126">Nell'esempio di codice VBScript seguente viene aggiunta una stampante locale.</span><span class="sxs-lookup"><span data-stu-id="87b85-126">The following VBScript code sample adds a local printer.</span></span>


```VB
Dim strPrinterName as String = "Isidoros Printer"
Dim strComputer AsString = My.Computer.Name
Dim objWMIService, objPrinter AsObject
objWMIService = GetObject(
"winmgmts:" _

& 
"{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

objPrinter = objWMIService.Get(
"Win32_Printer").SpawnInstance_
objPrinter.Name = strPrinterName
objPrinter.DriverName = "Generic / Text Only"
objPrinter.PortName = 
"c:\temp\file.prn"
objPrinter.DeviceID = strPrinterName
'objPrinter.Location = "Athens, Greece"
objPrinter.Network = 
False
objPrinter.Shared = 
False'objPrinter.ShareName = "MyShareName"
objPrinter.Put_()
```



## <a name="requirements"></a><span data-ttu-id="87b85-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87b85-127">Requirements</span></span>



| <span data-ttu-id="87b85-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="87b85-128">Requirement</span></span> | <span data-ttu-id="87b85-129">Valore</span><span class="sxs-lookup"><span data-stu-id="87b85-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87b85-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87b85-130">Minimum supported client</span></span><br/> | <span data-ttu-id="87b85-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87b85-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="87b85-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87b85-132">Minimum supported server</span></span><br/> | <span data-ttu-id="87b85-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87b85-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="87b85-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="87b85-134">Namespace</span></span><br/>                | <span data-ttu-id="87b85-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="87b85-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="87b85-136">MOF</span><span class="sxs-lookup"><span data-stu-id="87b85-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87b85-137"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87b85-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="87b85-138">DLL</span><span class="sxs-lookup"><span data-stu-id="87b85-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87b85-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87b85-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="87b85-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87b85-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b85-141">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="87b85-141">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="87b85-142">Attività WMI: stampanti e stampa</span><span class="sxs-lookup"><span data-stu-id="87b85-142">WMI Tasks: Printers and Printing</span></span>](/windows/desktop/WmiSdk/wmi-tasks--printers-and-printing)
</dt> <dt>

[<span data-ttu-id="87b85-143">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="87b85-143">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

