---
title: Classe Win32_TerminalTerminalSetting
description: Rappresenta l'associazione tra un terminale e le relative impostazioni di configurazione.
ms.assetid: c92d79ec-eca5-4a73-a89a-dfc55474d88b
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalTerminalSetting Servizi Desktop remoto
- Classe Win32_TerminalTerminalSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalTerminalSetting
- Win32_TerminalTerminalSetting.Caption
- Win32_TerminalTerminalSetting.Description
- Win32_TerminalTerminalSetting.InstallDate
- Win32_TerminalTerminalSetting.Name
- Win32_TerminalTerminalSetting.Status
- Win32_TerminalTerminalSetting.Element
- Win32_TerminalTerminalSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9e3b251ef81a6fab43d4973a8148c78f312ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476397"
---
# <a name="win32_terminalterminalsetting-class"></a><span data-ttu-id="8e7c8-105">Win32 \_ TerminalTerminalSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="8e7c8-105">Win32\_TerminalTerminalSetting class</span></span>

<span data-ttu-id="8e7c8-106">La classe WMI **\_ TerminalTerminalSetting Win32** rappresenta l'associazione tra un terminale e le relative impostazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-106">The **Win32\_TerminalTerminalSetting** WMI class represents the association between a terminal and its configuration settings.</span></span>

<span data-ttu-id="8e7c8-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-107">The following syntax is simplified from MOF code and includes all defined properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e7c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e7c8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALTERMINALSETTING_Prov"), AMENDMENT]
class Win32_TerminalTerminalSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_Terminal        REF Element;
  Win32_TerminalSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="8e7c8-109">Members</span><span class="sxs-lookup"><span data-stu-id="8e7c8-109">Members</span></span>

<span data-ttu-id="8e7c8-110">La classe **Win32 \_ TerminalTerminalSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8e7c8-110">The **Win32\_TerminalTerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="8e7c8-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e7c8-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e7c8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8e7c8-112">Properties</span></span>

<span data-ttu-id="8e7c8-113">La classe **Win32 \_ TerminalTerminalSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-113">The **Win32\_TerminalTerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e7c8-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8e7c8-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="8e7c8-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-123">Description of the object.</span></span>

<span data-ttu-id="8e7c8-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-125">**elemento**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-126">Tipo di dati **: \_ terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-126">Data type: **Win32\_Terminal**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e7c8-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-129">Rappresenta il terminale che può essere configurato tramite la proprietà **Setting** .</span><span class="sxs-lookup"><span data-stu-id="8e7c8-129">Represents the terminal that can be configured through the **Setting** property.</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-133">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-134">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-134">The date the object was installed.</span></span> <span data-ttu-id="8e7c8-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8e7c8-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-140">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-140">The name of the object.</span></span>

<span data-ttu-id="8e7c8-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-142">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-143">Tipo di dati: **Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-143">Data type: **Win32\_TerminalSetting**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8e7c8-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-146">Rappresenta le impostazioni che è possibile applicare al terminale specificato.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-146">Represents the settings that can be applied to the specified terminal.</span></span>

</dd> <dt>

<span data-ttu-id="8e7c8-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e7c8-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8e7c8-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e7c8-150">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="8e7c8-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="8e7c8-151">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-151">Current status of the object.</span></span> <span data-ttu-id="8e7c8-152">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8e7c8-153">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8e7c8-154">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="8e7c8-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8e7c8-155">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8e7c8-156">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8e7c8-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="8e7c8-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-159">("Errore")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-160">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-161">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-162">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-163">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-164">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="8e7c8-165">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="8e7c8-165">("Service")</span></span>


<span data-ttu-id="8e7c8-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8e7c8-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8e7c8-167">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e7c8-167">Remarks</span></span>

<span data-ttu-id="8e7c8-168">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-168">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8e7c8-169">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-169">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8e7c8-170">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8e7c8-170">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8e7c8-171">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8e7c8-171">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e7c8-172">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e7c8-172">Requirements</span></span>



| <span data-ttu-id="8e7c8-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e7c8-173">Requirement</span></span> | <span data-ttu-id="8e7c8-174">Valore</span><span class="sxs-lookup"><span data-stu-id="8e7c8-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e7c8-175">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e7c8-175">Minimum supported client</span></span><br/> | <span data-ttu-id="8e7c8-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e7c8-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e7c8-177">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e7c8-177">Minimum supported server</span></span><br/> | <span data-ttu-id="8e7c8-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e7c8-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e7c8-179">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8e7c8-179">Namespace</span></span><br/>                | <span data-ttu-id="8e7c8-180">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8e7c8-180">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8e7c8-181">MOF</span><span class="sxs-lookup"><span data-stu-id="8e7c8-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e7c8-182"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c8-182"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e7c8-183">DLL</span><span class="sxs-lookup"><span data-stu-id="8e7c8-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e7c8-184"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e7c8-184"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e7c8-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e7c8-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e7c8-186">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-186">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="8e7c8-187">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-187">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="8e7c8-188">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8e7c8-188">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

