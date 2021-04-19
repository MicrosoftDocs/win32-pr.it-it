---
description: Win32 \_ OSRecoveryConfiguration&\# 8194; La classe WMI rappresenta i tipi di informazioni che verranno raccolte dalla memoria quando si verifica un errore nel sistema operativo. Sono inclusi errori di avvio e arresti anomali del sistema.
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Classe Win32_OSRecoveryConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305159"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="fd6f1-104">Win32 \_ OSRecoveryConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="fd6f1-105">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OSRecoveryConfiguration Win32** rappresenta i tipi di informazioni che verranno raccolte dalla memoria quando si verifica un errore nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="fd6f1-106">Sono inclusi errori di avvio e arresti anomali del sistema.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="fd6f1-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fd6f1-108">Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6f1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd6f1-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="fd6f1-110">Members</span><span class="sxs-lookup"><span data-stu-id="fd6f1-110">Members</span></span>

<span data-ttu-id="fd6f1-111">La classe **Win32 \_ OSRecoveryConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fd6f1-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="fd6f1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd6f1-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd6f1-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fd6f1-113">Properties</span></span>

<span data-ttu-id="fd6f1-114">La classe **Win32 \_ OSRecoveryConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd6f1-115">**AutoReboot**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-116">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-117">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-118">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| autoriavvio")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-119">Il sistema verrà riavviato automaticamente durante un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-120">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-123">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-124">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-124">Short textual description of the current object.</span></span>

<span data-ttu-id="fd6f1-125">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fd6f1-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-126">**DebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-129">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| dumpfile")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-130">Percorso completo del file di debug.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-130">Full path to the debug file.</span></span> <span data-ttu-id="fd6f1-131">Un file di debug viene creato con lo stato della memoria del computer dopo un errore del computer.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="fd6f1-132">Esempio: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="fd6f1-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-133">**DebugInfoType**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-135">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-136">Tipo di informazioni di debug scritte nel file di log.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="fd6f1-137">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="fd6f1-138">**Dump completo memoria** (1)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="fd6f1-139">**Dump memoria kernel** (2)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="fd6f1-140">**Dump memoria piccola** (3)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fd6f1-141">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-144">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-144">Textual description of the current object.</span></span>

<span data-ttu-id="fd6f1-145">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fd6f1-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-146">**ExpandedDebugFilePath**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-149">Versione espansa della proprietà **DebugFilePath** .</span><span class="sxs-lookup"><span data-stu-id="fd6f1-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="fd6f1-150">Esempio: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="fd6f1-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-151">**ExpandedMiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-154">Versione espansa della proprietà **MiniDumpDirectory** .</span><span class="sxs-lookup"><span data-stu-id="fd6f1-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="fd6f1-155">Esempio: "C: \\ minidump di Windows \\ "</span><span class="sxs-lookup"><span data-stu-id="fd6f1-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-156">**KernelDumpOnly**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-157">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-158">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-159">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| KernelDumpOnly")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-160">Solo le informazioni di debug del kernel verranno scritte nel file di log di debug.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="fd6f1-161">Se **true**, solo lo stato del kernel viene scritto in un file in caso di errore di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="fd6f1-162">Se **false**, il sistema tenterà di registrare lo stato della memoria e di tutti i dispositivi in grado di fornire informazioni sul sistema in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-163">**MiniDumpDirectory**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-166">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| MiniDumpDir")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-167">Directory in cui verranno registrati e accumulati i file di dump di memoria di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="fd6f1-168">Esempio: "% systemRoot% \\ minidump"</span><span class="sxs-lookup"><span data-stu-id="fd6f1-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-169">**Nome**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-172">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-173">Identificazione del nome per questa istanza della classe **Win32 \_ OSRecoveryConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="fd6f1-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-174">**OverwriteExistingDebugFile**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-175">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-176">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-177">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| overwrite")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-178">Il nuovo file di debug sovrascriverà uno esistente.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-179">**SendAdminAlert**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-182">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| SendAlert")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-183">Il messaggio di avviso verrà inviato all'amministratore di sistema in caso di errore del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-187">Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="fd6f1-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-188">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="fd6f1-189">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fd6f1-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-190">**WriteDebugInfo**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-191">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-193">Qualificatori: [**deprecato**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| CrashDumpEnabled")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-194">Le informazioni di debug devono essere scritte in un file di log.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="fd6f1-195">**WriteToSystemLog**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd6f1-196">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-197">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="fd6f1-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fd6f1-198">Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ CrashControl \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="fd6f1-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="fd6f1-199">Gli eventi verranno scritti in un registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd6f1-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd6f1-200">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd6f1-200">Remarks</span></span>

<span data-ttu-id="fd6f1-201">La classe **Win32 \_ OSRecoveryConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="fd6f1-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6f1-202">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd6f1-202">Requirements</span></span>



| <span data-ttu-id="fd6f1-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6f1-203">Requirement</span></span> | <span data-ttu-id="fd6f1-204">Valore</span><span class="sxs-lookup"><span data-stu-id="fd6f1-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6f1-205">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd6f1-205">Minimum supported client</span></span><br/> | <span data-ttu-id="fd6f1-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd6f1-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd6f1-207">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd6f1-207">Minimum supported server</span></span><br/> | <span data-ttu-id="fd6f1-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd6f1-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd6f1-209">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd6f1-209">Namespace</span></span><br/>                | <span data-ttu-id="fd6f1-210">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fd6f1-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd6f1-211">MOF</span><span class="sxs-lookup"><span data-stu-id="fd6f1-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd6f1-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd6f1-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd6f1-213">DLL</span><span class="sxs-lookup"><span data-stu-id="fd6f1-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd6f1-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd6f1-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd6f1-215">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd6f1-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6f1-216">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="fd6f1-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="fd6f1-217">Classi del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fd6f1-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
