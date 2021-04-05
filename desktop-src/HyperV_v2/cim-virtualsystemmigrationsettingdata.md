---
description: Definisce le impostazioni per la migrazione del sistema virtuale gestita da un'istanza della classe CIM \_ VirtualSystemMigrationService.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: Classe CIM_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756272"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="7f528-103">CIM \_ VirtualSystemMigrationSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="7f528-103">CIM\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="7f528-104">Definisce le impostazioni per la migrazione del sistema virtuale gestita da un'istanza della classe [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7f528-104">Defines the settings for virtual system migration that is managed by an instance of the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f528-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f528-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a><span data-ttu-id="7f528-106">Members</span><span class="sxs-lookup"><span data-stu-id="7f528-106">Members</span></span>

<span data-ttu-id="7f528-107">La classe **CIM \_ VirtualSystemMigrationSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7f528-107">The **CIM\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7f528-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f528-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f528-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f528-109">Properties</span></span>

<span data-ttu-id="7f528-110">La classe **CIM \_ VirtualSystemMigrationSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f528-110">The **CIM\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f528-111">**Larghezza di banda**</span><span class="sxs-lookup"><span data-stu-id="7f528-111">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f528-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f528-114">Qualificatori: [**misuratore**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span><span class="sxs-lookup"><span data-stu-id="7f528-114">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**BandwidthUnit**")</span></span>
</dt> </dl>

<span data-ttu-id="7f528-115">Larghezza di banda assegnata o richiesta per un'operazione di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f528-115">The bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="7f528-116">"0" è la larghezza di banda predefinita per le richieste di migrazione.</span><span class="sxs-lookup"><span data-stu-id="7f528-116">"0" is default bandwidth for migration requests.</span></span>

<span data-ttu-id="7f528-117">Le proprietà **larghezza di banda** e **priorità** possono essere utilizzate insieme.</span><span class="sxs-lookup"><span data-stu-id="7f528-117">The **Bandwidth** and **Priority** properties may be used in conjunction.</span></span> <span data-ttu-id="7f528-118">I processi di migrazione con i valori con la massima **priorità** uguale condividono la larghezza di banda disponibile in base alla larghezza di banda richiesta.</span><span class="sxs-lookup"><span data-stu-id="7f528-118">Migration processes that have the highest equal **Priority** values share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="7f528-119">Se non viene utilizzata tutta la larghezza di banda da questo set di processi, i processi di migrazione con i successivi valori di **priorità** più bassa condividono la larghezza di banda rimanente.</span><span class="sxs-lookup"><span data-stu-id="7f528-119">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal **Priority** values share the remaining bandwidth.</span></span> <span data-ttu-id="7f528-120">Se rimane una maggiore larghezza di banda, verranno presi in considerazione i processi di migrazione con i valori di **priorità** inferiore uguali.</span><span class="sxs-lookup"><span data-stu-id="7f528-120">If more bandwidth remains, migration processes with the next lower equal **Priority** values are considered.</span></span>

<span data-ttu-id="7f528-121">L'unità utilizzata nella proprietà **Bandwidth** è specificata dal valore della proprietà **BandwidthUnit** .</span><span class="sxs-lookup"><span data-stu-id="7f528-121">The unit used in **Bandwidth** property is specified by the value of the **BandwidthUnit** property.</span></span>

<span data-ttu-id="7f528-122">Se il valore della proprietà **BandwidthUnit** è "percent", si applicano le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f528-122">If the value of the **BandwidthUnit** property is "percent", the following rules apply:</span></span>

-   <span data-ttu-id="7f528-123">Il valore della proprietà della **larghezza di banda** deve essere compreso tra "0" e "100", con valori più elevati che indicano una larghezza di banda maggiore.</span><span class="sxs-lookup"><span data-stu-id="7f528-123">The value of the **Bandwidth** property must be between "0" and "100", with higher values indicating a higher bandwidth.</span></span>
-   <span data-ttu-id="7f528-124">Il valore "100" indica tutta la larghezza di banda disponibile per l'esecuzione delle operazioni di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f528-124">A value of "100" indicates all available bandwidth for performing virtual system migration operations.</span></span>
-   <span data-ttu-id="7f528-125">I valori compresi tra "1" e "100" sono correlati in modo lineare con l'intervallo della larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f528-125">Values between "1" and "100" linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="7f528-126">Ad esempio, un valore di 50 richiede metà della larghezza di banda disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f528-126">For example, a value of 50 requests half of the available bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="7f528-127">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="7f528-127">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f528-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f528-130">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Larghezza di banda**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="7f528-130">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**Bandwidth**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="7f528-131">Unità utilizzata dalla proprietà della **larghezza di banda** .</span><span class="sxs-lookup"><span data-stu-id="7f528-131">The unit used by the **Bandwidth** property.</span></span> <span data-ttu-id="7f528-132">Il valore di questa proprietà deve essere un valore valido del qualificatore unità di codice definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="7f528-132">The value of this property should be a legal value of the Programmatic Units qualifier defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

