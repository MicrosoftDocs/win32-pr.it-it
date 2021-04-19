---
description: La \_ classe WMI BootConfiguration Win32 rappresenta la configurazione di avvio di un sistema di computer che esegue Windows.
ms.assetid: c2db28dd-3feb-44bb-a532-c91cab980ba3
ms.tgt_platform: multiple
title: Classe Win32_BootConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BootConfiguration
- Win32_BootConfiguration.Caption
- Win32_BootConfiguration.Description
- Win32_BootConfiguration.SettingID
- Win32_BootConfiguration.BootDirectory
- Win32_BootConfiguration.ConfigurationPath
- Win32_BootConfiguration.LastDrive
- Win32_BootConfiguration.Name
- Win32_BootConfiguration.ScratchDirectory
- Win32_BootConfiguration.TempDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 556688d7c80038f04dd5b94b7c61c5d6dfef3199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305171"
---
# <a name="win32_bootconfiguration-class"></a><span data-ttu-id="b2202-103">Win32 \_ BootConfiguration (classe)</span><span class="sxs-lookup"><span data-stu-id="b2202-103">Win32\_BootConfiguration class</span></span>

<span data-ttu-id="b2202-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BootConfiguration Win32** rappresenta la configurazione di avvio di un sistema di computer che esegue Windows.</span><span class="sxs-lookup"><span data-stu-id="b2202-104">The **Win32\_BootConfiguration** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the boot configuration of a computer system running Windows.</span></span>

<span data-ttu-id="b2202-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b2202-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b2202-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="b2202-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2202-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2202-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BootConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string BootDirectory;
  string ConfigurationPath;
  string LastDrive;
  string Name;
  string ScratchDirectory;
  string TempDirectory;
};
```

## <a name="members"></a><span data-ttu-id="b2202-108">Members</span><span class="sxs-lookup"><span data-stu-id="b2202-108">Members</span></span>

<span data-ttu-id="b2202-109">La classe **Win32 \_ BootConfiguration** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b2202-109">The **Win32\_BootConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b2202-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2202-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2202-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b2202-111">Properties</span></span>

<span data-ttu-id="b2202-112">La classe **Win32 \_ BootConfiguration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b2202-112">The **Win32\_BootConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2202-113">**BootDirectory**</span><span class="sxs-lookup"><span data-stu-id="b2202-113">**BootDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-116">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="b2202-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-117">Percorso dei file di sistema necessari per l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2202-117">Path to the system files required for booting the system.</span></span>

<span data-ttu-id="b2202-118">Esempio: "C: \\ Windows"</span><span class="sxs-lookup"><span data-stu-id="b2202-118">Example: "C:\\Windows"</span></span>

</dd> <dt>

<span data-ttu-id="b2202-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b2202-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b2202-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b2202-123">Breve descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="b2202-123">Short textual description of the current object.</span></span>

<span data-ttu-id="b2202-124">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b2202-124">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2202-125">**ConfigurationPath**</span><span class="sxs-lookup"><span data-stu-id="b2202-125">**ConfigurationPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-128">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Process and thread Functions \| [**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable) \| WinBootDir")</span><span class="sxs-lookup"><span data-stu-id="b2202-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Process and Thread Functions\|[**GetEnvironmentVariable**](/windows/desktop/api/winbase/nf-winbase-getenvironmentvariable)\|WinBootDir")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-129">Percorso dei file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b2202-129">Path to the configuration files.</span></span> <span data-ttu-id="b2202-130">Questo valore può essere simile al valore nella proprietà **BootDirectory** .</span><span class="sxs-lookup"><span data-stu-id="b2202-130">This value may be similar to the value in the **BootDirectory** property.</span></span>

</dd> <dt>

<span data-ttu-id="b2202-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b2202-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2202-134">Descrizione testuale dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="b2202-134">Textual description of the current object.</span></span>

<span data-ttu-id="b2202-135">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b2202-135">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2202-136">**LastDrive**</span><span class="sxs-lookup"><span data-stu-id="b2202-136">**LastDrive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetDriveType")</span><span class="sxs-lookup"><span data-stu-id="b2202-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetDriveType")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-140">Ultima lettera di unità a cui è assegnata un'unità fisica.</span><span class="sxs-lookup"><span data-stu-id="b2202-140">Last drive letter to which a physical drive is assigned.</span></span>

<span data-ttu-id="b2202-141">Esempio: "E:"</span><span class="sxs-lookup"><span data-stu-id="b2202-141">Example: "E:"</span></span>

</dd> <dt>

<span data-ttu-id="b2202-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b2202-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-145">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b2202-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-146">Nome della configurazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="b2202-146">Name of the boot configuration.</span></span> <span data-ttu-id="b2202-147">Si tratta di un identificatore per la configurazione di avvio.</span><span class="sxs-lookup"><span data-stu-id="b2202-147">It is an identifier for the boot configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b2202-148">**ScratchDirectory**</span><span class="sxs-lookup"><span data-stu-id="b2202-148">**ScratchDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-151">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="b2202-151">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-152">Directory in cui possono risiedere i file temporanei in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="b2202-152">Directory where temporary files can reside during boot time.</span></span>

</dd> <dt>

<span data-ttu-id="b2202-153">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b2202-153">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-156">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b2202-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b2202-157">Identificatore con cui è noto l'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="b2202-157">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b2202-158">Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b2202-158">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2202-159">**TempDirectory**</span><span class="sxs-lookup"><span data-stu-id="b2202-159">**TempDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2202-160">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b2202-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b2202-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b2202-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2202-162">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| file functions \| GetTempPath")</span><span class="sxs-lookup"><span data-stu-id="b2202-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|GetTempPath")</span></span>
</dt> </dl>

<span data-ttu-id="b2202-163">Directory in cui vengono archiviati i file temporanei.</span><span class="sxs-lookup"><span data-stu-id="b2202-163">Directory where temporary files are stored.</span></span>

<span data-ttu-id="b2202-164">Esempio: "C: \\ Temp"</span><span class="sxs-lookup"><span data-stu-id="b2202-164">Example: "C:\\TEMP"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2202-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2202-165">Remarks</span></span>

<span data-ttu-id="b2202-166">La classe **Win32 \_ BootConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b2202-166">The **Win32\_BootConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b2202-167">Esempio</span><span class="sxs-lookup"><span data-stu-id="b2202-167">Examples</span></span>

<span data-ttu-id="b2202-168">L' [elenco delle proprietà di configurazione di avvio di un esempio di computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl restituisce le informazioni di configurazione di avvio per un computer.</span><span class="sxs-lookup"><span data-stu-id="b2202-168">The [List the Boot Configuration Properties of a Computer](https://Gallery.TechNet.Microsoft.Com/55c35de3-bb6a-47f0-89f9-d2c49ab4cf19) Perl sample returns boot configuration information for a computer.</span></span>

<span data-ttu-id="b2202-169">Nell'esempio VBScript seguente vengono restituite informazioni sulla configurazione di avvio per un computer.</span><span class="sxs-lookup"><span data-stu-id="b2202-169">The following VBScript sample returns boot configuration information for a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BootConfiguration") 
 
For Each objItem in colItems 
    Wscript.Echo "Boot Directory: " & objItem.BootDirectory 
    Wscript.Echo "Configuration Path: " & objItem.ConfigurationPath 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Last Drive: " & objItem.LastDrive 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Scratch Directory: " & objItem.ScratchDirectory 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Temp Directory: " & objItem.TempDirectory 
Next 
```



