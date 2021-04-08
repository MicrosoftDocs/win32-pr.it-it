---
description: La \_ classe WMI PrinterDriver Win32 rappresenta i driver per un' \_ istanza di stampante Win32.
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877817"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="1d19f-103">Win32 \_ PrinterDriver (classe)</span><span class="sxs-lookup"><span data-stu-id="1d19f-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="1d19f-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterDriver Win32** rappresenta i driver per un'istanza di [**\_ stampante Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="1d19f-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="1d19f-105">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le proprietà ereditate, ma esclude i metodi.</span><span class="sxs-lookup"><span data-stu-id="1d19f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="1d19f-106">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="1d19f-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d19f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d19f-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="1d19f-108">Members</span><span class="sxs-lookup"><span data-stu-id="1d19f-108">Members</span></span>

<span data-ttu-id="1d19f-109">La classe **Win32 \_ PrinterDriver** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d19f-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="1d19f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="1d19f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d19f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d19f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d19f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="1d19f-112">Methods</span></span>

<span data-ttu-id="1d19f-113">La classe **Win32 \_ PrinterDriver** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1d19f-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="1d19f-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="1d19f-114">Method</span></span>                                                                           | <span data-ttu-id="1d19f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d19f-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="1d19f-116">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1d19f-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="1d19f-117">Crea un nuovo driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="1d19f-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="1d19f-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="1d19f-119">Avvia il servizio di stampa.</span><span class="sxs-lookup"><span data-stu-id="1d19f-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="1d19f-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="1d19f-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="1d19f-121">Arresta il servizio di stampa.</span><span class="sxs-lookup"><span data-stu-id="1d19f-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="1d19f-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d19f-122">Properties</span></span>

<span data-ttu-id="1d19f-123">La classe **Win32 \_ PrinterDriver** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d19f-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d19f-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="1d19f-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-127">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1d19f-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-128">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="1d19f-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="1d19f-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="1d19f-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-133">File di configurazione per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="1d19f-134">Esempio: "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="1d19f-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d19f-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-138">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome classe")</span><span class="sxs-lookup"><span data-stu-id="1d19f-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-139">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="1d19f-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="1d19f-140">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="1d19f-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d19f-141">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-142">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="1d19f-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-145">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile. FileName)</span><span class="sxs-lookup"><span data-stu-id="1d19f-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-146">File di dati per questo driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-146">Data file for this printer driver.</span></span>

<span data-ttu-id="1d19f-147">Esempio: "qms810. PPD"</span><span class="sxs-lookup"><span data-stu-id="1d19f-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-148">**DefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="1d19f-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-151">Tipo di dati predefinito per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="1d19f-152">Esempio: "EMF"</span><span class="sxs-lookup"><span data-stu-id="1d19f-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-153">**DependentFiles**</span><span class="sxs-lookup"><span data-stu-id="1d19f-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-154">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="1d19f-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-156">Matrice di file dipendenti per questo driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-157">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="1d19f-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-160">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="1d19f-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-161">Commento che descrive il collegamento.</span><span class="sxs-lookup"><span data-stu-id="1d19f-161">Comment that describes the link.</span></span>

<span data-ttu-id="1d19f-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="1d19f-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-166">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM \_ DataFile. Path)</span><span class="sxs-lookup"><span data-stu-id="1d19f-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-167">Percorso del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-167">Path for this printer driver.</span></span>

<span data-ttu-id="1d19f-168">Esempio: "C: \\ \\ drivers \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="1d19f-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-169">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="1d19f-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1d19f-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-172">Percorso del file INF utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-172">Path to the INF file being used.</span></span>

<span data-ttu-id="1d19f-173">Esempio: "c: \\ \\ temp \\ \\ driver"</span><span class="sxs-lookup"><span data-stu-id="1d19f-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="1d19f-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-175">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-177">File della Guida per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-177">Help file for this printer driver.</span></span>

