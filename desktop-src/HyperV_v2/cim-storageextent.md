---
description: Descrive le funzionalità e la gestione dei supporti che archivia i dati e consente il recupero dei dati. Questa superclasse viene utilizzata per rappresentare componenti RAID software e hardware o un'estensione logica non elaborata di supporti fisici.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: Classe CIM_StorageExtent (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312330"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="579a2-104">Classe CIM_StorageExtent (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="579a2-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="579a2-105">Descrive le funzionalità e la gestione dei supporti che archivia i dati e consente il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="579a2-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="579a2-106">Questa superclasse viene utilizzata per rappresentare componenti RAID software e hardware o un'estensione logica non elaborata di supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="579a2-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="579a2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="579a2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="579a2-108">Members</span><span class="sxs-lookup"><span data-stu-id="579a2-108">Members</span></span>

<span data-ttu-id="579a2-109">La classe **CIM \_ StorageExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="579a2-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="579a2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="579a2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="579a2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="579a2-111">Properties</span></span>

<span data-ttu-id="579a2-112">La classe **CIM \_ StorageExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="579a2-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="579a2-113">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="579a2-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-116">Descrizione del supporto di lettura/scrittura del supporto.</span><span class="sxs-lookup"><span data-stu-id="579a2-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="579a2-117">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="579a2-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="579a2-118">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="579a2-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="579a2-119">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="579a2-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="579a2-120">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="579a2-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="579a2-121">**Scrivi una sola volta** (4)</span><span class="sxs-lookup"><span data-stu-id="579a2-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="579a2-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="579a2-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-123">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="579a2-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-125">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Archiviazione host DMTF \| 001,4 "," MIB. IETF \| host-Resources-MIB. hrStorageAllocationUnits "," MIF. \|Dispositivi di archiviazione DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="579a2-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-126">Dimensione, in byte, dei blocchi che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="579a2-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="579a2-127">Se vengono utilizzate dimensioni del blocco di variabili, questa proprietà deve specificare la dimensione massima del blocco.</span><span class="sxs-lookup"><span data-stu-id="579a2-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="579a2-128">Se le dimensioni del blocco sono sconosciute o se un concetto di blocco non è valido (ad esempio, per **CIM \_ AggregateExtent**, [**CIM \_ Memory**](cim-memory.md) o [**CIM \_ disco logico**](cim-logicaldisk.md)), questa proprietà deve essere impostata su "1" (Unknow).</span><span class="sxs-lookup"><span data-stu-id="579a2-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="579a2-129">**ConsumableBlocks**</span><span class="sxs-lookup"><span data-stu-id="579a2-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-130">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="579a2-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-132">Numero massimo di blocchi che è possibile usare quando si esegue il layering **CIM \_ StorageExtent** usando l'associazione di classi [**CIM \_ BasedOn**](cim-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="579a2-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="579a2-133">Questa proprietà ha un significato solo quando si fa riferimento all'extent di archiviazione nella proprietà **precedente** in un oggetto **CIM \_ BasedOn** .</span><span class="sxs-lookup"><span data-stu-id="579a2-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-134">**Dataorganization**</span><span class="sxs-lookup"><span data-stu-id="579a2-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-137">Tipo di organizzazione dati utilizzato dal supporto.</span><span class="sxs-lookup"><span data-stu-id="579a2-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="579a2-138">**Altro** (0)</span><span class="sxs-lookup"><span data-stu-id="579a2-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="579a2-139">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="579a2-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="579a2-140">**Blocco fisso** (2)</span><span class="sxs-lookup"><span data-stu-id="579a2-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="579a2-141">**Blocco di variabili** (3)</span><span class="sxs-lookup"><span data-stu-id="579a2-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="579a2-142">**Conteggio dati chiave** (4)</span><span class="sxs-lookup"><span data-stu-id="579a2-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="579a2-143">**Ridondanza dataridondanza**</span><span class="sxs-lookup"><span data-stu-id="579a2-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-146">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**","**CIM \_ StorageSetting**.**DataRedundancyMax**","**CIM \_ StorageSetting**.**DataRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="579a2-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-147">Numero di copie complete dei dati attualmente gestiti.</span><span class="sxs-lookup"><span data-stu-id="579a2-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-148">**DeltaReservation**</span><span class="sxs-lookup"><span data-stu-id="579a2-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-149">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="579a2-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-151">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("percentuale"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**","**CIM \_ StorageSetting**.**DeltaReservationMax**","**CIM \_ StorageSetting**.**DeltaReservationMin**")</span><span class="sxs-lookup"><span data-stu-id="579a2-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-152">Valore corrente per la prenotazione Delta.</span><span class="sxs-lookup"><span data-stu-id="579a2-152">The current value for delta reservation.</span></span> <span data-ttu-id="579a2-153">Percentuale che specifica la quantità di spazio che deve essere riservata in una replica per la memorizzazione nella cache delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="579a2-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="579a2-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="579a2-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-157">Tipo di rilevamento e correzione degli errori supportato dall'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="579a2-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-158">**ExtentStatus**</span><span class="sxs-lookup"><span data-stu-id="579a2-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-159">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="579a2-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-161">Informazioni aggiuntive sullo stato.</span><span class="sxs-lookup"><span data-stu-id="579a2-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="579a2-162">**Altro** (0)</span><span class="sxs-lookup"><span data-stu-id="579a2-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="579a2-163">**Sconosciuto** (1)</span><span class="sxs-lookup"><span data-stu-id="579a2-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="579a2-164">**Nessuno/non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="579a2-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="579a2-165">**Interruppe** (3)</span><span class="sxs-lookup"><span data-stu-id="579a2-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="579a2-166">**Dati persi** (4)</span><span class="sxs-lookup"><span data-stu-id="579a2-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="579a2-167">**Riconfigurazione dinamica** (5)</span><span class="sxs-lookup"><span data-stu-id="579a2-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="579a2-168">**Esposto** (6)</span><span class="sxs-lookup"><span data-stu-id="579a2-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="579a2-169">**Esposto in frazioni** (7)</span><span class="sxs-lookup"><span data-stu-id="579a2-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="579a2-170">**Esposto parzialmente** (8)</span><span class="sxs-lookup"><span data-stu-id="579a2-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="579a2-171">**Protezione disabilitata** (9)</span><span class="sxs-lookup"><span data-stu-id="579a2-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="579a2-172">**Pronto** (10)</span><span class="sxs-lookup"><span data-stu-id="579a2-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="579a2-173">**Ricompila** (11)</span><span class="sxs-lookup"><span data-stu-id="579a2-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="579a2-174">**Ricalcola** (12)</span><span class="sxs-lookup"><span data-stu-id="579a2-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="579a2-175">**Ricambio in uso** (13)</span><span class="sxs-lookup"><span data-stu-id="579a2-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="579a2-176">**Verifica in corso** (14)</span><span class="sxs-lookup"><span data-stu-id="579a2-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="579a2-177">**Accesso in banda concesso** (15)</span><span class="sxs-lookup"><span data-stu-id="579a2-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="579a2-178">**Importato** (16)</span><span class="sxs-lookup"><span data-stu-id="579a2-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="579a2-179">**Esportato** (17)</span><span class="sxs-lookup"><span data-stu-id="579a2-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="579a2-180">**DMTF riservato** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="579a2-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="579a2-181">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="579a2-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="579a2-182">**IsBasedOnUnderlyingRedundancy**</span><span class="sxs-lookup"><span data-stu-id="579a2-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-183">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="579a2-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-185">**true** se gli extent di archiviazione sottostanti sono membri di [**un \_ StorageRedundancyGroup CIM**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="579a2-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-186">**Nome**</span><span class="sxs-lookup"><span data-stu-id="579a2-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-187">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="579a2-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-189">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCIs-T10 \| vital 83, Association 0 \| Identifier "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**","**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="579a2-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-190">Identificatore univoco per l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="579a2-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="579a2-191">La proprietà **NameFormat** specifica il formato di denominazione da utilizzare nella proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="579a2-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-192">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="579a2-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-195">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Nome**","**CIM \_ StorageExtent**.**NameNamespace**","**CIM \_ StorageExtent**.**OtherNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="579a2-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-196">Formato di denominazione per la proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="579a2-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="579a2-197">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="579a2-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="579a2-198">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="579a2-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="579a2-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="579a2-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="579a2-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="579a2-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="579a2-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="579a2-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="579a2-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="579a2-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="579a2-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="579a2-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="579a2-204">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="579a2-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="579a2-205">**NodeWWN** (8)</span><span class="sxs-lookup"><span data-stu-id="579a2-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="579a2-206">**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="579a2-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="579a2-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="579a2-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="579a2-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="579a2-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="579a2-209">**Nome dispositivo del sistema operativo** (12)</span><span class="sxs-lookup"><span data-stu-id="579a2-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="579a2-210">**NameNamespace**</span><span class="sxs-lookup"><span data-stu-id="579a2-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-213">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCIs-T10 \| vital 83, Association 0 \| Identifier "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Nome**","**CIM \_ StorageExtent**.**OtherNameNamespace**","**CIM \_ StorageExtent**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="579a2-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-214">Spazio dei nomi della proprietà Name.</span><span class="sxs-lookup"><span data-stu-id="579a2-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="579a2-215">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="579a2-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="579a2-216">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="579a2-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="579a2-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="579a2-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="579a2-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="579a2-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="579a2-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="579a2-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="579a2-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="579a2-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="579a2-221">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="579a2-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="579a2-222">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="579a2-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="579a2-223">**Spazio dei nomi del dispositivo del sistema operativo** (8)</span><span class="sxs-lookup"><span data-stu-id="579a2-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="579a2-224">**NoSinglePointOfFailure**</span><span class="sxs-lookup"><span data-stu-id="579a2-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-225">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="579a2-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-227">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span><span class="sxs-lookup"><span data-stu-id="579a2-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-228">**true** se non sono presenti singoli punti di errore. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="579a2-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="579a2-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-230">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="579a2-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-232">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Archiviazione host DMTF \| 001,5 "," MIB. \|Host IETF-risorse-MIB. hrStorageSize ")</span><span class="sxs-lookup"><span data-stu-id="579a2-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-233">Numero totale di blocchi logicamente contigui che formano l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="579a2-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="579a2-234">Le dimensioni totali dell'extent di archiviazione vengono calcolate moltiplicando **blockSize** per **Proprietà NumberOfBlocks**.</span><span class="sxs-lookup"><span data-stu-id="579a2-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="579a2-235">Se **blockSize** è "1", questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="579a2-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-236">**OtherNameFormat**</span><span class="sxs-lookup"><span data-stu-id="579a2-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="579a2-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-239">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="579a2-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-240">Formato della proprietà **Name** quando la proprietà **NameFormat** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="579a2-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="579a2-241">**OtherNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="579a2-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="579a2-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-244">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="579a2-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-245">Descrizione dello spazio dei nomi della proprietà **Name** quando la proprietà **NameNamespace** è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="579a2-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="579a2-246">**PackageRedundancy**</span><span class="sxs-lookup"><span data-stu-id="579a2-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="579a2-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-249">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**","**CIM \_ StorageSetting**.**PackageRedundancyMax**","**CIM \_ StorageSetting**.**PackageRedundancyMin**")</span><span class="sxs-lookup"><span data-stu-id="579a2-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-250">Numero corrente di pacchetti fisici che possono avere esito negativo senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="579a2-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="579a2-251">Ad esempio, in un dominio di archiviazione può corrispondere al numero di mandrini del disco.</span><span class="sxs-lookup"><span data-stu-id="579a2-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-252">**Originale**</span><span class="sxs-lookup"><span data-stu-id="579a2-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-253">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="579a2-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-255">**true** se l'extent di archiviazione è primordiale; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="579a2-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-256">**Scopo**</span><span class="sxs-lookup"><span data-stu-id="579a2-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="579a2-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="579a2-259">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Host IETF-risorse-MIB. hrStorageDescr ")</span><span class="sxs-lookup"><span data-stu-id="579a2-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="579a2-260">Descrizione dell'utilizzo del supporto.</span><span class="sxs-lookup"><span data-stu-id="579a2-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="579a2-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="579a2-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="579a2-262">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="579a2-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="579a2-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="579a2-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="579a2-264">**true** se l'accesso all'archiviazione viene eseguito in modo sequenziale da un oggetto [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) ; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="579a2-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="579a2-265">Requisiti</span><span class="sxs-lookup"><span data-stu-id="579a2-265">Requirements</span></span>



| <span data-ttu-id="579a2-266">Requisito</span><span class="sxs-lookup"><span data-stu-id="579a2-266">Requirement</span></span> | <span data-ttu-id="579a2-267">Valore</span><span class="sxs-lookup"><span data-stu-id="579a2-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579a2-268">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="579a2-268">Minimum supported client</span></span><br/> | <span data-ttu-id="579a2-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="579a2-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="579a2-270">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="579a2-270">Minimum supported server</span></span><br/> | <span data-ttu-id="579a2-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="579a2-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="579a2-272">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="579a2-272">Namespace</span></span><br/>                | <span data-ttu-id="579a2-273">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="579a2-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="579a2-274">MOF</span><span class="sxs-lookup"><span data-stu-id="579a2-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="579a2-275"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="579a2-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="579a2-276">DLL</span><span class="sxs-lookup"><span data-stu-id="579a2-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579a2-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="579a2-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="579a2-278">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="579a2-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579a2-279">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="579a2-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

