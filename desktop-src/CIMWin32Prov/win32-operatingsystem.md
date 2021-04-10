---
description: Rappresenta un sistema operativo basato su Windows installato in un computer.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Classe Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15a6a1bf7bec8c830d1a15ec690b01ec9ea22e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225764"
---
# <a name="win32_operatingsystem-class"></a><span data-ttu-id="dc69c-103">Win32 \_ OperatingSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="dc69c-103">Win32\_OperatingSystem class</span></span>

<span data-ttu-id="dc69c-104">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OperatingSystem Win32** rappresenta un sistema operativo basato su Windows installato in un computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-104">The **Win32\_OperatingSystem** [WMI class](../wmisdk/retrieving-a-class.md) represents a Windows-based operating system installed on a computer.</span></span>

<span data-ttu-id="dc69c-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dc69c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dc69c-106">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dc69c-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc69c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc69c-107">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a><span data-ttu-id="dc69c-108">Members</span><span class="sxs-lookup"><span data-stu-id="dc69c-108">Members</span></span>

<span data-ttu-id="dc69c-109">La classe **Win32 \_ OperatingSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dc69c-109">The **Win32\_OperatingSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="dc69c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="dc69c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="dc69c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc69c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dc69c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="dc69c-112">Methods</span></span>

<span data-ttu-id="dc69c-113">La classe **Win32 \_ OperatingSystem** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dc69c-113">The **Win32\_OperatingSystem** class has these methods.</span></span>



| <span data-ttu-id="dc69c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="dc69c-114">Method</span></span>                                                                                     | <span data-ttu-id="dc69c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc69c-115">Description</span></span>                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc69c-116">**Riavvio**</span><span class="sxs-lookup"><span data-stu-id="dc69c-116">**Reboot**</span></span>](reboot-method-in-class-win32-operatingsystem.md)                             | <span data-ttu-id="dc69c-117">Arresta e riavvia il sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-117">Shuts down and then restarts the computer system.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dc69c-118">**SetDateTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-118">**SetDateTime**</span></span>](setdatetime-method-in-class-win32-operatingsystem.md)                   | <span data-ttu-id="dc69c-119">Consente di impostare la data e l'ora del computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-119">Allows the computer date and time to be set.</span></span><br/>                                                                                                                                                                                                                |
| [<span data-ttu-id="dc69c-120">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="dc69c-120">**Shutdown**</span></span>](shutdown-method-in-class-win32-operatingsystem.md)                         | <span data-ttu-id="dc69c-121">Scarica i programmi e le dll nel punto in cui è sicuro spegnere il computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-121">Unloads programs and DLLs to the point where it is safe to turn off the computer.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="dc69c-122">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="dc69c-122">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)               | <span data-ttu-id="dc69c-123">Fornisce il set completo di opzioni di arresto supportate dai sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-123">Provides the full set of shutdown options supported by Windows operating systems.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="dc69c-124">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="dc69c-124">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | <span data-ttu-id="dc69c-125">Fornisce lo stesso set di opzioni di arresto supportate dal metodo [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) in **Win32 \_ OperatingSystem**, ma consente anche di specificare i commenti, il motivo dell'arresto o il timeout.</span><span class="sxs-lookup"><span data-stu-id="dc69c-125">Provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in **Win32\_OperatingSystem**, but also allows you to specify comments, a reason for shutdown, or a timeout.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dc69c-126">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dc69c-126">Properties</span></span>

<span data-ttu-id="dc69c-127">La classe **Win32 \_ OperatingSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc69c-127">The **Win32\_OperatingSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc69c-128">**BootDevice**</span><span class="sxs-lookup"><span data-stu-id="dc69c-128">**BootDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-131">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| drive \_ Map \_ info \| btInt13Unit")</span><span class="sxs-lookup"><span data-stu-id="dc69c-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|DRIVE\_MAP\_INFO\|btInt13Unit")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-132">Nome dell'unità disco da cui viene avviato il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-132">Name of the disk drive from which the Windows operating system starts.</span></span>

<span data-ttu-id="dc69c-133">Esempio: " \\ \\ Device \\ DiscoRigido0"</span><span class="sxs-lookup"><span data-stu-id="dc69c-133">Example: "\\\\Device\\Harddisk0"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-134">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="dc69c-134">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwBuildNumber")</span><span class="sxs-lookup"><span data-stu-id="dc69c-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwBuildNumber")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-138">Numero di build di un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-138">Build number of an operating system.</span></span> <span data-ttu-id="dc69c-139">Può essere usato per informazioni più precise sulla versione dei numeri di versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="dc69c-139">It can be used for more precise version information than product release version numbers.</span></span>

<span data-ttu-id="dc69c-140">Esempio: "1381"</span><span class="sxs-lookup"><span data-stu-id="dc69c-140">Example: "1381"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-141">**BuildType**</span><span class="sxs-lookup"><span data-stu-id="dc69c-141">**BuildType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-144">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| CurrentType")</span><span class="sxs-lookup"><span data-stu-id="dc69c-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|CurrentType")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-145">Tipo di compilazione utilizzata per un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-145">Type of build used for an operating system.</span></span>

<span data-ttu-id="dc69c-146">Esempi: "Build per la vendita al dettaglio" "," "compilazione controllata" "</span><span class="sxs-lookup"><span data-stu-id="dc69c-146">Examples: ""retail build"", ""checked build""</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-147">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="dc69c-147">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-150">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dc69c-150">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-151">Breve descrizione dell'oggetto, ovvero una stringa a una riga.</span><span class="sxs-lookup"><span data-stu-id="dc69c-151">Short description of the object—a one-line string.</span></span> <span data-ttu-id="dc69c-152">La stringa include la versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-152">The string includes the operating system version.</span></span> <span data-ttu-id="dc69c-153">Ad esempio, "Microsoft Windows 7 Enterprise".</span><span class="sxs-lookup"><span data-stu-id="dc69c-153">For example, "Microsoft Windows 7 Enterprise ".</span></span> <span data-ttu-id="dc69c-154">Questa proprietà può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-154">This property can be localized.</span></span>

<span data-ttu-id="dc69c-155">**Windows Vista e Windows 7:** Questa proprietà può contenere caratteri finali.</span><span class="sxs-lookup"><span data-stu-id="dc69c-155">**Windows Vista and Windows 7:** This property may contain trailing characters.</span></span> <span data-ttu-id="dc69c-156">Ad esempio, la stringa "Microsoft Windows 7 Enterprise" (spazio finale incluso) potrebbe essere necessaria per recuperare le informazioni tramite questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc69c-156">For example, the string "Microsoft Windows 7 Enterprise " (trailing space included) may be necessary to retrieve information using this property.</span></span>

<span data-ttu-id="dc69c-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-158">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="dc69c-158">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-161">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ IDEFAULTANSICODEPAGE")</span><span class="sxs-lookup"><span data-stu-id="dc69c-161">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (6), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_IDEFAULTANSICODEPAGE")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-162">Valore della tabella codici utilizzato da un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-162">Code page value an operating system uses.</span></span> <span data-ttu-id="dc69c-163">Una tabella codici contiene una tabella dei caratteri utilizzata da un sistema operativo per tradurre le stringhe per lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="dc69c-163">A code page contains a character table that an operating system uses to translate strings for different languages.</span></span> <span data-ttu-id="dc69c-164">Il American National Standards Institute (ANSI) elenca i valori che rappresentano tabelle codici definite.</span><span class="sxs-lookup"><span data-stu-id="dc69c-164">The American National Standards Institute (ANSI) lists values that represent defined code pages.</span></span> <span data-ttu-id="dc69c-165">Se un sistema operativo non usa una tabella codici ANSI, questo membro è impostato su 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-165">If an operating system does not use an ANSI code page, this member is set to 0 (zero).</span></span> <span data-ttu-id="dc69c-166">La stringa del **codificatore** può usare un massimo di sei caratteri per definire il valore della tabella codici.</span><span class="sxs-lookup"><span data-stu-id="dc69c-166">The **CodeSet** string can use a maximum of six characters to define the code page value.</span></span>

<span data-ttu-id="dc69c-167">Esempio: "1255"</span><span class="sxs-lookup"><span data-stu-id="dc69c-167">Example: "1255"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-168">**CountryCode**</span><span class="sxs-lookup"><span data-stu-id="dc69c-168">**CountryCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-171">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ICOUNTRY")</span><span class="sxs-lookup"><span data-stu-id="dc69c-171">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ICOUNTRY")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-172">Codice per il paese/area geografica utilizzato da un sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-172">Code for the country/region that an operating system uses.</span></span> <span data-ttu-id="dc69c-173">I valori sono basati sui prefissi di composizione telefonica internazionali, detti anche codici IBM Country/Region.</span><span class="sxs-lookup"><span data-stu-id="dc69c-173">Values are based on international phone dialing prefixes—also referred to as IBM country/region codes.</span></span> <span data-ttu-id="dc69c-174">Questa proprietà può usare un massimo di sei caratteri per definire il valore del codice paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="dc69c-174">This property can use a maximum of six characters to define the country/region code value.</span></span>

<span data-ttu-id="dc69c-175">Esempio: "1" (Stati Uniti)</span><span class="sxs-lookup"><span data-stu-id="dc69c-175">Example: "1" (United States)</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc69c-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-179">Qualificatori: [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="dc69c-179">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-180">Nome della prima classe concreta visualizzata nella catena di ereditarietà utilizzata per la creazione di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="dc69c-180">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="dc69c-181">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="dc69c-181">When used with other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="dc69c-182">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-182">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-183">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dc69c-183">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-184">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-186">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="dc69c-186">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-187">Nome della classe di creazione del computer di ambito.</span><span class="sxs-lookup"><span data-stu-id="dc69c-187">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="dc69c-188">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-188">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-189">**CSDVersion**</span><span class="sxs-lookup"><span data-stu-id="dc69c-189">**CSDVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-192">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **szCSDVersion**")</span><span class="sxs-lookup"><span data-stu-id="dc69c-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**szCSDVersion**")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-193">Stringa con terminazione **null** che indica la Service Pack più recente installata in un computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-193">**NULL**-terminated string that indicates the latest service pack installed on a computer.</span></span> <span data-ttu-id="dc69c-194">Se non è installato alcun Service Pack, la stringa è **null**.</span><span class="sxs-lookup"><span data-stu-id="dc69c-194">If no service pack is installed, the string is **NULL**.</span></span>

