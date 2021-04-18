---
title: Classe Win32_TSLegacyPlugin
description: Rappresenta un server Desktop remoto che i plug-in del servizio Servizio di gestione Connessione RemoteApp e desktop predefiniti eseguiranno una query per i programmi RemoteApp.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLegacyPlugin Servizi Desktop remoto
- Classe Win32_TSLegacyPlugin Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301060"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="947e9-105">Win32 \_ TSLegacyPlugin (classe)</span><span class="sxs-lookup"><span data-stu-id="947e9-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="947e9-106">Rappresenta un server Desktop remoto che i plug-in del servizio Servizio di gestione Connessione RemoteApp e desktop predefiniti eseguiranno una query per i programmi RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="947e9-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="947e9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="947e9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="947e9-108">Questa classe è deprecata a partire da Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="947e9-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="947e9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="947e9-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="947e9-110">Members</span><span class="sxs-lookup"><span data-stu-id="947e9-110">Members</span></span>

<span data-ttu-id="947e9-111">La classe **Win32 \_ TSLegacyPlugin** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="947e9-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="947e9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="947e9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="947e9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="947e9-113">Properties</span></span>

<span data-ttu-id="947e9-114">La classe **Win32 \_ TSLegacyPlugin** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="947e9-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="947e9-115">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="947e9-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="947e9-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947e9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="947e9-118">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="947e9-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="947e9-119">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="947e9-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="947e9-120">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="947e9-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="947e9-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="947e9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="947e9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947e9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="947e9-124">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="947e9-124">Description of the object.</span></span>

<span data-ttu-id="947e9-125">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="947e9-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="947e9-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="947e9-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-127">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="947e9-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947e9-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="947e9-129">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="947e9-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="947e9-130">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="947e9-130">The date the object was installed.</span></span> <span data-ttu-id="947e9-131">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="947e9-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="947e9-132">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="947e9-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="947e9-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="947e9-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="947e9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947e9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="947e9-136">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="947e9-136">The name of the object.</span></span>

<span data-ttu-id="947e9-137">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="947e9-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="947e9-138">**Status**</span><span class="sxs-lookup"><span data-stu-id="947e9-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-139">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="947e9-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="947e9-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="947e9-141">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="947e9-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="947e9-142">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="947e9-142">Current status of the object.</span></span> <span data-ttu-id="947e9-143">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="947e9-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="947e9-144">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="947e9-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="947e9-145">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="947e9-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="947e9-146">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="947e9-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="947e9-147">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="947e9-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="947e9-148">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="947e9-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="947e9-149">("OK")</span><span class="sxs-lookup"><span data-stu-id="947e9-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-150">("Errore")</span><span class="sxs-lookup"><span data-stu-id="947e9-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-151">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="947e9-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-152">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="947e9-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-153">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="947e9-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-154">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="947e9-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-155">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="947e9-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="947e9-156">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="947e9-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="947e9-157">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="947e9-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="947e9-158">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="947e9-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="947e9-159">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="947e9-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="947e9-160">Tipo del server Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="947e9-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="947e9-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="947e9-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="947e9-162">Server Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="947e9-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="947e9-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Terminal server fittizio per la farm VM (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="947e9-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="947e9-164">Server Desktop remoto artificiali per una farm di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="947e9-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="947e9-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="947e9-165">Requirements</span></span>



| <span data-ttu-id="947e9-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="947e9-166">Requirement</span></span> | <span data-ttu-id="947e9-167">Valore</span><span class="sxs-lookup"><span data-stu-id="947e9-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="947e9-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947e9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="947e9-169">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="947e9-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="947e9-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="947e9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="947e9-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="947e9-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="947e9-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="947e9-172">Namespace</span></span><br/>                | <span data-ttu-id="947e9-173">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="947e9-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="947e9-174">MOF</span><span class="sxs-lookup"><span data-stu-id="947e9-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="947e9-175"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="947e9-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="947e9-176">DLL</span><span class="sxs-lookup"><span data-stu-id="947e9-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="947e9-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="947e9-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

