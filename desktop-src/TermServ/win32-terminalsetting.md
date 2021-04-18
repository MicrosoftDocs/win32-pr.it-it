---
title: Classe Win32_TerminalSetting
description: Rappresenta le impostazioni che è possibile applicare a un terminale.
ms.assetid: e709aa60-f8fd-4e83-a5a1-d682ff469d23
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalSetting Servizi Desktop remoto
- Classe Win32_TerminalSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalSetting
- Win32_TerminalSetting.Caption
- Win32_TerminalSetting.Description
- Win32_TerminalSetting.InstallDate
- Win32_TerminalSetting.Name
- Win32_TerminalSetting.Status
- Win32_TerminalSetting.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa29438ddea518c9f17e35fdafc3b9a912694d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302436"
---
# <a name="win32_terminalsetting-class"></a><span data-ttu-id="0fe9b-105">Win32 \_ TerminalSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="0fe9b-105">Win32\_TerminalSetting class</span></span>

<span data-ttu-id="0fe9b-106">La classe WMI **\_ TerminalSetting Win32** rappresenta le impostazioni che è possibile applicare a un terminale.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-106">The **Win32\_TerminalSetting** WMI class represents the settings that can be applied to a terminal.</span></span>

<span data-ttu-id="0fe9b-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe9b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fe9b-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_TerminalSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="0fe9b-109">Members</span><span class="sxs-lookup"><span data-stu-id="0fe9b-109">Members</span></span>

<span data-ttu-id="0fe9b-110">La classe **Win32 \_ TerminalSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0fe9b-110">The **Win32\_TerminalSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="0fe9b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0fe9b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fe9b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0fe9b-112">Properties</span></span>

<span data-ttu-id="0fe9b-113">La classe **Win32 \_ TerminalSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-113">The **Win32\_TerminalSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fe9b-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0fe9b-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0fe9b-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe9b-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-123">Description of the object.</span></span>

<span data-ttu-id="0fe9b-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe9b-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-129">The date the object was installed.</span></span> <span data-ttu-id="0fe9b-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0fe9b-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe9b-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-135">The name of the object.</span></span>

<span data-ttu-id="0fe9b-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0fe9b-137">**Status**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-137">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-140">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0fe9b-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-141">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-141">Current status of the object.</span></span> <span data-ttu-id="0fe9b-142">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-142">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0fe9b-143">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-143">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0fe9b-144">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="0fe9b-144">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0fe9b-145">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-145">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0fe9b-146">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-146">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0fe9b-147">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0fe9b-148">("OK")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-148">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-149">("Errore")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-149">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-150">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-150">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-151">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-151">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-152">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-152">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-153">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-153">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-154">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-154">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0fe9b-155">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="0fe9b-155">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0fe9b-156">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-156">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fe9b-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0fe9b-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0fe9b-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fe9b-159">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-159">The name of the terminal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fe9b-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="0fe9b-160">Remarks</span></span>

<span data-ttu-id="0fe9b-161">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-161">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0fe9b-162">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-162">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0fe9b-163">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0fe9b-163">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0fe9b-164">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0fe9b-164">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0fe9b-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fe9b-165">Requirements</span></span>



| <span data-ttu-id="0fe9b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fe9b-166">Requirement</span></span> | <span data-ttu-id="0fe9b-167">Valore</span><span class="sxs-lookup"><span data-stu-id="0fe9b-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fe9b-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe9b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0fe9b-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fe9b-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fe9b-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0fe9b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0fe9b-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fe9b-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fe9b-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0fe9b-172">Namespace</span></span><br/>                | <span data-ttu-id="0fe9b-173">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0fe9b-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0fe9b-174">MOF</span><span class="sxs-lookup"><span data-stu-id="0fe9b-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fe9b-175"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fe9b-175"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fe9b-176">DLL</span><span class="sxs-lookup"><span data-stu-id="0fe9b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fe9b-177"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fe9b-177"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fe9b-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fe9b-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fe9b-179">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-179">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0fe9b-180">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-180">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="0fe9b-181">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="0fe9b-181">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

