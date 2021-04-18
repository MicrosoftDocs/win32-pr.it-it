---
title: Classe Win32_Workspace
description: Specifica Servizi Desktop remoto informazioni di configurazione dell'area di lavoro.
ms.assetid: 27192dca-cbb4-4620-ae52-c27aba4b4dff
ms.tgt_platform: multiple
keywords:
- Classe Win32_Workspace Servizi Desktop remoto
- Classe Win32_Workspace Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_Workspace
- Win32_Workspace.Caption
- Win32_Workspace.Description
- Win32_Workspace.InstallDate
- Win32_Workspace.Name
- Win32_Workspace.Status
- Win32_Workspace.IsDefaultName
- Win32_Workspace.ID
- Win32_Workspace.Redirector
- Win32_Workspace.RedirectorAlternateAddress
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1153a4eb8a260e539845a9458a5c8cee4581d30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301049"
---
# <a name="win32_workspace-class"></a><span data-ttu-id="b93d1-105">\_Classe dell'area di lavoro Win32</span><span class="sxs-lookup"><span data-stu-id="b93d1-105">Win32\_Workspace class</span></span>

<span data-ttu-id="b93d1-106">Specifica Servizi Desktop remoto informazioni di configurazione dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b93d1-106">Specifies Remote Desktop Services workspace configuration information.</span></span>

<span data-ttu-id="b93d1-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b93d1-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b93d1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b93d1-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov"), singleton]
class Win32_Workspace : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  IsDefaultName;
  string   ID;
  string   Redirector;
  string   RedirectorAlternateAddress;
};
```

## <a name="members"></a><span data-ttu-id="b93d1-109">Members</span><span class="sxs-lookup"><span data-stu-id="b93d1-109">Members</span></span>

<span data-ttu-id="b93d1-110">La classe dell' **\_ area di lavoro Win32** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b93d1-110">The **Win32\_Workspace** class has these types of members:</span></span>

-   [<span data-ttu-id="b93d1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b93d1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b93d1-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b93d1-112">Properties</span></span>

<span data-ttu-id="b93d1-113">La classe dell' **\_ area di lavoro Win32** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b93d1-113">The **Win32\_Workspace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b93d1-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="b93d1-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b93d1-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b93d1-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b93d1-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b93d1-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b93d1-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b93d1-123">Description of the object.</span></span>

<span data-ttu-id="b93d1-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b93d1-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="b93d1-125">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b93d1-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-128">Identificatore dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b93d1-128">The identifier of the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b93d1-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b93d1-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-132">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="b93d1-132">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-133">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b93d1-133">The date the object was installed.</span></span> <span data-ttu-id="b93d1-134">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="b93d1-134">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b93d1-135">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b93d1-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-136">**Impostazione predefinita**</span><span class="sxs-lookup"><span data-stu-id="b93d1-136">**IsDefaultName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-137">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="b93d1-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-139">Specifica se il nome dell'area di lavoro è il nome predefinito.</span><span class="sxs-lookup"><span data-stu-id="b93d1-139">Specifies if the workspace name is the default name.</span></span> <span data-ttu-id="b93d1-140">Contiene un valore diverso da zero se il nome è un nome predefinito o zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b93d1-140">Contains nonzero if the name is a default name or zero otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b93d1-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-144">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b93d1-144">The name of the object.</span></span>

<span data-ttu-id="b93d1-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b93d1-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-146">**Redirector**</span><span class="sxs-lookup"><span data-stu-id="b93d1-146">**Redirector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b93d1-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-149">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b93d1-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-150">Nome del computer del redirector per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b93d1-150">The machine name of the redirector for the workspace.</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-151">**RedirectorAlternateAddress**</span><span class="sxs-lookup"><span data-stu-id="b93d1-151">**RedirectorAlternateAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="b93d1-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-154">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b93d1-154">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-155">Indirizzo alternativo per il redirector.</span><span class="sxs-lookup"><span data-stu-id="b93d1-155">The alternate address for the redirector.</span></span>

</dd> <dt>

<span data-ttu-id="b93d1-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="b93d1-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b93d1-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b93d1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b93d1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b93d1-159">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b93d1-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b93d1-160">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="b93d1-160">Current status of the object.</span></span> <span data-ttu-id="b93d1-161">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="b93d1-161">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b93d1-162">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="b93d1-162">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b93d1-163">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="b93d1-163">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b93d1-164">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="b93d1-164">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b93d1-165">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="b93d1-165">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b93d1-166">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b93d1-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b93d1-167">("OK")</span><span class="sxs-lookup"><span data-stu-id="b93d1-167">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-168">("Errore")</span><span class="sxs-lookup"><span data-stu-id="b93d1-168">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-169">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="b93d1-169">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-170">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="b93d1-170">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-171">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="b93d1-171">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-172">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="b93d1-172">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-173">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="b93d1-173">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b93d1-174">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="b93d1-174">("Service")</span></span>


<span data-ttu-id="b93d1-175"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b93d1-175"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b93d1-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b93d1-176">Requirements</span></span>



| <span data-ttu-id="b93d1-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="b93d1-177">Requirement</span></span> | <span data-ttu-id="b93d1-178">Valore</span><span class="sxs-lookup"><span data-stu-id="b93d1-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b93d1-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b93d1-179">Minimum supported client</span></span><br/> | <span data-ttu-id="b93d1-180">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b93d1-180">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b93d1-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b93d1-181">Minimum supported server</span></span><br/> | <span data-ttu-id="b93d1-182">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b93d1-182">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b93d1-183">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b93d1-183">Namespace</span></span><br/>                | <span data-ttu-id="b93d1-184">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b93d1-184">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b93d1-185">MOF</span><span class="sxs-lookup"><span data-stu-id="b93d1-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b93d1-186"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b93d1-186"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="b93d1-187">DLL</span><span class="sxs-lookup"><span data-stu-id="b93d1-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b93d1-188"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b93d1-188"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