<span data-ttu-id="1d19f-178">Esempio: "PSCRPTUI. hlp"</span><span class="sxs-lookup"><span data-stu-id="1d19f-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-179">**InfName**</span><span class="sxs-lookup"><span data-stu-id="1d19f-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1d19f-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-182">Nome del file INF utilizzato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-182">Name of the INF file being used.</span></span> <span data-ttu-id="1d19f-183">Per impostazione predefinita, viene utilizzato un file INF della stampante fornito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1d19f-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="1d19f-184">Se il driver viene fornito direttamente dal produttore della stampante e non dal sistema operativo, viene utilizzato un nome file diverso.</span><span class="sxs-lookup"><span data-stu-id="1d19f-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d19f-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-186">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d19f-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-188">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="1d19f-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-189">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1d19f-189">Date and time the object is installed.</span></span> <span data-ttu-id="1d19f-190">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d19f-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-192">**MonitorName**</span><span class="sxs-lookup"><span data-stu-id="1d19f-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-195">Nome del monitoraggio del driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="1d19f-196">Esempio: "monitoraggio PJL"</span><span class="sxs-lookup"><span data-stu-id="1d19f-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-197">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1d19f-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-200">Qualificatori: [ **chiave**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="1d19f-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-201">Nome del driver per la stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-201">Driver name for this printer.</span></span> <span data-ttu-id="1d19f-202">Si tratta di una chiave composta costituita dai valori **Name**, **Version** e **SupportedPlatform** .</span><span class="sxs-lookup"><span data-stu-id="1d19f-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="1d19f-203">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) ed esegue l'override della definizione del **nome** in tale classe.</span><span class="sxs-lookup"><span data-stu-id="1d19f-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-204">**OEMUrl**</span><span class="sxs-lookup"><span data-stu-id="1d19f-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-207">Collegamento World Wide Web (WWW) al sito Web del produttore della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="1d19f-208">Si noti che questa proprietà non viene popolata quando viene utilizzato il file Win32. inf ed è applicabile solo ai driver forniti direttamente dal produttore.</span><span class="sxs-lookup"><span data-stu-id="1d19f-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-209">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="1d19f-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-210">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="1d19f-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-212">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="1d19f-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-213">Se **true**, il servizio viene avviato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="1d19f-214">Se **false**, il servizio viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="1d19f-215">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-216">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="1d19f-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-219">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modalità di avvio")</span><span class="sxs-lookup"><span data-stu-id="1d19f-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-220">La modalità di avvio del servizio viene avviata automaticamente da un sistema operativo o viene avviata solo quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="1d19f-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="1d19f-221">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="1d19f-222">Di seguito sono indicati i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="1d19f-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="1d19f-223">Automatica</span><span class="sxs-lookup"><span data-stu-id="1d19f-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="1d19f-224">Manuale</span><span class="sxs-lookup"><span data-stu-id="1d19f-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="1d19f-225">**Automatico** ("automatico")</span><span class="sxs-lookup"><span data-stu-id="1d19f-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="1d19f-226">**Manuale** ("manuale")</span><span class="sxs-lookup"><span data-stu-id="1d19f-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d19f-227">**Status**</span><span class="sxs-lookup"><span data-stu-id="1d19f-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-228">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-230">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="1d19f-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-231">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1d19f-231">Current status of the object.</span></span> <span data-ttu-id="1d19f-232">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="1d19f-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1d19f-233">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="1d19f-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1d19f-234">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="1d19f-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1d19f-235">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="1d19f-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1d19f-236">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="1d19f-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1d19f-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d19f-238">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d19f-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d19f-239">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1d19f-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d19f-240">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="1d19f-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d19f-241">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="1d19f-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d19f-242">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="1d19f-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d19f-243">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="1d19f-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d19f-244">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="1d19f-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d19f-245">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="1d19f-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d19f-246">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="1d19f-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d19f-247">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="1d19f-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d19f-248">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="1d19f-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d19f-249">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="1d19f-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d19f-250">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="1d19f-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d19f-251">**SupportedPlatform**</span><span class="sxs-lookup"><span data-stu-id="1d19f-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-253">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1d19f-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-254">Ambienti operativi per i quali il driver è destinato.</span><span class="sxs-lookup"><span data-stu-id="1d19f-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="1d19f-255">Esempio: "Windows NT x86".</span><span class="sxs-lookup"><span data-stu-id="1d19f-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-256">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d19f-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-259">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome classe di sistema ")</span><span class="sxs-lookup"><span data-stu-id="1d19f-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-260">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="1d19f-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="1d19f-261">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d19f-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-263">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d19f-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d19f-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-265">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome sistema ")</span><span class="sxs-lookup"><span data-stu-id="1d19f-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-266">Nome del sistema che ospita il servizio.</span><span class="sxs-lookup"><span data-stu-id="1d19f-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="1d19f-267">Questa proprietà viene ereditata [**dal \_ servizio CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d19f-268">**Versione**</span><span class="sxs-lookup"><span data-stu-id="1d19f-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d19f-269">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d19f-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d19f-270">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="1d19f-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d19f-271">Versione del sistema operativo per il driver della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="1d19f-272"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="1d19f-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="1d19f-273">Win2k</span><span class="sxs-lookup"><span data-stu-id="1d19f-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d19f-274">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d19f-274">Remarks</span></span>

<span data-ttu-id="1d19f-275">La classe **Win32 \_ PrinterDriver** deriva dal [**\_ servizio CIM**](cim-service.md) che deriva da [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d19f-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="1d19f-276">Gli utenti possono disinstallare un driver della stampante eliminando un'istanza corrispondente di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1d19f-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="1d19f-277">A tale scopo, il processo chiamante deve avere il privilegio **SeLoadDriverPrivilege** impostato per eliminare un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="1d19f-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="1d19f-278">Esempio</span><span class="sxs-lookup"><span data-stu-id="1d19f-278">Examples</span></span>

<span data-ttu-id="1d19f-279">L'esempio [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript gestisce i driver della stampante e le porte della stampante.</span><span class="sxs-lookup"><span data-stu-id="1d19f-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="1d19f-280">La seguente [discussione sui forum TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) descrive come creare una stampante e caricare i driver da un server.</span><span class="sxs-lookup"><span data-stu-id="1d19f-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="1d19f-281">Nell'esempio VBScript seguente sono elencati tutti i driver della stampante installati in un computer.</span><span class="sxs-lookup"><span data-stu-id="1d19f-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="1d19f-282">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d19f-282">Requirements</span></span>



| <span data-ttu-id="1d19f-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d19f-283">Requirement</span></span> | <span data-ttu-id="1d19f-284">Valore</span><span class="sxs-lookup"><span data-stu-id="1d19f-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d19f-285">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d19f-285">Minimum supported client</span></span><br/> | <span data-ttu-id="1d19f-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d19f-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="1d19f-287">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d19f-287">Minimum supported server</span></span><br/> | <span data-ttu-id="1d19f-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d19f-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="1d19f-289">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d19f-289">Namespace</span></span><br/>                | <span data-ttu-id="1d19f-290">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1d19f-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="1d19f-291">MOF</span><span class="sxs-lookup"><span data-stu-id="1d19f-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d19f-292"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d19f-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d19f-293">DLL</span><span class="sxs-lookup"><span data-stu-id="1d19f-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d19f-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d19f-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="1d19f-295">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d19f-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d19f-296">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="1d19f-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="1d19f-297">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="1d19f-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
