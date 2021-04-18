---
title: Classe Win32_RDPersonalDesktopAssignment
description: Elenco di assegnazioni desktop personali.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDPersonalDesktopAssignment Servizi Desktop remoto
- Classe Win32_RDPersonalDesktopAssignment Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301205"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="812d5-105">Win32 \_ RDPersonalDesktopAssignment (classe)</span><span class="sxs-lookup"><span data-stu-id="812d5-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="812d5-106">Elenco di assegnazioni desktop personali.</span><span class="sxs-lookup"><span data-stu-id="812d5-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="812d5-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="812d5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="812d5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="812d5-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="812d5-109">Members</span><span class="sxs-lookup"><span data-stu-id="812d5-109">Members</span></span>

<span data-ttu-id="812d5-110">La classe **Win32 \_ RDPersonalDesktopAssignment** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="812d5-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="812d5-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="812d5-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="812d5-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="812d5-112">Properties</span></span>

<span data-ttu-id="812d5-113">La classe **Win32 \_ RDPersonalDesktopAssignment** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="812d5-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="812d5-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="812d5-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="812d5-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812d5-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="812d5-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="812d5-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="812d5-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="812d5-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812d5-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812d5-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="812d5-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="812d5-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812d5-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="812d5-123">Description of the object.</span></span>

<span data-ttu-id="812d5-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812d5-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812d5-125">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="812d5-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="812d5-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="812d5-128">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="812d5-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="812d5-129">Nome di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="812d5-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="812d5-130">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="812d5-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="812d5-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="812d5-133">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="812d5-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="812d5-134">Farm in cui è stato assegnato il desktop personale.</span><span class="sxs-lookup"><span data-stu-id="812d5-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="812d5-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="812d5-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-136">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="812d5-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="812d5-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812d5-138">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="812d5-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="812d5-139">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="812d5-139">The date the object was installed.</span></span> <span data-ttu-id="812d5-140">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="812d5-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="812d5-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812d5-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812d5-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="812d5-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="812d5-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="812d5-145">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="812d5-145">The name of the object.</span></span>

<span data-ttu-id="812d5-146">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812d5-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="812d5-147">**Status**</span><span class="sxs-lookup"><span data-stu-id="812d5-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-148">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="812d5-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="812d5-150">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="812d5-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="812d5-151">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="812d5-151">Current status of the object.</span></span> <span data-ttu-id="812d5-152">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="812d5-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="812d5-153">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="812d5-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="812d5-154">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="812d5-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="812d5-155">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="812d5-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="812d5-156">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="812d5-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="812d5-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="812d5-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="812d5-158">("OK")</span><span class="sxs-lookup"><span data-stu-id="812d5-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-159">("Errore")</span><span class="sxs-lookup"><span data-stu-id="812d5-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-160">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="812d5-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-161">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="812d5-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-162">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="812d5-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-163">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="812d5-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-164">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="812d5-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="812d5-165">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="812d5-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="812d5-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="812d5-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-168">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="812d5-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="812d5-169">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="812d5-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="812d5-170">Nome utente a cui è stato assegnato personal desktop.</span><span class="sxs-lookup"><span data-stu-id="812d5-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="812d5-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="812d5-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="812d5-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="812d5-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="812d5-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="812d5-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="812d5-174">Nome della macchina virtuale assegnata.</span><span class="sxs-lookup"><span data-stu-id="812d5-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="812d5-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="812d5-175">Requirements</span></span>



| <span data-ttu-id="812d5-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="812d5-176">Requirement</span></span> | <span data-ttu-id="812d5-177">Valore</span><span class="sxs-lookup"><span data-stu-id="812d5-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="812d5-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="812d5-178">Minimum supported client</span></span><br/> | <span data-ttu-id="812d5-179">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="812d5-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="812d5-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="812d5-180">Minimum supported server</span></span><br/> | <span data-ttu-id="812d5-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="812d5-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="812d5-182">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="812d5-182">Namespace</span></span><br/>                | <span data-ttu-id="812d5-183">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="812d5-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="812d5-184">MOF</span><span class="sxs-lookup"><span data-stu-id="812d5-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="812d5-185"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="812d5-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="812d5-186">DLL</span><span class="sxs-lookup"><span data-stu-id="812d5-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="812d5-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="812d5-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

