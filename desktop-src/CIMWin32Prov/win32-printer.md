---
description: Rappresenta un dispositivo connesso a un computer in cui è in esecuzione un sistema operativo Microsoft Windows che può produrre un'immagine stampata o un testo su carta o altro supporto.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225656"
---
# <a name="win32_printer-class"></a><span data-ttu-id="d833b-103">\_Classe stampante Win32</span><span class="sxs-lookup"><span data-stu-id="d833b-103">Win32\_Printer class</span></span>

<span data-ttu-id="d833b-104">La [classe WMI](../wmisdk/retrieving-a-class.md) della **\_ stampante Win32** rappresenta un dispositivo connesso a un computer in cui è in esecuzione un sistema operativo Microsoft Windows che può produrre un'immagine stampata o un testo su carta o altro supporto.</span><span class="sxs-lookup"><span data-stu-id="d833b-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="d833b-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d833b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d833b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d833b-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="d833b-107">Members</span><span class="sxs-lookup"><span data-stu-id="d833b-107">Members</span></span>

<span data-ttu-id="d833b-108">La **classe \_ stampante Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d833b-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="d833b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d833b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d833b-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d833b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d833b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d833b-111">Methods</span></span>

<span data-ttu-id="d833b-112">Per la classe **\_ Printer Win32** sono disponibili questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d833b-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="d833b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="d833b-113">Method</span></span>                                                                               | <span data-ttu-id="d833b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d833b-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d833b-115">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="d833b-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="d833b-116">Aggiunge una connessione alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="d833b-117">**CancelAllJobs**</span><span class="sxs-lookup"><span data-stu-id="d833b-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="d833b-118">Annulla tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="d833b-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="d833b-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d833b-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="d833b-120">Restituisce il descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="d833b-121">**Sospendere**</span><span class="sxs-lookup"><span data-stu-id="d833b-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="d833b-122">Mette in pausa la coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="d833b-123">**PrintTestPage**</span><span class="sxs-lookup"><span data-stu-id="d833b-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="d833b-124">Stampa una pagina di test.</span><span class="sxs-lookup"><span data-stu-id="d833b-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="d833b-125">**RenamePrinter**</span><span class="sxs-lookup"><span data-stu-id="d833b-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="d833b-126">Rinomina una stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="d833b-127">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="d833b-127">**Reset**</span></span>                                                                            | <span data-ttu-id="d833b-128">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d833b-128">Not implemented.</span></span> <span data-ttu-id="d833b-129">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**Reset**](reset-method-in-class-cim-controller.md) nella [**\_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="d833b-130">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="d833b-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="d833b-131">Riprende la coda di stampa sospesa.</span><span class="sxs-lookup"><span data-stu-id="d833b-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="d833b-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="d833b-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="d833b-133">Imposta la stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="d833b-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="d833b-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d833b-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="d833b-135">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="d833b-135">Not implemented.</span></span> <span data-ttu-id="d833b-136">Per ulteriori informazioni sull'implementazione di questo metodo, vedere il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) in [**CIM \_ Printer**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="d833b-137">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d833b-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="d833b-138">Scrive una versione aggiornata del descrittore di sicurezza che controlla l'accesso alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="d833b-139">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d833b-139">Properties</span></span>

<span data-ttu-id="d833b-140">La **classe \_ Printer Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d833b-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d833b-141">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="d833b-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-144">Bitmap degli attributi per un dispositivo di stampa basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="d833b-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="d833b-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Stampante \_ ATTRIBUTO in \_ coda** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d833b-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-146">Queued</span><span class="sxs-lookup"><span data-stu-id="d833b-146">Queued</span></span>

<span data-ttu-id="d833b-147">I processi di stampa vengono memorizzati nel buffer e accodati.</span><span class="sxs-lookup"><span data-stu-id="d833b-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="d833b-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Stampante \_ ATTRIBUTO \_ diretto** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="d833b-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-149">Connessione diretta</span><span class="sxs-lookup"><span data-stu-id="d833b-149">Direct</span></span>

<span data-ttu-id="d833b-150">Documento da inviare direttamente alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="d833b-151">Questo valore viene utilizzato se i processi di stampa non vengono accodati correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="d833b-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Stampante \_ ATTRIBUTO \_ predefinito** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d833b-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-153">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d833b-153">Default</span></span>

<span data-ttu-id="d833b-154">Stampante predefinita in un computer.</span><span class="sxs-lookup"><span data-stu-id="d833b-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="d833b-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Stampante \_ ATTRIBUTO \_ Shared** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="d833b-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-156">Condiviso</span><span class="sxs-lookup"><span data-stu-id="d833b-156">Shared</span></span>

<span data-ttu-id="d833b-157">Disponibile come risorsa di rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="d833b-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="d833b-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Stampante \_ \_Rete attributi** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d833b-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-159">Rete</span><span class="sxs-lookup"><span data-stu-id="d833b-159">Network</span></span>

<span data-ttu-id="d833b-160">Collegato a una rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-160">Attached to a network.</span></span> <span data-ttu-id="d833b-161">Se sono impostati sia i bit locali che quelli di rete, indica una stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="d833b-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Stampante \_ ATTRIBUTO \_ nascosto** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d833b-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-163">Nascosto</span><span class="sxs-lookup"><span data-stu-id="d833b-163">Hidden</span></span>

<span data-ttu-id="d833b-164">Nascosto da alcuni utenti nella rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="d833b-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Stampante \_ ATTRIBUTO \_ local** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="d833b-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-166">Locale</span><span class="sxs-lookup"><span data-stu-id="d833b-166">Local</span></span>

<span data-ttu-id="d833b-167">Connessione diretta a un computer.</span><span class="sxs-lookup"><span data-stu-id="d833b-167">Directly connected to a computer.</span></span> <span data-ttu-id="d833b-168">Se sono impostati sia i bit locali che quelli di rete, indica una stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="d833b-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Stampante \_ ATTRIBUTO \_ ENABLEDEVQ** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d833b-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-170">EnableDevQ</span><span class="sxs-lookup"><span data-stu-id="d833b-170">EnableDevQ</span></span>

<span data-ttu-id="d833b-171">Abilitare la coda sulla stampante, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="d833b-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="d833b-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Stampante \_ ATTRIBUTO \_ KEEPPRINTEDJOBS** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="d833b-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="d833b-173">KeepPrintedJobs</span></span>

<span data-ttu-id="d833b-174">Lo spooler non deve eliminare i documenti dopo la stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="d833b-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Stampante \_ \_Primo attributo \_ completato \_** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="d833b-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-176">DoCompleteFirst</span><span class="sxs-lookup"><span data-stu-id="d833b-176">DoCompleteFirst</span></span>

<span data-ttu-id="d833b-177">Avviare prima i processi per i quali è stato completato lo spooling.</span><span class="sxs-lookup"><span data-stu-id="d833b-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="d833b-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Stampante \_ \_Funzione attributo \_ OFFLINE** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="d833b-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="d833b-179">WorkOffline</span></span>

<span data-ttu-id="d833b-180">Accoda i processi di stampa quando una stampante non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="d833b-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="d833b-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Stampante \_ ATTRIBUTO \_ enable \_ BIDI** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="d833b-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="d833b-182">EnableBIDI</span></span>

<span data-ttu-id="d833b-183">Abilitare la stampa bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="d833b-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="d833b-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Stampante \_ \_ \_ Solo attributo RAW** (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="d833b-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-185">Consente di eseguire lo spooling solo dei processi con tipi di dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="d833b-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="d833b-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Stampante \_ ATTRIBUTO \_ pubblicato** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="d833b-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="d833b-187">Pubblicato</span><span class="sxs-lookup"><span data-stu-id="d833b-187">Published</span></span>

<span data-ttu-id="d833b-188">Pubblicata nel servizio directory di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-189">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="d833b-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-192">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,5 "," MIB. \|Host IETF-risorse-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="d833b-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-193">Disponibilità e stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-193">Availability and status of the device.</span></span>

<span data-ttu-id="d833b-194">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d833b-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Esecuzione/potenza completa** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-198">Esecuzione o alimentazione completa</span><span class="sxs-lookup"><span data-stu-id="d833b-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d833b-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Avviso** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d833b-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d833b-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d833b-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Spegnimento (7** )</span><span class="sxs-lookup"><span data-stu-id="d833b-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d833b-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Offline (8** )</span><span class="sxs-lookup"><span data-stu-id="d833b-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d833b-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d833b-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d833b-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Non installato** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d833b-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Errore di installazione** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d833b-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Risparmio energia-sconosciuto** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-209">Il dispositivo è noto come modalità di risparmio energia, ma lo stato esatto è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d833b-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d833b-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia-modalità a basso consumo** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-211">Il dispositivo è in uno stato di risparmio energia, ma è ancora funzionante e può presentare prestazioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="d833b-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d833b-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia-standby** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-213">Il dispositivo non funziona, ma potrebbe essere portato a una potenza completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d833b-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d833b-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Risparmio energia-avviso** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-216">Il dispositivo è in uno stato di avviso, anche in modalità di risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="d833b-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d833b-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-218">Il dispositivo è sospeso.</span><span class="sxs-lookup"><span data-stu-id="d833b-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d833b-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Non pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-220">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="d833b-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d833b-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Non configurata** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-222">Il dispositivo non è configurato.</span><span class="sxs-lookup"><span data-stu-id="d833b-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d833b-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inattivo** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-224">Il dispositivo è silenzioso.</span><span class="sxs-lookup"><span data-stu-id="d833b-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-225">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="d833b-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-226">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-228">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="d833b-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-229">Matrice di tutti i fogli di lavoro disponibili in una stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="d833b-230">Può essere utilizzato anche per descrivere il banner che può essere fornito da una stampante all'inizio di ogni processo o altre opzioni specificate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d833b-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="d833b-231">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="d833b-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-233">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-235">Frequenza di stampa, in numero medio di pagine al minuto, che una stampante può produrre output.</span><span class="sxs-lookup"><span data-stu-id="d833b-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="d833b-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-237">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-239">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indicizzato"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. finishing "," CIM \_ printservice. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="d833b-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-240">Matrice delle funzionalità della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-240">Array of printer capabilities.</span></span>

<span data-ttu-id="d833b-241">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="d833b-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="d833b-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="d833b-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="d833b-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="d833b-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="d833b-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="d833b-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="d833b-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="d833b-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="d833b-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="d833b-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="d833b-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="d833b-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-257">Two-Sided bordo lungo</span><span class="sxs-lookup"><span data-stu-id="d833b-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="d833b-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-259">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="d833b-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="d833b-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="d833b-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="d833b-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="d833b-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="d833b-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="d833b-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="d833b-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-267">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d833b-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-268">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-270">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indicizzato"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="d833b-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-271">Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità della stampante indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="d833b-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="d833b-272">Ogni voce di questa matrice è correlata a una voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="d833b-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="d833b-273">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-274">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d833b-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-277">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d833b-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-278">Breve descrizione di un oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="d833b-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="d833b-279">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-280">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-281">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-283">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. charset"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="d833b-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-284">Matrice di set di caratteri disponibili per l'output.</span><span class="sxs-lookup"><span data-stu-id="d833b-284">Array of available character sets for output.</span></span> <span data-ttu-id="d833b-285">Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate dalla sezione 4.1.2 ("charset Parameters") in RFC 2046 (MIME Part 2) e contenute nel registro di sistema del set di caratteri IANA.</span><span class="sxs-lookup"><span data-stu-id="d833b-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="d833b-286">Gli esempi includono "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="d833b-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="d833b-287">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-288">**Commento**</span><span class="sxs-lookup"><span data-stu-id="d833b-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-290">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-291">Commento per una coda di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-291">Comment for a print queue.</span></span>

<span data-ttu-id="d833b-292">Esempio: stampante a colori</span><span class="sxs-lookup"><span data-stu-id="d833b-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="d833b-293">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d833b-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-294">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-296">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d833b-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-297">Codice di errore Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d833b-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d833b-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d833b-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Il dispositivo funziona correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d833b-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d833b-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-301">Il dispositivo funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d833b-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Questo dispositivo non è configurato correttamente.**</span><span class="sxs-lookup"><span data-stu-id="d833b-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d833b-303">(1)</span><span class="sxs-lookup"><span data-stu-id="d833b-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-304">Il dispositivo non è configurato correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d833b-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows non è in grado di caricare il driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d833b-306">(2)</span><span class="sxs-lookup"><span data-stu-id="d833b-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d833b-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Il driver per questo dispositivo potrebbe essere danneggiato oppure è possibile che la memoria del sistema sia insufficiente o che altre risorse.**</span><span class="sxs-lookup"><span data-stu-id="d833b-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d833b-308">(3)</span><span class="sxs-lookup"><span data-stu-id="d833b-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-309">Il driver per questo dispositivo potrebbe essere danneggiato oppure la memoria o altre risorse del sistema potrebbero essere insufficienti.</span><span class="sxs-lookup"><span data-stu-id="d833b-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d833b-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il dispositivo non funziona correttamente. Uno dei driver o del registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d833b-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d833b-311">(4)</span><span class="sxs-lookup"><span data-stu-id="d833b-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-312">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-312">Device is not working properly.</span></span> <span data-ttu-id="d833b-313">Uno dei suoi driver o il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d833b-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d833b-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Il driver per questo dispositivo richiede una risorsa che Windows non è in grado di gestire.**</span><span class="sxs-lookup"><span data-stu-id="d833b-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d833b-315">(5)</span><span class="sxs-lookup"><span data-stu-id="d833b-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-316">Il driver per il dispositivo richiede una risorsa che Windows non è in grado di gestire.</span><span class="sxs-lookup"><span data-stu-id="d833b-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d833b-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configurazione di avvio per questo dispositivo è in conflitto con altri dispositivi.**</span><span class="sxs-lookup"><span data-stu-id="d833b-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d833b-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-319">La configurazione di avvio per il dispositivo è in conflitto con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d833b-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d833b-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Impossibile filtrare.**</span><span class="sxs-lookup"><span data-stu-id="d833b-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d833b-321">(7)</span><span class="sxs-lookup"><span data-stu-id="d833b-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d833b-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Il caricatore driver del dispositivo è mancante.**</span><span class="sxs-lookup"><span data-stu-id="d833b-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d833b-323">(8)</span><span class="sxs-lookup"><span data-stu-id="d833b-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-324">Il caricatore driver del dispositivo è mancante.</span><span class="sxs-lookup"><span data-stu-id="d833b-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d833b-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Questo dispositivo non funziona correttamente perché il firmware di controllo segnala le risorse per il dispositivo in modo non corretto.**</span><span class="sxs-lookup"><span data-stu-id="d833b-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d833b-326">(9)</span><span class="sxs-lookup"><span data-stu-id="d833b-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-327">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-327">Device is not working properly.</span></span> <span data-ttu-id="d833b-328">Il firmware di controllo segnala erroneamente le risorse per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d833b-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Impossibile avviare il dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d833b-330">(10)</span><span class="sxs-lookup"><span data-stu-id="d833b-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-331">Non è possibile avviare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d833b-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Errore del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d833b-333">(11)</span><span class="sxs-lookup"><span data-stu-id="d833b-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-334">Errore del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d833b-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Questo dispositivo non è in grado di trovare sufficienti risorse gratuite da usare.**</span><span class="sxs-lookup"><span data-stu-id="d833b-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d833b-336">12</span><span class="sxs-lookup"><span data-stu-id="d833b-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-337">Il dispositivo non riesce a trovare risorse disponibili sufficienti da usare.</span><span class="sxs-lookup"><span data-stu-id="d833b-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d833b-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows non è in grado di verificare le risorse del dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d833b-339">(13)</span><span class="sxs-lookup"><span data-stu-id="d833b-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-340">Windows non è in grado di verificare le risorse del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d833b-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Questo dispositivo non funziona correttamente finché non si riavvia il computer.**</span><span class="sxs-lookup"><span data-stu-id="d833b-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d833b-342">(14)</span><span class="sxs-lookup"><span data-stu-id="d833b-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-343">Il dispositivo non funziona correttamente finché il computer non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="d833b-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d833b-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Il dispositivo non funziona correttamente perché è probabile che si verifichi un problema di rienumerazione.**</span><span class="sxs-lookup"><span data-stu-id="d833b-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d833b-345">(15)</span><span class="sxs-lookup"><span data-stu-id="d833b-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-346">Il dispositivo non funziona correttamente a causa di un possibile problema di rienumerazione.</span><span class="sxs-lookup"><span data-stu-id="d833b-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d833b-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d833b-348">(16)</span><span class="sxs-lookup"><span data-stu-id="d833b-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-349">Windows non è in grado di identificare tutte le risorse utilizzate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d833b-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Il dispositivo richiede un tipo di risorsa sconosciuto.**</span><span class="sxs-lookup"><span data-stu-id="d833b-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d833b-351">(17)</span><span class="sxs-lookup"><span data-stu-id="d833b-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-352">Il dispositivo richiede un tipo di risorsa sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="d833b-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d833b-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstallare i driver per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d833b-354">(18)</span><span class="sxs-lookup"><span data-stu-id="d833b-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-355">È necessario reinstallare i driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d833b-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Errore durante l'utilizzo del caricatore VxD.**</span><span class="sxs-lookup"><span data-stu-id="d833b-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d833b-357">(19)</span><span class="sxs-lookup"><span data-stu-id="d833b-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d833b-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Il registro di sistema potrebbe essere danneggiato.**</span><span class="sxs-lookup"><span data-stu-id="d833b-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d833b-359">(20)</span><span class="sxs-lookup"><span data-stu-id="d833b-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-360">Il registro di sistema potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="d833b-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d833b-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se non funziona, vedere la documentazione dell'hardware. Windows sta rimuovendo questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d833b-362">(21)</span><span class="sxs-lookup"><span data-stu-id="d833b-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-363">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d833b-363">System failure.</span></span> <span data-ttu-id="d833b-364">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d833b-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d833b-365">Windows sta rimuovendo il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d833b-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Il dispositivo è disabilitato.**</span><span class="sxs-lookup"><span data-stu-id="d833b-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d833b-367">(22)</span><span class="sxs-lookup"><span data-stu-id="d833b-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-368">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d833b-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d833b-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Errore di sistema: provare a modificare il driver per questo dispositivo. Se questa operazione non funziona, vedere la documentazione dell'hardware.**</span><span class="sxs-lookup"><span data-stu-id="d833b-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d833b-370">(23)</span><span class="sxs-lookup"><span data-stu-id="d833b-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-371">Errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="d833b-371">System failure.</span></span> <span data-ttu-id="d833b-372">Se la modifica del driver di dispositivo non è efficace, vedere la documentazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="d833b-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d833b-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Questo dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.**</span><span class="sxs-lookup"><span data-stu-id="d833b-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d833b-374">(24)</span><span class="sxs-lookup"><span data-stu-id="d833b-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-375">Il dispositivo non è presente, non funziona correttamente o non sono installati tutti i driver.</span><span class="sxs-lookup"><span data-stu-id="d833b-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d833b-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d833b-377">(25)</span><span class="sxs-lookup"><span data-stu-id="d833b-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-378">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d833b-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows sta ancora impostando questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d833b-380">(26)</span><span class="sxs-lookup"><span data-stu-id="d833b-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-381">Windows sta ancora impostando il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d833b-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Questo dispositivo non ha una configurazione di log valida.**</span><span class="sxs-lookup"><span data-stu-id="d833b-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d833b-383">(27)</span><span class="sxs-lookup"><span data-stu-id="d833b-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-384">Il dispositivo non dispone di una configurazione di log valida.</span><span class="sxs-lookup"><span data-stu-id="d833b-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d833b-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**I driver per questo dispositivo non sono installati.**</span><span class="sxs-lookup"><span data-stu-id="d833b-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d833b-386">(28)</span><span class="sxs-lookup"><span data-stu-id="d833b-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-387">I driver di dispositivo non sono installati.</span><span class="sxs-lookup"><span data-stu-id="d833b-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d833b-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Questo dispositivo è disabilitato perché il firmware del dispositivo non ha fornito le risorse necessarie.**</span><span class="sxs-lookup"><span data-stu-id="d833b-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d833b-389">(29)</span><span class="sxs-lookup"><span data-stu-id="d833b-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-390">Il dispositivo è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="d833b-390">Device is disabled.</span></span> <span data-ttu-id="d833b-391">Il firmware del dispositivo non ha fornito le risorse necessarie.</span><span class="sxs-lookup"><span data-stu-id="d833b-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d833b-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Questo dispositivo usa una risorsa di richiesta di interrupt (IRQ) usata da un altro dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d833b-393">(30)</span><span class="sxs-lookup"><span data-stu-id="d833b-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-394">Il dispositivo usa una risorsa IRQ usata da un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d833b-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d833b-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Questo dispositivo non funziona correttamente perché Windows non è in grado di caricare i driver necessari per questo dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="d833b-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d833b-396">31</span><span class="sxs-lookup"><span data-stu-id="d833b-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-397">Il dispositivo non funziona correttamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-397">Device is not working properly.</span></span> <span data-ttu-id="d833b-398">Windows non è in grado di caricare i driver di dispositivo necessari.</span><span class="sxs-lookup"><span data-stu-id="d833b-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-399">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="d833b-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-400">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-402">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d833b-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-403">Se **true**, il dispositivo usa una configurazione definita dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d833b-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d833b-404">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d833b-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-406">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-408">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-409">Nome della prima classe concreta da visualizzare nella catena di ereditarietà utilizzata per creare un'istanza.</span><span class="sxs-lookup"><span data-stu-id="d833b-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="d833b-410">Se utilizzata con altre proprietà chiave della classe, la proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="d833b-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d833b-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-412">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d833b-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-413">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-415">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="d833b-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-416">Matrice di funzionalità della stampante attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="d833b-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="d833b-417">Una voce in questa proprietà deve essere elencata anche nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="d833b-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="d833b-418">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="d833b-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="d833b-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="d833b-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="d833b-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="d833b-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="d833b-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="d833b-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="d833b-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="d833b-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="d833b-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="d833b-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="d833b-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="d833b-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-434">Two-Sided bordo lungo</span><span class="sxs-lookup"><span data-stu-id="d833b-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="d833b-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-436">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="d833b-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="d833b-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="d833b-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="d833b-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="d833b-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="d833b-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="d833b-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="d833b-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-444">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="d833b-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-445">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-447">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="d833b-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-448">Set di caratteri attualmente utilizzato per l'output.</span><span class="sxs-lookup"><span data-stu-id="d833b-448">The character set currently used for output.</span></span> <span data-ttu-id="d833b-449">Le stringhe fornite in questa proprietà devono essere conformi alla semantica e alla sintassi specificate dalla sezione 4.1.2 ("charset Parameters") in RFC 2046 (MIME Part 2) e contenute nel registro di sistema del set di caratteri IANA.</span><span class="sxs-lookup"><span data-stu-id="d833b-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="d833b-450">Gli esempi includono "UTF-8", "US-ASCII" e ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="d833b-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="d833b-451">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="d833b-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-453">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-455">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported ","**CIM \_ Printer**.**CurrentMimeType**")</span><span class="sxs-lookup"><span data-stu-id="d833b-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-456">Lingua della stampante attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="d833b-456">Printer language currently used.</span></span> <span data-ttu-id="d833b-457">La lingua usata deve essere elencata nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="d833b-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="d833b-458">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="d833b-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="d833b-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="d833b-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="d833b-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="d833b-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="d833b-466"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="d833b-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="d833b-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="d833b-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="d833b-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="d833b-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="d833b-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="d833b-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-474">LineData</span><span class="sxs-lookup"><span data-stu-id="d833b-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="d833b-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-476">DODCA</span><span class="sxs-lookup"><span data-stu-id="d833b-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="d833b-477"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="d833b-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="d833b-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="d833b-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="d833b-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="d833b-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="d833b-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="d833b-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="d833b-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="d833b-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="d833b-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="d833b-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="d833b-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="d833b-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="d833b-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="d833b-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="d833b-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="d833b-488"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="d833b-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="d833b-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="d833b-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="d833b-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="d833b-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="d833b-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="d833b-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="d833b-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="d833b-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="d833b-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="d833b-494"><span id="DOC"></span><span id="doc"></span>**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="d833b-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="d833b-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="d833b-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="d833b-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="d833b-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="d833b-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="d833b-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="d833b-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="d833b-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="d833b-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="d833b-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="d833b-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="d833b-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="d833b-501"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="d833b-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="d833b-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="d833b-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d833b-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="d833b-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="d833b-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="d833b-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="d833b-505"><span id="EXCL"></span><span id="excl"></span>**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="d833b-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="d833b-506"><span id="LCDS"></span><span id="lcds"></span>**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="d833b-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="d833b-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="d833b-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="d833b-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="d833b-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="d833b-509">48</span><span class="sxs-lookup"><span data-stu-id="d833b-509">48</span></span>
</dt> <dd>

<span data-ttu-id="d833b-510">XPS</span><span class="sxs-lookup"><span data-stu-id="d833b-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="d833b-511">49</span><span class="sxs-lookup"><span data-stu-id="d833b-511">49</span></span>
</dt> <dd>

<span data-ttu-id="d833b-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="d833b-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="d833b-513">50</span><span class="sxs-lookup"><span data-stu-id="d833b-513">50</span></span>
</dt> <dd>

<span data-ttu-id="d833b-514">PCLXL</span><span class="sxs-lookup"><span data-stu-id="d833b-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-515">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="d833b-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-516">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-517">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-518">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="d833b-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-519">Tipo MIME attualmente in uso se **CurrentLanguage** è un tipo MIME (value = 47).</span><span class="sxs-lookup"><span data-stu-id="d833b-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="d833b-520">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-521">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="d833b-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-522">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-523">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-524">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="d833b-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-525">Lingua utilizzata attualmente dalla stampante per la gestione.</span><span class="sxs-lookup"><span data-stu-id="d833b-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="d833b-526">La lingua elencata qui deve essere elencata anche nella proprietà **NaturalLanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="d833b-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="d833b-527">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-528">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="d833b-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-529">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-531">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="d833b-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-532">Tipo di carta utilizzato dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-532">Type of paper the printer is using.</span></span> <span data-ttu-id="d833b-533">Deve essere espressa nel formato specificato dall'applicazione di stampa documenti ISO/IEC 10175, riepilogata nell'Appendice C di RFC 1759 (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="d833b-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="d833b-534">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-535">**Default**</span><span class="sxs-lookup"><span data-stu-id="d833b-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-536">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-537">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-538">Se **true**, la stampante è la stampante predefinita.</span><span class="sxs-lookup"><span data-stu-id="d833b-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-539">**DefaultCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d833b-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-540">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-541">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-542">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="d833b-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-543">Matrice delle funzionalità della stampante usate per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="d833b-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="d833b-544">Ogni voce nella matrice **DefaultCapabilities** deve essere elencata anche nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="d833b-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="d833b-545">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="d833b-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Stampa a colori** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="d833b-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Stampa duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="d833b-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copie** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="d833b-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Regole di confronto** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="d833b-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Graffatura** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="d833b-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Stampa trasparenza** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="d833b-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="d833b-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Copertura** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="d833b-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Binding** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="d833b-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Stampa in bianco e nero** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="d833b-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Un lato** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="d833b-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="d833b-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Bordo lungo due lati** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-561">Two-Sided bordo lungo</span><span class="sxs-lookup"><span data-stu-id="d833b-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="d833b-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Bordo corto a due lati** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-563">Two-Sided Short Edge</span><span class="sxs-lookup"><span data-stu-id="d833b-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="d833b-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Verticale** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="d833b-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Orizzontale** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="d833b-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Verticale inverso** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="d833b-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Orizzontale inverso** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="d833b-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualità elevata** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="d833b-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Normale qualità** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="d833b-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualità bassa** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-571">**DefaultCopies**</span><span class="sxs-lookup"><span data-stu-id="d833b-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-572">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-573">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-574">Numero di copie prodotte per un processo, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="d833b-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="d833b-575">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="d833b-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-577">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-578">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-579">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported ","**CIM \_ Printer**.**DefaultMimeType**")</span><span class="sxs-lookup"><span data-stu-id="d833b-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-580">Lingua predefinita della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-580">Default printer language.</span></span> <span data-ttu-id="d833b-581">La lingua elencata qui deve essere elencata anche nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="d833b-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="d833b-582">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="d833b-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="d833b-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="d833b-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="d833b-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="d833b-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="d833b-590"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="d833b-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="d833b-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="d833b-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="d833b-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="d833b-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="d833b-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="d833b-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-598">LineData</span><span class="sxs-lookup"><span data-stu-id="d833b-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="d833b-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-600">DODCA</span><span class="sxs-lookup"><span data-stu-id="d833b-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="d833b-601"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="d833b-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="d833b-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="d833b-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="d833b-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="d833b-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="d833b-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="d833b-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="d833b-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="d833b-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="d833b-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="d833b-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="d833b-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="d833b-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="d833b-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="d833b-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="d833b-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="d833b-612"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="d833b-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="d833b-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="d833b-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="d833b-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="d833b-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="d833b-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="d833b-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="d833b-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="d833b-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="d833b-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="d833b-618"><span id="DOC"></span><span id="doc"></span>**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="d833b-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="d833b-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="d833b-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="d833b-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="d833b-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="d833b-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="d833b-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="d833b-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="d833b-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="d833b-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="d833b-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="d833b-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="d833b-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="d833b-625"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="d833b-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="d833b-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="d833b-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d833b-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="d833b-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="d833b-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="d833b-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="d833b-629"><span id="EXCL"></span><span id="excl"></span>**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="d833b-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="d833b-630"><span id="LCDS"></span><span id="lcds"></span>**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="d833b-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="d833b-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="d833b-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="d833b-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="d833b-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="d833b-633">48</span><span class="sxs-lookup"><span data-stu-id="d833b-633">48</span></span>
</dt> <dd>

<span data-ttu-id="d833b-634">XPS</span><span class="sxs-lookup"><span data-stu-id="d833b-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="d833b-635">49</span><span class="sxs-lookup"><span data-stu-id="d833b-635">49</span></span>
</dt> <dd>

<span data-ttu-id="d833b-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="d833b-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="d833b-637">50</span><span class="sxs-lookup"><span data-stu-id="d833b-637">50</span></span>
</dt> <dd>

<span data-ttu-id="d833b-638">PCLXL</span><span class="sxs-lookup"><span data-stu-id="d833b-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-639">**DefaultMimeType**</span><span class="sxs-lookup"><span data-stu-id="d833b-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-640">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-641">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-642">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="d833b-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-643">Tipo MIME attualmente in uso, se il valore **defaultLanguage** è un tipo MIME (value = 47).</span><span class="sxs-lookup"><span data-stu-id="d833b-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="d833b-644">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-645">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="d833b-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-646">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-647">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-648">Numero di pagine del flusso di stampa in cui viene eseguito il rendering della stampante su un foglio multimediale, a meno che un processo non specifichi diversamente.</span><span class="sxs-lookup"><span data-stu-id="d833b-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="d833b-649">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-650">**DefaultPaperType**</span><span class="sxs-lookup"><span data-stu-id="d833b-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-651">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-652">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-653">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="d833b-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-654">Tipo di carta utilizzato dalla stampante, a meno che un processo di stampa non specifichi un tipo di carta diverso.</span><span class="sxs-lookup"><span data-stu-id="d833b-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="d833b-655">La stringa deve essere espressa nel formato specificato da ISO/IEC 1017 Document Printing Application (DPA), riepilogato nell'Appendice C di [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="d833b-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="d833b-656">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-657">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="d833b-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-658">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-659">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-660">Valore di priorità predefinito assegnato a ogni processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-661">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d833b-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-662">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-663">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-664">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="d833b-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-665">Descrizione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d833b-665">Description of an object.</span></span>

<span data-ttu-id="d833b-666">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="d833b-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-668">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-669">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-670">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="d833b-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-671">Informazioni sull'errore della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-671">Printer error information.</span></span>

<span data-ttu-id="d833b-672">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-673">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-674">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="d833b-675">**Nessun errore** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="d833b-676">**Carta bassa** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="d833b-677">**Nessun documento** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="d833b-678">**Toner basso** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="d833b-679">**Nessun toner** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="d833b-680">**Sportello aperto** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="d833b-681">**Bloccato** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="d833b-682">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="d833b-683">**Servizio richiesto** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="d833b-684">**Bin di output completo** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d833b-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-686">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-687">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-688">Qualificatori: [ **\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-689">Identificatore univoco della stampante in un sistema.</span><span class="sxs-lookup"><span data-stu-id="d833b-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="d833b-690">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-691">**Diretta**</span><span class="sxs-lookup"><span data-stu-id="d833b-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-692">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-693">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-694">Se **true**, il processo di stampa viene inviato direttamente alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="d833b-695">Se **false**, viene eseguito lo spooling del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-696">**DoCompleteFirst**</span><span class="sxs-lookup"><span data-stu-id="d833b-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-697">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-698">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-699">Se **true**, la stampante avvia i processi che hanno completato lo spooling.</span><span class="sxs-lookup"><span data-stu-id="d833b-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="d833b-700">Se **false**, la stampante avvia i processi nell'ordine in cui vengono ricevuti i processi.</span><span class="sxs-lookup"><span data-stu-id="d833b-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="d833b-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-702">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-703">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-704">Nome del driver della stampante Windows.</span><span class="sxs-lookup"><span data-stu-id="d833b-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="d833b-705">Esempio: driver fax di Windows</span><span class="sxs-lookup"><span data-stu-id="d833b-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="d833b-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="d833b-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-707">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-708">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-709">Se **true**, la stampante è in grado di stampare in bidirezionale.</span><span class="sxs-lookup"><span data-stu-id="d833b-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-710">**EnableDevQueryPrint**</span><span class="sxs-lookup"><span data-stu-id="d833b-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-711">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-712">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-713">Se **true**, la stampante include i documenti nella coda quando le impostazioni del documento e della stampante non corrispondono.</span><span class="sxs-lookup"><span data-stu-id="d833b-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-714">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="d833b-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-715">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-716">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-717">Se **true**, l'errore segnalato in **LastErrorCode** è stato cancellato.</span><span class="sxs-lookup"><span data-stu-id="d833b-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="d833b-718">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d833b-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-720">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-721">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-722">Informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="d833b-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="d833b-723">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="d833b-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-725">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-726">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d833b-727">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md).**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="d833b-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-728">Matrice di informazioni aggiuntive per lo stato di errore corrente indicato in **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="d833b-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="d833b-729">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="d833b-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-731">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-732">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-733">Segnala informazioni sull'errore standard.</span><span class="sxs-lookup"><span data-stu-id="d833b-733">Reports standard error information.</span></span> <span data-ttu-id="d833b-734">È necessario registrare informazioni aggiuntive in **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="d833b-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="d833b-735">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="d833b-735">Values are:</span></span>

<dt>

<span data-ttu-id="d833b-736">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="d833b-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-737">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d833b-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="d833b-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d833b-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-739">Altro</span><span class="sxs-lookup"><span data-stu-id="d833b-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="d833b-740">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d833b-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-741">Nessun errore</span><span class="sxs-lookup"><span data-stu-id="d833b-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="d833b-742">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="d833b-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-743">Carta in esaurimento</span><span class="sxs-lookup"><span data-stu-id="d833b-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="d833b-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d833b-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-745">Carta esaurita</span><span class="sxs-lookup"><span data-stu-id="d833b-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="d833b-746">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="d833b-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-747">Toner insufficiente</span><span class="sxs-lookup"><span data-stu-id="d833b-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="d833b-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="d833b-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-749">Toner esaurito</span><span class="sxs-lookup"><span data-stu-id="d833b-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="d833b-750">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="d833b-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-751">Sportello aperto</span><span class="sxs-lookup"><span data-stu-id="d833b-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="d833b-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d833b-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-753">Fogli bloccati</span><span class="sxs-lookup"><span data-stu-id="d833b-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="d833b-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="d833b-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-755">Necessaria manutenzione</span><span class="sxs-lookup"><span data-stu-id="d833b-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="d833b-756">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="d833b-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-757">Raccoglitore pieno</span><span class="sxs-lookup"><span data-stu-id="d833b-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="d833b-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="d833b-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-759">Problema relativo alla carta</span><span class="sxs-lookup"><span data-stu-id="d833b-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="d833b-760">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="d833b-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-761">Impossibile stampare la pagina</span><span class="sxs-lookup"><span data-stu-id="d833b-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="d833b-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="d833b-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-763">Intervento dell'utente richiesto</span><span class="sxs-lookup"><span data-stu-id="d833b-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="d833b-764">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="d833b-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-765">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="d833b-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="d833b-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="d833b-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-767">Server sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d833b-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-768">**ExtendedPrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="d833b-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-769">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-770">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-771">Informazioni sullo stato di una stampante diverse dalle informazioni specificate nella proprietà di **disponibilità** .</span><span class="sxs-lookup"><span data-stu-id="d833b-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="d833b-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d833b-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-773">Altro</span><span class="sxs-lookup"><span data-stu-id="d833b-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="d833b-774">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d833b-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-775">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d833b-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="d833b-776">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="d833b-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-777">Idle</span><span class="sxs-lookup"><span data-stu-id="d833b-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="d833b-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d833b-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-779">Stampa</span><span class="sxs-lookup"><span data-stu-id="d833b-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="d833b-780">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="d833b-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-781">Riscaldamento</span><span class="sxs-lookup"><span data-stu-id="d833b-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="d833b-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="d833b-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-783">Stampa interrotta</span><span class="sxs-lookup"><span data-stu-id="d833b-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="d833b-784">7</span><span class="sxs-lookup"><span data-stu-id="d833b-784">7</span></span>
</dt> <dd>

<span data-ttu-id="d833b-785">Offline</span><span class="sxs-lookup"><span data-stu-id="d833b-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="d833b-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d833b-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-787">Paused</span><span class="sxs-lookup"><span data-stu-id="d833b-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="d833b-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="d833b-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-789">Errore</span><span class="sxs-lookup"><span data-stu-id="d833b-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="d833b-790">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="d833b-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-791">Busy</span><span class="sxs-lookup"><span data-stu-id="d833b-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="d833b-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="d833b-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-793">Non disponibile</span><span class="sxs-lookup"><span data-stu-id="d833b-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="d833b-794">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="d833b-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-795">Attesa</span><span class="sxs-lookup"><span data-stu-id="d833b-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="d833b-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="d833b-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-797">Elaborazione in corso</span><span class="sxs-lookup"><span data-stu-id="d833b-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="d833b-798">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="d833b-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-799">Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="d833b-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="d833b-800">15</span><span class="sxs-lookup"><span data-stu-id="d833b-800">15</span></span>
</dt> <dd>

<span data-ttu-id="d833b-801">Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="d833b-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="d833b-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d833b-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-803">Eliminazione in sospeso</span><span class="sxs-lookup"><span data-stu-id="d833b-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="d833b-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="d833b-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-805">I/O attivo</span><span class="sxs-lookup"><span data-stu-id="d833b-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="d833b-806">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="d833b-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="d833b-807">Feed manuale</span><span class="sxs-lookup"><span data-stu-id="d833b-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-808">**Hidden**</span><span class="sxs-lookup"><span data-stu-id="d833b-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-809">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-810">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-811">Se **true**, la stampante è nascosta agli utenti di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="d833b-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-813">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-814">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-815">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unità**](../wmisdk/standard-qualifiers.md) ("pixel per pollice")</span><span class="sxs-lookup"><span data-stu-id="d833b-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-816">Risoluzione orizzontale della stampante, in pixel per pollice.</span><span class="sxs-lookup"><span data-stu-id="d833b-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="d833b-817">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d833b-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-819">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-820">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-821">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="d833b-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-822">Data e ora di installazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d833b-822">Date and time an object was installed.</span></span> <span data-ttu-id="d833b-823">L'oggetto può essere installato senza che venga scritto un valore in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="d833b-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="d833b-824">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-825">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="d833b-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-826">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-827">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-828">Qualificatori: **contatore**</span><span class="sxs-lookup"><span data-stu-id="d833b-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="d833b-829">Numero di processi di stampa dall'ultima reimpostazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="d833b-830">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="d833b-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-832">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-833">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-834">Se **true**, lo spooler di stampa non elimina i processi completati.</span><span class="sxs-lookup"><span data-stu-id="d833b-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-836">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-837">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-838">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ printservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="d833b-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-839">Matrice delle lingue di stampa supportate in modo nativo.</span><span class="sxs-lookup"><span data-stu-id="d833b-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="d833b-840">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="d833b-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="d833b-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="d833b-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="d833b-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="d833b-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="d833b-848"><span id="IPDS"></span><span id="ipds"></span>**IPD** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="d833b-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="d833b-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="d833b-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="d833b-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="d833b-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interstampa** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="d833b-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="d833b-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dati riga** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-856">LineData</span><span class="sxs-lookup"><span data-stu-id="d833b-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="d833b-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-858">DODCA</span><span class="sxs-lookup"><span data-stu-id="d833b-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="d833b-859"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="d833b-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="d833b-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="d833b-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="d833b-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="d833b-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="d833b-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="d833b-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="d833b-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="d833b-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="d833b-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="d833b-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="d833b-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="d833b-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="d833b-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="d833b-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="d833b-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="d833b-870"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="d833b-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="d833b-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="d833b-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="d833b-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="d833b-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="d833b-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Testo semplice** (31)</span><span class="sxs-lookup"><span data-stu-id="d833b-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="d833b-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="d833b-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="d833b-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="d833b-876"><span id="DOC"></span><span id="doc"></span>**Documento** (33)</span><span class="sxs-lookup"><span data-stu-id="d833b-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="d833b-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**impressione** (34)</span><span class="sxs-lookup"><span data-stu-id="d833b-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="d833b-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="d833b-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="d833b-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="d833b-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="d833b-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="d833b-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="d833b-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatico** (38)</span><span class="sxs-lookup"><span data-stu-id="d833b-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="d833b-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pagine** (39)</span><span class="sxs-lookup"><span data-stu-id="d833b-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="d833b-883"><span id="LIPS"></span><span id="lips"></span>**Lip** (40)</span><span class="sxs-lookup"><span data-stu-id="d833b-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="d833b-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="d833b-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d833b-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostica** (42)</span><span class="sxs-lookup"><span data-stu-id="d833b-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="d833b-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Capsal** (43)</span><span class="sxs-lookup"><span data-stu-id="d833b-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="d833b-887"><span id="EXCL"></span><span id="excl"></span>**Escl** (44)</span><span class="sxs-lookup"><span data-stu-id="d833b-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="d833b-888"><span id="LCDS"></span><span id="lcds"></span>**LCD** (45)</span><span class="sxs-lookup"><span data-stu-id="d833b-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="d833b-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span><span class="sxs-lookup"><span data-stu-id="d833b-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="d833b-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="d833b-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="d833b-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="d833b-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="d833b-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="d833b-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="d833b-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="d833b-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="d833b-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-895">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-896">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-897">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d833b-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="d833b-898">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-899">**Locale**</span><span class="sxs-lookup"><span data-stu-id="d833b-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-900">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-901">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-902">Se **true**, la stampante non è collegata a una rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="d833b-903">Se entrambe le proprietà **local** e **Network** sono impostate su **true**, la stampante è una stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-904">**Posizione**</span><span class="sxs-lookup"><span data-stu-id="d833b-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-905">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-906">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-907">Posizione fisica della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-907">Physical location of the printer.</span></span>

<span data-ttu-id="d833b-908">Esempio: Bldg.</span><span class="sxs-lookup"><span data-stu-id="d833b-908">Example: Bldg.</span></span> <span data-ttu-id="d833b-909">38, stanza 1164</span><span class="sxs-lookup"><span data-stu-id="d833b-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="d833b-910">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="d833b-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-911">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-912">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-913">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="d833b-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-914">Tecnologia di contrassegno utilizzata dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="d833b-915">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-916">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-917">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="d833b-918">**LED elettrofotografica** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="d833b-919">**Elettrofotografica laser** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="d833b-920">**Elettrofotografica other** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="d833b-921">**Influisca sulla matrice del punto principale 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="d833b-922">**Influisca sulla matrice del punto principale 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="d833b-923">Effetto sullo stato di una **matrice del punto principale** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="d833b-924">**Effetto della testa di trasferimento completamente formato** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="d833b-925">**Gruppo di effetti** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="d833b-926">**Altro effetto** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="d833b-927">**Inkjet acquoso** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="d833b-928">**Solido Inkjet** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="d833b-929">**Altro Inkjet** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="d833b-930">**Penna** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="d833b-931">**Trasferimento termico** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="d833b-932">**Sensibile alla temperatura** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="d833b-933">**Diffusione termica** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="d833b-934">**Altro termico** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="d833b-935">**Elettroerosione** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="d833b-936">**Elettrostatica** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="d833b-937">**Microscheda fotografica** (22)</span><span class="sxs-lookup"><span data-stu-id="d833b-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="d833b-938">**Fotounità fotografico** (23)</span><span class="sxs-lookup"><span data-stu-id="d833b-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="d833b-939">**Altro fotografico** (24)</span><span class="sxs-lookup"><span data-stu-id="d833b-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="d833b-940">**Deposizione degli ioni** (25)</span><span class="sxs-lookup"><span data-stu-id="d833b-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="d833b-941">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="d833b-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="d833b-942">**Tipografo** (27)</span><span class="sxs-lookup"><span data-stu-id="d833b-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-943">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="d833b-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-944">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-945">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-946">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Copies")</span><span class="sxs-lookup"><span data-stu-id="d833b-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-947">Numero massimo di copie che la stampante può produrre per un unico processo.</span><span class="sxs-lookup"><span data-stu-id="d833b-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="d833b-948">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-949">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="d833b-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-950">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-951">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-952">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="d833b-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-953">Numero massimo di pagine del flusso di stampa in cui è possibile eseguire il rendering della stampante su un foglio multimediale, ad esempio la carta.</span><span class="sxs-lookup"><span data-stu-id="d833b-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="d833b-954">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-955">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-956">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-957">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-958">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. JobSize"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="d833b-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-959">Il processo più grande come flusso di byte, in kilobyte, che la stampante può accettare.</span><span class="sxs-lookup"><span data-stu-id="d833b-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="d833b-960">Il valore 0 (zero) indica che non è impostato alcun limite.</span><span class="sxs-lookup"><span data-stu-id="d833b-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="d833b-961">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-962">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-963">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-964">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-965">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ Printer**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. mimetypes "," CIM \_ printservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="d833b-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-966">Matrice di spiegazioni dettagliate del tipo MIME supportate dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="d833b-967">Se vengono forniti dati, il valore 47 ("MIME") deve essere incluso nella proprietà **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="d833b-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="d833b-968">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-969">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d833b-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-970">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-971">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-972">Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="d833b-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-973">Nome della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-973">Name of the printer.</span></span>

<span data-ttu-id="d833b-974">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-975">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-976">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-977">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-978">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. naturallanguage ")</span><span class="sxs-lookup"><span data-stu-id="d833b-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-979">Matrice di linguaggi supportata per le stringhe utilizzate dalla stampante per l'output delle informazioni di gestione.</span><span class="sxs-lookup"><span data-stu-id="d833b-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="d833b-980">Deve essere conforme allo [standard RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span><span class="sxs-lookup"><span data-stu-id="d833b-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="d833b-981">Ad esempio, "en" viene usato per la lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="d833b-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="d833b-982">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-983">**Network**</span><span class="sxs-lookup"><span data-stu-id="d833b-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-984">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-985">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-986">Se **true**, la stampante è una stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="d833b-987">Se entrambe le proprietà **local** e **Network** sono impostate su **true**, la stampante è una stampante di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-988">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-989">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-990">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-991">Matrice dei tipi di carta supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="d833b-992">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="d833b-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="d833b-996"><span id="B"></span><span id="b"></span>**B** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="d833b-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="d833b-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="d833b-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="d833b-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Lettera** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="d833b-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="d833b-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="d833b-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="d833b-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="d833b-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="d833b-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="d833b-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-Number-10-busta** (11)</span><span class="sxs-lookup"><span data-stu-id="d833b-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="d833b-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="d833b-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="d833b-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="d833b-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="d833b-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="d833b-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="d833b-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-Number-9-busta** (15)</span><span class="sxs-lookup"><span data-stu-id="d833b-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="d833b-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="d833b-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="d833b-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="d833b-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="d833b-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="d833b-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="d833b-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="d833b-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="d833b-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="d833b-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="d833b-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="d833b-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="d833b-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="d833b-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="d833b-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="d833b-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="d833b-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="d833b-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="d833b-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="d833b-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="d833b-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="d833b-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="d833b-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="d833b-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="d833b-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="d833b-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="d833b-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="d833b-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="d833b-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="d833b-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="d833b-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="d833b-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="d833b-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="d833b-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="d833b-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="d833b-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="d833b-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="d833b-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="d833b-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="d833b-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="d833b-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="d833b-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="d833b-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="d833b-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="d833b-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="d833b-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="d833b-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="d833b-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="d833b-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="d833b-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="d833b-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="d833b-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1035">C2</span><span class="sxs-lookup"><span data-stu-id="d833b-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="d833b-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="d833b-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1037">C3</span><span class="sxs-lookup"><span data-stu-id="d833b-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="d833b-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="d833b-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1039">C4</span><span class="sxs-lookup"><span data-stu-id="d833b-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="d833b-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="d833b-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1041">C5</span><span class="sxs-lookup"><span data-stu-id="d833b-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="d833b-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="d833b-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1043">C6</span><span class="sxs-lookup"><span data-stu-id="d833b-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="d833b-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="d833b-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1045">C7</span><span class="sxs-lookup"><span data-stu-id="d833b-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="d833b-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Designato da ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="d833b-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1047">C8</span><span class="sxs-lookup"><span data-stu-id="d833b-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="d833b-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="d833b-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="d833b-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="d833b-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="d833b-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="d833b-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="d833b-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="d833b-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="d833b-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="d833b-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="d833b-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="d833b-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="d833b-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="d833b-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="d833b-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="d833b-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="d833b-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="d833b-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="d833b-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="d833b-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="d833b-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="d833b-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="d833b-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="d833b-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="d833b-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="d833b-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="d833b-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="d833b-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="d833b-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1067">JIS B8</span><span class="sxs-lookup"><span data-stu-id="d833b-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="d833b-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="d833b-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1069">JIS B9</span><span class="sxs-lookup"><span data-stu-id="d833b-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="d833b-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Na-Letter** (59)</span><span class="sxs-lookup"><span data-stu-id="d833b-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1071">B10 DI JIS</span><span class="sxs-lookup"><span data-stu-id="d833b-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="d833b-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="d833b-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="d833b-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-busta** (61)</span><span class="sxs-lookup"><span data-stu-id="d833b-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="d833b-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Busta** (62)</span><span class="sxs-lookup"><span data-stu-id="d833b-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="d833b-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**Busta C3** (63)</span><span class="sxs-lookup"><span data-stu-id="d833b-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="d833b-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**Busta C4** (64)</span><span class="sxs-lookup"><span data-stu-id="d833b-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="d833b-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-busta** (65)</span><span class="sxs-lookup"><span data-stu-id="d833b-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="d833b-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**Busta C6** (66)</span><span class="sxs-lookup"><span data-stu-id="d833b-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="d833b-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designata-busta lunga** (67)</span><span class="sxs-lookup"><span data-stu-id="d833b-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="d833b-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarca-busta** (68)</span><span class="sxs-lookup"><span data-stu-id="d833b-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="d833b-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Dirigente** (69)</span><span class="sxs-lookup"><span data-stu-id="d833b-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="d833b-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span><span class="sxs-lookup"><span data-stu-id="d833b-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="d833b-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Fattura** (71)</span><span class="sxs-lookup"><span data-stu-id="d833b-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="d833b-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span><span class="sxs-lookup"><span data-stu-id="d833b-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="d833b-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="d833b-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1086">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="d833b-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1087">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1088">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1089">Qualificatori: [**arrayType**](../wmisdk/standard-qualifiers.md) ("indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ printservice. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="d833b-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1090">Matrice di tipi di carta attualmente disponibili sulla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="d833b-1091">Ogni stringa deve essere espressa nel formato specificato da ISO/IEC 10175 Document Printing Application (DPA), riepilogato nell'Appendice C di [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span><span class="sxs-lookup"><span data-stu-id="d833b-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="d833b-1092">Qualsiasi formato di carta identificato in questa proprietà deve essere incluso anche nella proprietà **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="d833b-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="d833b-1093">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="d833b-1094">Esempio: ISO-A4-colorato</span><span class="sxs-lookup"><span data-stu-id="d833b-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1095">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="d833b-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1096">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1097">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1098">Parametri facoltativi per il processore di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="d833b-1099">Esempio: "copie = 2"</span><span class="sxs-lookup"><span data-stu-id="d833b-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d833b-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1101">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1102">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1103">Qualificatori: [**schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d833b-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1104">Identificatore del dispositivo Windows Plug and Play del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d833b-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d833b-1105">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="d833b-1106">Esempio: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="d833b-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1107">**PortName**</span><span class="sxs-lookup"><span data-stu-id="d833b-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1108">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1109">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1110">Porta utilizzata per trasmettere dati a una stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="d833b-1111">Se una stampante è connessa a più di una porta, i nomi di ogni porta sono separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="d833b-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="d833b-1112">Esempio: LPT1:, LPT2:, LPT3:</span><span class="sxs-lookup"><span data-stu-id="d833b-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1113">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="d833b-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1114">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1116">Matrice delle funzionalità specifiche relative al risparmio di energia di un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d833b-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d833b-1117">Questa proprietà viene ereditata da **CIM \_ LogicalDevice**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="d833b-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d833b-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d833b-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d833b-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1122">Le funzionalità di risparmio energia sono attualmente abilitate, ma il set di funzionalità esatto è sconosciuto oppure le informazioni non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="d833b-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d833b-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modalità di risparmio energia immesse automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1124">Il dispositivo può modificare lo stato di alimentazione in base all'utilizzo o ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="d833b-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d833b-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Stato di alimentazione impostabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1126">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="d833b-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d833b-1127">Questo metodo è disponibile nella classe **\_ LogicalDevice CIM** padre e può essere implementato.</span><span class="sxs-lookup"><span data-stu-id="d833b-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d833b-1128">Per ulteriori informazioni, vedere [progettazione di classi Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d833b-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling supportato** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1130">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione).</span><span class="sxs-lookup"><span data-stu-id="d833b-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d833b-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Alimentazione temporizzata supportata** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1132">Tempo Power-On supportato</span><span class="sxs-lookup"><span data-stu-id="d833b-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="d833b-1133">Il metodo [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) può essere richiamato con il parametro *PowerState* impostato su 5 (ciclo di alimentazione) e *ora* impostato su una data e un'ora specifiche, o su un intervallo, per l'accensione.</span><span class="sxs-lookup"><span data-stu-id="d833b-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1134">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="d833b-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1135">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1137">Se **true**, la potenza del dispositivo può essere gestita, il che significa che è possibile attivare la modalità di sospensione.</span><span class="sxs-lookup"><span data-stu-id="d833b-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="d833b-1138">La proprietà non indica che le funzionalità di risparmio energia sono abilitate, solo che il dispositivo logico è in grado di gestire il risparmio di energia.</span><span class="sxs-lookup"><span data-stu-id="d833b-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d833b-1139">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1140">**PrinterPaperNames**</span><span class="sxs-lookup"><span data-stu-id="d833b-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1141">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d833b-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1143">Matrice di formati della carta supportati dalla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="d833b-1144">I nomi specificati dalla stampante vengono utilizzati per rappresentare i formati di carta supportati.</span><span class="sxs-lookup"><span data-stu-id="d833b-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="d833b-1145">Esempio: B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="d833b-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1146">**PrinterState**</span><span class="sxs-lookup"><span data-stu-id="d833b-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1149">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1150">Uno degli stati possibili relativi a questa stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="d833b-1151">Questa proprietà è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d833b-1151">This property is obsolete.</span></span> <span data-ttu-id="d833b-1152">Al posto di questa proprietà, usare **PrinterStatus**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="d833b-1153">0</span><span class="sxs-lookup"><span data-stu-id="d833b-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1154">Inattività: per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="d833b-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1155">1</span><span class="sxs-lookup"><span data-stu-id="d833b-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1156">Paused</span><span class="sxs-lookup"><span data-stu-id="d833b-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1157">2</span><span class="sxs-lookup"><span data-stu-id="d833b-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1158">Errore</span><span class="sxs-lookup"><span data-stu-id="d833b-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1159">3</span><span class="sxs-lookup"><span data-stu-id="d833b-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1160">Eliminazione in sospeso</span><span class="sxs-lookup"><span data-stu-id="d833b-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1161">4</span><span class="sxs-lookup"><span data-stu-id="d833b-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1162">Inceppamento carta</span><span class="sxs-lookup"><span data-stu-id="d833b-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1163">5</span><span class="sxs-lookup"><span data-stu-id="d833b-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1164">Carta in uscita</span><span class="sxs-lookup"><span data-stu-id="d833b-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1165">6</span><span class="sxs-lookup"><span data-stu-id="d833b-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1166">Feed manuale</span><span class="sxs-lookup"><span data-stu-id="d833b-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1167">7</span><span class="sxs-lookup"><span data-stu-id="d833b-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1168">Problema relativo alla carta</span><span class="sxs-lookup"><span data-stu-id="d833b-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1169">8</span><span class="sxs-lookup"><span data-stu-id="d833b-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1170">Offline</span><span class="sxs-lookup"><span data-stu-id="d833b-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1171">9</span><span class="sxs-lookup"><span data-stu-id="d833b-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1172">I/O attivo</span><span class="sxs-lookup"><span data-stu-id="d833b-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1173">10</span><span class="sxs-lookup"><span data-stu-id="d833b-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1174">Busy</span><span class="sxs-lookup"><span data-stu-id="d833b-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1175">11</span><span class="sxs-lookup"><span data-stu-id="d833b-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1176">Stampa</span><span class="sxs-lookup"><span data-stu-id="d833b-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1177">12</span><span class="sxs-lookup"><span data-stu-id="d833b-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1178">Raccoglitore pieno</span><span class="sxs-lookup"><span data-stu-id="d833b-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1179">13</span><span class="sxs-lookup"><span data-stu-id="d833b-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1180">Non disponibile</span><span class="sxs-lookup"><span data-stu-id="d833b-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1181">14</span><span class="sxs-lookup"><span data-stu-id="d833b-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1182">Attesa</span><span class="sxs-lookup"><span data-stu-id="d833b-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1183">15</span><span class="sxs-lookup"><span data-stu-id="d833b-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1184">Elaborazione in corso</span><span class="sxs-lookup"><span data-stu-id="d833b-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1185">16</span><span class="sxs-lookup"><span data-stu-id="d833b-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1186">Inizializzazione</span><span class="sxs-lookup"><span data-stu-id="d833b-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1187">17</span><span class="sxs-lookup"><span data-stu-id="d833b-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1188">Riscaldamento</span><span class="sxs-lookup"><span data-stu-id="d833b-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1189">18</span><span class="sxs-lookup"><span data-stu-id="d833b-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1190">Toner basso</span><span class="sxs-lookup"><span data-stu-id="d833b-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1191">19</span><span class="sxs-lookup"><span data-stu-id="d833b-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1192">Toner esaurito</span><span class="sxs-lookup"><span data-stu-id="d833b-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1193">20</span><span class="sxs-lookup"><span data-stu-id="d833b-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1194">Punt pagina</span><span class="sxs-lookup"><span data-stu-id="d833b-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1195">21</span><span class="sxs-lookup"><span data-stu-id="d833b-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1196">Intervento dell'utente richiesto</span><span class="sxs-lookup"><span data-stu-id="d833b-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1197">22</span><span class="sxs-lookup"><span data-stu-id="d833b-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1198">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="d833b-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1199">23</span><span class="sxs-lookup"><span data-stu-id="d833b-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1200">Sportello aperto</span><span class="sxs-lookup"><span data-stu-id="d833b-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1201">24</span><span class="sxs-lookup"><span data-stu-id="d833b-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1202">Server \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="d833b-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1203">25</span><span class="sxs-lookup"><span data-stu-id="d833b-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="d833b-1204">Risparmio energia</span><span class="sxs-lookup"><span data-stu-id="d833b-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1205">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="d833b-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1206">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1208">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="d833b-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1209">Informazioni sullo stato di una stampante diverse dalle informazioni specificate nella proprietà di **disponibilità** del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d833b-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="d833b-1210">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="d833b-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inattivo** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1214">Inattività: per ulteriori informazioni, vedere la sezione Osservazioni riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="d833b-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="d833b-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Stampa** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="d833b-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Riscaldamento** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d833b-1217">Riscaldamento</span><span class="sxs-lookup"><span data-stu-id="d833b-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="d833b-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stampa interrotta** (6)</span><span class="sxs-lookup"><span data-stu-id="d833b-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="d833b-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="d833b-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="d833b-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1222">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1223">Tipo di dati di un processo di stampa in attesa del dispositivo di stampa basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="d833b-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1224">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="d833b-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1227">Nome dello spooler di stampa che gestisce i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="d833b-1228">Esempio: SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="d833b-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1229">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="d833b-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1230">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1231">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1232">Priorità della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1232">Priority of the printer.</span></span> <span data-ttu-id="d833b-1233">I processi con una stampante con priorità più alta vengono pianificati per primi.</span><span class="sxs-lookup"><span data-stu-id="d833b-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1234">**Pubblicato**</span><span class="sxs-lookup"><span data-stu-id="d833b-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1235">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1236">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1237">Se **true**, la stampante è pubblicata nel servizio directory di rete.</span><span class="sxs-lookup"><span data-stu-id="d833b-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1238">**Queued**</span><span class="sxs-lookup"><span data-stu-id="d833b-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1240">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1241">Se il valore è **true**, la stampante memorizza i buffer e accoda i processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="d833b-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1242">**RawOnly**</span><span class="sxs-lookup"><span data-stu-id="d833b-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1243">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1244">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1245">Se **true**, la stampante accetta solo dati non elaborati di cui eseguire lo spooling.</span><span class="sxs-lookup"><span data-stu-id="d833b-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1246">**SeparatorFile**</span><span class="sxs-lookup"><span data-stu-id="d833b-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1248">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1249">Nome del file utilizzato per creare una pagina separatore.</span><span class="sxs-lookup"><span data-stu-id="d833b-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="d833b-1250">Questa pagina viene utilizzata per separare i processi di stampa inviati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="d833b-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1254">Nome del server che controlla la stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="d833b-1255">Se la stringa è **null**, la stampante viene controllata localmente.</span><span class="sxs-lookup"><span data-stu-id="d833b-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1256">**Condivisa**</span><span class="sxs-lookup"><span data-stu-id="d833b-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1257">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1258">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1259">Se **true**, la stampante è disponibile come risorsa di rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="d833b-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1260">**ShareName**</span><span class="sxs-lookup"><span data-stu-id="d833b-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1263">Nome condivisione del dispositivo di stampa basato su Windows.</span><span class="sxs-lookup"><span data-stu-id="d833b-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="d833b-1264">Esempio: " \\ \\ PRINTSERVER1 \\ PRINTER2"</span><span class="sxs-lookup"><span data-stu-id="d833b-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1265">**SpoolEnabled**</span><span class="sxs-lookup"><span data-stu-id="d833b-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1266">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1268">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1269">Questa proprietà è obsoleta. Non usare.</span><span class="sxs-lookup"><span data-stu-id="d833b-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="d833b-1270">Se **true**, lo spooling è abilitato per la stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1272">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1273">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1274">Data e ora in cui una stampante può iniziare a stampare un processo, se la stampante è limitata alla stampa in momenti specifici.</span><span class="sxs-lookup"><span data-stu-id="d833b-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="d833b-1275">Questo valore è espresso come tempo trascorso dal giorno 12:00 GMT (ora di Greenwich).</span><span class="sxs-lookup"><span data-stu-id="d833b-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1276">**Status**</span><span class="sxs-lookup"><span data-stu-id="d833b-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1277">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1279">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="d833b-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1280">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d833b-1280">Current status of the object.</span></span> <span data-ttu-id="d833b-1281">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="d833b-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d833b-1282">Gli stati operativi includono: **OK**, **danneggiato** e prevedi errore **(un** elemento, ad esempio un'unità disco rigido abilitata per Smart, può funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="d833b-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d833b-1283">Gli Stati non operativi includono: **Error**, **Starting**, **Stop** e **Service**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="d833b-1284">Il secondo, **servizio**, può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="d833b-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d833b-1285">Non tutto questo lavoro è online, ma l'elemento gestito non è né **OK** né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="d833b-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="d833b-1286">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d833b-1287">Sono inclusi i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="d833b-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d833b-1288">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="d833b-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d833b-1289">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="d833b-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d833b-1290">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="d833b-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-1291">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="d833b-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d833b-1292">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="d833b-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d833b-1293">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="d833b-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d833b-1294">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="d833b-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d833b-1295">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="d833b-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d833b-1296">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="d833b-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d833b-1297">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="d833b-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d833b-1298">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="d833b-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d833b-1299">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="d833b-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d833b-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1301">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d833b-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1303">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Stato operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d833b-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1304">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="d833b-1304">State of the logical device.</span></span> <span data-ttu-id="d833b-1305">Se questa proprietà non si applica al dispositivo logico, è necessario utilizzare il valore 5 (**non applicabile**).</span><span class="sxs-lookup"><span data-stu-id="d833b-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="d833b-1306">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d833b-1307">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="d833b-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d833b-1308">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="d833b-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d833b-1309">**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d833b-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d833b-1310">**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="d833b-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d833b-1311">**Non applicabile** (5)</span><span class="sxs-lookup"><span data-stu-id="d833b-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d833b-1312">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d833b-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1315">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1316">Valore della proprietà **CreationClassName** del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="d833b-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d833b-1317">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d833b-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d833b-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1321">Qualificatori: [**propagato**](../wmisdk/standard-qualifiers.md) ("[**\_ sistema CIM**](cim-system.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="d833b-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1322">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="d833b-1322">Name of the scoping system.</span></span>

<span data-ttu-id="d833b-1323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="d833b-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1325">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1327">Data e ora dell'ultima reimpostazione della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="d833b-1328">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1330">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d833b-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1331">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1332">Data e ora in cui una stampante può stampare l'ultimo processo, se la stampante è limitata alla stampa in momenti specifici.</span><span class="sxs-lookup"><span data-stu-id="d833b-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="d833b-1333">Questo valore è espresso come tempo trascorso dal giorno 12:00 GMT (ora di Greenwich).</span><span class="sxs-lookup"><span data-stu-id="d833b-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="d833b-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1335">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d833b-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d833b-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1337">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unità**](../wmisdk/standard-qualifiers.md) ("pixel per pollice")</span><span class="sxs-lookup"><span data-stu-id="d833b-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1338">Risoluzione verticale, in pixel per pollice, della stampante.</span><span class="sxs-lookup"><span data-stu-id="d833b-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="d833b-1339">Questa proprietà viene ereditata [**dalla \_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="d833b-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="d833b-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d833b-1341">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d833b-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d833b-1342">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d833b-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d833b-1343">Se **true**, è possibile accodare i processi di stampa nel computer quando la stampante è offline.</span><span class="sxs-lookup"><span data-stu-id="d833b-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d833b-1344">Commenti</span><span class="sxs-lookup"><span data-stu-id="d833b-1344">Remarks</span></span>

<span data-ttu-id="d833b-1345">La **classe \_ stampante Win32** è derivata dalla [**\_ stampante CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="d833b-1346">Prima di chiamare [**SWbemObject. \_ put**](../wmisdk/swbemobject-put-.md) o [**IWbemServices::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) per un'istanza di **\_ stampante Win32** , è necessario abilitare il privilegio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** per Visual Basic e LoadDriver per i moniker di scripting).</span><span class="sxs-lookup"><span data-stu-id="d833b-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="d833b-1347">Per altre informazioni, vedere [**costanti Privilege**](../wmisdk/privilege-constants.md) ed [esecuzione di operazioni con privilegi](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d833b-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="d833b-1348">Nell'esempio di codice VBScript seguente viene illustrato come abilitare il privilegio **SetLoadDriverPrivilege** nello script.</span><span class="sxs-lookup"><span data-stu-id="d833b-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="d833b-1349">Per l'utilizzo dei cluster di stampanti MSCS, utilizzare l'assembly prnadmin.dll, oppure lo spazio dei nomi [System. Printing](/dotnet/api/system.printing) di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="d833b-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="d833b-1350">Windows utilizza le credenziali dell'utente che esegue lo script per determinare quali sono le stampanti disponibili.</span><span class="sxs-lookup"><span data-stu-id="d833b-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="d833b-1351">Pertanto, se si esegue uno script in modalità remota, è possibile accedere solo a qualsiasi stampante disponibile per l'account utente nel sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="d833b-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="d833b-1352">Non è possibile usare la classe **\_ stampante Win32** per le stampanti in un cluster di stampa MSCS.</span><span class="sxs-lookup"><span data-stu-id="d833b-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="d833b-1353">In alternativa, potrebbe essere necessario usare lo strumento PrinterAdmin (PrnAdmin.dll) o lo spazio dei nomi .NET Framework [System. Printing](/dotnet/api/system.printing) .</span><span class="sxs-lookup"><span data-stu-id="d833b-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="d833b-1354">Se si sta recuperando **PrinterStatus** = 3 o **PrinterState** = 0, è possibile che il driver della stampante non stia inserendo informazioni accurate in WMI.</span><span class="sxs-lookup"><span data-stu-id="d833b-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="d833b-1355">WMI recupera le informazioni sulla stampante dal processo spoolsv.exe.</span><span class="sxs-lookup"><span data-stu-id="d833b-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="d833b-1356">È possibile che il driver della stampante non segnali lo stato sullo spooler.</span><span class="sxs-lookup"><span data-stu-id="d833b-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="d833b-1357">In questo caso, la stampante **Win32 \_** segnala la stampante come **inattiva**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d833b-1358">Esempio</span><span class="sxs-lookup"><span data-stu-id="d833b-1358">Examples</span></span>

<span data-ttu-id="d833b-1359">L'esempio di [creazione di un disegno di configurazione computer tramite](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell PowerShell nella raccolta TechNet usa la **\_ stampante Win32** per interagire con il modello di automazione di Visio per creare un disegno di Visio.</span><span class="sxs-lookup"><span data-stu-id="d833b-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="d833b-1360">Lo [script PowerShell Remote PC info](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) utilizza alcune classi, inclusa la **\_ stampante Win32**, per recuperare informazioni su un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="d833b-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="d833b-1361">Nell'esempio di codice PowerShell seguente viene illustrato come determinare la stampante predefinita del computer locale.</span><span class="sxs-lookup"><span data-stu-id="d833b-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="d833b-1362">Nell'esempio di codice VBScript seguente viene descritto come recuperare le statistiche delle stampanti dalle istanze della **\_ stampante Win32**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="d833b-1363">Nell'esempio di codice Perl seguente viene descritto come recuperare le statistiche delle stampanti dalle istanze della **\_ stampante Win32**.</span><span class="sxs-lookup"><span data-stu-id="d833b-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="d833b-1364">Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere il nome della stampante predefinita per un computer.</span><span class="sxs-lookup"><span data-stu-id="d833b-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="d833b-1365">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d833b-1365">Requirements</span></span>



| <span data-ttu-id="d833b-1366">Requisito</span><span class="sxs-lookup"><span data-stu-id="d833b-1366">Requirement</span></span> | <span data-ttu-id="d833b-1367">Valore</span><span class="sxs-lookup"><span data-stu-id="d833b-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d833b-1368">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d833b-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="d833b-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d833b-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d833b-1370">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d833b-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="d833b-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d833b-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d833b-1372">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d833b-1372">Namespace</span></span><br/>                | <span data-ttu-id="d833b-1373">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d833b-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d833b-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="d833b-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d833b-1375"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d833b-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d833b-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="d833b-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d833b-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d833b-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d833b-1378">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d833b-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d833b-1379">**\_Stampante CIM**</span><span class="sxs-lookup"><span data-stu-id="d833b-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="d833b-1380">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d833b-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d833b-1381">Attività WMI: stampanti e stampa</span><span class="sxs-lookup"><span data-stu-id="d833b-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
