---
title: Classe Win32_TSSystemInfo
description: Rappresenta il servizio informazioni server di pubblicazione centralizzato.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSSystemInfo Servizi Desktop remoto
- Classe Win32_TSSystemInfo Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476193"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="c10a0-105">Win32 \_ TSSystemInfo (classe)</span><span class="sxs-lookup"><span data-stu-id="c10a0-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="c10a0-106">Rappresenta il servizio informazioni server di pubblicazione centralizzato</span><span class="sxs-lookup"><span data-stu-id="c10a0-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="c10a0-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c10a0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c10a0-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="c10a0-109">Members</span><span class="sxs-lookup"><span data-stu-id="c10a0-109">Members</span></span>

<span data-ttu-id="c10a0-110">La classe **Win32 \_ TSSystemInfo** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c10a0-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="c10a0-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c10a0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c10a0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c10a0-112">Properties</span></span>

<span data-ttu-id="c10a0-113">La classe **Win32 \_ TSSystemInfo** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c10a0-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c10a0-114">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c10a0-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c10a0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-117">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c10a0-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-118">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c10a0-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c10a0-119">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c10a0-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c10a0-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c10a0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-123">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c10a0-123">Description of the object.</span></span>

<span data-ttu-id="c10a0-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c10a0-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c10a0-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-126">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c10a0-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-128">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c10a0-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-129">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c10a0-129">The date the object was installed.</span></span> <span data-ttu-id="c10a0-130">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="c10a0-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c10a0-131">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c10a0-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c10a0-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c10a0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-135">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c10a0-135">The name of the object.</span></span>

<span data-ttu-id="c10a0-136">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c10a0-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="c10a0-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c10a0-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-140">Numero di versione del provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c10a0-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-141">**RDUGroup**</span><span class="sxs-lookup"><span data-stu-id="c10a0-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c10a0-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-144">Il gruppo Desktop remoto Users, in formato SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="c10a0-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="c10a0-145">**Status**</span><span class="sxs-lookup"><span data-stu-id="c10a0-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c10a0-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c10a0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c10a0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c10a0-148">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c10a0-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c10a0-149">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c10a0-149">Current status of the object.</span></span> <span data-ttu-id="c10a0-150">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="c10a0-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c10a0-151">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="c10a0-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c10a0-152">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="c10a0-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c10a0-153">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="c10a0-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c10a0-154">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="c10a0-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c10a0-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c10a0-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c10a0-156">("OK")</span><span class="sxs-lookup"><span data-stu-id="c10a0-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-157">("Errore")</span><span class="sxs-lookup"><span data-stu-id="c10a0-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-158">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="c10a0-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-159">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="c10a0-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-160">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="c10a0-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-161">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="c10a0-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-162">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="c10a0-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c10a0-163">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="c10a0-163">("Service")</span></span>


<span data-ttu-id="c10a0-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c10a0-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c10a0-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c10a0-165">Requirements</span></span>



| <span data-ttu-id="c10a0-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="c10a0-166">Requirement</span></span> | <span data-ttu-id="c10a0-167">Valore</span><span class="sxs-lookup"><span data-stu-id="c10a0-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c10a0-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10a0-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c10a0-169">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c10a0-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c10a0-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c10a0-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c10a0-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c10a0-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="c10a0-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c10a0-172">Namespace</span></span><br/>                | <span data-ttu-id="c10a0-173">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c10a0-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c10a0-174">MOF</span><span class="sxs-lookup"><span data-stu-id="c10a0-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c10a0-175"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c10a0-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c10a0-176">DLL</span><span class="sxs-lookup"><span data-stu-id="c10a0-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c10a0-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c10a0-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

