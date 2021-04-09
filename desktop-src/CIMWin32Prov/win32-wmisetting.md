---
description: La \_ classe WMI WMISetting singleton Win32 contiene i parametri operativi per il servizio WMI. Questa classe può avere una sola istanza, che esiste sempre per ogni sistema Windows e non può essere eliminata. Non è possibile creare istanze aggiuntive.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877326"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="25939-105">Win32 \_ WMISetting (classe)</span><span class="sxs-lookup"><span data-stu-id="25939-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="25939-106">La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ WMISetting singleton Win32** contiene i parametri operativi per il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="25939-107">Questa classe può avere una sola istanza, che esiste sempre per ogni sistema Windows e non può essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="25939-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="25939-108">Non è possibile creare istanze aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="25939-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="25939-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="25939-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="25939-110">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="25939-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25939-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25939-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="25939-112">Members</span><span class="sxs-lookup"><span data-stu-id="25939-112">Members</span></span>

<span data-ttu-id="25939-113">La classe **Win32 \_ WMISetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="25939-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="25939-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25939-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25939-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25939-115">Properties</span></span>

<span data-ttu-id="25939-116">La classe **Win32 \_ WMISetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="25939-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25939-117">**ASPScriptDefaultNamespace**</span><span class="sxs-lookup"><span data-stu-id="25939-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-118">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-120">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| Default Namespace")</span><span class="sxs-lookup"><span data-stu-id="25939-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="25939-121">Spazio dei nomi dello script predefinito.</span><span class="sxs-lookup"><span data-stu-id="25939-121">Default script namespace.</span></span> <span data-ttu-id="25939-122">Questa proprietà contiene lo spazio dei nomi utilizzato dalle chiamate dall'API di scripting per WMI se non ne è stato specificato alcuno dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="25939-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="25939-123">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-124">**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **scripting \| default namespace**    </span><span class="sxs-lookup"><span data-stu-id="25939-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="25939-125">Esempio: radice \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="25939-125">Example: root\\cimv2</span></span>

<span data-ttu-id="25939-126">Per uno script di esempio che usa questa proprietà, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="25939-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="25939-127">**ASPScriptEnabled**</span><span class="sxs-lookup"><span data-stu-id="25939-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25939-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25939-129">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-130">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| Enable for ASP")</span><span class="sxs-lookup"><span data-stu-id="25939-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="25939-131">Se **true**, lo scripting WMI può essere utilizzato in Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="25939-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="25939-132">Questa proprietà è valida solo nei sistemi che eseguono versioni non supportate di Windows.</span><span class="sxs-lookup"><span data-stu-id="25939-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="25939-133">Per i sistemi Windows supportati, lo scripting WMI è sempre consentito in ASP.</span><span class="sxs-lookup"><span data-stu-id="25939-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="25939-134">**AutorecoverMofs**</span><span class="sxs-lookup"><span data-stu-id="25939-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-135">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="25939-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="25939-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-137">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| autocover file MOF")</span><span class="sxs-lookup"><span data-stu-id="25939-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="25939-138">Elenco dei nomi di file MOF completi utilizzati per inizializzare o ripristinare il repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="25939-139">L'elenco determina l'ordine in cui vengono compilati i file MOF.</span><span class="sxs-lookup"><span data-stu-id="25939-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="25939-140">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-141">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| autocover file MOF**    </span><span class="sxs-lookup"><span data-stu-id="25939-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="25939-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="25939-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-143">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-145">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")</span><span class="sxs-lookup"><span data-stu-id="25939-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="25939-146">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="25939-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="25939-147">**Non avviare** (0)</span><span class="sxs-lookup"><span data-stu-id="25939-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="25939-148">**Avvio automatico** (1)</span><span class="sxs-lookup"><span data-stu-id="25939-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="25939-149">**Avvio al riavvio** (2)</span><span class="sxs-lookup"><span data-stu-id="25939-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25939-150">**BackupInterval**</span><span class="sxs-lookup"><span data-stu-id="25939-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-151">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-152">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-153">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| backup Interval Threshold"), [**unità**](../wmisdk/standard-qualifiers.md) ("minutes")</span><span class="sxs-lookup"><span data-stu-id="25939-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="25939-154">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="25939-154">Not supported.</span></span> <span data-ttu-id="25939-155">Eseguire invece il backup manuale del repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="25939-156">**BackupLastTime**</span><span class="sxs-lookup"><span data-stu-id="25939-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-157">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="25939-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="25939-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-159">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")</span><span class="sxs-lookup"><span data-stu-id="25939-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="25939-160">Data e ora in cui è stato eseguito l'ultimo backup.</span><span class="sxs-lookup"><span data-stu-id="25939-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="25939-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="25939-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-164">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")</span><span class="sxs-lookup"><span data-stu-id="25939-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="25939-165">Informazioni sulla versione per il servizio WMI attualmente installato.</span><span class="sxs-lookup"><span data-stu-id="25939-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="25939-166">Lunghezza del tempo che trascorre tra i backup del database WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="25939-167">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-168">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| Build**</span><span class="sxs-lookup"><span data-stu-id="25939-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="25939-169">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="25939-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-172">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="25939-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="25939-173">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="25939-173">Short textual description of the current object.</span></span>

