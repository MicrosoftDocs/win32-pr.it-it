---
title: Classe Win32_TSCPubPlugin
description: Rappresenta un plug-in configurato per l'utilizzo tramite il servizio Servizio di gestione Connessione RemoteApp e desktop.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSCPubPlugin Servizi Desktop remoto
- Classe Win32_TSCPubPlugin Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873693"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="46dd9-105">Win32 \_ TSCPubPlugin (classe)</span><span class="sxs-lookup"><span data-stu-id="46dd9-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="46dd9-106">Rappresenta un plug-in configurato per l'utilizzo tramite il servizio Servizio di gestione Connessione RemoteApp e desktop.</span><span class="sxs-lookup"><span data-stu-id="46dd9-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="46dd9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="46dd9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46dd9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46dd9-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="46dd9-109">Members</span><span class="sxs-lookup"><span data-stu-id="46dd9-109">Members</span></span>

<span data-ttu-id="46dd9-110">La classe **Win32 \_ TSCPubPlugin** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="46dd9-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="46dd9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46dd9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46dd9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="46dd9-112">Properties</span></span>

<span data-ttu-id="46dd9-113">La classe **Win32 \_ TSCPubPlugin** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="46dd9-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46dd9-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="46dd9-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46dd9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="46dd9-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46dd9-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="46dd9-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46dd9-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-120">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="46dd9-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46dd9-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-123">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46dd9-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-124">CLSID del plug-in.</span><span class="sxs-lookup"><span data-stu-id="46dd9-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-125">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="46dd9-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46dd9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-128">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46dd9-128">Description of the object.</span></span>

<span data-ttu-id="46dd9-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46dd9-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="46dd9-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-131">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="46dd9-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-133">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="46dd9-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-134">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46dd9-134">The date the object was installed.</span></span> <span data-ttu-id="46dd9-135">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="46dd9-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="46dd9-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46dd9-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="46dd9-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="46dd9-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="46dd9-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-140">Specifica se il plug-in è abilitato.</span><span class="sxs-lookup"><span data-stu-id="46dd9-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="46dd9-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46dd9-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-144">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46dd9-144">The name of the object.</span></span>

<span data-ttu-id="46dd9-145">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46dd9-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="46dd9-146">**Status**</span><span class="sxs-lookup"><span data-stu-id="46dd9-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46dd9-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="46dd9-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="46dd9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46dd9-149">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="46dd9-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="46dd9-150">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="46dd9-150">Current status of the object.</span></span> <span data-ttu-id="46dd9-151">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="46dd9-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="46dd9-152">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="46dd9-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="46dd9-153">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="46dd9-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="46dd9-154">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="46dd9-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="46dd9-155">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="46dd9-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="46dd9-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="46dd9-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="46dd9-157">("OK")</span><span class="sxs-lookup"><span data-stu-id="46dd9-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-158">("Errore")</span><span class="sxs-lookup"><span data-stu-id="46dd9-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-159">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="46dd9-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-160">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="46dd9-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-161">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="46dd9-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-162">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="46dd9-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-163">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="46dd9-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="46dd9-164">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="46dd9-164">("Service")</span></span>


<span data-ttu-id="46dd9-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="46dd9-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="46dd9-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46dd9-166">Requirements</span></span>



| <span data-ttu-id="46dd9-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="46dd9-167">Requirement</span></span> | <span data-ttu-id="46dd9-168">Valore</span><span class="sxs-lookup"><span data-stu-id="46dd9-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46dd9-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46dd9-169">Minimum supported client</span></span><br/> | <span data-ttu-id="46dd9-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46dd9-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="46dd9-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46dd9-171">Minimum supported server</span></span><br/> | <span data-ttu-id="46dd9-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46dd9-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="46dd9-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46dd9-173">Namespace</span></span><br/>                | <span data-ttu-id="46dd9-174">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46dd9-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="46dd9-175">MOF</span><span class="sxs-lookup"><span data-stu-id="46dd9-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46dd9-176"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46dd9-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="46dd9-177">DLL</span><span class="sxs-lookup"><span data-stu-id="46dd9-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46dd9-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46dd9-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