<span data-ttu-id="b2202-170">Nell'esempio di codice seguente viene illustrato l'utilizzo della classe WMI **Win32 \_ BootConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="b2202-170">The following code sample demonstrates the use of the **Win32\_BootConfiguration** WMI class.</span></span>


```PowerShell
# Get Boot configuration from WMI

$boot = Get-WMIObject Win32_BootConfiguration

# Display information

"Boot Directory     : {0}" -f $boot.bootdirectory
"Caption            : {0}" -f $boot.caption
"Description        : {0}" -f $boot.description
"Last Drive         : {0}" -f $boot.lastdrive
"Scratch Directory  : {0}" -f $boot.scratchdirectory
"Temp Directory     : {0}" -f $boot.tempdirectory

```



<span data-ttu-id="b2202-171">L'esempio di codice precedente crea l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="b2202-171">The previous code sample creates the following output:</span></span>

``` syntax
Boot Directory     : \WINDOWS
Caption            : \Device\Harddisk0\Partition1
Description        : \Device\Harddisk0\Partition1
Last Drive         : K:
Scratch Directory  : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
Temp Directory     : C:\WINDOWS\system32\config\systemprofile\Local Settings\Temp
```

## <a name="requirements"></a><span data-ttu-id="b2202-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2202-172">Requirements</span></span>



| <span data-ttu-id="b2202-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2202-173">Requirement</span></span> | <span data-ttu-id="b2202-174">Valore</span><span class="sxs-lookup"><span data-stu-id="b2202-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2202-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2202-175">Minimum supported client</span></span><br/> | <span data-ttu-id="b2202-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b2202-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b2202-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2202-177">Minimum supported server</span></span><br/> | <span data-ttu-id="b2202-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b2202-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b2202-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b2202-179">Namespace</span></span><br/>                | <span data-ttu-id="b2202-180">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="b2202-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b2202-181">MOF</span><span class="sxs-lookup"><span data-stu-id="b2202-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2202-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2202-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2202-183">DLL</span><span class="sxs-lookup"><span data-stu-id="b2202-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2202-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2202-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2202-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2202-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2202-186">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="b2202-186">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="b2202-187">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2202-187">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