<span data-ttu-id="25939-174">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="25939-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="25939-175">**DatabaseDirectory**</span><span class="sxs-lookup"><span data-stu-id="25939-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-176">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-178">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| repository directory")</span><span class="sxs-lookup"><span data-stu-id="25939-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="25939-179">Percorso della directory che contiene il repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="25939-180">**DatabaseMaxSize**</span><span class="sxs-lookup"><span data-stu-id="25939-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-181">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-183">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB Size"), [**unità**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="25939-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="25939-184">Dimensioni massime del repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="25939-185">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="25939-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25939-188">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="25939-188">Textual description of the current object.</span></span>

<span data-ttu-id="25939-189">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="25939-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="25939-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="25939-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-191">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25939-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25939-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-193">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")</span><span class="sxs-lookup"><span data-stu-id="25939-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="25939-194">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="25939-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="25939-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="25939-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25939-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25939-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")</span><span class="sxs-lookup"><span data-stu-id="25939-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="25939-199">Se **true**, il sottosistema di eventi WMI deve essere abilitato.</span><span class="sxs-lookup"><span data-stu-id="25939-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="25939-200">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-201">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="25939-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="25939-202">**EnableStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="25939-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-203">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="25939-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25939-204">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-205">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")</span><span class="sxs-lookup"><span data-stu-id="25939-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="25939-206">Se **true**, WMI crea un heap preallocato con la dimensione del valore **LastStartupHeapPreallocation** quando WMI viene inizializzato.</span><span class="sxs-lookup"><span data-stu-id="25939-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="25939-207">**HighThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="25939-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-209">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-210">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alta soglia per oggetti client"), [**unità**](../wmisdk/standard-qualifiers.md) ("oggetti al secondo")</span><span class="sxs-lookup"><span data-stu-id="25939-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="25939-211">Frequenza massima con cui è possibile recapitare gli oggetti creati dal provider ai client.</span><span class="sxs-lookup"><span data-stu-id="25939-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="25939-212">Per gestire le differenze di velocità tra provider e client, WMI include gli oggetti nelle code prima di distribuirli ai consumer.</span><span class="sxs-lookup"><span data-stu-id="25939-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="25939-213">Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider.</span><span class="sxs-lookup"><span data-stu-id="25939-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="25939-214">Se la memoria utilizzata dagli oggetti non raccolti raggiunge **LowThresholdOnObjects**, WMI rallenta l'aggiunta di nuovi oggetti nella coda.</span><span class="sxs-lookup"><span data-stu-id="25939-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="25939-215">Se gli eventi non raccolti continuano ad accumularsi e viene raggiunta la quantità massima di tempo di attesa per il recapito di eventi in **MaxWaitOnClientObjects** mentre la memoria usata è in corrispondenza del valore di **HighThresholdOnClientObjects**, WMI non accetta più oggetti dai provider e restituisce **WBEM \_ e \_ \_ \_ memoria insufficiente** ai client.</span><span class="sxs-lookup"><span data-stu-id="25939-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="25939-216">**HighThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="25939-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-217">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-218">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-219">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alta soglia per gli eventi"), [**unità**](../wmisdk/standard-qualifiers.md) ("eventi al secondo")</span><span class="sxs-lookup"><span data-stu-id="25939-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="25939-220">Frequenza massima con cui gli eventi devono essere recapitati ai client.</span><span class="sxs-lookup"><span data-stu-id="25939-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="25939-221">Per gestire le differenze di velocità tra provider e client, WMI Accoda gli eventi prima di distribuirli agli utenti.</span><span class="sxs-lookup"><span data-stu-id="25939-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="25939-222">Per maggiore efficienza, i consumer devono raccogliere gli eventi a un ritmo corrispondente al provider.</span><span class="sxs-lookup"><span data-stu-id="25939-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="25939-223">Se la memoria utilizzata dagli eventi non raccolti raggiunge **LowThresholdOnObjects**, WMI rallenta l'aggiunta di nuovi eventi alla coda.</span><span class="sxs-lookup"><span data-stu-id="25939-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="25939-224">Se gli eventi non raccolti continuano ad accumularsi e viene raggiunta la quantità massima di tempo di attesa per il recapito di eventi in **MaxWaitOnEvents** mentre la memoria usata è in corrispondenza del valore di **HighThresholdOnEvents**, WMI non accetta più eventi dai provider e restituisce **WBEM \_ e \_ \_ \_ memoria insufficiente** ai client.</span><span class="sxs-lookup"><span data-stu-id="25939-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="25939-225">La limitazione viene eseguita solo per i consumer di eventi permanenti, quindi i consumer temporanei non dovrebbero prevedere la limitazione quando viene eseguito il backup degli eventi nella coda degli eventi interni WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="25939-226">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-227">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per oggetti client (B)**    </span><span class="sxs-lookup"><span data-stu-id="25939-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="25939-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="25939-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-229">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-231">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Installation Directory")</span><span class="sxs-lookup"><span data-stu-id="25939-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="25939-232">Percorso della directory in cui è stato installato il software WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="25939-233">Il percorso predefinito è \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="25939-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="25939-234">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-235">**HKEY \_ Directory di installazione del software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \|**</span><span class="sxs-lookup"><span data-stu-id="25939-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="25939-236">**LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="25939-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-237">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-239">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="25939-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="25939-240">Dimensioni dell'heap pre-allocato creato da WMI durante l'inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="25939-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="25939-241">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-242">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**</span><span class="sxs-lookup"><span data-stu-id="25939-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="25939-243">**LoggingDirectory**</span><span class="sxs-lookup"><span data-stu-id="25939-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-245">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-246">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging directory")</span><span class="sxs-lookup"><span data-stu-id="25939-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="25939-247">Percorso della directory che contiene il percorso dei file di registro di sistema WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="25939-248">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-249">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging directory**</span><span class="sxs-lookup"><span data-stu-id="25939-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="25939-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="25939-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-251">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-252">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-253">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging")</span><span class="sxs-lookup"><span data-stu-id="25939-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="25939-254">Abilitazione della registrazione degli eventi e del livello di dettaglio della registrazione usata.</span><span class="sxs-lookup"><span data-stu-id="25939-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="25939-255">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-256">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| Logging**</span><span class="sxs-lookup"><span data-stu-id="25939-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="25939-257">**Disattivato** (0)</span><span class="sxs-lookup"><span data-stu-id="25939-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="25939-258">**Registrazione degli errori** (1)</span><span class="sxs-lookup"><span data-stu-id="25939-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="25939-259">**Registrazione dettagliata degli errori** (2)</span><span class="sxs-lookup"><span data-stu-id="25939-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25939-260">**LowThresholdOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="25939-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-261">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-262">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-263">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| bassa soglia per oggetti client"), [**unità**](../wmisdk/standard-qualifiers.md) ("oggetti al secondo")</span><span class="sxs-lookup"><span data-stu-id="25939-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="25939-264">Frequenza con cui WMI inizia a rallentare la creazione di nuovi oggetti creati per i client.</span><span class="sxs-lookup"><span data-stu-id="25939-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="25939-265">Per gestire le differenze di velocità tra provider e client, WMI include gli oggetti nelle code prima di distribuirli ai consumer.</span><span class="sxs-lookup"><span data-stu-id="25939-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="25939-266">Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider.</span><span class="sxs-lookup"><span data-stu-id="25939-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="25939-267">Se il numero di richieste per gli oggetti raggiunge **LowThresholdOnClientObjects**, WMI rallenta gradualmente la creazione di nuovi oggetti in modo che corrispondano alla frequenza di utilizzo del client.</span><span class="sxs-lookup"><span data-stu-id="25939-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="25939-268">Questo rallentamento inizia quando la velocità con cui vengono creati gli oggetti supera il valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="25939-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="25939-269">Vedere **HighThresholdOnClientObjects**.</span><span class="sxs-lookup"><span data-stu-id="25939-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="25939-270">Questa proprietà riflette il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-270">This property reflects the registry value.</span></span>