<span data-ttu-id="dc69c-195">Esempio: "Service Pack 3"</span><span class="sxs-lookup"><span data-stu-id="dc69c-195">Example: "Service Pack 3"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-196">**CSName**</span><span class="sxs-lookup"><span data-stu-id="dc69c-196">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-199">Qualificatori: [**propagati**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**\_ chiave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="dc69c-199">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-200">Nome del sistema di ambito del computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-200">Name of the scoping computer system.</span></span>

<span data-ttu-id="dc69c-201">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-201">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-202">**CurrentTimeZone**</span><span class="sxs-lookup"><span data-stu-id="dc69c-202">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-203">Tipo di dati: **sint16**</span><span class="sxs-lookup"><span data-stu-id="dc69c-203">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-205">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("minuti")</span><span class="sxs-lookup"><span data-stu-id="dc69c-205">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-206">Numero, in minuti, di offset di un sistema operativo rispetto all'ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="dc69c-206">Number, in minutes, an operating system is offset from Greenwich mean time (GMT).</span></span> <span data-ttu-id="dc69c-207">Il numero è positivo, negativo o zero.</span><span class="sxs-lookup"><span data-stu-id="dc69c-207">The number is positive, negative, or zero.</span></span>

<span data-ttu-id="dc69c-208">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-208">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-209">**\_32BitApplications DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="dc69c-209">**DataExecutionPrevention\_32BitApplications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-210">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-212">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-213">Quando è disponibile la funzionalità hardware per la prevenzione dell'esecuzione dei dati, questa proprietà indica che la funzionalità è impostata per funzionare per le applicazioni a 32 bit se **true**.</span><span class="sxs-lookup"><span data-stu-id="dc69c-213">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for 32-bit applications if **True**.</span></span> <span data-ttu-id="dc69c-214">Nei computer a 64 bit la funzionalità Protezione esecuzione programmi è configurata nell'archivio di [dati configurazione di avvio (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) e le proprietà in **Win32 \_ OperatingSystem** vengono impostate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="dc69c-214">On 64-bit computers, the data execution prevention feature is configured in the [Boot Configuration Data (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-215">**DataExecutionPrevention \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="dc69c-215">**DataExecutionPrevention\_Available**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-216">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-218">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-219">La prevenzione dell'esecuzione dei dati è una funzionalità hardware che impedisce gli attacchi di sovraccarico del buffer arrestando l'esecuzione del codice nelle pagine di memoria del tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="dc69c-219">Data execution prevention is a hardware feature to prevent buffer overrun attacks by stopping the execution of code on data-type memory pages.</span></span> <span data-ttu-id="dc69c-220">Se **true**, questa funzionalità è disponibile.</span><span class="sxs-lookup"><span data-stu-id="dc69c-220">If **True**, then this feature is available.</span></span> <span data-ttu-id="dc69c-221">Nei computer a 64 bit la funzionalità Protezione esecuzione programmi è configurata nell'archivio BCD e le proprietà in **Win32 \_ OperatingSystem** vengono impostate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="dc69c-221">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-222">**\_Driver DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="dc69c-222">**DataExecutionPrevention\_Drivers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-223">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-223">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-225">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-226">Quando è disponibile la funzionalità hardware per la prevenzione dell'esecuzione dei dati, questa proprietà indica che la funzionalità è impostata per funzionare per i driver se **true**.</span><span class="sxs-lookup"><span data-stu-id="dc69c-226">When the data execution prevention hardware feature is available, this property indicates that the feature is set to work for drivers if **True**.</span></span> <span data-ttu-id="dc69c-227">Nei computer a 64 bit la funzionalità Protezione esecuzione programmi è configurata nell'archivio BCD e le proprietà in **Win32 \_ OperatingSystem** vengono impostate di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="dc69c-227">On 64-bit computers, the data execution prevention feature is configured in the BCD store and the properties in **Win32\_OperatingSystem** are set accordingly.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-228">**\_SupportPolicy DataExecutionPrevention**</span><span class="sxs-lookup"><span data-stu-id="dc69c-228">**DataExecutionPrevention\_SupportPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-229">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc69c-229">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-231">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-232">Indica quale impostazione DEP (Data Execution Prevention) viene applicata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-232">Indicates which Data Execution Prevention (DEP) setting is applied.</span></span> <span data-ttu-id="dc69c-233">L'impostazione DEP specifica la portata a cui DEP si applica alle applicazioni a 32 bit nel sistema.</span><span class="sxs-lookup"><span data-stu-id="dc69c-233">The DEP setting specifies the extent to which DEP applies to 32-bit applications on the system.</span></span> <span data-ttu-id="dc69c-234">DEP viene sempre applicato al kernel di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-234">DEP is always applied to the Windows kernel.</span></span>

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span data-ttu-id="dc69c-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Sempre disattivato** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-235"><span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Always Off** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-236">DEP è disattivato per tutte le applicazioni a 32 bit nel computer senza eccezioni.</span><span class="sxs-lookup"><span data-stu-id="dc69c-236">DEP is turned off for all 32-bit applications on the computer with no exceptions.</span></span> <span data-ttu-id="dc69c-237">Questa impostazione non è disponibile per l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dc69c-237">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span data-ttu-id="dc69c-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-238"><span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always On** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-239">DEP è abilitato per tutte le applicazioni a 32 bit nel computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-239">DEP is enabled for all 32-bit applications on the computer.</span></span> <span data-ttu-id="dc69c-240">Questa impostazione non è disponibile per l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="dc69c-240">This setting is not available for the user interface.</span></span>

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span data-ttu-id="dc69c-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Acconsenti esplicitamente** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-241"><span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Opt In** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-242">DEP è abilitato per un numero limitato di file binari, il kernel e tutti i servizi basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-242">DEP is enabled for a limited number of binaries, the kernel, and all Windows-based services.</span></span> <span data-ttu-id="dc69c-243">Tuttavia, è disattivata per impostazione predefinita per tutte le applicazioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="dc69c-243">However, it is off by default for all 32-bit applications.</span></span> <span data-ttu-id="dc69c-244">Un utente o un amministratore deve scegliere esplicitamente l'impostazione **Always on** o **opt out** prima che DEP possa essere applicato a applicazioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="dc69c-244">A user or administrator must explicitly choose either the **Always On** or the **Opt Out** setting before DEP can be applied to 32-bit applications.</span></span>

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span data-ttu-id="dc69c-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Rifiutare esplicitamente** (3)</span><span class="sxs-lookup"><span data-stu-id="dc69c-245"><span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Opt Out** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-246">DEP è abilitato per impostazione predefinita per tutte le applicazioni a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="dc69c-246">DEP is enabled by default for all 32-bit applications.</span></span> <span data-ttu-id="dc69c-247">Un utente o un amministratore può rimuovere in modo esplicito il supporto per un'applicazione a 32 bit aggiungendo l'applicazione a un elenco di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="dc69c-247">A user or administrator can explicitly remove support for a 32-bit application by adding the application to an exceptions list.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-248">**Eseguire il debug**</span><span class="sxs-lookup"><span data-stu-id="dc69c-248">**Debug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-249">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-251">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ debug")</span><span class="sxs-lookup"><span data-stu-id="dc69c-251">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)\|SM\_DEBUG")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-252">Il sistema operativo è una compilazione controllata (debug).</span><span class="sxs-lookup"><span data-stu-id="dc69c-252">Operating system is a checked (debug) build.</span></span> <span data-ttu-id="dc69c-253">Se **true**, viene installata la versione di debug.</span><span class="sxs-lookup"><span data-stu-id="dc69c-253">If **True**, the debugging version is installed.</span></span> <span data-ttu-id="dc69c-254">Le compilazioni selezionate forniscono controllo degli errori, verifica degli argomenti e codice di debug del sistema.</span><span class="sxs-lookup"><span data-stu-id="dc69c-254">Checked builds provide error checking, argument verification, and system debugging code.</span></span> <span data-ttu-id="dc69c-255">Il codice aggiuntivo in un file binario selezionato genera un messaggio di errore del debugger del kernel e si interrompe nel debugger.</span><span class="sxs-lookup"><span data-stu-id="dc69c-255">Additional code in a checked binary generates a kernel debugger error message and breaks into the debugger.</span></span> <span data-ttu-id="dc69c-256">Questo consente di determinare immediatamente la ragione e la posizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="dc69c-256">This helps immediately determine the cause and location of the error.</span></span> <span data-ttu-id="dc69c-257">Le prestazioni possono essere influenzate da una compilazione controllata a causa del codice aggiuntivo eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc69c-257">Performance may be affected in a checked build due to the additional code that is executed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-258">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dc69c-258">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-259">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-260">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc69c-260">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-261">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-261">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Description"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-262">Descrizione del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-262">Description of the Windows operating system.</span></span> <span data-ttu-id="dc69c-263">Alcune interfacce utente, ad esempio quelle che consentono di modificare questa descrizione, ne limitano la lunghezza a 48 caratteri.</span><span class="sxs-lookup"><span data-stu-id="dc69c-263">Some user interfaces for example, those that allow editing of this description, limit its length to 48 characters.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-264">**Distribuita**</span><span class="sxs-lookup"><span data-stu-id="dc69c-264">**Distributed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-265">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-267">Se **true**, il sistema operativo viene distribuito tra più nodi di sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-267">If **True**, the operating system is distributed across several computer system nodes.</span></span> <span data-ttu-id="dc69c-268">In tal caso, questi nodi devono essere raggruppati come cluster.</span><span class="sxs-lookup"><span data-stu-id="dc69c-268">If so, these nodes should be grouped as a cluster.</span></span>

<span data-ttu-id="dc69c-269">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-269">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-270">**EncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="dc69c-270">**EncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-271">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-271">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-273">Livello di crittografia per le transazioni sicure: 40 bit, 128 bit o *n* bit.</span><span class="sxs-lookup"><span data-stu-id="dc69c-273">Encryption level for secure transactions: 40-bit, 128-bit, or *n*-bit.</span></span>

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

<span data-ttu-id="dc69c-274">**40 bit** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-274">**40-bit** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

<span data-ttu-id="dc69c-275">**128 bit** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-275">**128-bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

<span data-ttu-id="dc69c-276">**n bit** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-276">**n-bit** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-277">**ForegroundApplicationBoost**</span><span class="sxs-lookup"><span data-stu-id="dc69c-277">**ForegroundApplicationBoost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-278">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc69c-278">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-279">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc69c-279">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-280">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="dc69c-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-281">L'aumento della priorità viene assegnato all'applicazione in primo piano.</span><span class="sxs-lookup"><span data-stu-id="dc69c-281">Increase in priority is given to the foreground application.</span></span> <span data-ttu-id="dc69c-282">Il potenziamento delle applicazioni viene implementato assegnando a un'applicazione più intervalli di tempo di esecuzione (lunghezze del Quantum).</span><span class="sxs-lookup"><span data-stu-id="dc69c-282">Application boost is implemented by giving an application more execution time slices (quantum lengths).</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="dc69c-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-283"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-284">Il sistema incrementa la lunghezza del quantum di 6.</span><span class="sxs-lookup"><span data-stu-id="dc69c-284">The system boosts the quantum length by 6.</span></span>

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="dc69c-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimo** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-285"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-286">Il sistema incrementa la lunghezza del quantum di 12.</span><span class="sxs-lookup"><span data-stu-id="dc69c-286">The system boosts the quantum length by 12.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="dc69c-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-287"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-288">Il sistema incrementa la lunghezza del quantum di 18.</span><span class="sxs-lookup"><span data-stu-id="dc69c-288">The system boosts the quantum length by 18.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-289">**FreePhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="dc69c-289">**FreePhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-290">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-292">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-292">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-293">Numero, in kilobyte, della memoria fisica attualmente inutilizzata e disponibile.</span><span class="sxs-lookup"><span data-stu-id="dc69c-293">Number, in kilobytes, of physical memory currently unused and available.</span></span>

<span data-ttu-id="dc69c-294">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-294">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-295">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-295">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-296">**FreeSpaceInPagingFiles**</span><span class="sxs-lookup"><span data-stu-id="dc69c-296">**FreeSpaceInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-297">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-299">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Impostazioni memoria \| di sistema 001,4 "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.4"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-300">Numero, in kilobyte, di cui è possibile eseguire il mapping nei file di paging del sistema operativo senza causare lo swapping di altre pagine.</span><span class="sxs-lookup"><span data-stu-id="dc69c-300">Number, in kilobytes, that can be mapped into the operating system paging files without causing any other pages to be swapped out.</span></span>

<span data-ttu-id="dc69c-301">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-301">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-302">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-302">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-303">**FreeVirtualMemory**</span><span class="sxs-lookup"><span data-stu-id="dc69c-303">**FreeVirtualMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-304">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-304">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-306">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-306">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-307">Numero, in kilobyte, della memoria virtuale attualmente inutilizzata e disponibile.</span><span class="sxs-lookup"><span data-stu-id="dc69c-307">Number, in kilobytes, of virtual memory currently unused and available.</span></span>

<span data-ttu-id="dc69c-308">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-308">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-309">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-309">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-310">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dc69c-310">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-311">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-313">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-313">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-314">Oggetto Data installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-314">Date object was installed.</span></span> <span data-ttu-id="dc69c-315">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-315">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dc69c-316">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-317">**LargeSystemCache**</span><span class="sxs-lookup"><span data-stu-id="dc69c-317">**LargeSystemCache**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-318">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-320">Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="dc69c-320">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-321">Questa proprietà è obsoleta e non è supportata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-321">This property is obsolete and not supported.</span></span>

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span data-ttu-id="dc69c-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Ottimizza per le applicazioni** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-322"><span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Optimize for Applications** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-323">Ottimizzare la memoria per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dc69c-323">Optimize memory for applications.</span></span>

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span data-ttu-id="dc69c-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Ottimizzare le prestazioni del sistema** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-324"><span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Optimize for System Performance** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-325">Ottimizzare la memoria per le prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="dc69c-325">Optimize memory for system performance.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-326">**LastBootUpTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-326">**LastBootUpTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-327">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-327">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-329">Data e ora dell'ultimo riavvio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-329">Date and time the operating system was last restarted.</span></span>

<span data-ttu-id="dc69c-330">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-330">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-331">**LocalDateTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-331">**LocalDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-332">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dc69c-332">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-334">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| host-Resources-MIB. hrSystemDate "," MIF. DMTF \| informazioni generali \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemDate", "MIF.DMTF\|General Information\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-335">Versione del sistema operativo della data locale e dell'ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="dc69c-335">Operating system version of the local date and time-of-day.</span></span>

<span data-ttu-id="dc69c-336">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-336">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-337">**Impostazioni locali**</span><span class="sxs-lookup"><span data-stu-id="dc69c-337">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-338">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-340">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| National Language Support Functions \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ ILANGUAGE")</span><span class="sxs-lookup"><span data-stu-id="dc69c-340">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|National Language Support Functions\|[**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)\|LOCALE\_ILANGUAGE")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-341">Identificatore di lingua utilizzato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-341">Language identifier used by the operating system.</span></span> <span data-ttu-id="dc69c-342">Un identificatore di lingua è un'abbreviazione numerica internazionale standard per un paese/area geografica.</span><span class="sxs-lookup"><span data-stu-id="dc69c-342">A language identifier is a standard international numeric abbreviation for a country/region.</span></span> <span data-ttu-id="dc69c-343">Ogni lingua dispone di un identificatore di lingua univoco (LANGID), un valore a 16 bit costituito da un identificatore di lingua principale e un identificatore della lingua secondaria.</span><span class="sxs-lookup"><span data-stu-id="dc69c-343">Each language has a unique language identifier (LANGID), a 16-bit value that consists of a primary language identifier and a secondary language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-344">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="dc69c-344">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-347">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-347">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-348">Nome del produttore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-348">Name of the operating system manufacturer.</span></span> <span data-ttu-id="dc69c-349">Per i sistemi basati su Windows, questo valore è "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="dc69c-349">For Windows-based systems, this value is "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-350">**MaxNumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="dc69c-350">**MaxNumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-351">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-353">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Host IETF-risorse-MIB. hrSystemMaxProcesses ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-353">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemMaxProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-354">Numero massimo di contesti di processo che il sistema operativo può supportare.</span><span class="sxs-lookup"><span data-stu-id="dc69c-354">Maximum number of process contexts the operating system can support.</span></span> <span data-ttu-id="dc69c-355">Il valore predefinito impostato dal provider è 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="dc69c-355">The default value set by the provider is 4294967295 (0xFFFFFFFF).</span></span> <span data-ttu-id="dc69c-356">Se non è presente alcun valore massimo fisso, il valore deve essere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-356">If there is no fixed maximum, the value should be 0 (zero).</span></span> <span data-ttu-id="dc69c-357">Nei sistemi con un valore massimo fisso, questo oggetto può aiutare a diagnosticare gli errori che si verificano quando viene raggiunto il valore massimo, se sconosciuto, immettere 4294967295 (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="dc69c-357">On systems that have a fixed maximum, this object can help diagnose failures that occur when the maximum is reached—if unknown, enter 4294967295 (0xFFFFFFFF).</span></span>

<span data-ttu-id="dc69c-358">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-358">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-359">**MaxProcessMemorySize**</span><span class="sxs-lookup"><span data-stu-id="dc69c-359">**MaxProcessMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-360">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-362">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-362">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-363">Numero massimo, in kilobyte, della memoria che può essere allocata a un processo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-363">Maximum number, in kilobytes, of memory that can be allocated to a process.</span></span> <span data-ttu-id="dc69c-364">Per i sistemi operativi senza memoria virtuale, questo valore è in genere uguale alla quantità totale di memoria fisica meno la memoria usata dal BIOS e dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-364">For operating systems with no virtual memory, typically this value is equal to the total amount of physical memory minus the memory used by the BIOS and the operating system.</span></span> <span data-ttu-id="dc69c-365">Per alcuni sistemi operativi, questo valore può essere infinito, nel qual caso è necessario immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-365">For some operating systems, this value may be infinity, in which case 0 (zero) should be entered.</span></span> <span data-ttu-id="dc69c-366">In altri casi, questo valore può essere una costante, ad esempio 2G o 4G.</span><span class="sxs-lookup"><span data-stu-id="dc69c-366">In other cases, this value could be a constant, for example, 2G or 4G.</span></span>

