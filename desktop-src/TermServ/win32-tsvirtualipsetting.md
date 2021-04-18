---
title: Classe Win32_TSVirtualIPSetting
description: Rappresenta l'associazione tra una \_ classe di elementi Win32 TerminalService e una \_ classe di impostazioni TSVirtualIP Win32.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVirtualIPSetting Servizi Desktop remoto
- Classe Win32_TSVirtualIPSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301054"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="f8fa7-105">Win32 \_ TSVirtualIPSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="f8fa7-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="f8fa7-106">Rappresenta l'associazione tra una classe di elementi [**Win32 \_ TerminalService**](win32-terminalservice.md) e una classe di impostazioni [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="f8fa7-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="f8fa7-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8fa7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8fa7-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="f8fa7-109">Members</span><span class="sxs-lookup"><span data-stu-id="f8fa7-109">Members</span></span>

<span data-ttu-id="f8fa7-110">La classe **Win32 \_ TSVirtualIPSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f8fa7-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f8fa7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8fa7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f8fa7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f8fa7-112">Properties</span></span>

<span data-ttu-id="f8fa7-113">La classe **Win32 \_ TSVirtualIPSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f8fa7-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f8fa7-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f8fa7-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-123">Description of the object.</span></span>

<span data-ttu-id="f8fa7-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-125">**elemento**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-126">Tipo di dati: **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8fa7-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-129">Riferimento a un oggetto [**Win32 \_ TerminalService**](win32-terminalservice.md) che rappresenta la classe di elementi per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-133">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-134">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-134">The date the object was installed.</span></span> <span data-ttu-id="f8fa7-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f8fa7-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-137">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-140">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-140">The name of the object.</span></span>

<span data-ttu-id="f8fa7-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-142">**Impostazione**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-143">Tipo di dati: **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-145">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f8fa7-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-146">Riferimento a un oggetto [**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md) che rappresenta la classe Setting per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="f8fa7-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f8fa7-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f8fa7-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f8fa7-150">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f8fa7-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f8fa7-151">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-151">Current status of the object.</span></span> <span data-ttu-id="f8fa7-152">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f8fa7-153">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f8fa7-154">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f8fa7-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f8fa7-155">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f8fa7-156">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f8fa7-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f8fa7-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f8fa7-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f8fa7-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-159">("Errore")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-160">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-161">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-162">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-163">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-164">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f8fa7-165">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="f8fa7-165">("Service")</span></span>


<span data-ttu-id="f8fa7-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f8fa7-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f8fa7-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8fa7-167">Requirements</span></span>



| <span data-ttu-id="f8fa7-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8fa7-168">Requirement</span></span> | <span data-ttu-id="f8fa7-169">Valore</span><span class="sxs-lookup"><span data-stu-id="f8fa7-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8fa7-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8fa7-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f8fa7-171">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f8fa7-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f8fa7-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8fa7-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f8fa7-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8fa7-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f8fa7-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f8fa7-174">Namespace</span></span><br/>                | <span data-ttu-id="f8fa7-175">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f8fa7-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f8fa7-176">MOF</span><span class="sxs-lookup"><span data-stu-id="f8fa7-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8fa7-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8fa7-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8fa7-178">DLL</span><span class="sxs-lookup"><span data-stu-id="f8fa7-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8fa7-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8fa7-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8fa7-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8fa7-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8fa7-181">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="f8fa7-182">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f8fa7-183">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="f8fa7-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