<span data-ttu-id="25939-271">**Chiave \_ di Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per oggetti client (B)**    </span><span class="sxs-lookup"><span data-stu-id="25939-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="25939-272">**LowThresholdOnEvents**</span><span class="sxs-lookup"><span data-stu-id="25939-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-274">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-275">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| soglia bassa per gli eventi"), [**unità**](../wmisdk/standard-qualifiers.md) ("eventi al secondo")</span><span class="sxs-lookup"><span data-stu-id="25939-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="25939-276">Frequenza con cui WMI inizia a rallentare il recapito di nuovi eventi.</span><span class="sxs-lookup"><span data-stu-id="25939-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="25939-277">Per gestire le differenze di velocità tra provider e client, WMI Accoda gli eventi prima di distribuirli agli utenti.</span><span class="sxs-lookup"><span data-stu-id="25939-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="25939-278">Per maggiore efficienza, i consumer devono raccogliere gli oggetti a un ritmo corrispondente al provider.</span><span class="sxs-lookup"><span data-stu-id="25939-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="25939-279">Se la coda cresce fuori controllo, le limitazioni di WMI rallentano, ovvero il recapito degli eventi gradualmente per allinearsi alla velocità del client.</span><span class="sxs-lookup"><span data-stu-id="25939-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="25939-280">Questo rallentamento inizia quando la frequenza con cui vengono generati gli eventi supera il valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="25939-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="25939-281">Vedere **HighThresholdOnEvents**.</span><span class="sxs-lookup"><span data-stu-id="25939-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="25939-282">La limitazione viene eseguita solo per i consumer di eventi permanenti, quindi i consumer temporanei non dovrebbero prevedere la limitazione quando viene eseguito il backup degli eventi nella coda degli eventi interni WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="25939-283">Questa proprietà riflette il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-283">This property reflects the registry value.</span></span>