<span data-ttu-id="dc69c-367">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-368">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-368">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-369">**MUILanguages**</span><span class="sxs-lookup"><span data-stu-id="dc69c-369">**MUILanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-370">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dc69c-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-372">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-372">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-373">Lingue Multilingual User Interface Pack (MUI Pack) installate nel computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-373">Multilingual User Interface Pack (MUI Pack ) languages installed on the computer.</span></span> <span data-ttu-id="dc69c-374">Ad esempio, "en-US".</span><span class="sxs-lookup"><span data-stu-id="dc69c-374">For example, "en-us".</span></span> <span data-ttu-id="dc69c-375">MUI Pack lingue sono file di risorse che possono essere installati nella versione in lingua inglese del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-375">MUI Pack languages are resource files that can be installed on the English version of the operating system.</span></span> <span data-ttu-id="dc69c-376">Quando viene installata una MUI Pack, è possibile modificare la lingua dell'interfaccia utente in una delle 33 lingue supportate.</span><span class="sxs-lookup"><span data-stu-id="dc69c-376">When an MUI Pack is installed, you can can change the user interface language to one of 33 supported languages.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-377">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dc69c-377">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-378">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-378">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-380">Istanza del sistema operativo all'interno di un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-380">Operating system instance within a computer system.</span></span>

<span data-ttu-id="dc69c-381">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-381">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-382">**NumberOfLicensedUsers**</span><span class="sxs-lookup"><span data-stu-id="dc69c-382">**NumberOfLicensedUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-383">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-383">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-385">Numero di licenze utente per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-385">Number of user licenses for the operating system.</span></span> <span data-ttu-id="dc69c-386">Se illimitato, immettere 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-386">If unlimited, enter 0 (zero).</span></span> <span data-ttu-id="dc69c-387">Se è sconosciuto, immettere-1.</span><span class="sxs-lookup"><span data-stu-id="dc69c-387">If unknown, enter -1.</span></span>

<span data-ttu-id="dc69c-388">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-388">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-389">**NumberOfProcesses**</span><span class="sxs-lookup"><span data-stu-id="dc69c-389">**NumberOfProcesses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-390">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-392">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Host IETF-risorse-MIB. hrSystemProcesses ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-392">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemProcesses")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-393">Numero di contesti di processo attualmente caricati o in esecuzione nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-393">Number of process contexts currently loaded or running on the operating system.</span></span>

<span data-ttu-id="dc69c-394">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-394">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-395">**NumberOfUsers**</span><span class="sxs-lookup"><span data-stu-id="dc69c-395">**NumberOfUsers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-396">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-396">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-398">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. \|Host IETF-risorse-MIB. hrSystemNumUsers ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-398">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrSystemNumUsers")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-399">Numero di sessioni utente per le quali il sistema operativo archivia attualmente le informazioni sullo stato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-399">Number of user sessions for which the operating system is storing state information currently.</span></span>

