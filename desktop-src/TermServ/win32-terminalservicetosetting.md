---
title: Classe Win32_TerminalServiceToSetting
description: Rappresenta l'associazione tra un'istanza della classe Win32 \_ TerminalService e l'impostazione di una particolare \_ Proprietà TerminalServiceSetting Win32.
ms.assetid: 4c206812-7549-4410-b6ba-1163f20d2bee
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalServiceToSetting Servizi Desktop remoto
- Classe Win32_TerminalServiceToSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalServiceToSetting
- Win32_TerminalServiceToSetting.Caption
- Win32_TerminalServiceToSetting.Description
- Win32_TerminalServiceToSetting.InstallDate
- Win32_TerminalServiceToSetting.Name
- Win32_TerminalServiceToSetting.Status
- Win32_TerminalServiceToSetting.Element
- Win32_TerminalServiceToSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d37a255b0a894ab257166f17c765f009d33b075
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400564"
---
# <a name="win32_terminalservicetosetting-class"></a><span data-ttu-id="acb63-105">Win32 \_ TerminalServiceToSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="acb63-105">Win32\_TerminalServiceToSetting class</span></span>

<span data-ttu-id="acb63-106">La classe WMI **\_ TerminalServiceToSetting Win32** rappresenta l'associazione tra un'istanza della classe [**\_ TerminalService Win32**](win32-terminalservice.md) e l'impostazione di una particolare proprietà [**\_ TerminalServiceSetting Win32**](win32-terminalservicesetting.md) .</span><span class="sxs-lookup"><span data-stu-id="acb63-106">The **Win32\_TerminalServiceToSetting** WMI class represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span> <span data-ttu-id="acb63-107">Le impostazioni di configurazione includono host sessione Desktop remoto modalità server Host sessione Desktop remoto, licenze, desktop attivo, funzionalità autorizzazioni, eliminazione di cartelle temporanee e cartelle temporanee per sessione.</span><span class="sxs-lookup"><span data-stu-id="acb63-107">Configuration settings include Remote Desktop Session Host (RD Session Host) server mode, Licensing, Active Desktop, Permissions Capability, Deletion of Temporary Folders and Temporary Folders-Per-Session.</span></span>

<span data-ttu-id="acb63-108">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite.</span><span class="sxs-lookup"><span data-stu-id="acb63-108">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="acb63-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="acb63-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TERMINALSERVICETOSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceToSetting : CIM_ElementSetting
{
  string                           Caption;
  string                           Description;
  datetime                         InstallDate;
  string                           Name;
  string                           Status;
  Win32_TerminalService        REF Element;
  Win32_TerminalServiceSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="acb63-110">Members</span><span class="sxs-lookup"><span data-stu-id="acb63-110">Members</span></span>

<span data-ttu-id="acb63-111">La classe **Win32 \_ TerminalServiceToSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="acb63-111">The **Win32\_TerminalServiceToSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="acb63-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acb63-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acb63-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="acb63-113">Properties</span></span>

<span data-ttu-id="acb63-114">La classe **Win32 \_ TerminalServiceToSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="acb63-114">The **Win32\_TerminalServiceToSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acb63-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="acb63-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acb63-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acb63-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="acb63-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="acb63-119">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acb63-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="acb63-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="acb63-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="acb63-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="acb63-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acb63-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acb63-124">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acb63-124">Description of the object.</span></span>

<span data-ttu-id="acb63-125">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="acb63-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="acb63-126">**elemento**</span><span class="sxs-lookup"><span data-stu-id="acb63-126">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-127">Tipo di dati: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="acb63-127">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acb63-129">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="acb63-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="acb63-130">Rappresenta l'istanza di [**Win32 \_ TerminalService**](win32-terminalservice.md) che può essere configurata con la proprietà **Setting** .</span><span class="sxs-lookup"><span data-stu-id="acb63-130">Represents the instance of [**Win32\_TerminalService**](win32-terminalservice.md) that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="acb63-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="acb63-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-132">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="acb63-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acb63-134">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="acb63-134">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="acb63-135">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acb63-135">The date the object was installed.</span></span> <span data-ttu-id="acb63-136">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="acb63-136">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="acb63-137">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="acb63-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="acb63-138">**Nome**</span><span class="sxs-lookup"><span data-stu-id="acb63-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acb63-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="acb63-141">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acb63-141">The name of the object.</span></span>

<span data-ttu-id="acb63-142">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="acb63-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="acb63-143">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="acb63-143">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-144">Tipo di dati: **Win32 \_ TerminalServiceSetting**</span><span class="sxs-lookup"><span data-stu-id="acb63-144">Data type: **Win32\_TerminalServiceSetting**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acb63-146">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="acb63-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="acb63-147">Rappresenta le impostazioni di configurazione Servizi Desktop remoto che è possibile applicare al server Host sessione Desktop remoto associato.</span><span class="sxs-lookup"><span data-stu-id="acb63-147">Represents the Remote Desktop Services configuration settings that can be applied to the associated RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="acb63-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="acb63-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acb63-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="acb63-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="acb63-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="acb63-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acb63-151">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="acb63-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="acb63-152">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="acb63-152">Current status of the object.</span></span> <span data-ttu-id="acb63-153">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="acb63-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="acb63-154">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="acb63-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="acb63-155">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="acb63-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="acb63-156">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="acb63-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="acb63-157">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="acb63-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="acb63-158">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="acb63-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="acb63-159">("OK")</span><span class="sxs-lookup"><span data-stu-id="acb63-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-160">("Errore")</span><span class="sxs-lookup"><span data-stu-id="acb63-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-161">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="acb63-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-162">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="acb63-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-163">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="acb63-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-164">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="acb63-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-165">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="acb63-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="acb63-166">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="acb63-166">("Service")</span></span>


<span data-ttu-id="acb63-167"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="acb63-167"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="acb63-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="acb63-168">Remarks</span></span>

<span data-ttu-id="acb63-169">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="acb63-169">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="acb63-170">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="acb63-170">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="acb63-171">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="acb63-171">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="acb63-172">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="acb63-172">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="acb63-173">Requisiti</span><span class="sxs-lookup"><span data-stu-id="acb63-173">Requirements</span></span>



| <span data-ttu-id="acb63-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb63-174">Requirement</span></span> | <span data-ttu-id="acb63-175">Valore</span><span class="sxs-lookup"><span data-stu-id="acb63-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acb63-176">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acb63-176">Minimum supported client</span></span><br/> | <span data-ttu-id="acb63-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acb63-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acb63-178">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="acb63-178">Minimum supported server</span></span><br/> | <span data-ttu-id="acb63-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acb63-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acb63-180">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="acb63-180">Namespace</span></span><br/>                | <span data-ttu-id="acb63-181">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="acb63-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="acb63-182">MOF</span><span class="sxs-lookup"><span data-stu-id="acb63-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acb63-183"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acb63-183"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="acb63-184">DLL</span><span class="sxs-lookup"><span data-stu-id="acb63-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acb63-185"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acb63-185"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acb63-186">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="acb63-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb63-187">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="acb63-187">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="acb63-188">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="acb63-188">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="acb63-189">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="acb63-189">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="acb63-190">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="acb63-190">**CIM\_ElementSetting**</span></span>](/windows/desktop/CIMWin32Prov/cim-elementsetting)
</dt> </dl>

 