<span data-ttu-id="25939-284">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| High Threshold per gli oggetti client {B}**    </span><span class="sxs-lookup"><span data-stu-id="25939-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="25939-285">**MaxLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="25939-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-286">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-287">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-288">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log file di dimensioni massime"), [**unità**](../wmisdk/standard-qualifiers.md) ("byte")</span><span class="sxs-lookup"><span data-stu-id="25939-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="25939-289">Dimensioni massime dei file di log generati dal servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="25939-290">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-291">**HKEY \_ \_** \\  \\  \\ **\| \| Dimensioni massime del file di log** del software del computer locale Microsoft WBEM CIMOM</span><span class="sxs-lookup"><span data-stu-id="25939-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="25939-292">**MaxWaitOnClientObjects**</span><span class="sxs-lookup"><span data-stu-id="25939-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-293">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-294">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-295">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="25939-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="25939-296">Quantità di tempo in cui un oggetto appena creato resta in attesa di essere utilizzato dal client prima che venga eliminato e viene restituito un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="25939-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="25939-297">Questa proprietà interagisce con le proprietà **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** per limitare, rallentare, il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.</span><span class="sxs-lookup"><span data-stu-id="25939-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="25939-298">**MaxWaitOnEvents**</span><span class="sxs-lookup"><span data-stu-id="25939-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-299">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25939-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25939-300">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="25939-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="25939-301">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max wait on Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span><span class="sxs-lookup"><span data-stu-id="25939-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="25939-302">Quantità di tempo per cui un evento inviato a un client viene accodato prima di essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="25939-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="25939-303">Questa proprietà interacts0 con **LowThresholdOnEvents** e **HighThresholdOnEvents** per limitare il rallentamento, ovvero il recapito di oggetti ai consumer quando il consumer riceve gli oggetti troppo lentamente.</span><span class="sxs-lookup"><span data-stu-id="25939-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="25939-304">Questa proprietà riflette il valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-304">This property reflects the registry value.</span></span>