<span data-ttu-id="dc69c-400">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-400">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-401">**OperatingSystemSKU**</span><span class="sxs-lookup"><span data-stu-id="dc69c-401">**OperatingSystemSKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-402">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-402">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-404">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-404">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-405">Numero di unità di supporto (SKU) per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-405">Stock Keeping Unit (SKU) number for the operating system.</span></span> <span data-ttu-id="dc69c-406">Questi valori corrispondono alle costanti \**Product \_ \** _ definite in Winnt. h utilizzate con la funzione [_ *GetProductInfo* \*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="dc69c-406">These values are the same as the \**PRODUCT\_\** _ constants defined in WinNT.h that are used with the [_ *GetProductInfo*\*](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span>

<span data-ttu-id="dc69c-407">Nell'elenco seguente sono elencati i valori di SKU possibili.</span><span class="sxs-lookup"><span data-stu-id="dc69c-407">The following list lists possible SKU values.</span></span>

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span data-ttu-id="dc69c-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Prodotto \_ Non definito** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-408"><span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**PRODUCT\_UNDEFINED** (0)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-409">Non definito</span><span class="sxs-lookup"><span data-stu-id="dc69c-409">Undefined</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span data-ttu-id="dc69c-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Prodotto \_ ULTIMATE** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-410"><span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**PRODUCT\_ULTIMATE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-411">Ultimate Edition, ad esempio Windows Vista Ultimate.</span><span class="sxs-lookup"><span data-stu-id="dc69c-411">Ultimate Edition, e.g. Windows Vista Ultimate.</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span data-ttu-id="dc69c-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Prodotto \_ HOME \_ Basic** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-412"><span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**PRODUCT\_HOME\_BASIC** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-413">Home Basic Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-413">Home Basic Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span data-ttu-id="dc69c-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Prodotto \_ HOME \_ Premium** (3)</span><span class="sxs-lookup"><span data-stu-id="dc69c-414"><span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**PRODUCT\_HOME\_PREMIUM** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-415">Home Premium Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-415">Home Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span data-ttu-id="dc69c-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Prodotto \_ ENTERPRISE** (4)</span><span class="sxs-lookup"><span data-stu-id="dc69c-416"><span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**PRODUCT\_ENTERPRISE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-417">Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-417">Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span data-ttu-id="dc69c-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Prodotto \_ BUSINESS** (6)</span><span class="sxs-lookup"><span data-stu-id="dc69c-418"><span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**PRODUCT\_BUSINESS** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-419">Business Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-419">Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span data-ttu-id="dc69c-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Prodotto \_ \_Server standard** (7)</span><span class="sxs-lookup"><span data-stu-id="dc69c-420"><span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**PRODUCT\_STANDARD\_SERVER** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-421">Windows Server Standard Edition (installazione esperienza desktop)</span><span class="sxs-lookup"><span data-stu-id="dc69c-421">Windows Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span data-ttu-id="dc69c-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Prodotto \_ \_Server Datacenter** (8)</span><span class="sxs-lookup"><span data-stu-id="dc69c-422"><span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**PRODUCT\_DATACENTER\_SERVER** (8)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-423">Windows Server Datacenter Edition (installazione esperienza desktop)</span><span class="sxs-lookup"><span data-stu-id="dc69c-423">Windows Server Datacenter Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span data-ttu-id="dc69c-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Prodotto \_ \_Server SMALLBUSINESS** (9)</span><span class="sxs-lookup"><span data-stu-id="dc69c-424"><span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**PRODUCT\_SMALLBUSINESS\_SERVER** (9)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-425">Edizione di Small Business Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-425">Small Business Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span data-ttu-id="dc69c-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Prodotto \_ \_Server aziendale** (10)</span><span class="sxs-lookup"><span data-stu-id="dc69c-426"><span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**PRODUCT\_ENTERPRISE\_SERVER** (10)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-427">Edizione Enterprise Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-427">Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span data-ttu-id="dc69c-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Prodotto \_ STARTER** (11)</span><span class="sxs-lookup"><span data-stu-id="dc69c-428"><span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**PRODUCT\_STARTER** (11)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-429"> Starter Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-429">Starter Edition</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span data-ttu-id="dc69c-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Prodotto \_ Datacenter \_ server \_ Core** (12)</span><span class="sxs-lookup"><span data-stu-id="dc69c-430"><span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE** (12)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-431">Edizione core Datacenter Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-431">Datacenter Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span data-ttu-id="dc69c-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Prodotto \_ \_Server \_ core standard** (13)</span><span class="sxs-lookup"><span data-stu-id="dc69c-432"><span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**PRODUCT\_STANDARD\_SERVER\_CORE** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-433">Edizione server core standard</span><span class="sxs-lookup"><span data-stu-id="dc69c-433">Standard Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span data-ttu-id="dc69c-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Prodotto \_ ENTERPRISE \_ server \_ Core** (14)</span><span class="sxs-lookup"><span data-stu-id="dc69c-434"><span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-435">Enterprise Server Core Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-435">Enterprise Server Core Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span data-ttu-id="dc69c-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Prodotto \_ \_Server Web** (17)</span><span class="sxs-lookup"><span data-stu-id="dc69c-436"><span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**PRODUCT\_WEB\_SERVER** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-437">Edizione server Web</span><span class="sxs-lookup"><span data-stu-id="dc69c-437">Web Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span data-ttu-id="dc69c-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Prodotto \_ \_Server Home** (19)</span><span class="sxs-lookup"><span data-stu-id="dc69c-438"><span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**PRODUCT\_HOME\_SERVER** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-439">Edizione Home Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-439">Home Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span data-ttu-id="dc69c-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Prodotto \_ \_ \_ Server di archiviazione Express** (20)</span><span class="sxs-lookup"><span data-stu-id="dc69c-440"><span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-441">Edizione di storage Express Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-441">Storage Express Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span data-ttu-id="dc69c-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Prodotto \_ \_ \_ Server standard di archiviazione** (21)</span><span class="sxs-lookup"><span data-stu-id="dc69c-442"><span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-443">Windows Storage Server Standard Edition (installazione esperienza desktop)</span><span class="sxs-lookup"><span data-stu-id="dc69c-443">Windows Storage Server Standard Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span data-ttu-id="dc69c-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Prodotto \_ STORAGE \_ Workgroup \_ server** (22)</span><span class="sxs-lookup"><span data-stu-id="dc69c-444"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER** (22)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-445">Windows Storage Server Workgroup Edition (installazione esperienza desktop)</span><span class="sxs-lookup"><span data-stu-id="dc69c-445">Windows Storage Server Workgroup Edition (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span data-ttu-id="dc69c-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Prodotto \_ STORAGE \_ Enterprise \_ server** (23)</span><span class="sxs-lookup"><span data-stu-id="dc69c-446"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER** (23)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-447">Archiviazione Enterprise Server Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-447">Storage Enterprise Server Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span data-ttu-id="dc69c-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Prodotto \_ SERVER \_ per \_ SMALLBUSINESS** (24)</span><span class="sxs-lookup"><span data-stu-id="dc69c-448"><span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**PRODUCT\_SERVER\_FOR\_SMALLBUSINESS** (24)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-449">Server per Small Business Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-449">Server For Small Business Edition</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span data-ttu-id="dc69c-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Prodotto \_ \_Server SMALLBUSINESS \_ Premium** (25)</span><span class="sxs-lookup"><span data-stu-id="dc69c-450"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM** (25)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-451">Small Business Server Premium Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-451">Small Business Server Premium Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span data-ttu-id="dc69c-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Prodotto \_ ENTERPRISE \_ N** (27)</span><span class="sxs-lookup"><span data-stu-id="dc69c-452"><span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**PRODUCT\_ENTERPRISE\_N** (27)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-453">Windows Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-453">Windows Enterprise Edition</span></span>

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span data-ttu-id="dc69c-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Prodotto \_ ULTIMATE \_ N** (28)</span><span class="sxs-lookup"><span data-stu-id="dc69c-454"><span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**PRODUCT\_ULTIMATE\_N** (28)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-455">Edizione di Windows Ultimate</span><span class="sxs-lookup"><span data-stu-id="dc69c-455">Windows Ultimate Edition</span></span>

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span data-ttu-id="dc69c-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Prodotto \_ \_Server \_ Core Web** (29)</span><span class="sxs-lookup"><span data-stu-id="dc69c-456"><span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**PRODUCT\_WEB\_SERVER\_CORE** (29)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-457">Windows Server Web Server Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-457">Windows Server Web Server Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span data-ttu-id="dc69c-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Prodotto \_ \_Server standard \_ V** (36)</span><span class="sxs-lookup"><span data-stu-id="dc69c-458"><span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**PRODUCT\_STANDARD\_SERVER\_V** (36)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-459">Windows Server Standard Edition senza Hyper-V</span><span class="sxs-lookup"><span data-stu-id="dc69c-459">Windows Server Standard Edition without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span data-ttu-id="dc69c-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Prodotto \_ Datacenter \_ server \_ V** (37)</span><span class="sxs-lookup"><span data-stu-id="dc69c-460"><span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**PRODUCT\_DATACENTER\_SERVER\_V** (37)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-461">Windows Server Datacenter Edition senza Hyper-V (installazione completa)</span><span class="sxs-lookup"><span data-stu-id="dc69c-461">Windows Server Datacenter Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span data-ttu-id="dc69c-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Prodotto \_ ENTERPRISE \_ server \_ V** (38)</span><span class="sxs-lookup"><span data-stu-id="dc69c-462"><span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_V** (38)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-463">Windows Server Enterprise Edition senza Hyper-V (installazione completa)</span><span class="sxs-lookup"><span data-stu-id="dc69c-463">Windows Server Enterprise Edition without Hyper-V (full installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span data-ttu-id="dc69c-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Prodotto \_ Datacenter \_ server \_ Core \_ V** (39)</span><span class="sxs-lookup"><span data-stu-id="dc69c-464"><span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**PRODUCT\_DATACENTER\_SERVER\_CORE\_V** (39)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-465">Windows Server Datacenter Edition senza Hyper-V (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-465">Windows Server Datacenter Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span data-ttu-id="dc69c-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Prodotto \_ \_Server \_ core standard \_ V** (40)</span><span class="sxs-lookup"><span data-stu-id="dc69c-466"><span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**PRODUCT\_STANDARD\_SERVER\_CORE\_V** (40)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-467">Windows Server Standard Edition senza Hyper-V (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-467">Windows Server Standard Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span data-ttu-id="dc69c-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Prodotto \_ ENTERPRISE \_ server \_ Core \_ V** (41)</span><span class="sxs-lookup"><span data-stu-id="dc69c-468"><span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**PRODUCT\_ENTERPRISE\_SERVER\_CORE\_V** (41)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-469">Windows Server Enterprise Edition senza Hyper-V (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-469">Windows Server Enterprise Edition without Hyper-V (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span data-ttu-id="dc69c-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Prodotto \_ HYPERV** (42)</span><span class="sxs-lookup"><span data-stu-id="dc69c-470"><span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**PRODUCT\_HYPERV** (42)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-471">Microsoft Hyper-V Server</span><span class="sxs-lookup"><span data-stu-id="dc69c-471">Microsoft Hyper-V Server</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span data-ttu-id="dc69c-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Prodotto \_ STORAGE \_ Express \_ server \_ Core** (43)</span><span class="sxs-lookup"><span data-stu-id="dc69c-472"><span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**PRODUCT\_STORAGE\_EXPRESS\_SERVER\_CORE** (43)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-473">Storage Server Express Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-473">Storage Server Express Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span data-ttu-id="dc69c-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Prodotto \_ ARCHIVIAZIONE \_ standard \_ server \_ Core** (44)</span><span class="sxs-lookup"><span data-stu-id="dc69c-474"><span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**PRODUCT\_STORAGE\_STANDARD\_SERVER\_CORE** (44)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-475">Storage Server Standard Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-475">Storage Server Standard Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span data-ttu-id="dc69c-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Prodotto \_ STORAGE \_ Workgroup \_ server \_ Core** (45)</span><span class="sxs-lookup"><span data-stu-id="dc69c-476"><span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**PRODUCT\_STORAGE\_WORKGROUP\_SERVER\_CORE** (45)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-477">Storage Server Workgroup Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-477">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span data-ttu-id="dc69c-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Prodotto \_ STORAGE \_ Enterprise \_ server \_ Core** (46)</span><span class="sxs-lookup"><span data-stu-id="dc69c-478"><span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**PRODUCT\_STORAGE\_ENTERPRISE\_SERVER\_CORE** (46)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-479">Storage Server Workgroup Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-479">Storage Server Workgroup Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span data-ttu-id="dc69c-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Prodotto \_ PROFESSIONAL** (48)</span><span class="sxs-lookup"><span data-stu-id="dc69c-480"><span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**PRODUCT\_PROFESSIONAL** (48)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-481">Windows Professional</span><span class="sxs-lookup"><span data-stu-id="dc69c-481">Windows Professional</span></span>

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span data-ttu-id="dc69c-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Prodotto \_ \_ \_ Server della soluzione SB** (50)</span><span class="sxs-lookup"><span data-stu-id="dc69c-482"><span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**PRODUCT\_SB\_SOLUTION\_SERVER** (50)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-483">Windows Server Essentials (installazione esperienza desktop)</span><span class="sxs-lookup"><span data-stu-id="dc69c-483">Windows Server Essentials (Desktop Experience installation)</span></span>

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span data-ttu-id="dc69c-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Prodotto \_ \_Server SMALLBUSINESS \_ Premium \_ Core** (63)</span><span class="sxs-lookup"><span data-stu-id="dc69c-484"><span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**PRODUCT\_SMALLBUSINESS\_SERVER\_PREMIUM\_CORE** (63)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-485">Small Business Server Premium (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-485">Small Business Server Premium (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span data-ttu-id="dc69c-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Prodotto \_ \_Server cluster \_ V** (64)</span><span class="sxs-lookup"><span data-stu-id="dc69c-486"><span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**PRODUCT\_CLUSTER\_SERVER\_V** (64)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-487">Windows Compute Cluster Server senza Hyper-V</span><span class="sxs-lookup"><span data-stu-id="dc69c-487">Windows Compute Cluster Server without Hyper-V</span></span>

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span data-ttu-id="dc69c-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Prodotto \_ \_ARM core** (97)</span><span class="sxs-lookup"><span data-stu-id="dc69c-488"><span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**PRODUCT\_CORE\_ARM** (97)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-489">Windows RT</span><span class="sxs-lookup"><span data-stu-id="dc69c-489">Windows RT</span></span>

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span data-ttu-id="dc69c-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**Prodotto \_ CORE** (101)</span><span class="sxs-lookup"><span data-stu-id="dc69c-490"><span id="PRODUCT_CORE"></span><span id="product_core"></span>**PRODUCT\_CORE** (101)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-491">Home page di Windows</span><span class="sxs-lookup"><span data-stu-id="dc69c-491">Windows Home</span></span>

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span data-ttu-id="dc69c-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Prodotto \_ \_WMC professionale** (103)</span><span class="sxs-lookup"><span data-stu-id="dc69c-492"><span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**PRODUCT\_PROFESSIONAL\_WMC** (103)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-493">Windows Professional con Media Center</span><span class="sxs-lookup"><span data-stu-id="dc69c-493">Windows Professional with Media Center</span></span>

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span data-ttu-id="dc69c-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Prodotto \_ MOBILE \_ Core** (104)</span><span class="sxs-lookup"><span data-stu-id="dc69c-494"><span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**PRODUCT\_MOBILE\_CORE** (104)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-495">Windows Mobile</span><span class="sxs-lookup"><span data-stu-id="dc69c-495">Windows Mobile</span></span>

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span data-ttu-id="dc69c-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Prodotto \_ IOTUAP** (123)</span><span class="sxs-lookup"><span data-stu-id="dc69c-496"><span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**PRODUCT\_IOTUAP** (123)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-497">Componenti di base di Windows (Internet delle cose)</span><span class="sxs-lookup"><span data-stu-id="dc69c-497">Windows IoT (Internet of Things) Core</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span data-ttu-id="dc69c-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Prodotto \_ \_Nano \_ server del data center** (143)</span><span class="sxs-lookup"><span data-stu-id="dc69c-498"><span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**PRODUCT\_DATACENTER\_NANO\_SERVER** (143)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-499">Windows Server Datacenter Edition (installazione di nano Server)</span><span class="sxs-lookup"><span data-stu-id="dc69c-499">Windows Server Datacenter Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span data-ttu-id="dc69c-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Prodotto \_ \_Nano \_ Server STANDARD** (144)</span><span class="sxs-lookup"><span data-stu-id="dc69c-500"><span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**PRODUCT\_STANDARD\_NANO\_SERVER** (144)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-501">Windows Server Standard Edition (installazione di nano Server)</span><span class="sxs-lookup"><span data-stu-id="dc69c-501">Windows Server Standard Edition (Nano Server installation)</span></span>

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span data-ttu-id="dc69c-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Prodotto \_ Data CENTER \_ WS \_ server \_ Core** (147)</span><span class="sxs-lookup"><span data-stu-id="dc69c-502"><span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**PRODUCT\_DATACENTER\_WS\_SERVER\_CORE** (147)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-503">Windows Server Datacenter Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-503">Windows Server Datacenter Edition (Server Core installation)</span></span>

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span data-ttu-id="dc69c-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Prodotto \_ \_WS \_ server \_ CORE standard** (148)</span><span class="sxs-lookup"><span data-stu-id="dc69c-504"><span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**PRODUCT\_STANDARD\_WS\_SERVER\_CORE** (148)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-505">Windows Server Standard Edition (installazione Server Core)</span><span class="sxs-lookup"><span data-stu-id="dc69c-505">Windows Server Standard Edition (Server Core installation)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-506">**Organizzazione**</span><span class="sxs-lookup"><span data-stu-id="dc69c-506">**Organization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-507">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-508">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-508">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-509">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")</span><span class="sxs-lookup"><span data-stu-id="dc69c-509">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows\\\\CurrentVersion\|RegisteredOrganization")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-510">Nome della società per l'utente registrato del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-510">Company name for the registered user of the operating system.</span></span>

<span data-ttu-id="dc69c-511">Esempio: "Microsoft Corporation"</span><span class="sxs-lookup"><span data-stu-id="dc69c-511">Example: "Microsoft Corporation"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-512">**OSArchitecture**</span><span class="sxs-lookup"><span data-stu-id="dc69c-512">**OSArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-513">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-513">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-515">Architettura del sistema operativo, invece del processore.</span><span class="sxs-lookup"><span data-stu-id="dc69c-515">Architecture of the operating system, as opposed to the processor.</span></span> <span data-ttu-id="dc69c-516">Questa proprietà può essere localizzata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-516">This property can be localized.</span></span>

<span data-ttu-id="dc69c-517">Esempio: 32 bit</span><span class="sxs-lookup"><span data-stu-id="dc69c-517">Example: 32-bit</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-518">**OSLanguage**</span><span class="sxs-lookup"><span data-stu-id="dc69c-518">**OSLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-519">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-519">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-520">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-520">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-521">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| impostazioni \\ \\ \\ \\ locali internazionali del pannello di controllo" \| )</span><span class="sxs-lookup"><span data-stu-id="dc69c-521">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|DEFAULT\\\\Control Panel\\\\International\|Locale")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-522">Versione in lingua del sistema operativo installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-522">Language version of the operating system installed.</span></span> <span data-ttu-id="dc69c-523">Nell'elenco seguente sono elencati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="dc69c-523">The following list lists the possible values.</span></span> <span data-ttu-id="dc69c-524">Esempio: 0x0807 (tedesco, Svizzera).</span><span class="sxs-lookup"><span data-stu-id="dc69c-524">Example: 0x0807 (German, Switzerland).</span></span>

<dt>

<span data-ttu-id="dc69c-525">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-525">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-526">Arabo</span><span class="sxs-lookup"><span data-stu-id="dc69c-526">Arabic</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-527">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="dc69c-527">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-528">Cinese (semplificato) – Cina</span><span class="sxs-lookup"><span data-stu-id="dc69c-528">Chinese (Simplified)– China</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-529">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="dc69c-529">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-530">Inglese</span><span class="sxs-lookup"><span data-stu-id="dc69c-530">English</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-531">1025 (0x401)</span><span class="sxs-lookup"><span data-stu-id="dc69c-531">1025 (0x401)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-532">Arabo – Arabia Saudita</span><span class="sxs-lookup"><span data-stu-id="dc69c-532">Arabic – Saudi Arabia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-533">1026 (0x402)</span><span class="sxs-lookup"><span data-stu-id="dc69c-533">1026 (0x402)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-534">Bulgaro</span><span class="sxs-lookup"><span data-stu-id="dc69c-534">Bulgarian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-535">1027 (0x403)</span><span class="sxs-lookup"><span data-stu-id="dc69c-535">1027 (0x403)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-536">Catalano</span><span class="sxs-lookup"><span data-stu-id="dc69c-536">Catalan</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-537">1028 (0x404)</span><span class="sxs-lookup"><span data-stu-id="dc69c-537">1028 (0x404)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-538">Cinese (tradizionale) – Taiwan</span><span class="sxs-lookup"><span data-stu-id="dc69c-538">Chinese (Traditional) – Taiwan</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-539">1029 (0x405)</span><span class="sxs-lookup"><span data-stu-id="dc69c-539">1029 (0x405)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-540">Ceco</span><span class="sxs-lookup"><span data-stu-id="dc69c-540">Czech</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-541">1030 (0x406)</span><span class="sxs-lookup"><span data-stu-id="dc69c-541">1030 (0x406)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-542">Danese</span><span class="sxs-lookup"><span data-stu-id="dc69c-542">Danish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-543">1031 (0x407)</span><span class="sxs-lookup"><span data-stu-id="dc69c-543">1031 (0x407)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-544">Tedesco (Germania)</span><span class="sxs-lookup"><span data-stu-id="dc69c-544">German – Germany</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-545">1032 (0x408)</span><span class="sxs-lookup"><span data-stu-id="dc69c-545">1032 (0x408)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-546">Greco</span><span class="sxs-lookup"><span data-stu-id="dc69c-546">Greek</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-547">1033 (0x409)</span><span class="sxs-lookup"><span data-stu-id="dc69c-547">1033 (0x409)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-548">Inglese – Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="dc69c-548">English – United States</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-549">1034 (0x40A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-549">1034 (0x40A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-550">Spagnolo – ordinamento tradizionale</span><span class="sxs-lookup"><span data-stu-id="dc69c-550">Spanish – Traditional Sort</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-551">1035 (0x40B)</span><span class="sxs-lookup"><span data-stu-id="dc69c-551">1035 (0x40B)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-552">Finlandese</span><span class="sxs-lookup"><span data-stu-id="dc69c-552">Finnish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-553">1036 (0x40C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-553">1036 (0x40C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-554">Francese (Francia)</span><span class="sxs-lookup"><span data-stu-id="dc69c-554">French – France</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-555">1037 (0x40D)</span><span class="sxs-lookup"><span data-stu-id="dc69c-555">1037 (0x40D)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-556">Ebraico</span><span class="sxs-lookup"><span data-stu-id="dc69c-556">Hebrew</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-557">1038 (0x40E)</span><span class="sxs-lookup"><span data-stu-id="dc69c-557">1038 (0x40E)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-558">Ungherese</span><span class="sxs-lookup"><span data-stu-id="dc69c-558">Hungarian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-559">1039 (0x40F)</span><span class="sxs-lookup"><span data-stu-id="dc69c-559">1039 (0x40F)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-560">Islandese</span><span class="sxs-lookup"><span data-stu-id="dc69c-560">Icelandic</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-561">1040 (0x410)</span><span class="sxs-lookup"><span data-stu-id="dc69c-561">1040 (0x410)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-562">Italiano (Italia)</span><span class="sxs-lookup"><span data-stu-id="dc69c-562">Italian – Italy</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-563">1041 (0x411)</span><span class="sxs-lookup"><span data-stu-id="dc69c-563">1041 (0x411)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-564">Giapponese</span><span class="sxs-lookup"><span data-stu-id="dc69c-564">Japanese</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-565">1042 (0x412)</span><span class="sxs-lookup"><span data-stu-id="dc69c-565">1042 (0x412)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-566">Coreano</span><span class="sxs-lookup"><span data-stu-id="dc69c-566">Korean</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-567">1043 (0x413)</span><span class="sxs-lookup"><span data-stu-id="dc69c-567">1043 (0x413)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-568">Olandese (Paesi Bassi)</span><span class="sxs-lookup"><span data-stu-id="dc69c-568">Dutch – Netherlands</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-569">1044 (0x414)</span><span class="sxs-lookup"><span data-stu-id="dc69c-569">1044 (0x414)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-570">Norvegese – Bokmal</span><span class="sxs-lookup"><span data-stu-id="dc69c-570">Norwegian – Bokmal</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-571">1045 (0x415)</span><span class="sxs-lookup"><span data-stu-id="dc69c-571">1045 (0x415)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-572">Polacco</span><span class="sxs-lookup"><span data-stu-id="dc69c-572">Polish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-573">1046 (0x416)</span><span class="sxs-lookup"><span data-stu-id="dc69c-573">1046 (0x416)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-574">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="dc69c-574">Portuguese – Brazil</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-575">1047 (0x417)</span><span class="sxs-lookup"><span data-stu-id="dc69c-575">1047 (0x417)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-576">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="dc69c-576">Rhaeto-Romanic</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-577">1048 (0x418)</span><span class="sxs-lookup"><span data-stu-id="dc69c-577">1048 (0x418)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-578">Romeno</span><span class="sxs-lookup"><span data-stu-id="dc69c-578">Romanian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-579">1049 (0x419)</span><span class="sxs-lookup"><span data-stu-id="dc69c-579">1049 (0x419)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-580">Russo</span><span class="sxs-lookup"><span data-stu-id="dc69c-580">Russian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-581">1050 (0x41A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-581">1050 (0x41A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-582">Croato</span><span class="sxs-lookup"><span data-stu-id="dc69c-582">Croatian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-583">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="dc69c-583">1051 (0x41B)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-584">Slovacco</span><span class="sxs-lookup"><span data-stu-id="dc69c-584">Slovak</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-585">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-585">1052 (0x41C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-586">Albanese</span><span class="sxs-lookup"><span data-stu-id="dc69c-586">Albanian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-587">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="dc69c-587">1053 (0x41D)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-588">Svedese</span><span class="sxs-lookup"><span data-stu-id="dc69c-588">Swedish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-589">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="dc69c-589">1054 (0x41E)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-590">Thai</span><span class="sxs-lookup"><span data-stu-id="dc69c-590">Thai</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-591">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="dc69c-591">1055 (0x41F)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-592">Turco</span><span class="sxs-lookup"><span data-stu-id="dc69c-592">Turkish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-593">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="dc69c-593">1056 (0x420)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-594">Urdu</span><span class="sxs-lookup"><span data-stu-id="dc69c-594">Urdu</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-595">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="dc69c-595">1057 (0x421)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-596">Indonesiano</span><span class="sxs-lookup"><span data-stu-id="dc69c-596">Indonesian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-597">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="dc69c-597">1058 (0x422)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-598">Ucraino</span><span class="sxs-lookup"><span data-stu-id="dc69c-598">Ukrainian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-599">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="dc69c-599">1059 (0x423)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-600">Bielorusso</span><span class="sxs-lookup"><span data-stu-id="dc69c-600">Belarusian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-601">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="dc69c-601">1060 (0x424)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-602">Sloveno</span><span class="sxs-lookup"><span data-stu-id="dc69c-602">Slovenian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-603">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="dc69c-603">1061 (0x425)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-604">Estone</span><span class="sxs-lookup"><span data-stu-id="dc69c-604">Estonian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-605">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="dc69c-605">1062 (0x426)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-606">Lettone</span><span class="sxs-lookup"><span data-stu-id="dc69c-606">Latvian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-607">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="dc69c-607">1063 (0x427)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-608">Lituano</span><span class="sxs-lookup"><span data-stu-id="dc69c-608">Lithuanian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-609">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="dc69c-609">1065 (0x429)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-610">Persiano</span><span class="sxs-lookup"><span data-stu-id="dc69c-610">Persian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-611">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-611">1066 (0x42A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-612">Vietnamita</span><span class="sxs-lookup"><span data-stu-id="dc69c-612">Vietnamese</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-613">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="dc69c-613">1069 (0x42D)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-614">Basco (Basco)</span><span class="sxs-lookup"><span data-stu-id="dc69c-614">Basque (Basque)</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-615">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="dc69c-615">1070 (0x42E)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-616">Serbo</span><span class="sxs-lookup"><span data-stu-id="dc69c-616">Serbian</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-617">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="dc69c-617">1071 (0x42F)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-618">Macedone (Macedonia settentrionale)</span><span class="sxs-lookup"><span data-stu-id="dc69c-618">Macedonian (North Macedonia)</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-619">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="dc69c-619">1072 (0x430)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-620">Sutu</span><span class="sxs-lookup"><span data-stu-id="dc69c-620">Sutu</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-621">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="dc69c-621">1073 (0x431)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-622">Tsonga</span><span class="sxs-lookup"><span data-stu-id="dc69c-622">Tsonga</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-623">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="dc69c-623">1074 (0x432)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-624">Tswana</span><span class="sxs-lookup"><span data-stu-id="dc69c-624">Tswana</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-625">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="dc69c-625">1076 (0x434)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-626">Xhosa</span><span class="sxs-lookup"><span data-stu-id="dc69c-626">Xhosa</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-627">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="dc69c-627">1077 (0x435)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-628">Zulù</span><span class="sxs-lookup"><span data-stu-id="dc69c-628">Zulu</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-629">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="dc69c-629">1078 (0x436)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-630">Afrikaans</span><span class="sxs-lookup"><span data-stu-id="dc69c-630">Afrikaans</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-631">1080 (nell'0x438)</span><span class="sxs-lookup"><span data-stu-id="dc69c-631">1080 (0x438)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-632">Faeroese</span><span class="sxs-lookup"><span data-stu-id="dc69c-632">Faeroese</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-633">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="dc69c-633">1081 (0x439)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-634">Hindi</span><span class="sxs-lookup"><span data-stu-id="dc69c-634">Hindi</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-635">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-635">1082 (0x43A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-636">Maltese</span><span class="sxs-lookup"><span data-stu-id="dc69c-636">Maltese</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-637">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-637">1084 (0x43C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-638">Gaelico scozzese (Regno Unito)</span><span class="sxs-lookup"><span data-stu-id="dc69c-638">Scottish Gaelic (United Kingdom)</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-639">1085 (0x43D)</span><span class="sxs-lookup"><span data-stu-id="dc69c-639">1085 (0x43D)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-640">Yiddish</span><span class="sxs-lookup"><span data-stu-id="dc69c-640">Yiddish</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-641">1086 (0x43E)</span><span class="sxs-lookup"><span data-stu-id="dc69c-641">1086 (0x43E)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-642">Malese – Malaysia</span><span class="sxs-lookup"><span data-stu-id="dc69c-642">Malay – Malaysia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-643">2049 (0x801)</span><span class="sxs-lookup"><span data-stu-id="dc69c-643">2049 (0x801)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-644">Arabo – Iraq</span><span class="sxs-lookup"><span data-stu-id="dc69c-644">Arabic – Iraq</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-645">2052 (0x804)</span><span class="sxs-lookup"><span data-stu-id="dc69c-645">2052 (0x804)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-646">Cinese (semplificato)-PRC</span><span class="sxs-lookup"><span data-stu-id="dc69c-646">Chinese (Simplified) – PRC</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-647">2055 (0x807)</span><span class="sxs-lookup"><span data-stu-id="dc69c-647">2055 (0x807)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-648">Tedesco – Svizzera</span><span class="sxs-lookup"><span data-stu-id="dc69c-648">German – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-649">2057 (0x809)</span><span class="sxs-lookup"><span data-stu-id="dc69c-649">2057 (0x809)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-650">Inglese – Regno Unito</span><span class="sxs-lookup"><span data-stu-id="dc69c-650">English – United Kingdom</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-651">2058 (0x80A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-651">2058 (0x80A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-652">Spagnolo – Messico</span><span class="sxs-lookup"><span data-stu-id="dc69c-652">Spanish – Mexico</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-653">2060 (0x80C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-653">2060 (0x80C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-654">Francese – Belgio</span><span class="sxs-lookup"><span data-stu-id="dc69c-654">French – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-655">2064 (0x810)</span><span class="sxs-lookup"><span data-stu-id="dc69c-655">2064 (0x810)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-656">Italiano – Svizzera</span><span class="sxs-lookup"><span data-stu-id="dc69c-656">Italian – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-657">2067 (0x813)</span><span class="sxs-lookup"><span data-stu-id="dc69c-657">2067 (0x813)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-658">Olandese – Belgio</span><span class="sxs-lookup"><span data-stu-id="dc69c-658">Dutch – Belgium</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-659">2068 (0x814)</span><span class="sxs-lookup"><span data-stu-id="dc69c-659">2068 (0x814)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-660">Norvegese – Nynorsk</span><span class="sxs-lookup"><span data-stu-id="dc69c-660">Norwegian – Nynorsk</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-661">2070 (0x816)</span><span class="sxs-lookup"><span data-stu-id="dc69c-661">2070 (0x816)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-662">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="dc69c-662">Portuguese – Portugal</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-663">2072 (0x818)</span><span class="sxs-lookup"><span data-stu-id="dc69c-663">2072 (0x818)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-664">Rumeno – Moldova</span><span class="sxs-lookup"><span data-stu-id="dc69c-664">Romanian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-665">2073 (0x819)</span><span class="sxs-lookup"><span data-stu-id="dc69c-665">2073 (0x819)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-666">Russo – Moldova</span><span class="sxs-lookup"><span data-stu-id="dc69c-666">Russian – Moldova</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-667">2074 (0x81A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-667">2074 (0x81A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-668">Serbo – alfabeto latino</span><span class="sxs-lookup"><span data-stu-id="dc69c-668">Serbian – Latin</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-669">2077 (0x81D)</span><span class="sxs-lookup"><span data-stu-id="dc69c-669">2077 (0x81D)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-670">Svedese – Finlandia</span><span class="sxs-lookup"><span data-stu-id="dc69c-670">Swedish – Finland</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-671">3073 (0xC01)</span><span class="sxs-lookup"><span data-stu-id="dc69c-671">3073 (0xC01)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-672">Arabo – Egitto</span><span class="sxs-lookup"><span data-stu-id="dc69c-672">Arabic – Egypt</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-673">3076 (0xC04)</span><span class="sxs-lookup"><span data-stu-id="dc69c-673">3076 (0xC04)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-674">Cinese (tradizionale) – Hong Kong SAR</span><span class="sxs-lookup"><span data-stu-id="dc69c-674">Chinese (Traditional) – Hong Kong SAR</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-675">3079 (0xC07)</span><span class="sxs-lookup"><span data-stu-id="dc69c-675">3079 (0xC07)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-676">Tedesco – Austria</span><span class="sxs-lookup"><span data-stu-id="dc69c-676">German – Austria</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-677">3081 (0xC09)</span><span class="sxs-lookup"><span data-stu-id="dc69c-677">3081 (0xC09)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-678">Inglese – Australia</span><span class="sxs-lookup"><span data-stu-id="dc69c-678">English – Australia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-679">3082 (0xC0A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-679">3082 (0xC0A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-680">Spagnolo – ordinamento internazionale</span><span class="sxs-lookup"><span data-stu-id="dc69c-680">Spanish – International Sort</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-681">3084 (0xC0C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-681">3084 (0xC0C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-682">Francese – Canada</span><span class="sxs-lookup"><span data-stu-id="dc69c-682">French – Canada</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-683">3098 (0xC1A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-683">3098 (0xC1A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-684">Serbo – alfabeto cirillico</span><span class="sxs-lookup"><span data-stu-id="dc69c-684">Serbian – Cyrillic</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-685">4097 (0x1001)</span><span class="sxs-lookup"><span data-stu-id="dc69c-685">4097 (0x1001)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-686">Arabo – Libia</span><span class="sxs-lookup"><span data-stu-id="dc69c-686">Arabic – Libya</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-687">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="dc69c-687">4100 (0x1004)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-688">Cinese (semplificato) – Singapore</span><span class="sxs-lookup"><span data-stu-id="dc69c-688">Chinese (Simplified) – Singapore</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-689">4103 (0x1007)</span><span class="sxs-lookup"><span data-stu-id="dc69c-689">4103 (0x1007)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-690">Tedesco – Lussemburgo</span><span class="sxs-lookup"><span data-stu-id="dc69c-690">German – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-691">4105 (0x1009)</span><span class="sxs-lookup"><span data-stu-id="dc69c-691">4105 (0x1009)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-692">Inglese – Canada</span><span class="sxs-lookup"><span data-stu-id="dc69c-692">English – Canada</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-693">4106 (0x100A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-693">4106 (0x100A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-694">Spagnolo – Guatemala</span><span class="sxs-lookup"><span data-stu-id="dc69c-694">Spanish – Guatemala</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-695">4108 (0x100C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-695">4108 (0x100C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-696">Francese – Svizzera</span><span class="sxs-lookup"><span data-stu-id="dc69c-696">French – Switzerland</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-697">5121 (0x1401)</span><span class="sxs-lookup"><span data-stu-id="dc69c-697">5121 (0x1401)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-698">Arabo – Algeria</span><span class="sxs-lookup"><span data-stu-id="dc69c-698">Arabic – Algeria</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-699">5127 (0x1407)</span><span class="sxs-lookup"><span data-stu-id="dc69c-699">5127 (0x1407)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-700">Tedesco – Liechtenstein</span><span class="sxs-lookup"><span data-stu-id="dc69c-700">German – Liechtenstein</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-701">5129 (0x1409)</span><span class="sxs-lookup"><span data-stu-id="dc69c-701">5129 (0x1409)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-702">Inglese – Nuova Zelanda</span><span class="sxs-lookup"><span data-stu-id="dc69c-702">English – New Zealand</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-703">5130 (0x140A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-703">5130 (0x140A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-704">Spagnolo – Costa Rica</span><span class="sxs-lookup"><span data-stu-id="dc69c-704">Spanish – Costa Rica</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-705">5132 (0x140C)</span><span class="sxs-lookup"><span data-stu-id="dc69c-705">5132 (0x140C)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-706">Francese – Lussemburgo</span><span class="sxs-lookup"><span data-stu-id="dc69c-706">French – Luxembourg</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-707">6145 (0x1801)</span><span class="sxs-lookup"><span data-stu-id="dc69c-707">6145 (0x1801)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-708">Arabo – Marocco</span><span class="sxs-lookup"><span data-stu-id="dc69c-708">Arabic – Morocco</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-709">6153 (0x1809)</span><span class="sxs-lookup"><span data-stu-id="dc69c-709">6153 (0x1809)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-710">Inglese – Irlanda</span><span class="sxs-lookup"><span data-stu-id="dc69c-710">English – Ireland</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-711">6154 (0x180A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-711">6154 (0x180A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-712">Spagnolo – Panama</span><span class="sxs-lookup"><span data-stu-id="dc69c-712">Spanish – Panama</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-713">7169 (0x1C01)</span><span class="sxs-lookup"><span data-stu-id="dc69c-713">7169 (0x1C01)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-714">Arabo – Tunisia</span><span class="sxs-lookup"><span data-stu-id="dc69c-714">Arabic – Tunisia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-715">7177 (0x1C09)</span><span class="sxs-lookup"><span data-stu-id="dc69c-715">7177 (0x1C09)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-716">Inglese – Sudafrica</span><span class="sxs-lookup"><span data-stu-id="dc69c-716">English – South Africa</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-717">7178 (0x1C0A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-717">7178 (0x1C0A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-718">Spagnolo – Repubblica Dominicana</span><span class="sxs-lookup"><span data-stu-id="dc69c-718">Spanish – Dominican Republic</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-719">8193 (0x2001)</span><span class="sxs-lookup"><span data-stu-id="dc69c-719">8193 (0x2001)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-720">Arabo – Oman</span><span class="sxs-lookup"><span data-stu-id="dc69c-720">Arabic – Oman</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-721">8201 (0x2009)</span><span class="sxs-lookup"><span data-stu-id="dc69c-721">8201 (0x2009)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-722">Inglese – Giamaica</span><span class="sxs-lookup"><span data-stu-id="dc69c-722">English – Jamaica</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-723">8202 (0x200A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-723">8202 (0x200A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-724">Spagnolo – Venezuela</span><span class="sxs-lookup"><span data-stu-id="dc69c-724">Spanish – Venezuela</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-725">9217 (0x2401)</span><span class="sxs-lookup"><span data-stu-id="dc69c-725">9217 (0x2401)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-726">Arabo – Yemen</span><span class="sxs-lookup"><span data-stu-id="dc69c-726">Arabic – Yemen</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-727">9226 (0x240A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-727">9226 (0x240A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-728">Spagnolo – Colombia</span><span class="sxs-lookup"><span data-stu-id="dc69c-728">Spanish – Colombia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-729">10241 (0x2801)</span><span class="sxs-lookup"><span data-stu-id="dc69c-729">10241 (0x2801)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-730">Arabo – Siria</span><span class="sxs-lookup"><span data-stu-id="dc69c-730">Arabic – Syria</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-731">10249 (0x2809)</span><span class="sxs-lookup"><span data-stu-id="dc69c-731">10249 (0x2809)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-732">Inglese – Belize</span><span class="sxs-lookup"><span data-stu-id="dc69c-732">English – Belize</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-733">10250 (0x280A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-733">10250 (0x280A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-734">Spagnolo – Perù</span><span class="sxs-lookup"><span data-stu-id="dc69c-734">Spanish – Peru</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-735">11265 (0x2C01)</span><span class="sxs-lookup"><span data-stu-id="dc69c-735">11265 (0x2C01)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-736">Arabo – Giordania</span><span class="sxs-lookup"><span data-stu-id="dc69c-736">Arabic – Jordan</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-737">11273 (0x2C09)</span><span class="sxs-lookup"><span data-stu-id="dc69c-737">11273 (0x2C09)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-738">Inglese – Trinidad</span><span class="sxs-lookup"><span data-stu-id="dc69c-738">English – Trinidad</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-739">11274 (0x2C0A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-739">11274 (0x2C0A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-740">Spagnolo – Argentina</span><span class="sxs-lookup"><span data-stu-id="dc69c-740">Spanish – Argentina</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-741">12289 (0x3001)</span><span class="sxs-lookup"><span data-stu-id="dc69c-741">12289 (0x3001)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-742">Arabo (Libano)</span><span class="sxs-lookup"><span data-stu-id="dc69c-742">Arabic – Lebanon</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-743">12298 (0x300A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-743">12298 (0x300A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-744">Spagnolo – Ecuador</span><span class="sxs-lookup"><span data-stu-id="dc69c-744">Spanish – Ecuador</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-745">13313 (0x3401)</span><span class="sxs-lookup"><span data-stu-id="dc69c-745">13313 (0x3401)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-746">Arabo – Kuwait</span><span class="sxs-lookup"><span data-stu-id="dc69c-746">Arabic – Kuwait</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-747">13322 (0x340A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-747">13322 (0x340A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-748">Spagnolo – Cile</span><span class="sxs-lookup"><span data-stu-id="dc69c-748">Spanish – Chile</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-749">14337 (0x3801)</span><span class="sxs-lookup"><span data-stu-id="dc69c-749">14337 (0x3801)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-750">Arabo – Emirati Arabi Uniti</span><span class="sxs-lookup"><span data-stu-id="dc69c-750">Arabic – U.A.E.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-751">14346 (0x380A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-751">14346 (0x380A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-752">Spagnolo – Uruguay</span><span class="sxs-lookup"><span data-stu-id="dc69c-752">Spanish – Uruguay</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-753">15361 (0x3C01)</span><span class="sxs-lookup"><span data-stu-id="dc69c-753">15361 (0x3C01)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-754">Arabo – Bahrain</span><span class="sxs-lookup"><span data-stu-id="dc69c-754">Arabic – Bahrain</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-755">15370 (0x3C0A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-755">15370 (0x3C0A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-756">Spagnolo – Paraguay</span><span class="sxs-lookup"><span data-stu-id="dc69c-756">Spanish – Paraguay</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-757">16385 (0x4001)</span><span class="sxs-lookup"><span data-stu-id="dc69c-757">16385 (0x4001)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-758">Arabo – Qatar</span><span class="sxs-lookup"><span data-stu-id="dc69c-758">Arabic – Qatar</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-759">16394 (0x400A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-759">16394 (0x400A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-760">Spagnolo – Bolivia</span><span class="sxs-lookup"><span data-stu-id="dc69c-760">Spanish – Bolivia</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-761">17418 (0x440A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-761">17418 (0x440A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-762">Spagnolo – El Salvador</span><span class="sxs-lookup"><span data-stu-id="dc69c-762">Spanish – El Salvador</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-763">18442 (0x480A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-763">18442 (0x480A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-764">Spagnolo – Honduras</span><span class="sxs-lookup"><span data-stu-id="dc69c-764">Spanish – Honduras</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-765">19466 (0x4C0A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-765">19466 (0x4C0A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-766">Spagnolo – Nicaragua</span><span class="sxs-lookup"><span data-stu-id="dc69c-766">Spanish – Nicaragua</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-767">20490 (0x500A)</span><span class="sxs-lookup"><span data-stu-id="dc69c-767">20490 (0x500A)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-768">Spagnolo – Puerto Rico</span><span class="sxs-lookup"><span data-stu-id="dc69c-768">Spanish – Puerto Rico</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-769">**OSProductSuite**</span><span class="sxs-lookup"><span data-stu-id="dc69c-769">**OSProductSuite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-770">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-770">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-771">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-771">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-772">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ ProductOptions \| ProductSuite uguale a"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business (restricted)", "embedded NT", "Data Center")</span><span class="sxs-lookup"><span data-stu-id="dc69c-772">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\ProductOptions\|ProductSuite"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Small Business", "Enterprise", "BackOffice", "Communication Server", "Terminal Server", "Small Business(Restricted)", "Embedded NT", "Data Center")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-773">Aggiunte del prodotto di sistema installate e concessi in licenza al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-773">Installed and licensed system product additions to the operating system.</span></span> <span data-ttu-id="dc69c-774">Ad esempio, il valore di 146 (0x92) per **OSProductSuite** indica Enterprise, Servizi terminal e Data Center (bit uno, quattro e sette impostati).</span><span class="sxs-lookup"><span data-stu-id="dc69c-774">For example, the value of 146 (0x92) for **OSProductSuite** indicates Enterprise, Terminal Services, and Data Center (bits one, four, and seven set).</span></span> <span data-ttu-id="dc69c-775">Nell'elenco seguente sono elencati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="dc69c-775">The following list lists possible values.</span></span>

<dt>

<span data-ttu-id="dc69c-776">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-776">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-777">Microsoft Small Business Server è stato installato, ma potrebbe essere stato aggiornato a un'altra versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-777">Microsoft Small Business Server was once installed, but may have been upgraded to another version of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-778">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-778">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-779">Windows Server 2008 Enterprise è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-779">Windows Server 2008 Enterprise is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-780">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="dc69c-780">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-781">I componenti di Windows BackOffice sono installati.</span><span class="sxs-lookup"><span data-stu-id="dc69c-781">Windows BackOffice components are installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-782">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="dc69c-782">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-783">Il server di comunicazione è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-783">Communication Server is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-784">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="dc69c-784">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-785">Servizi terminal è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-785">Terminal Services is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-786">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="dc69c-786">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-787">Microsoft Small Business Server viene installato con la licenza client restrittiva.</span><span class="sxs-lookup"><span data-stu-id="dc69c-787">Microsoft Small Business Server is installed with the restrictive client license.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-788">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="dc69c-788">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-789">Windows Embedded è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-789">Windows Embedded is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-790">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="dc69c-790">128 (0x80)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-791">È installata un'edizione Datacenter.</span><span class="sxs-lookup"><span data-stu-id="dc69c-791">A Datacenter edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-792">256 (0x100)</span><span class="sxs-lookup"><span data-stu-id="dc69c-792">256 (0x100)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-793">Servizi terminal è installato, ma è supportata una sola sessione interattiva.</span><span class="sxs-lookup"><span data-stu-id="dc69c-793">Terminal Services is installed, but only one interactive session is supported.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-794">512 (0x200)</span><span class="sxs-lookup"><span data-stu-id="dc69c-794">512 (0x200)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-795">Windows Home Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-795">Windows Home Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-796">1024 (0x400)</span><span class="sxs-lookup"><span data-stu-id="dc69c-796">1024 (0x400)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-797">Server Web Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-797">Web Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-798">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="dc69c-798">8192 (0x2000)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-799">Storage Server Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-799">Storage Server Edition is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-800">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="dc69c-800">16384 (0x4000)</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-801">Compute Cluster Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-801">Compute Cluster Edition is installed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-802">**OSType**</span><span class="sxs-lookup"><span data-stu-id="dc69c-802">**OSType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-803">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc69c-803">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-804">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-804">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-805">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="dc69c-805">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-806">Tipo di sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-806">Type of operating system.</span></span> <span data-ttu-id="dc69c-807">Nell'elenco seguente vengono identificati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="dc69c-807">The following list identifies the possible values.</span></span>

<span data-ttu-id="dc69c-808">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-808">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc69c-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-809"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dc69c-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-810"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="dc69c-811"><span id="MACOS"></span><span id="macos"></span>**MacOS** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-811"><span id="MACOS"></span><span id="macos"></span>**MACOS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-812">MACRO</span><span class="sxs-lookup"><span data-stu-id="dc69c-812">MACROS</span></span>

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="dc69c-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="dc69c-813"><span id="ATTUNIX"></span><span id="attunix"></span>**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="dc69c-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="dc69c-814"><span id="DGUX"></span><span id="dgux"></span>**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="dc69c-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="dc69c-815"><span id="DECNT"></span><span id="decnt"></span>**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="dc69c-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**UNIX digitale** (6)</span><span class="sxs-lookup"><span data-stu-id="dc69c-816"><span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="dc69c-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="dc69c-817"><span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="dc69c-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span><span class="sxs-lookup"><span data-stu-id="dc69c-818"><span id="HPUX"></span><span id="hpux"></span>**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="dc69c-819"><span id="AIX"></span><span id="aix"></span>**Aix** (9)</span><span class="sxs-lookup"><span data-stu-id="dc69c-819"><span id="AIX"></span><span id="aix"></span>**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="dc69c-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="dc69c-820"><span id="MVS"></span><span id="mvs"></span>**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="dc69c-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="dc69c-821"><span id="OS400"></span><span id="os400"></span>**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="dc69c-822"><span id="OS_2"></span><span id="os_2"></span>**Sistema operativo/2** (12)</span><span class="sxs-lookup"><span data-stu-id="dc69c-822"><span id="OS_2"></span><span id="os_2"></span>**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="dc69c-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Javavm** (13)</span><span class="sxs-lookup"><span data-stu-id="dc69c-823"><span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="dc69c-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="dc69c-824"><span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="dc69c-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="dc69c-825"><span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="dc69c-826"><span id="WIN95"></span><span id="win95"></span>**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="dc69c-826"><span id="WIN95"></span><span id="win95"></span>**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="dc69c-827"><span id="WIN98"></span><span id="win98"></span>**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="dc69c-827"><span id="WIN98"></span><span id="win98"></span>**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="dc69c-828"><span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="dc69c-828"><span id="WINNT"></span><span id="winnt"></span>**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="dc69c-829"><span id="WINCE"></span><span id="wince"></span>**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="dc69c-829"><span id="WINCE"></span><span id="wince"></span>**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="dc69c-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="dc69c-830"><span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="dc69c-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="dc69c-831"><span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="dc69c-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span><span class="sxs-lookup"><span data-stu-id="dc69c-832"><span id="OSF"></span><span id="osf"></span>**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="dc69c-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span><span class="sxs-lookup"><span data-stu-id="dc69c-833"><span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="dc69c-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**UNIX Reliant** (24)</span><span class="sxs-lookup"><span data-stu-id="dc69c-834"><span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="dc69c-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="dc69c-835"><span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="dc69c-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="dc69c-836"><span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="dc69c-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span><span class="sxs-lookup"><span data-stu-id="dc69c-837"><span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="dc69c-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="dc69c-838"><span id="IRIX"></span><span id="irix"></span>**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="dc69c-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="dc69c-839"><span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)</span></span>


</dt> <dd>

<span data-ttu-id="dc69c-840">Solaris</span><span class="sxs-lookup"><span data-stu-id="dc69c-840">Solaris</span></span>

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="dc69c-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="dc69c-841"><span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="dc69c-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="dc69c-842"><span id="U6000"></span><span id="u6000"></span>**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="dc69c-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span><span class="sxs-lookup"><span data-stu-id="dc69c-843"><span id="ASERIES"></span><span id="aseries"></span>**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="dc69c-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="dc69c-844"><span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="dc69c-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="dc69c-845"><span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="dc69c-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="dc69c-846"><span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="dc69c-847"><span id="LINUX"></span><span id="linux"></span>**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="dc69c-847"><span id="LINUX"></span><span id="linux"></span>**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="dc69c-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="dc69c-848"><span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="dc69c-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span><span class="sxs-lookup"><span data-stu-id="dc69c-849"><span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="dc69c-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="dc69c-850"><span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="dc69c-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**UNIX interattivo** (40)</span><span class="sxs-lookup"><span data-stu-id="dc69c-851"><span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="dc69c-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="dc69c-852"><span id="BSDUNIX"></span><span id="bsdunix"></span>**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="dc69c-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="dc69c-853"><span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="dc69c-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="dc69c-854"><span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="dc69c-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="dc69c-855"><span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="dc69c-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="dc69c-856"><span id="OS9"></span><span id="os9"></span>**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="dc69c-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="dc69c-857"><span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="dc69c-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="dc69c-858"><span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="dc69c-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="dc69c-859"><span id="QNX"></span><span id="qnx"></span>**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="dc69c-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="dc69c-860"><span id="EPOC"></span><span id="epoc"></span>**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="dc69c-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="dc69c-861"><span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="dc69c-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="dc69c-862"><span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="dc69c-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="dc69c-863"><span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="dc69c-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="dc69c-864"><span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="dc69c-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP mpe** (54)</span><span class="sxs-lookup"><span data-stu-id="dc69c-865"><span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="dc69c-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="dc69c-866"><span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="dc69c-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="dc69c-867"><span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="dc69c-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="dc69c-868"><span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="dc69c-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="dc69c-869"><span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="dc69c-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (59)</span><span class="sxs-lookup"><span data-stu-id="dc69c-870"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span data-ttu-id="dc69c-871"><span id="OS_390"></span><span id="os_390"></span>**Sistema operativo/390** (60)</span><span class="sxs-lookup"><span data-stu-id="dc69c-871"><span id="OS_390"></span><span id="os_390"></span>**OS/390** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="dc69c-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span><span class="sxs-lookup"><span data-stu-id="dc69c-872"><span id="VSE"></span><span id="vse"></span>**VSE** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="dc69c-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span><span class="sxs-lookup"><span data-stu-id="dc69c-873"><span id="TPF"></span><span id="tpf"></span>**TPF** (62)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-874">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="dc69c-874">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-875">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-875">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-876">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-876">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-877">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="dc69c-877">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-878">Descrizione aggiuntiva per la versione corrente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-878">Additional description for the current operating system version.</span></span>

<span data-ttu-id="dc69c-879">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-879">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-880">**PAEEnabled**</span><span class="sxs-lookup"><span data-stu-id="dc69c-880">**PAEEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-881">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-881">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-882">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-882">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-883">Se **true**, le estensioni di indirizzo fisico (PAE) sono abilitate dal sistema operativo in esecuzione su processori Intel.</span><span class="sxs-lookup"><span data-stu-id="dc69c-883">If **True**, the physical address extensions (PAE) are enabled by the operating system running on Intel processors.</span></span> <span data-ttu-id="dc69c-884">Il PAE consente alle applicazioni di gestire più di 4 GB di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="dc69c-884">PAE allows applications to address more than 4 GB of physical memory.</span></span> <span data-ttu-id="dc69c-885">Quando è abilitata la funzionalità PAE, il sistema operativo usa la conversione di indirizzi lineari a tre livelli anziché a due livelli.</span><span class="sxs-lookup"><span data-stu-id="dc69c-885">When PAE is enabled, the operating system uses three-level linear address translation rather than two-level.</span></span> <span data-ttu-id="dc69c-886">Fornire una quantità maggiore di memoria fisica a un'applicazione riduce la necessità di scambiare memoria con il file di paging e di aumentare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="dc69c-886">Providing more physical memory to an application reduces the need to swap memory to the page file and increases performance.</span></span> <span data-ttu-id="dc69c-887">Per abilitare la PAE, utilizzare l'opzione "/PAE" nel file di Boot.ini.</span><span class="sxs-lookup"><span data-stu-id="dc69c-887">To enable, PAE, use the "/PAE" switch in the Boot.ini file.</span></span> <span data-ttu-id="dc69c-888">Per ulteriori informazioni sulla funzionalità di estensione degli indirizzi fisici, vedere <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .</span><span class="sxs-lookup"><span data-stu-id="dc69c-888">For more information about the Physical Address Extension feature, see <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912>.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-889">**PlusProductID**</span><span class="sxs-lookup"><span data-stu-id="dc69c-889">**PlusProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-890">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-890">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-891">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-891">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-892">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus Plus</span><span class="sxs-lookup"><span data-stu-id="dc69c-892">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="dc69c-893">ProductId ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-893">ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-894">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-894">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-895">**PlusVersionNumber**</span><span class="sxs-lookup"><span data-stu-id="dc69c-895">**PlusVersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-896">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-896">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-897">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-897">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-898">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus Plus</span><span class="sxs-lookup"><span data-stu-id="dc69c-898">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|Plus!</span></span> <span data-ttu-id="dc69c-899">VersionNumber ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-899">VersionNumber")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-900">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="dc69c-900">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-901">**PortableOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="dc69c-901">**PortableOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-902">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-902">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-903">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-903">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-904">Specifica se il sistema operativo è stato avviato da un dispositivo USB esterno.</span><span class="sxs-lookup"><span data-stu-id="dc69c-904">Specifies whether the operating system booted from an external USB device.</span></span> <span data-ttu-id="dc69c-905">Se true, il sistema operativo ha rilevato l'avvio in un dispositivo di archiviazione connesso localmente.</span><span class="sxs-lookup"><span data-stu-id="dc69c-905">If true, the operating system has detected it is booting on a supported locally connected storage device.</span></span>

<span data-ttu-id="dc69c-906">**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è supportata prima di Windows 8 e Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="dc69c-906">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-907">**Server/istanza primaria**</span><span class="sxs-lookup"><span data-stu-id="dc69c-907">**Primary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-908">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dc69c-908">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-909">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-909">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-910">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="dc69c-910">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-911">Specifica se si tratta del sistema operativo primario.</span><span class="sxs-lookup"><span data-stu-id="dc69c-911">Specifies whether this is the primary operating system.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-912">**ProductType**</span><span class="sxs-lookup"><span data-stu-id="dc69c-912">**ProductType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-913">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-913">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-914">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-914">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-915">Ulteriori informazioni sul sistema.</span><span class="sxs-lookup"><span data-stu-id="dc69c-915">Additional system information.</span></span>

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

<span data-ttu-id="dc69c-916">**Stazione di lavoro** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-916">**Work Station** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

<span data-ttu-id="dc69c-917">**Controller di dominio** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-917">**Domain Controller** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

<span data-ttu-id="dc69c-918">**Server** (3)</span><span class="sxs-lookup"><span data-stu-id="dc69c-918">**Server** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-919">**QuantumLength**</span><span class="sxs-lookup"><span data-stu-id="dc69c-919">**QuantumLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-920">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc69c-920">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-921">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc69c-921">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-922">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ PriorityControl \| Win32PrioritySeparation")</span><span class="sxs-lookup"><span data-stu-id="dc69c-922">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\PriorityControl\|Win32PrioritySeparation")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-923">Non supportato</span><span class="sxs-lookup"><span data-stu-id="dc69c-923">Not supported</span></span>

<span data-ttu-id="dc69c-924">\* \* Windows Server 2008 e Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="dc69c-924">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="dc69c-925">La proprietà **QuantumLength** definisce il numero di tick del clock per Quantum.</span><span class="sxs-lookup"><span data-stu-id="dc69c-925">The **QuantumLength** property defines the number of clock ticks per quantum.</span></span> <span data-ttu-id="dc69c-926">Un quantum è un'unità di tempo di esecuzione che l'utilità di pianificazione può assegnare a un'applicazione prima di passare ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="dc69c-926">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to other applications.</span></span> <span data-ttu-id="dc69c-927">Quando un thread esegue un quantum, il kernel lo precede e lo sposta alla fine di una coda per le applicazioni con uguale priorità.</span><span class="sxs-lookup"><span data-stu-id="dc69c-927">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="dc69c-928">La lunghezza effettiva del quantum di un thread varia in diverse piattaforme Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-928">The actual length of a thread's quantum varies across different Windows platforms.</span></span> <span data-ttu-id="dc69c-929">Solo per Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dc69c-929">For Windows NT/Windows 2000 only.</span></span>

<span data-ttu-id="dc69c-930">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="dc69c-930">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc69c-931">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-931">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

<span data-ttu-id="dc69c-932">**Un segno** di selezione (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-932">**One tick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

<span data-ttu-id="dc69c-933">**Due cicli** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-933">**Two ticks** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-934">**QuantumType**</span><span class="sxs-lookup"><span data-stu-id="dc69c-934">**QuantumType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-935">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc69c-935">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-936">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="dc69c-936">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-937">Non supportato</span><span class="sxs-lookup"><span data-stu-id="dc69c-937">Not supported</span></span>

<span data-ttu-id="dc69c-938">\* \* Windows Server 2008 e Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="dc69c-938">\*\*Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="dc69c-939">La proprietà **QuantumType** specifica i quantum a lunghezza fissa o variabile.</span><span class="sxs-lookup"><span data-stu-id="dc69c-939">The **QuantumType** property specifies either fixed or variable length quantums.</span></span> <span data-ttu-id="dc69c-940">Per impostazione predefinita, Windows utilizza Quantum a lunghezza variabile in cui l'applicazione in primo piano ha un quantum più lungo rispetto alle applicazioni in background.</span><span class="sxs-lookup"><span data-stu-id="dc69c-940">Windows defaults to variable length quantums where the foreground application has a longer quantum than the background applications.</span></span> <span data-ttu-id="dc69c-941">Per impostazione predefinita, Windows Server prevede Quantum a lunghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="dc69c-941">Windows Server defaults to fixed-length quantums.</span></span> <span data-ttu-id="dc69c-942">Un quantum è un'unità di tempo di esecuzione che l'utilità di pianificazione può assegnare a un'applicazione prima di passare a un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="dc69c-942">A quantum is a unit of execution time that the scheduler is allowed to give to an application before switching to another application.</span></span> <span data-ttu-id="dc69c-943">Quando un thread esegue un quantum, il kernel lo precede e lo sposta alla fine di una coda per le applicazioni con uguale priorità.</span><span class="sxs-lookup"><span data-stu-id="dc69c-943">When a thread runs one quantum, the kernel preempts it and moves it to the end of a queue for applications with equal priorities.</span></span> <span data-ttu-id="dc69c-944">La lunghezza effettiva del quantum di un thread varia in diverse piattaforme Windows.</span><span class="sxs-lookup"><span data-stu-id="dc69c-944">The actual length of a thread's quantum varies across different Windows platforms.</span></span>

<span data-ttu-id="dc69c-945">I valori possibili sono.</span><span class="sxs-lookup"><span data-stu-id="dc69c-945">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc69c-946">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dc69c-946">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

<span data-ttu-id="dc69c-947">**Corretto** (1)</span><span class="sxs-lookup"><span data-stu-id="dc69c-947">**Fixed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

<span data-ttu-id="dc69c-948">**Variabile** (2)</span><span class="sxs-lookup"><span data-stu-id="dc69c-948">**Variable** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-949">**RegisteredUser**</span><span class="sxs-lookup"><span data-stu-id="dc69c-949">**RegisteredUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-950">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-950">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-951">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-952">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| RegisteredOwner")</span><span class="sxs-lookup"><span data-stu-id="dc69c-952">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|RegisteredOwner")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-953">Nome dell'utente registrato del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-953">Name of the registered user of the operating system.</span></span>

<span data-ttu-id="dc69c-954">Esempio: "Ben Smith"</span><span class="sxs-lookup"><span data-stu-id="dc69c-954">Example: "Ben Smith"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-955">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="dc69c-955">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-956">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-956">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-957">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-958">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductID")</span><span class="sxs-lookup"><span data-stu-id="dc69c-958">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\|ProductId")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-959">Numero di identificazione seriale del prodotto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-959">Operating system product serial identification number.</span></span>

<span data-ttu-id="dc69c-960">Esempio: "10497-OEM-0031416-71674"</span><span class="sxs-lookup"><span data-stu-id="dc69c-960">Example: "10497-OEM-0031416-71674"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-961">**ServicePackMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="dc69c-961">**ServicePackMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-962">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc69c-962">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-963">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-963">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-964">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMajor**")</span><span class="sxs-lookup"><span data-stu-id="dc69c-964">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMajor**")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-965">Numero di versione principale del Service Pack installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-965">Major version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="dc69c-966">Se non è stato installato alcun Service Pack, il valore è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-966">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-967">**ServicePackMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="dc69c-967">**ServicePackMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-968">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dc69c-968">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-969">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-969">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-970">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **wServicePackMinor**")</span><span class="sxs-lookup"><span data-stu-id="dc69c-970">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|**wServicePackMinor**")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-971">Numero di versione secondario del Service Pack installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="dc69c-971">Minor version number of the service pack installed on the computer system.</span></span> <span data-ttu-id="dc69c-972">Se non è stato installato alcun Service Pack, il valore è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="dc69c-972">If no service pack has been installed, the value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-973">**SizeStoredInPagingFiles)**</span><span class="sxs-lookup"><span data-stu-id="dc69c-973">**SizeStoredInPagingFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-974">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-974">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-975">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-975">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-976">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| Impostazioni memoria \| di sistema 001,3 "), [**unità**](../wmisdk/standard-qualifiers.md) (" kilobyte ")</span><span class="sxs-lookup"><span data-stu-id="dc69c-976">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Memory Settings\|001.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-977">Numero totale di kilobyte che possono essere archiviati nei file di paging del sistema operativo: 0 (zero) indica che non sono presenti file di paging.</span><span class="sxs-lookup"><span data-stu-id="dc69c-977">Total number of kilobytes that can be stored in the operating system paging files—0 (zero) indicates that there are no paging files.</span></span> <span data-ttu-id="dc69c-978">Tenere presente che questo numero non rappresenta le dimensioni fisiche effettive del file di paging su disco.</span><span class="sxs-lookup"><span data-stu-id="dc69c-978">Be aware that this number does not represent the actual physical size of the paging file on disk.</span></span>

<span data-ttu-id="dc69c-979">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-979">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-980">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-980">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-981">**Status**</span><span class="sxs-lookup"><span data-stu-id="dc69c-981">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-982">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-982">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-983">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-983">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-984">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="dc69c-984">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-985">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dc69c-985">Current status of the object.</span></span> <span data-ttu-id="dc69c-986">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="dc69c-986">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="dc69c-987">Gli stati operativi includono: "OK", "danneggiato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, può funzionare correttamente, ma prevede un errore a breve).</span><span class="sxs-lookup"><span data-stu-id="dc69c-987">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive may function properly, but predicts a failure in the near future).</span></span> <span data-ttu-id="dc69c-988">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="dc69c-988">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="dc69c-989">Lo stato del servizio si applica al lavoro amministrativo, ad esempio il riutilizzo del mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="dc69c-989">The Service status applies to administrative work, such as mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="dc69c-990">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="dc69c-990">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="dc69c-991">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-991">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dc69c-992">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="dc69c-992">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dc69c-993">**Errore** ("errore")</span><span class="sxs-lookup"><span data-stu-id="dc69c-993">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dc69c-994">Ridotto **("danneggiato"** )</span><span class="sxs-lookup"><span data-stu-id="dc69c-994">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dc69c-995">**Sconosciuto** ("sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="dc69c-995">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dc69c-996">**Errore di predazione** ("Predator fail")</span><span class="sxs-lookup"><span data-stu-id="dc69c-996">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dc69c-997">**Avvio** di ("avvio")</span><span class="sxs-lookup"><span data-stu-id="dc69c-997">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dc69c-998">**Arresto** in corso ("arresto")</span><span class="sxs-lookup"><span data-stu-id="dc69c-998">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dc69c-999">**Servizio** ("servizio")</span><span class="sxs-lookup"><span data-stu-id="dc69c-999">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dc69c-1000">**Sottolineato** (sottolineato)</span><span class="sxs-lookup"><span data-stu-id="dc69c-1000">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dc69c-1001">**Noncover** ("noncover")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1001">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dc69c-1002">**Nessun contatto** ("nessun contatto")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1002">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dc69c-1003">**Comunicazione persa** ("comunicazione persa")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1003">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-1004">**SuiteMask**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1004">**SuiteMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1005">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1005">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1006">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1006">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1007">Qualificatori: [**bitmap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, BackOffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "single user", "Windows Home Edition", "Windows Server, Web Edition")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1007">Qualifiers: [**BitMap**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**BitValues**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows Server, Enterprise Edition", "Windows Server, Backoffice Edition", "Windows Server, Communications Edition", "Microsoft Terminal Services", "Windows Server, Small Business Edition Restricted", "Windows Embedded", "Windows Server, Datacenter Edition", "Single User", "Windows Home Edition", "Windows Server, Web Edition")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1008">Flag di bit che identificano i gruppi di prodotti disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1008">Bit flags that identify the product suites available on the system.</span></span>

<span data-ttu-id="dc69c-1009">Ad esempio, per specificare sia Personal che BackOffice, impostare **SuiteMask** su `4 | 512` o `516` .</span><span class="sxs-lookup"><span data-stu-id="dc69c-1009">For example, to specify both Personal and BackOffice, set **SuiteMask** to `4 | 512` or `516`.</span></span>

<dt>

<span data-ttu-id="dc69c-1010">1</span><span class="sxs-lookup"><span data-stu-id="dc69c-1010">1</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1011">Piccole imprese</span><span class="sxs-lookup"><span data-stu-id="dc69c-1011">Small Business</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1012">2</span><span class="sxs-lookup"><span data-stu-id="dc69c-1012">2</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1013">Enterprise</span><span class="sxs-lookup"><span data-stu-id="dc69c-1013">Enterprise</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1014">4</span><span class="sxs-lookup"><span data-stu-id="dc69c-1014">4</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1015">BackOffice</span><span class="sxs-lookup"><span data-stu-id="dc69c-1015">BackOffice</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1016">8</span><span class="sxs-lookup"><span data-stu-id="dc69c-1016">8</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1017">Comunicazioni</span><span class="sxs-lookup"><span data-stu-id="dc69c-1017">Communications</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1018">16</span><span class="sxs-lookup"><span data-stu-id="dc69c-1018">16</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1019">Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="dc69c-1019">Terminal Services</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1020">32</span><span class="sxs-lookup"><span data-stu-id="dc69c-1020">32</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1021">Small Business con restrizioni</span><span class="sxs-lookup"><span data-stu-id="dc69c-1021">Small Business Restricted</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1022">64</span><span class="sxs-lookup"><span data-stu-id="dc69c-1022">64</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1023">Edizione incorporata</span><span class="sxs-lookup"><span data-stu-id="dc69c-1023">Embedded Edition</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1024">128</span><span class="sxs-lookup"><span data-stu-id="dc69c-1024">128</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1025">Datacenter Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-1025">Datacenter Edition</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1026">256</span><span class="sxs-lookup"><span data-stu-id="dc69c-1026">256</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1027">Utente singolo</span><span class="sxs-lookup"><span data-stu-id="dc69c-1027">Single User</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1028">512</span><span class="sxs-lookup"><span data-stu-id="dc69c-1028">512</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1029">Home Edition</span><span class="sxs-lookup"><span data-stu-id="dc69c-1029">Home Edition</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1030">1024</span><span class="sxs-lookup"><span data-stu-id="dc69c-1030">1024</span></span>
</dt> <dd>

<span data-ttu-id="dc69c-1031">Edizione server Web</span><span class="sxs-lookup"><span data-stu-id="dc69c-1031">Web Server Edition</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dc69c-1032">**SystemDevice**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1032">**SystemDevice**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1033">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1033">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1034">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1034">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1035">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| funzioni del registro di sistema \| [**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| percorsi \| dispositivo")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1035">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Registry Functions\|[**GetPrivateProfileString**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring)\|Paths\|TargetDevice")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1036">Partizione del disco fisico in cui è installato il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1036">Physical disk partition on which the operating system is installed.</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1037">**SystemDirectory**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1037">**SystemDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1038">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1038">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1039">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1039">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1040">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span><span class="sxs-lookup"><span data-stu-id="dc69c-1040">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1041">Directory di sistema del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1041">System directory of the operating system.</span></span>