> [!Note]  
> <span data-ttu-id="7f528-133">I profili come DMTF DSP1081 definiscono il modo in cui i client possono individuare il set di unità supportate da un'implementazione e gli intervalli e gli incrementi per i valori della proprietà della **larghezza di banda** .</span><span class="sxs-lookup"><span data-stu-id="7f528-133">Profiles such as DMTF DSP1081 define how clients can discover the set of units supported by an implementation, and ranges and increments for values of the **Bandwidth** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="7f528-134">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="7f528-134">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f528-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f528-137">Tipo di operazione di migrazione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="7f528-137">The type of migration operation to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f528-138">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7f528-138">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f528-139">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7f528-139">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

<span data-ttu-id="7f528-140">**Live** (2)</span><span class="sxs-lookup"><span data-stu-id="7f528-140">**Live** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

<span data-ttu-id="7f528-141">**Riprendi** (3)</span><span class="sxs-lookup"><span data-stu-id="7f528-141">**Resume** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

<span data-ttu-id="7f528-142">**Riavvio** (4)</span><span class="sxs-lookup"><span data-stu-id="7f528-142">**Restart** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7f528-143">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="7f528-143">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-144">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f528-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f528-146">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")</span><span class="sxs-lookup"><span data-stu-id="7f528-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**TransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="7f528-147">Tipo di trasporto da applicare se il valore di **TransportType** è "1" (other).</span><span class="sxs-lookup"><span data-stu-id="7f528-147">The type of transport to apply if the value of **TransportType** is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="7f528-148">**Priorità**</span><span class="sxs-lookup"><span data-stu-id="7f528-148">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f528-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f528-151">Importanza della migrazione relativa che l'implementazione della migrazione del sistema virtuale può utilizzare per ordinare o assegnare preferenza tra più richieste di migrazione in sospeso.</span><span class="sxs-lookup"><span data-stu-id="7f528-151">The relative migration importance that the virtual system migration implementation may use to order or assign preference among multiple pending migration requests.</span></span> <span data-ttu-id="7f528-152">Più basso è il valore, maggiore è la priorità.</span><span class="sxs-lookup"><span data-stu-id="7f528-152">The lower the value, the higher the priority.</span></span> <span data-ttu-id="7f528-153">"0" è la larghezza di banda predefinita per le richieste di migrazione.</span><span class="sxs-lookup"><span data-stu-id="7f528-153">"0" is default bandwidth for migration requests.</span></span>

</dd> <dt>

<span data-ttu-id="7f528-154">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="7f528-154">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f528-155">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f528-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f528-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f528-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f528-157">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")</span><span class="sxs-lookup"><span data-stu-id="7f528-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VirtualSystemMigrationSettingData**.**OtherTransportType**")</span></span>
</dt> </dl>

<span data-ttu-id="7f528-158">Tipo di trasporto da applicare a un'operazione di migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f528-158">The type of transport to apply to a virtual system migration operation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7f528-159">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7f528-159">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7f528-160">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7f528-160">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="7f528-161">**SSH** (2)</span><span class="sxs-lookup"><span data-stu-id="7f528-161">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="7f528-162">**TLS** (3)</span><span class="sxs-lookup"><span data-stu-id="7f528-162">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="7f528-163">**TLS Strict** (4)</span><span class="sxs-lookup"><span data-stu-id="7f528-163">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="7f528-164">**TCP** (5)</span><span class="sxs-lookup"><span data-stu-id="7f528-164">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="7f528-165">**IPC** (6)</span><span class="sxs-lookup"><span data-stu-id="7f528-165">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7f528-166">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7f528-166">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7f528-167">**Fornitore riservato** (32768...)</span><span class="sxs-lookup"><span data-stu-id="7f528-167">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="7f528-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7f528-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7f528-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f528-169">Requirements</span></span>



| <span data-ttu-id="7f528-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f528-170">Requirement</span></span> | <span data-ttu-id="7f528-171">Valore</span><span class="sxs-lookup"><span data-stu-id="7f528-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f528-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f528-172">Minimum supported client</span></span><br/> | <span data-ttu-id="7f528-173">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7f528-173">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="7f528-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f528-174">Minimum supported server</span></span><br/> | <span data-ttu-id="7f528-175">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f528-175">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="7f528-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f528-176">Namespace</span></span><br/>                | <span data-ttu-id="7f528-177">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7f528-177">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7f528-178">MOF</span><span class="sxs-lookup"><span data-stu-id="7f528-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f528-179"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f528-179"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f528-180">DLL</span><span class="sxs-lookup"><span data-stu-id="7f528-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f528-181"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f528-181"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7f528-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f528-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f528-183">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7f528-183">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