<span data-ttu-id="25939-305">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Max Wait for Events (MS)**    </span><span class="sxs-lookup"><span data-stu-id="25939-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="25939-306">**MofSelfInstallDirectory**</span><span class="sxs-lookup"><span data-stu-id="25939-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-309">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install directory")</span><span class="sxs-lookup"><span data-stu-id="25939-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="25939-310">Percorso della directory per le applicazioni che installano i file MOF nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="25939-311">WMI compila automaticamente tutti i file MOF presenti in questa directory e, a seconda del suo esito positivo, sposta il file MOF in una sottodirectory contrassegnata come valida o non valida.</span><span class="sxs-lookup"><span data-stu-id="25939-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="25939-312">Se il \# comando [pragma autocover](../wmisdk/pragma-autorecover.md) è incluso, il nome file completo viene aggiunto all'elenco **AutoRecoverMofs** usato durante l'inizializzazione o il recupero del repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="25939-313">L'elenco determina l'ordine in cui vengono compilate file MOF.</span><span class="sxs-lookup"><span data-stu-id="25939-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="25939-314">Questa proprietà riflette il valore nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="25939-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="25939-315">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = install directory**</span><span class="sxs-lookup"><span data-stu-id="25939-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="25939-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="25939-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25939-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="25939-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25939-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25939-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25939-319">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="25939-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="25939-320">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="25939-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="25939-321">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="25939-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25939-322">Commenti</span><span class="sxs-lookup"><span data-stu-id="25939-322">Remarks</span></span>

<span data-ttu-id="25939-323">La classe **Win32 \_ WMISetting** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="25939-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="25939-324">In un computer può esistere una sola istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="25939-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="25939-325">Sapere come WMI è configurato in un computer può essere molto utile quando si esegue il debug di script o si risolvono problemi con il servizio WMI stesso.</span><span class="sxs-lookup"><span data-stu-id="25939-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="25939-326">Molti script WMI, ad esempio, vengono scritti nel presupposto che root \\ CIMV2 sia lo spazio dei nomi predefinito nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="25939-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="25939-327">Di conseguenza, gli autori di script che devono accedere a una classe in "root \\ CIMv2" spesso non riescono a includere lo spazio dei nomi nel moniker GetObject, come illustrato nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="25939-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="25939-328">Se il \\ CIMV2 radice non è lo spazio dei nomi predefinito nel computer di destinazione, lo script avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="25939-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="25939-329">Per evitare che ciò accada, è necessario includere il CIMV2 radice dello spazio dei nomi \\ nel moniker, come illustrato nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="25939-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="25939-330">Se lo spazio dei nomi predefinito nel computer di destinazione è diverso dallo spazio dei nomi utilizzato da uno script, lo script avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="25939-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="25939-331">A questo proposito, all'utente viene visualizzato il messaggio di errore "classe non valida".</span><span class="sxs-lookup"><span data-stu-id="25939-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="25939-332">In realtà, l'errore non è dovuto al fatto che la classe non è valida, ma perché non è possibile trovare la classe nello spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="25939-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="25939-333">Si tratta di un problema difficile da risolvere, perché è probabile che si verifichino possibili problemi con la classe piuttosto che problemi con lo spazio dei nomi (o, in questo caso, non è stato specificato).</span><span class="sxs-lookup"><span data-stu-id="25939-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="25939-334">È possibile utilizzare la classe **Win32 \_ WMISetting** per determinare la modalità di configurazione di WMI in un computer.</span><span class="sxs-lookup"><span data-stu-id="25939-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="25939-335">I dettagli di configurazione come lo spazio dei nomi predefinito o il numero di build WMI possono essere utili per la risoluzione dei problemi relativi agli script.</span><span class="sxs-lookup"><span data-stu-id="25939-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="25939-336">Queste impostazioni forniscono inoltre informazioni amministrative importanti, ad esempio come, o anche se, gli errori WMI vengono registrati in un computer e quali provider WMI verranno ricaricati automaticamente se è necessario ricompilare il repository WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="25939-337">Esempio</span><span class="sxs-lookup"><span data-stu-id="25939-337">Examples</span></span>