<span data-ttu-id="dc69c-1042">Esempio: "C: \\ Windows \\ system32"</span><span class="sxs-lookup"><span data-stu-id="dc69c-1042">Example: "C:\\WINDOWS\\SYSTEM32"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1043">**SystemDrive**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1043">**SystemDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1044">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1044">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1045">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1045">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1046">Lettera dell'unità disco in cui risiede il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1046">Letter of the disk drive on which the operating system resides.</span></span> <span data-ttu-id="dc69c-1047">Esempio: "C:"</span><span class="sxs-lookup"><span data-stu-id="dc69c-1047">Example: "C:"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1048">**TotalSwapSpaceSize**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1048">**TotalSwapSpaceSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1049">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1049">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1050">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1050">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1051">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1051">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1052">Spazio di swapping totale, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1052">Total swap space in kilobytes.</span></span> <span data-ttu-id="dc69c-1053">Questo valore può essere **null** (non specificato) se lo spazio di swapping non è distinto dai file di paging.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1053">This value may be **NULL** (unspecified) if the swap space is not distinguished from page files.</span></span> <span data-ttu-id="dc69c-1054">Tuttavia, alcuni sistemi operativi distinguono questi concetti.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1054">However, some operating systems distinguish these concepts.</span></span> <span data-ttu-id="dc69c-1055">In UNIX, ad esempio, è possibile scambiare interi processi quando l'elenco di pagine disponibili è inferiore a un importo specificato.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1055">For example, in UNIX, whole processes can be swapped out when the free page list falls and remains below a specified amount.</span></span>

