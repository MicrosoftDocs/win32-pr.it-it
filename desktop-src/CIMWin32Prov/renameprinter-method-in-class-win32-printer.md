---
description: Rinomina una stampante.
ms.assetid: afbef871-5153-4b9e-9ad3-4d271a497c37
ms.tgt_platform: multiple
title: Metodo RenamePrinter della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.RenamePrinter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6066dfd4280f7c43c9804933fb1ed5fb931bfa08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225519"
---
# <a name="renameprinter-method-of-the-win32_printer-class"></a><span data-ttu-id="5c249-103">Metodo RenamePrinter della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="5c249-103">RenamePrinter method of the Win32\_Printer class</span></span>

<span data-ttu-id="5c249-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **RenamePrinter** Rinomina una stampante.</span><span class="sxs-lookup"><span data-stu-id="5c249-104">The **RenamePrinter** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a printer.</span></span>

<span data-ttu-id="5c249-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5c249-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5c249-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5c249-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c249-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c249-107">Syntax</span></span>


```mof
uint32 RenamePrinter(
  [in] string NewPrinterName
);
```



## <a name="parameters"></a><span data-ttu-id="5c249-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c249-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c249-109">*NewPrinterName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c249-109">*NewPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c249-110">Nuovo nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="5c249-110">New printer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c249-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c249-111">Return value</span></span>

<span data-ttu-id="5c249-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="5c249-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="5c249-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5c249-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5c249-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5c249-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5c249-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5c249-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5c249-116">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="5c249-116">Success</span></span>

</dd> <dt>

<span data-ttu-id="5c249-117">**5**</span><span class="sxs-lookup"><span data-stu-id="5c249-117">**5**</span></span>
</dt> <dd>

<span data-ttu-id="5c249-118">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="5c249-118">Access Denied</span></span>

</dd> <dt>

<span data-ttu-id="5c249-119">**1801**</span><span class="sxs-lookup"><span data-stu-id="5c249-119">**1801**</span></span>
</dt> <dd>

<span data-ttu-id="5c249-120">Nome stampante non valido</span><span class="sxs-lookup"><span data-stu-id="5c249-120">Invalid Printer Name</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5c249-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c249-121">Examples</span></span>

<span data-ttu-id="5c249-122">Nell'esempio VBScript seguente vengono rinominate sia una stampante che il relativo nome di condivisione della stampante.</span><span class="sxs-lookup"><span data-stu-id="5c249-122">The following VBScript example renames both a printer and its printer share name.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_Printer Where DeviceID = 'HP LaserJet 4Si M'") 
 
For Each objPrinter in colPrinters 
    objPrinter.RenamePrinter("ArtDepartmentPrinter") 
Next 
 
Set colPrinters = objWMIService.ExecQuery _ 
    ("Select * From Win32_Printer Where DeviceID = 'ArtDepartmentPrinter' ") 
 
For Each objPrinter in colPrinters 
    objPrinter.ShareName = "ArtDepartmentPrinter" 
    objPrinter.Put_ 
Next 
```



## <a name="requirements"></a><span data-ttu-id="5c249-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c249-123">Requirements</span></span>



| <span data-ttu-id="5c249-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c249-124">Requirement</span></span> | <span data-ttu-id="5c249-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5c249-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c249-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c249-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c249-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c249-127">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5c249-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c249-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c249-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c249-129">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5c249-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c249-130">Namespace</span></span><br/>                | <span data-ttu-id="5c249-131">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5c249-131">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="5c249-132">MOF</span><span class="sxs-lookup"><span data-stu-id="5c249-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c249-133"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c249-133"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c249-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5c249-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c249-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c249-135"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="5c249-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c249-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c249-137">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="5c249-137">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5c249-138">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="5c249-138">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

