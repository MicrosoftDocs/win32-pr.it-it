---
description: Crea un nuovo driver della stampante.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Metodo AddPrinterDriver della classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03c029d7689743150235d20b0658cd154ef64a4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401382"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a><span data-ttu-id="fba8a-103">Metodo AddPrinterDriver della \_ classe PrinterDriver Win32</span><span class="sxs-lookup"><span data-stu-id="fba8a-103">AddPrinterDriver method of the Win32\_PrinterDriver class</span></span>

<span data-ttu-id="fba8a-104">Il metodo della classe **AddPrinterDriver** crea un nuovo driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="fba8a-104">The **AddPrinterDriver** class method creates a new printer driver.</span></span>

<span data-ttu-id="fba8a-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fba8a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fba8a-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fba8a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fba8a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fba8a-107">Syntax</span></span>


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="fba8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fba8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba8a-109">*DriverInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fba8a-109">*DriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba8a-110">Istanza della classe [**Win32 \_ PrinterDriver**](win32-printerdriver.md) che rappresenta il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="fba8a-110">An instance of the [**Win32\_PrinterDriver**](win32-printerdriver.md) class that represents the printer driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba8a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fba8a-111">Return value</span></span>

<span data-ttu-id="fba8a-112">Restituisce uno dei valori elencati nell'elenco seguente o qualsiasi altro valore per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fba8a-112">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="fba8a-113">Per i valori diversi da quelli elencati nell'elenco seguente, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants).</span><span class="sxs-lookup"><span data-stu-id="fba8a-113">For values different from those listed in the following list, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants).</span></span>

<dl> <dt>

<span data-ttu-id="fba8a-114">**0**</span><span class="sxs-lookup"><span data-stu-id="fba8a-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="fba8a-115">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fba8a-115">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fba8a-116">**5**</span><span class="sxs-lookup"><span data-stu-id="fba8a-116">**5**</span></span>
</dt> <dd>

<span data-ttu-id="fba8a-117">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="fba8a-117">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fba8a-118">**87**</span><span class="sxs-lookup"><span data-stu-id="fba8a-118">**87**</span></span>
</dt> <dd>

<span data-ttu-id="fba8a-119">Parametro non corretto.</span><span class="sxs-lookup"><span data-stu-id="fba8a-119">The parameter is incorrect.</span></span> <span data-ttu-id="fba8a-120">Può verificarsi quando l'oggetto non è riempito correttamente o quando il driver non è stato trovato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="fba8a-120">May occur when the object is not correctly filled or when driver can not be found in the system.</span></span> <span data-ttu-id="fba8a-121">In alternativa, l'attributo del nome può essere diverso dal modello specificato nel file con estensione inf.</span><span class="sxs-lookup"><span data-stu-id="fba8a-121">Alternately, the name attribute may be different than the model specified in the .inf file.</span></span> <span data-ttu-id="fba8a-122">In alternativa, potrebbe essere presente una barra rovesciata (" \\ ") mancante in un attributo pathFile.</span><span class="sxs-lookup"><span data-stu-id="fba8a-122">Or, there may be a missing backslash ("\\") on a PathFile attribute.</span></span>

</dd> <dt>

<span data-ttu-id="fba8a-123">**1797**</span><span class="sxs-lookup"><span data-stu-id="fba8a-123">**1797**</span></span>
</dt> <dd>

<span data-ttu-id="fba8a-124">Il driver della stampante è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="fba8a-124">The printer driver is unknown.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fba8a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="fba8a-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fba8a-126">Quando si usa il metodo **AddPrinterDriver** , è necessario usare **SeLoadDriverPrivilege** per caricare o scaricare un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fba8a-126">When using the **AddPrinterDriver** method you must use **SeLoadDriverPrivilege** to load or unload a device driver.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fba8a-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="fba8a-127">Examples</span></span>

<span data-ttu-id="fba8a-128">L'esempio di[installazione di un driver della stampante non trovato nell'esempio di codice CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript di driver installa una stampante ipotetica utilizzando un driver di stampa non trovato in Drivers.cab.</span><span class="sxs-lookup"><span data-stu-id="fba8a-128">The[Install a Printer Driver not Found in Drivers Cab](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) VBScript code example installs a hypothetical printer using a print driver not found in Drivers.cab.</span></span>

<span data-ttu-id="fba8a-129">Nell'esempio VBScript seguente viene installato il driver della stampante per una stampante Apple LaserWriter 8500.</span><span class="sxs-lookup"><span data-stu-id="fba8a-129">The following VBScript sample installs the printer driver for an Apple LaserWriter 8500 printer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a><span data-ttu-id="fba8a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fba8a-130">Requirements</span></span>



| <span data-ttu-id="fba8a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba8a-131">Requirement</span></span> | <span data-ttu-id="fba8a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fba8a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba8a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fba8a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fba8a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fba8a-134">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="fba8a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fba8a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fba8a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fba8a-136">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="fba8a-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fba8a-137">Namespace</span></span><br/>                | <span data-ttu-id="fba8a-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fba8a-138">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="fba8a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fba8a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba8a-140"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba8a-140"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba8a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fba8a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba8a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba8a-142"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="fba8a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fba8a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba8a-144">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="fba8a-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fba8a-145">**\_PrinterDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="fba8a-145">**Win32\_PrinterDriver**</span></span>](win32-printerdriver.md)
</dt> </dl>

 