<span data-ttu-id="dc69c-1056">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1056">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-1057">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1057">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1058">**TotalVirtualMemorySize**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1058">**TotalVirtualMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1059">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1059">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1060">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1060">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1061">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1061">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1062">Numero, in kilobyte, della memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1062">Number, in kilobytes, of virtual memory.</span></span> <span data-ttu-id="dc69c-1063">Questo può essere calcolato, ad esempio, aggiungendo la quantità di RAM totale alla quantità di spazio di paging, ovvero aggiungendo la quantità di memoria in o aggregata dal sistema del computer alla proprietà **SizeStoredInPagingFiles)**.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1063">For example, this may be calculated by adding the amount of total RAM to the amount of paging space, that is, adding the amount of memory in or aggregated by the computer system to the property, **SizeStoredInPagingFiles**.</span></span>

<span data-ttu-id="dc69c-1064">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1064">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-1065">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1065">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1066">**TotalVisibleMemorySize**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1066">**TotalVisibleMemorySize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1067">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1067">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1068">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1068">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1069">Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) ("kilobyte")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1069">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1070">Quantità totale, espressa in kilobyte, della memoria fisica disponibile per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1070">Total amount, in kilobytes, of physical memory available to the operating system.</span></span> <span data-ttu-id="dc69c-1071">Questo valore non indica necessariamente la vera quantità di memoria fisica, ma ciò che viene segnalato al sistema operativo come disponibile.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1071">This value does not necessarily indicate the true amount of physical memory, but what is reported to the operating system as available to it.</span></span>

