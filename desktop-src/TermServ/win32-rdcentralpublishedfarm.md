---
title: Classe Win32_RDCentralPublishedFarm
description: Elenco di farm da cui sono stati pubblicati i desktop o le applicazioni.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedFarm Servizi Desktop remoto
- Classe Win32_RDCentralPublishedFarm Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476211"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="5c3a0-105">Win32 \_ RDCentralPublishedFarm (classe)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="5c3a0-106">Elenco di farm da cui sono stati pubblicati i desktop o le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="5c3a0-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c3a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c3a0-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="5c3a0-109">Members</span><span class="sxs-lookup"><span data-stu-id="5c3a0-109">Members</span></span>

<span data-ttu-id="5c3a0-110">La classe **Win32 \_ RDCentralPublishedFarm** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5c3a0-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="5c3a0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c3a0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c3a0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c3a0-112">Properties</span></span>

<span data-ttu-id="5c3a0-113">La classe **Win32 \_ RDCentralPublishedFarm** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c3a0-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-118">Nome della farm dalla quale sono stati pubblicati i desktop o le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-123">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5c3a0-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-128">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-128">Description of the object.</span></span>

<span data-ttu-id="5c3a0-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-130">**FarmType**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-132">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-133">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-134">Tipo di farm:</span><span class="sxs-lookup"><span data-stu-id="5c3a0-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="5c3a0-135">**RDSH** (0)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="5c3a0-136">**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="5c3a0-137">**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="5c3a0-138">**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c3a0-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-140">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-142">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-143">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-143">The date the object was installed.</span></span> <span data-ttu-id="5c3a0-144">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5c3a0-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-146">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-147">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-149">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-150">**true** se è necessario aggiungere un utente al gruppo Administrators locale dopo la connessione. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="5c3a0-151">Applicabile solo ai tipi di farm ManualPersonalVm e AutoPersonalVM.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-152">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-155">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-155">The name of the object.</span></span>

<span data-ttu-id="5c3a0-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-157">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-158">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-160">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-161">**true** per eseguire automaticamente il rollback della macchina virtuale a uno snapshot dopo la disconnessione dell'utente. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="5c3a0-162">Applicabile solo ai tipi di farm TempVm.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-166">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-167">Nome del descrittore di sicurezza che controlla l'accesso all'applicazione in formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="5c3a0-168">L'uso di una stringa vuota implica l'autorizzazione All Access.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="5c3a0-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-172">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-173">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-173">Current status of the object.</span></span> <span data-ttu-id="5c3a0-174">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5c3a0-175">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5c3a0-176">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5c3a0-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5c3a0-177">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5c3a0-178">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5c3a0-179">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5c3a0-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5c3a0-180">("OK")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-181">("Errore")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-182">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-183">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-184">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-185">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-186">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5c3a0-187">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="5c3a0-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5c3a0-188">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c3a0-189">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5c3a0-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-190">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5c3a0-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5c3a0-191">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c3a0-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c3a0-192">Impostazioni della farm della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5c3a0-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c3a0-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c3a0-193">Requirements</span></span>



| <span data-ttu-id="5c3a0-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c3a0-194">Requirement</span></span> | <span data-ttu-id="5c3a0-195">Valore</span><span class="sxs-lookup"><span data-stu-id="5c3a0-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3a0-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c3a0-196">Minimum supported client</span></span><br/> | <span data-ttu-id="5c3a0-197">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5c3a0-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5c3a0-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c3a0-198">Minimum supported server</span></span><br/> | <span data-ttu-id="5c3a0-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5c3a0-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5c3a0-200">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c3a0-200">Namespace</span></span><br/>                | <span data-ttu-id="5c3a0-201">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5c3a0-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5c3a0-202">MOF</span><span class="sxs-lookup"><span data-stu-id="5c3a0-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c3a0-203"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c3a0-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5c3a0-204">DLL</span><span class="sxs-lookup"><span data-stu-id="5c3a0-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c3a0-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c3a0-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

