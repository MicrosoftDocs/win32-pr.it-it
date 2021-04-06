---
title: Classe Win32_TSVmMetadataItem
description: Rappresenta un elemento di metadati per una macchina virtuale Desktop remoto.
ms.assetid: d2678eb0-8634-450c-b73f-611b6f68d556
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVmMetadataItem Servizi Desktop remoto
- Classe Win32_TSVmMetadataItem Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataItem
- Win32_TSVmMetadataItem.Caption
- Win32_TSVmMetadataItem.Description
- Win32_TSVmMetadataItem.InstallDate
- Win32_TSVmMetadataItem.Name
- Win32_TSVmMetadataItem.Status
- Win32_TSVmMetadataItem.VmName
- Win32_TSVmMetadataItem.SectionId
- Win32_TSVmMetadataItem.Value
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 872cec5bf3ff0e7b45ab07cb41b6227bcfb8636d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963817"
---
# <a name="win32_tsvmmetadataitem-class"></a><span data-ttu-id="ec27b-105">Win32 \_ TSVmMetadataItem (classe)</span><span class="sxs-lookup"><span data-stu-id="ec27b-105">Win32\_TSVmMetadataItem class</span></span>

<span data-ttu-id="ec27b-106">Rappresenta un elemento di metadati per una macchina virtuale Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-106">Represents a metadata item for a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="ec27b-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ec27b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec27b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ec27b-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  sint32   SectionId;
  string   Value;
};
```

## <a name="members"></a><span data-ttu-id="ec27b-109">Members</span><span class="sxs-lookup"><span data-stu-id="ec27b-109">Members</span></span>

<span data-ttu-id="ec27b-110">La classe **Win32 \_ TSVmMetadataItem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ec27b-110">The **Win32\_TSVmMetadataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="ec27b-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec27b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec27b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ec27b-112">Properties</span></span>

<span data-ttu-id="ec27b-113">La classe **Win32 \_ TSVmMetadataItem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ec27b-113">The **Win32\_TSVmMetadataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec27b-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ec27b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ec27b-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ec27b-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec27b-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ec27b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-123">Description of the object.</span></span>

<span data-ttu-id="ec27b-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec27b-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ec27b-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ec27b-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="ec27b-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-129">The date the object was installed.</span></span> <span data-ttu-id="ec27b-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="ec27b-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ec27b-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec27b-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ec27b-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-135">The name of the object.</span></span>

<span data-ttu-id="ec27b-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec27b-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-137">**SectionId**</span><span class="sxs-lookup"><span data-stu-id="ec27b-137">**SectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-138">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ec27b-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-140">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec27b-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-141">Specifica la sezione all'interno dei metadati in cui si trova l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ec27b-141">Specifies the section within the metadata where this item resides.</span></span>

<dt>

<span data-ttu-id="ec27b-142">0</span><span class="sxs-lookup"><span data-stu-id="ec27b-142">0</span></span>
</dt> <dd>

<span data-ttu-id="ec27b-143">Sezione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="ec27b-143">Configuration section.</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-144">1</span><span class="sxs-lookup"><span data-stu-id="ec27b-144">1</span></span>
</dt> <dd>

<span data-ttu-id="ec27b-145">Sezione impostazioni di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="ec27b-145">Enlightenment settings section.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ec27b-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="ec27b-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-149">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ec27b-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-150">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ec27b-150">Current status of the object.</span></span> <span data-ttu-id="ec27b-151">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="ec27b-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ec27b-152">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="ec27b-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ec27b-153">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="ec27b-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ec27b-154">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="ec27b-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ec27b-155">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="ec27b-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ec27b-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ec27b-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ec27b-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="ec27b-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-158">("Errore")</span><span class="sxs-lookup"><span data-stu-id="ec27b-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-159">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="ec27b-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-160">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="ec27b-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-161">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="ec27b-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-162">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="ec27b-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-163">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="ec27b-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ec27b-164">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="ec27b-164">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ec27b-165">**Valore**</span><span class="sxs-lookup"><span data-stu-id="ec27b-165">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ec27b-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-168">Valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="ec27b-168">The value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="ec27b-169">**VmName**</span><span class="sxs-lookup"><span data-stu-id="ec27b-169">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec27b-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ec27b-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ec27b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec27b-172">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ec27b-172">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ec27b-173">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ec27b-173">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec27b-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec27b-174">Requirements</span></span>



| <span data-ttu-id="ec27b-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec27b-175">Requirement</span></span> | <span data-ttu-id="ec27b-176">Valore</span><span class="sxs-lookup"><span data-stu-id="ec27b-176">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec27b-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec27b-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ec27b-178">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ec27b-178">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ec27b-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec27b-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ec27b-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec27b-180">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ec27b-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ec27b-181">Namespace</span></span><br/>                | <span data-ttu-id="ec27b-182">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ec27b-182">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ec27b-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ec27b-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec27b-184"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec27b-184"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ec27b-185">DLL</span><span class="sxs-lookup"><span data-stu-id="ec27b-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec27b-186"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec27b-186"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