<span data-ttu-id="dc69c-1072">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1072">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="dc69c-1073">Questa proprietà viene ereditata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1073">This property is inherited from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1074">**Versione**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1074">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1075">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1075">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1076">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1076">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1077">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Structures \| [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| dwMajorVersion, dwMinorVersion")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1077">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Version"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Structures\|[**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa)\|dwMajorVersion, dwMinorVersion")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1078">Numero di versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1078">Version number of the operating system.</span></span>

<span data-ttu-id="dc69c-1079">Esempio: "4,0"</span><span class="sxs-lookup"><span data-stu-id="dc69c-1079">Example: "4.0"</span></span>

</dd> <dt>

<span data-ttu-id="dc69c-1080">**WindowsDirectory**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1080">**WindowsDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc69c-1081">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1081">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1082">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dc69c-1082">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dc69c-1083">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span><span class="sxs-lookup"><span data-stu-id="dc69c-1083">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|System Information Functions\|[**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")</span></span>
</dt> </dl>

<span data-ttu-id="dc69c-1084">Directory Windows del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1084">Windows directory of the operating system.</span></span>

<span data-ttu-id="dc69c-1085">Esempio: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="dc69c-1085">Example: "C:\\WINDOWS"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc69c-1086">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc69c-1086">Remarks</span></span>

<span data-ttu-id="dc69c-1087">La classe **Win32 \_ OperatingSystem** è derivata da [**CIM \_ OperatingSystem**](cim-operatingsystem.md).</span><span class="sxs-lookup"><span data-stu-id="dc69c-1087">The **Win32\_OperatingSystem** class is derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md).</span></span>