<span data-ttu-id="25939-338">Nell'esempio relativo alla [modifica delle impostazioni WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) per il codice VBScript della raccolta TechNet viene utilizzata la classe **Win32 \_ WMISetting** per configurare l'intervallo di backup e il livello di registrazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="25939-339">L'esempio di codice VBScript [dello spazio dei nomi predefinito](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) nella raccolta TechNet usa la classe **Win32 \_ WMISetting** per recuperare e visualizzare l'impostazione WMI corrente "spazio dei nomi predefinito per lo scripting".</span><span class="sxs-lookup"><span data-stu-id="25939-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="25939-340">Nell'esempio relativo alla [modifica del codice VBScript dello spazio dei nomi WMI predefinito](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) nella raccolta TechNet viene utilizzata la proprietà **ASPScriptDefaultNamespace** per impostare l'impostazione "spazio dei nomi predefinito per lo script" di WMI su "root \\ cimv2".</span><span class="sxs-lookup"><span data-stu-id="25939-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="25939-341">L' [elenco di tutti gli](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) esempi di codice VBSCript delle impostazioni WMI usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.</span><span class="sxs-lookup"><span data-stu-id="25939-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="25939-342">L' [elenco di informazioni sull'impostazione WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) di esempio codice JavaScript usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.</span><span class="sxs-lookup"><span data-stu-id="25939-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="25939-343">L'elenco di esempi di codice Python per [informazioni sull'impostazione WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.</span><span class="sxs-lookup"><span data-stu-id="25939-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="25939-344">L' [elenco WMI setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example usa una serie di proprietà in **Win32 \_ WMISetting** per restituire un elenco di impostazioni WMI configurate in un computer.</span><span class="sxs-lookup"><span data-stu-id="25939-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="25939-345">Nell'esempio di codice VBScript riportato di seguito viene illustrato come ottenere la versione di WMI in esecuzione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="25939-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="25939-346">"Win32 \_ WMISetting = @" indica la singola istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="25939-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="25939-347">Per ulteriori informazioni, vedere versioni WMI.</span><span class="sxs-lookup"><span data-stu-id="25939-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="25939-348">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25939-348">Requirements</span></span>



| <span data-ttu-id="25939-349">Requisito</span><span class="sxs-lookup"><span data-stu-id="25939-349">Requirement</span></span> | <span data-ttu-id="25939-350">Valore</span><span class="sxs-lookup"><span data-stu-id="25939-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25939-351">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25939-351">Minimum supported client</span></span><br/> | <span data-ttu-id="25939-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25939-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25939-353">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25939-353">Minimum supported server</span></span><br/> | <span data-ttu-id="25939-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25939-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25939-355">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="25939-355">Namespace</span></span><br/>                | <span data-ttu-id="25939-356">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="25939-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25939-357">MOF</span><span class="sxs-lookup"><span data-stu-id="25939-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25939-358"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25939-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25939-359">DLL</span><span class="sxs-lookup"><span data-stu-id="25939-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25939-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25939-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25939-361">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25939-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25939-362">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="25939-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="25939-363">Classi di gestione del servizio WMI</span><span class="sxs-lookup"><span data-stu-id="25939-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
