---
description: Stampa una pagina di test.
ms.assetid: 7968e637-9817-4111-89f5-d3c6961395e5
ms.tgt_platform: multiple
title: Metodo PrintTestPage della classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.PrintTestPage
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: abf31237918d533ec43586ddd3d71204f2c8ae21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305286"
---
# <a name="printtestpage-method-of-the-win32_printer-class"></a><span data-ttu-id="bef9d-103">Metodo PrintTestPage della \_ classe Printer Win32</span><span class="sxs-lookup"><span data-stu-id="bef9d-103">PrintTestPage method of the Win32\_Printer class</span></span>

<span data-ttu-id="bef9d-104">Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PrintTestPage** stampa una pagina di prova.</span><span class="sxs-lookup"><span data-stu-id="bef9d-104">The **PrintTestPage** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method prints a test page.</span></span>

<span data-ttu-id="bef9d-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bef9d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bef9d-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bef9d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bef9d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bef9d-107">Syntax</span></span>


```mof
uint32 PrintTestPage();
```



## <a name="parameters"></a><span data-ttu-id="bef9d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bef9d-108">Parameters</span></span>

<span data-ttu-id="bef9d-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bef9d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bef9d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bef9d-110">Return value</span></span>

<span data-ttu-id="bef9d-111">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="bef9d-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="bef9d-112">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="bef9d-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="bef9d-113">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="bef9d-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="bef9d-114">**0**</span><span class="sxs-lookup"><span data-stu-id="bef9d-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="bef9d-115">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="bef9d-115">Success</span></span>

</dd> <dt>

<span data-ttu-id="bef9d-116">**5**</span><span class="sxs-lookup"><span data-stu-id="bef9d-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="bef9d-117">Accesso negato</span><span class="sxs-lookup"><span data-stu-id="bef9d-117">Access Denied</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bef9d-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="bef9d-118">Examples</span></span>

<span data-ttu-id="bef9d-119">Nell'esempio di codice PowerShell seguente viene stampata una pagina di test.</span><span class="sxs-lookup"><span data-stu-id="bef9d-119">The following PowerShell code sample prints a test page.</span></span>


```PowerShell
# Get printer objects from  WMI
$printers=Get-WmiObject Win32_Printer
"{0} Printers defined on this system" -f $printers.count

# Get a specific printer
$printer = $printers | where {$_.name -eq "\\smallguy\HP LaserJet 5M"}

# Display info
"Printer share name: {0}\{1}" -f $printer.servername, $printer.sharename
"Printer Port      : {0}    " -f $printer.PortName
  
# Print a test page
$printer.PrintTestPage()
```



## <a name="requirements"></a><span data-ttu-id="bef9d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bef9d-120">Requirements</span></span>



| <span data-ttu-id="bef9d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef9d-121">Requirement</span></span> | <span data-ttu-id="bef9d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="bef9d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef9d-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bef9d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="bef9d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bef9d-124">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bef9d-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bef9d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="bef9d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bef9d-126">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bef9d-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bef9d-127">Namespace</span></span><br/>                | <span data-ttu-id="bef9d-128">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bef9d-128">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="bef9d-129">MOF</span><span class="sxs-lookup"><span data-stu-id="bef9d-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bef9d-130"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bef9d-130"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="bef9d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="bef9d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef9d-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bef9d-132"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bef9d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bef9d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef9d-134">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="bef9d-134">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="bef9d-135">**\_Stampante Win32**</span><span class="sxs-lookup"><span data-stu-id="bef9d-135">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> </dl>

 