<span data-ttu-id="dc69c-1088">Qualsiasi sistema operativo che può essere installato in un computer in grado di eseguire un sistema operativo basato su Windows è un discendente o un membro di questa classe.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1088">Any operating system that can be installed on a computer that can run a Windows-based operating system is a descendant or member of this class.</span></span> <span data-ttu-id="dc69c-1089">**Win32 \_ OperatingSystem** è una classe singleton.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1089">**Win32\_OperatingSystem** is a singleton class.</span></span> <span data-ttu-id="dc69c-1090">Per ottenere la singola istanza, usare "@" per la chiave.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1090">To get the single instance, use "@" for the key.</span></span>

<span data-ttu-id="dc69c-1091">A differenza della maggior parte delle altre classi WMI generate da MgmtClassGen, il metodo **OperatingSystem. CreateInstance**() restituirà un oggetto **OperatingSystem** vuoto.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1091">Unlike most of the other WMI classes generated by MgmtClassGen, the **OperatingSystem.CreateInstance**() method will return a blank **OperatingSystem** object.</span></span> <span data-ttu-id="dc69c-1092">Se quindi si usa C \# con Mgmtclassgen, è possibile usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="dc69c-1092">Therefore, if you are using C\# with MgmtClassGen, you can use the following code:</span></span>


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a><span data-ttu-id="dc69c-1093">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc69c-1093">Examples</span></span>

<span data-ttu-id="dc69c-1094">È possibile trovare un esempio VBScript che ottenga dati del sistema operativo e del processore da [**Win32 \_ ComputerSystem**](win32-computersystem.md), [**\_ processore Win32**](win32-processor.md)e **\_ OperatingSystem Win32** negli esempi di argomenti del [**\_ processore Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="dc69c-1094">You can find a VBScript example that obtains operating system and processor data from [**Win32\_ComputerSystem**](win32-computersystem.md), [**Win32\_Processor**](win32-processor.md), and **Win32\_OperatingSystem** in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="dc69c-1095">L'esempio di [generazione di report dell'ambiente di Exchange tramite PowerShell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell nella raccolta TechNet usa una classe **\_ OperatingSystem Win32** come parte di un'applicazione più grande per generare report per gli ambienti di Exchange.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1095">The [Generate Exchange Environment Reports using Powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) PowerShell sample on TechNet Gallery uses a **Win32\_OperatingSystem** class as part of a larger application to generate exchange environment reports.</span></span>

<span data-ttu-id="dc69c-1096">L'esempio per ottenere il tempo di attività del [Server tramite WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) nella raccolta TechNet usa la proprietà **LastBootupTime** per determinare la durata del server.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1096">The [Get Server Uptime Using WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) sample in the TechNet Gallery uses the **LastBootupTime** property to determine how long the server has been active.</span></span> <span data-ttu-id="dc69c-1097">Nell'esempio viene inoltre utilizzata l'opzione timeout per assicurarsi che la chiamata WMI non venga sospesa.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1097">The sample also uses the timeout option to ensure that the WMI call does not hang.</span></span>

<span data-ttu-id="dc69c-1098">Nell'esempio di codice VBScript [Information Retriever WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) della raccolta TechNet viene utilizzata la classe **Win32 \_ OperatingSystem** per recuperare le informazioni sul sistema operativo da un numero di computer remoti.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1098">The [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) VBScript code example on the TechNet Gallery uses the **Win32\_OperatingSystem** class to retrieve OS information from a number of remote computers.</span></span>

<span data-ttu-id="dc69c-1099">Lo script seguente ottiene le istanze di **Win32 \_ OperatingSystem** nello \\ spazio dei nomi "root CIMv2" predefinito, quindi Visualizza le informazioni sul sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1099">The following script obtains the instances of **Win32\_OperatingSystem** in the default "Root\\CIMv2" namespace, and then displays information about the operating system.</span></span>


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="dc69c-1100">Nell'esempio di codice PowerShell seguente vengono visualizzate tutte le informazioni operative sul sistema operativo corrente.</span><span class="sxs-lookup"><span data-stu-id="dc69c-1100">The following PowerShell code sample displays all the operating information about the current OS.</span></span>


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a><span data-ttu-id="dc69c-1101">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc69c-1101">Requirements</span></span>



| <span data-ttu-id="dc69c-1102">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc69c-1102">Requirement</span></span> | <span data-ttu-id="dc69c-1103">Valore</span><span class="sxs-lookup"><span data-stu-id="dc69c-1103">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc69c-1104">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc69c-1104">Minimum supported client</span></span><br/> | <span data-ttu-id="dc69c-1105">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc69c-1105">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc69c-1106">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc69c-1106">Minimum supported server</span></span><br/> | <span data-ttu-id="dc69c-1107">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc69c-1107">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc69c-1108">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc69c-1108">Namespace</span></span><br/>                | <span data-ttu-id="dc69c-1109">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dc69c-1109">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc69c-1110">MOF</span><span class="sxs-lookup"><span data-stu-id="dc69c-1110">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc69c-1111"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc69c-1111"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc69c-1112">DLL</span><span class="sxs-lookup"><span data-stu-id="dc69c-1112">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc69c-1113"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc69c-1113"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc69c-1114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc69c-1114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc69c-1115">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="dc69c-1115">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="dc69c-1116">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="dc69c-1116">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="dc69c-1117">Attività WMI: sistemi operativi</span><span class="sxs-lookup"><span data-stu-id="dc69c-1117">WMI Tasks: Operating Systems</span></span>](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[<span data-ttu-id="dc69c-1118">Attività WMI: hardware del computer</span><span class="sxs-lookup"><span data-stu-id="dc69c-1118">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[<span data-ttu-id="dc69c-1119">Attività WMI: gestione desktop</span><span class="sxs-lookup"><span data-stu-id="dc69c-1119">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
