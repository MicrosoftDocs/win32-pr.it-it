---
title: Classe Win32_TSSessionDirectorySetting
description: Rappresenta l'associazione tra un'istanza della classe Win32 \_ TerminalService e un'istanza della \_ classe TSSessionDirectory Win32.
ms.assetid: b6350f7b-386f-4f6b-8ab1-29d5d21fae02
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSessionDirectorySetting Servizi Desktop remoto
- Classe Win32_TSSessionDirectorySetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectorySetting
- Win32_TSSessionDirectorySetting.Caption
- Win32_TSSessionDirectorySetting.Description
- Win32_TSSessionDirectorySetting.InstallDate
- Win32_TSSessionDirectorySetting.Name
- Win32_TSSessionDirectorySetting.Status
- Win32_TSSessionDirectorySetting.Element
- Win32_TSSessionDirectorySetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 667f501ff850cb7ee8c40448de11c06898ab8a85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047952"
---
# <a name="win32_tssessiondirectorysetting-class"></a><span data-ttu-id="f8274-105">Win32 \_ TSSessionDirectorySetting (classe)</span><span class="sxs-lookup"><span data-stu-id="f8274-105">Win32\_TSSessionDirectorySetting class</span></span>

<span data-ttu-id="f8274-106">Rappresenta l'associazione tra un'istanza della classe [**Win32 \_ TerminalService**](win32-terminalservice.md) e un'istanza della classe [**\_ TSSessionDirectory Win32**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="f8274-106">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

<span data-ttu-id="f8274-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="f8274-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8274-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8274-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSSESSIONDIRECTORYSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectorySetting : CIM_ElementSetting
{
  string                       Caption;
  string                       Description;
  datetime                     InstallDate;
  string                       Name;
  string                       Status;
  Win32_TerminalService    REF Element;
  Win32_TSSessionDirectory REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="f8274-109">Members</span><span class="sxs-lookup"><span data-stu-id="f8274-109">Members</span></span>

<span data-ttu-id="f8274-110">La classe **Win32 \_ TSSessionDirectorySetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8274-110">The **Win32\_TSSessionDirectorySetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f8274-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8274-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8274-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8274-112">Properties</span></span>

<span data-ttu-id="f8274-113">La classe **Win32 \_ TSSessionDirectorySetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8274-113">The **Win32\_TSSessionDirectorySetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8274-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f8274-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8274-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8274-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8274-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8274-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8274-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f8274-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8274-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8274-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f8274-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8274-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8274-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8274-123">Description of the object.</span></span>

<span data-ttu-id="f8274-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8274-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8274-125">**elemento**</span><span class="sxs-lookup"><span data-stu-id="f8274-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-126">Tipo di dati: **Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="f8274-126">Data type: **Win32\_TerminalService**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8274-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8274-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f8274-129">Rappresenta l'istanza di **Win32 \_ TerminalService** che può essere configurata con la proprietà **Setting** .</span><span class="sxs-lookup"><span data-stu-id="f8274-129">Represents the instance of **Win32\_TerminalService** that can be configured with the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="f8274-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8274-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8274-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8274-133">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f8274-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f8274-134">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8274-134">The date the object was installed.</span></span> <span data-ttu-id="f8274-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f8274-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f8274-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8274-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8274-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f8274-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8274-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8274-140">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8274-140">The name of the object.</span></span>

<span data-ttu-id="f8274-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8274-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8274-142">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="f8274-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-143">Tipo di dati: **Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="f8274-143">Data type: **Win32\_TSSessionDirectory**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8274-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8274-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f8274-146">Rappresenta le impostazioni di gestore connessione Desktop remoto che è possibile applicare al server Host sessione Desktop remoto associato.</span><span class="sxs-lookup"><span data-stu-id="f8274-146">Represents the RD Connection Broker settings that can be applied to the associated RD Session Host Server.</span></span>

</dd> <dt>

<span data-ttu-id="f8274-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="f8274-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8274-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8274-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8274-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8274-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8274-150">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f8274-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f8274-151">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8274-151">Current status of the object.</span></span> <span data-ttu-id="f8274-152">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="f8274-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f8274-153">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="f8274-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f8274-154">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f8274-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f8274-155">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f8274-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f8274-156">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f8274-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f8274-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8274-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f8274-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="f8274-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-159">("Errore")</span><span class="sxs-lookup"><span data-stu-id="f8274-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-160">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="f8274-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-161">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f8274-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-162">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="f8274-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-163">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="f8274-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-164">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="f8274-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8274-165">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="f8274-165">("Service")</span></span>


<span data-ttu-id="f8274-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f8274-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f8274-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8274-167">Remarks</span></span>

<span data-ttu-id="f8274-168">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f8274-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8274-169">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f8274-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f8274-170">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f8274-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8274-171">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f8274-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8274-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8274-172">Requirements</span></span>



| <span data-ttu-id="f8274-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8274-173">Requirement</span></span> | <span data-ttu-id="f8274-174">Valore</span><span class="sxs-lookup"><span data-stu-id="f8274-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8274-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8274-175">Minimum supported client</span></span><br/> | <span data-ttu-id="f8274-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8274-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f8274-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8274-177">Minimum supported server</span></span><br/> | <span data-ttu-id="f8274-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8274-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f8274-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8274-179">Namespace</span></span><br/>                | <span data-ttu-id="f8274-180">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f8274-180">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="f8274-181">MOF</span><span class="sxs-lookup"><span data-stu-id="f8274-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8274-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8274-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8274-183">DLL</span><span class="sxs-lookup"><span data-stu-id="f8274-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8274-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8274-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8274-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8274-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8274-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="f8274-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="f8274-187">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f8274-187">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f8274-188">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="f8274-188">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

