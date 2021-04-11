---
description: Rappresenta le impostazioni specifiche relative all'allocazione di archiviazione virtuale.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Classe Msvm_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232265"
---
# <a name="msvm_storageallocationsettingdata-class"></a><span data-ttu-id="7c429-103">\_Classe MSVM StorageAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="7c429-103">Msvm\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="7c429-104">Rappresenta le impostazioni specifiche relative all'allocazione di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-104">Represents settings specifically related to the allocation of virtual storage.</span></span>

<span data-ttu-id="7c429-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7c429-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c429-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c429-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a><span data-ttu-id="7c429-107">Members</span><span class="sxs-lookup"><span data-stu-id="7c429-107">Members</span></span>

<span data-ttu-id="7c429-108">La **classe \_ StorageAllocationSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7c429-108">The **Msvm\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7c429-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c429-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c429-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c429-110">Properties</span></span>

<span data-ttu-id="7c429-111">La **classe \_ StorageAllocationSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7c429-111">The **Msvm\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c429-112">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="7c429-112">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-115">Specifica l'accesso alla risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c429-115">Specifies the storage access.</span></span> <span data-ttu-id="7c429-116">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-116">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="7c429-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-117"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="7c429-118"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-119"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-120"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c429-121">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="7c429-121">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-124">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-124">The address of the resource.</span></span> <span data-ttu-id="7c429-125">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-125">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-126">**AddressOnParent**</span><span class="sxs-lookup"><span data-stu-id="7c429-126">**AddressOnParent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-129">Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="7c429-129">Describes the address of this resource in the context of the parent.</span></span> <span data-ttu-id="7c429-130">Le proprietà **Parent** e **AddressOnParent** vengono usate per descrivere la relazione del controller, nonché l'ordine dei dispositivi in un controller.</span><span class="sxs-lookup"><span data-stu-id="7c429-130">The **Parent** and **AddressOnParent** properties are used to describe the controller relationship as well as the ordering of devices on a controller.</span></span> <span data-ttu-id="7c429-131">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-131">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-132">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="7c429-132">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-135">Unità di allocazione utilizzate dalle proprietà di **prenotazione** e **limite** .</span><span class="sxs-lookup"><span data-stu-id="7c429-135">The units of allocation used by the **Reservation** and **Limit** properties.</span></span> <span data-ttu-id="7c429-136">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-136">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-137">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="7c429-137">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-138">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c429-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-140">Indica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c429-140">Indicates whether the resource will be automatically allocated.</span></span> <span data-ttu-id="7c429-141">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-141">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-142">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="7c429-142">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c429-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-145">Indica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c429-145">Indicates whether the resource will be automatically deallocated.</span></span> <span data-ttu-id="7c429-146">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-146">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-147">**CachingMode**</span><span class="sxs-lookup"><span data-stu-id="7c429-147">**CachingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-150">Indica se e come usare la memorizzazione nella cache dei file in memoria per questo disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-150">Indicates whether and how in-memory file caching should be used for this VHD.</span></span> <span data-ttu-id="7c429-151">Il criterio predefinito è impostato nel campo **DefaultVirtualHardDiskCachingMode** della classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="7c429-151">The default policy is set in the **DefaultVirtualHardDiskCachingMode** field of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-152">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7c429-152">Added in Windows 10.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7c429-153">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="7c429-154">**Impostazione predefinita** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-154">**Default** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

<span data-ttu-id="7c429-155">**Nessuna memorizzazione nella cache** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-155">**No Caching** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

<span data-ttu-id="7c429-156">**Memorizzare nella cache elementi padre condivisibili** (4)</span><span class="sxs-lookup"><span data-stu-id="7c429-156">**Cache Sharable Parents** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7c429-157">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7c429-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-160">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7c429-160">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="7c429-161">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c429-161">A short description of the object.</span></span> <span data-ttu-id="7c429-162">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "impostazioni predefinite immagine disco rigido".</span><span class="sxs-lookup"><span data-stu-id="7c429-162">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hard Disk Image Default Settings".</span></span>

</dd> <dt>

<span data-ttu-id="7c429-163">**Connection**</span><span class="sxs-lookup"><span data-stu-id="7c429-163">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-164">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c429-164">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c429-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-166">Dispositivo a cui è connessa la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-166">The device to which this resource is connected.</span></span> <span data-ttu-id="7c429-167">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-167">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-168">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="7c429-168">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-169">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-171">Visibilità del consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="7c429-171">The consumer's visibility to the allocated resource.</span></span> <span data-ttu-id="7c429-172">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-172">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="7c429-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passato** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-174"><span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Passed-Through** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualizzato** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-175"><span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualized** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Non rappresentata** (4)</span><span class="sxs-lookup"><span data-stu-id="7c429-176"><span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Not represented** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c429-177">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7c429-177">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-180">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7c429-180">A description of the object.</span></span> <span data-ttu-id="7c429-181">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "descrive le impostazioni predefinite per le risorse dell'immagine del disco rigido".</span><span class="sxs-lookup"><span data-stu-id="7c429-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Describes the default settings for the hard disk image resources".</span></span>

</dd> <dt>

<span data-ttu-id="7c429-182">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7c429-182">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-183">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-185">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c429-185">A display name for the object.</span></span> <span data-ttu-id="7c429-186">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c429-186">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-187">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="7c429-187">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-190">Identificatore univoco per l'extent dell'host.</span><span class="sxs-lookup"><span data-stu-id="7c429-190">A unique identifier for the host extent.</span></span> <span data-ttu-id="7c429-191">L'extent dell'host identificato viene usato per l'allocazione delle risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c429-191">The identified host extent is used for the storage resource allocation.</span></span> <span data-ttu-id="7c429-192">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-192">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-193">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="7c429-193">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-194">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-196">Identifica il formato utilizzato per la proprietà **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="7c429-196">Identifies the format that is used for the **HostExtentName** property.</span></span> <span data-ttu-id="7c429-197">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-197">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="7c429-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-198"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c429-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="7c429-200"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="7c429-201"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="7c429-202"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="7c429-203"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome dispositivo del sistema operativo** (12)</span><span class="sxs-lookup"><span data-stu-id="7c429-204"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="7c429-205"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7c429-206">)</span><span class="sxs-lookup"><span data-stu-id="7c429-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c429-207">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7c429-207">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-210">Se l'extent dell'host è un volume SCSI, l'origine preferita per i nomi di volume SCSI è SCSI Vital pagina 83 risposte.</span><span class="sxs-lookup"><span data-stu-id="7c429-210">If the host extent is a SCSI volume, then the preferred source for SCSI volume names is SCSI VPD Page 83 responses.</span></span> <span data-ttu-id="7c429-211">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-211">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

<dl> <dt>

<span data-ttu-id="7c429-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c429-213"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-214"><span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-215"><span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="7c429-216"><span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="7c429-217"><span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="7c429-218"><span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="7c429-219"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Spazio dei nomi del dispositivo del sistema operativo** (8)</span><span class="sxs-lookup"><span data-stu-id="7c429-220"><span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**OS Device Namespace** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="7c429-221"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7c429-222">)</span><span class="sxs-lookup"><span data-stu-id="7c429-222">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c429-223">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7c429-223">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-224">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-224">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-226">Identifica l'indirizzo iniziale nell'extent di archiviazione dell'host, identificato dalla proprietà **HostExtentName** , utilizzato per l'allocazione dell'extent di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-226">Identifies the starting address on the host storage extent, identified by the **HostExtentName** property, that is used for the allocation of the virtual storage extent.</span></span> <span data-ttu-id="7c429-227">Un valore **null** indica che non esiste alcun mapping diretto dell'extent di archiviazione virtuale all'extent di archiviazione dell'host a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="7c429-227">A **Null** value indicates that there is no direct mapping of the virtual storage extent to the referenced host storage extent.</span></span> <span data-ttu-id="7c429-228">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-228">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-229">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="7c429-229">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-230">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c429-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c429-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-232">È possibile assegnare una sola risorsa host a ogni dispositivo della macchina virtuale, in modo che sia possibile impostare solo il primo elemento della matrice.</span><span class="sxs-lookup"><span data-stu-id="7c429-232">Only one host resource can be assigned to each device in the virtual machine, so only the first element of this array can be set.</span></span> <span data-ttu-id="7c429-233">Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare.</span><span class="sxs-lookup"><span data-stu-id="7c429-233">For devices that support this feature, set the first element of the **HostResource** array to contain a reference to the underlying host resource to be assigned.</span></span> <span data-ttu-id="7c429-234">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-234">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7c429-235">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7c429-235">This is a read-only property.</span></span> <span data-ttu-id="7c429-236">Tuttavia, se la proprietà **ResourceType** è 31 (disco logico) e la proprietà **ResourceSubType** è "Microsoft: Hyper-v: disco rigido virtuale", "Microsoft: Hyper-v: disco CD/DVD virtuale" o "Microsoft: Hyper-v: disco floppy virtuale", è possibile modificare la proprietà **HostResource** usando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7c429-236">But if the **ResourceType** property is 31 (Logical Disk) and the **ResourceSubType** property is "Microsoft:Hyper-V:Virtual Hard Disk", "Microsoft:Hyper-V:Virtual CD/DVD Disk", or "Microsoft:Hyper-V:Virtual Floppy Disk", the **HostResource** property can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-237">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="7c429-237">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-238">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-238">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-240">Dimensione, in byte, dei blocchi allocati nell'host come risultato della richiesta di allocazione delle risorse di archiviazione o di allocazione delle risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c429-240">The size, in bytes, of the blocks that are allocated at the host as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="7c429-241">Se la dimensione del blocco è variabile, verranno specificate le dimensioni massime del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="7c429-241">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="7c429-242">Se le dimensioni del blocco sono sconosciute o se non si applica un concetto di blocco, verrà utilizzato il valore 1.</span><span class="sxs-lookup"><span data-stu-id="7c429-242">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="7c429-243">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-243">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-244">**IgnoreFlushes**</span><span class="sxs-lookup"><span data-stu-id="7c429-244">**IgnoreFlushes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c429-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-247">Se impostato su true, Hyper-V ignorerà lo scaricamento in scrittura per la macchina virtuale specifica.</span><span class="sxs-lookup"><span data-stu-id="7c429-247">If set to true, Hyper-V will ignore write back flushing for that particular virtual machine.</span></span> <span data-ttu-id="7c429-248">Se è impostato su false, Hyper-V continuerà a eseguire il writeback sul disco a ogni svuotamento.</span><span class="sxs-lookup"><span data-stu-id="7c429-248">If set to false, Hyper-V will continue to write back to the disk on every flush.</span></span> <span data-ttu-id="7c429-249">L'impostazione predefinita è false.</span><span class="sxs-lookup"><span data-stu-id="7c429-249">The default setting is false.</span></span>

<span data-ttu-id="7c429-250">**Windows 10:** Questo valore non è supportato fino a Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7c429-250">**Windows 10:** This value is not supported until Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-251">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7c429-251">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-252">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-253">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-254">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7c429-254">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7c429-255">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7c429-255">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7c429-256">Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c429-256">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-257">**IOPSAllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="7c429-257">**IOPSAllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-260">Specifica le unità di allocazione utilizzate dalle proprietà **IOPSLimit** e **IOPSReservation** .</span><span class="sxs-lookup"><span data-stu-id="7c429-260">Specifies the allocation units used by the **IOPSLimit** and **IOPSReservation** properties.</span></span> <span data-ttu-id="7c429-261">Questa proprietà ha sempre il valore:</span><span class="sxs-lookup"><span data-stu-id="7c429-261">This property always has the value:</span></span>

<span data-ttu-id="7c429-262">"conteggio (I/O normalizzato)/secondo"</span><span class="sxs-lookup"><span data-stu-id="7c429-262">"count(normalized I/O) / second"</span></span>

<span data-ttu-id="7c429-263">La velocità effettiva viene misurata in operazioni di I/O normalizzate al secondo (IOPS) anziché IOPS non elaborate.</span><span class="sxs-lookup"><span data-stu-id="7c429-263">Throughput is measured in normalized I/O operations per second (IOPS) instead of raw IOPS.</span></span> <span data-ttu-id="7c429-264">Quando si utilizzano IOPS normalizzate, ogni richiesta di I/O viene rappresentata come 1 I/O normalizzato se le dimensioni della richiesta sono inferiori o uguali a una dimensione di base predefinita (8 KB).</span><span class="sxs-lookup"><span data-stu-id="7c429-264">When using normalized IOPS, each I/O request is accounted for as 1 normalized I/O if the size of the request is less than or equal to a predefined base size (8 KB).</span></span> <span data-ttu-id="7c429-265">Le richieste di dimensioni superiori a quelle di base sono rappresentate come N operazioni di I/O, dove N è il valore arrotondato per eccesso della dimensione della richiesta divisa per le dimensioni di base.</span><span class="sxs-lookup"><span data-stu-id="7c429-265">Requests that are larger than the base size are accounted for as N I/O operations, where N is the rounded-up value of the request size divided by the base size.</span></span> <span data-ttu-id="7c429-266">Se, ad esempio, le dimensioni di base sono pari a 8 KB, una richiesta da 16 KB viene conteggiata come 2 operazioni di I/O normalizzate, una richiesta di 32 KB come 4 operazioni di I/O normalizzate e così via.</span><span class="sxs-lookup"><span data-stu-id="7c429-266">For example, if the base size is 8 KB, a 16-KB request is counted as 2 normalized I/O operations, a 32-KB request as 4 normalized I/O operations, and so on.</span></span>

<span data-ttu-id="7c429-267">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7c429-267">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-268">**IOPSLimit**</span><span class="sxs-lookup"><span data-stu-id="7c429-268">**IOPSLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-269">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-269">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-270">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-271">Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 miliardo)</span><span class="sxs-lookup"><span data-stu-id="7c429-271">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="7c429-272">Numero massimo di operazioni di I/O al secondo (IOPS) che verranno gestite per questo extent di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-272">The maximum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span> <span data-ttu-id="7c429-273">Se il valore non è definito o è zero, non esiste alcun limite al numero di IOPS che il dispositivo può emettere.</span><span class="sxs-lookup"><span data-stu-id="7c429-273">If the value isn't defined or is zero, there is no limit to the number of IOPS that the device can issue.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-274">Per modificare il valore di questa proprietà, è possibile usare il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7c429-274">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="7c429-275">Questa proprietà è significativa solo per le istanze di **\_ StorageAllocationSettingData MSVM** che richiedono allocazioni di risorse per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7c429-275">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="7c429-276">Viene ignorato durante l'allocazione delle risorse a un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="7c429-276">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="7c429-277">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7c429-277">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-278">**IOPSReservation**</span><span class="sxs-lookup"><span data-stu-id="7c429-278">**IOPSReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-279">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-281">Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 miliardo)</span><span class="sxs-lookup"><span data-stu-id="7c429-281">Qualifiers: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)</span></span>
</dt> </dl>

<span data-ttu-id="7c429-282">Numero minimo di operazioni di I/O al secondo (IOPS) che verranno gestite per questo extent di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-282">The minimum number of I/O operations per second (IOPS) that will be serviced for this virtual storage extent.</span></span>

<span data-ttu-id="7c429-283">Se sono definiti sia **IOPSLimit** che **IOPSReservation** , il valore di **IOPSLimit** deve essere maggiore o uguale al valore di **IOPSReservation**.</span><span class="sxs-lookup"><span data-stu-id="7c429-283">If both **IOPSLimit** and **IOPSReservation** are defined, the value of **IOPSLimit** must be greater than or equal to the value of **IOPSReservation**.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-284">Per modificare il valore di questa proprietà, è possibile usare il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7c429-284">You can use the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class to modify the value of this property.</span></span> <span data-ttu-id="7c429-285">Questa proprietà è significativa solo per le istanze di **\_ StorageAllocationSettingData MSVM** che richiedono allocazioni di risorse per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="7c429-285">This property is meaningful only for **Msvm\_StorageAllocationSettingData** instances that request resource allocations for virtual machines.</span></span> <span data-ttu-id="7c429-286">Viene ignorato durante l'allocazione delle risorse a un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="7c429-286">It's ignored when allocating resources to a child pool.</span></span>

 

<span data-ttu-id="7c429-287">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7c429-287">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-288">**Limite**</span><span class="sxs-lookup"><span data-stu-id="7c429-288">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-289">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-289">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-291">Numero massimo di blocchi che verranno concessi per l'allocazione delle risorse di archiviazione nell'host.</span><span class="sxs-lookup"><span data-stu-id="7c429-291">The maximum number of blocks that will be granted for this storage resource allocation at the host.</span></span> <span data-ttu-id="7c429-292">La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="7c429-292">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="7c429-293">In genere il valore di questa proprietà riflette una dimensione massima per l'extent dell'host allocato che corrisponde alla dimensione dell'extent di archiviazione virtuale presentato al consumer.</span><span class="sxs-lookup"><span data-stu-id="7c429-293">Usually the value of this property would reflect a maximum size for the allocated host extent that matches the size of the virtual storage extent presented to the consumer.</span></span> <span data-ttu-id="7c429-294">Un valore minore di che indica una situazione in cui è previsto un extent di archiviazione virtuale a bassa densità, in cui la velocità di riempimento è limitata dal valore della proprietà Limit.</span><span class="sxs-lookup"><span data-stu-id="7c429-294">A value less than that would indicate a situation where a sparsely populated virtual storage extent is expected, where the fill rate is limited by the value of the Limit property.</span></span> <span data-ttu-id="7c429-295">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-295">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-296">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="7c429-296">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-297">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-299">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7c429-299">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="7c429-300">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-300">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-301">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="7c429-301">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-304">Stringa che descrive il formato della proprietà **HostExtentName** se la proprietà **HostExtentNameFormat** è 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7c429-304">A string that describes the format of the **HostExtentName** property if the **HostExtentNameFormat** property is 1 (Other).</span></span> <span data-ttu-id="7c429-305">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-305">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-306">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="7c429-306">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-309">Stringa che descrive lo spazio dei nomi della proprietà **HostExtentName** se la proprietà **HostExtentNameNamespace** contiene 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7c429-309">A string that describes the namespace of the **HostExtentName** property if the **HostExtentNameNamespace** property contains 1 (Other).</span></span> <span data-ttu-id="7c429-310">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-310">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-311">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="7c429-311">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-312">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-313">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-314">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7c429-314">A string that describes the resource type when a well-defined value is not available and [**ResourceType**](msvm-processorsettingdata.md) has the value 1(Other).</span></span> <span data-ttu-id="7c429-315">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-315">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-316">**Parent**</span><span class="sxs-lookup"><span data-stu-id="7c429-316">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-317">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-319">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-319">The parent of the resource.</span></span> <span data-ttu-id="7c429-320">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-320">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-321">**PersistentReservationsSupported**</span><span class="sxs-lookup"><span data-stu-id="7c429-321">**PersistentReservationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-322">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c429-322">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-323">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-324">Indica se il disco rigido virtuale supporta le prenotazioni permanenti SCSI-3.</span><span class="sxs-lookup"><span data-stu-id="7c429-324">Indicates whether the virtual hard disk supports SCSI-3 persistent reservations.</span></span>

<span data-ttu-id="7c429-325">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="7c429-325">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-326">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="7c429-326">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-329">Identificatore del pool di risorse da cui è stata allocata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-329">The identifier of the resource pool from which this resource was allocated.</span></span> <span data-ttu-id="7c429-330">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-330">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-331">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="7c429-331">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-332">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-332">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-334">Qualificatori: **override** ("Reservation"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")</span><span class="sxs-lookup"><span data-stu-id="7c429-334">Qualifiers: **Override** ("Reservation"), **ModelCorrespondence** ("CIM\_StorageAllocationSettingData.HostResourceBlockSize")</span></span>
</dt> </dl>

<span data-ttu-id="7c429-335">Numero di blocchi garantiti per l'allocazione delle risorse di archiviazione nell'host.</span><span class="sxs-lookup"><span data-stu-id="7c429-335">The number of blocks that are guaranteed to be available for this storage resource allocation at the host.</span></span> <span data-ttu-id="7c429-336">La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="7c429-336">The block size is specified by the **HostResourceBlockSize** property.</span></span> <span data-ttu-id="7c429-337">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-337">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-338">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="7c429-338">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-341">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-341">A string that describes an implementation-specific subtype for this resource.</span></span> <span data-ttu-id="7c429-342">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c429-342">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="7c429-343">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-343">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-344">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="7c429-344">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-345">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-347">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="7c429-347">The type of resource this allocation setting represents.</span></span> <span data-ttu-id="7c429-348">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-348">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<dl> <dt>

<span data-ttu-id="7c429-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7c429-349"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-350"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-351"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="7c429-352"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="7c429-353"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="7c429-354"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="7c429-355"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="7c429-356"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="7c429-357"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="7c429-358"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="7c429-359"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="7c429-360"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="7c429-361"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unità dischetto** (14)</span><span class="sxs-lookup"><span data-stu-id="7c429-362"><span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskette Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="7c429-363"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="7c429-364"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)</span><span class="sxs-lookup"><span data-stu-id="7c429-365"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)</span><span class="sxs-lookup"><span data-stu-id="7c429-366"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (19)</span><span class="sxs-lookup"><span data-stu-id="7c429-367"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (20)</span><span class="sxs-lookup"><span data-stu-id="7c429-368"><span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)</span><span class="sxs-lookup"><span data-stu-id="7c429-369"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)</span><span class="sxs-lookup"><span data-stu-id="7c429-370"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)</span><span class="sxs-lookup"><span data-stu-id="7c429-371"><span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (24)</span><span class="sxs-lookup"><span data-stu-id="7c429-372"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controller IEEE 1394** (25)</span><span class="sxs-lookup"><span data-stu-id="7c429-373"><span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="7c429-374"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="7c429-375"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)</span><span class="sxs-lookup"><span data-stu-id="7c429-376"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="7c429-377"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta switch Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="7c429-378"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)</span><span class="sxs-lookup"><span data-stu-id="7c429-379"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volume di archiviazione** (32)</span><span class="sxs-lookup"><span data-stu-id="7c429-380"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="7c429-381"><span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (30 32767)</span><span class="sxs-lookup"><span data-stu-id="7c429-382"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (30 32767)</span></span>
</dt> <dt>

<span data-ttu-id="7c429-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="7c429-383"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c429-384">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="7c429-384">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-385">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-386">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-387">GUID che rappresenta lo snapshot all'interno del file del set VHD da collegare.</span><span class="sxs-lookup"><span data-stu-id="7c429-387">A GUID representing which snapshot within the VHD Set file is to be attached.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-388">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7c429-388">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="7c429-389">**StorageQoSPolicyID**</span><span class="sxs-lookup"><span data-stu-id="7c429-389">**StorageQoSPolicyID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-390">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-390">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-392">Specifica l'identificatore univoco dei criteri QoS di archiviazione da applicare a questo extent di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c429-392">Specifies the unique identifier of the Storage QoS Policy to be applied to this virtual storage extent.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-393">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7c429-393">Added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="7c429-394">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="7c429-394">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-395">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-395">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-396">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-397">Numero di blocchi presentati al consumer.</span><span class="sxs-lookup"><span data-stu-id="7c429-397">The number of blocks that are presented to the consumer.</span></span> <span data-ttu-id="7c429-398">La dimensione del blocco viene specificata dalla proprietà **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="7c429-398">The block size is specified by the **VirtualResourceBlockSize** property.</span></span> <span data-ttu-id="7c429-399">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-399">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="7c429-400">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="7c429-400">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c429-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-403">Specifica le unità utilizzate dalla proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="7c429-403">Specifies the units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="7c429-404">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-404">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>



| <span data-ttu-id="7c429-405">Valore</span><span class="sxs-lookup"><span data-stu-id="7c429-405">Value</span></span>                                                                                                | <span data-ttu-id="7c429-406">Significato</span><span class="sxs-lookup"><span data-stu-id="7c429-406">Meaning</span></span>                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c429-407"><dt>"conteggio (blocco a dimensione fissa)"</dt></span><span class="sxs-lookup"><span data-stu-id="7c429-407"><dt>"count(fixed size block)"</dt></span></span> </dl> | <span data-ttu-id="7c429-408">Le dimensioni fisse del blocco sono contenute nella proprietà **VirtualResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="7c429-408">The fixed block size is contained in the **VirtualResourceBlockSize** property.</span></span><br/> |
| <dl> <span data-ttu-id="7c429-409"><dt>byte</dt></span><span class="sxs-lookup"><span data-stu-id="7c429-409"><dt>"byte"</dt></span></span> </dl>                    | <span data-ttu-id="7c429-410">La proprietà **VirtualQuantity** è misurata in byte.</span><span class="sxs-lookup"><span data-stu-id="7c429-410">The **VirtualQuantity** property is measured in bytes.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="7c429-411">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="7c429-411">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-412">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c429-412">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-414">Dimensione, in byte, dei blocchi presentati al consumer come risultato della richiesta di allocazione delle risorse di archiviazione o di allocazione delle risorse di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c429-414">The size, in bytes, of the blocks that are presented to the consumer as the result of this storage resource allocation or storage resource allocation request.</span></span> <span data-ttu-id="7c429-415">Se la dimensione del blocco è variabile, verranno specificate le dimensioni massime del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="7c429-415">If the block size is variable, then the maximum block size, in bytes, will be specified.</span></span> <span data-ttu-id="7c429-416">Se le dimensioni del blocco sono sconosciute o se non si applica un concetto di blocco, verrà utilizzato il valore 1.</span><span class="sxs-lookup"><span data-stu-id="7c429-416">If the block size is unknown or if a block concept does not apply, then the value 1 will be used.</span></span> <span data-ttu-id="7c429-417">Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="7c429-417">This property is inherited from **CIM\_StorageAllocationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="7c429-418">**Weight**</span><span class="sxs-lookup"><span data-stu-id="7c429-418">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-419">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c429-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-420">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c429-421">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span><span class="sxs-lookup"><span data-stu-id="7c429-421">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)</span></span>
</dt> </dl>

<span data-ttu-id="7c429-422">Specifica una priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c429-422">Specifies a relative priority for this allocation in relation to other allocations from the same resource pool.</span></span> <span data-ttu-id="7c429-423">Questa proprietà non dispone di unità di misura ed è pertinente solo se confrontata con altre allocazioni in competizione per le stesse risorse host.</span><span class="sxs-lookup"><span data-stu-id="7c429-423">This property has no unit of measure and is only relevant when compared to other allocations vying for the same host resources.</span></span> <span data-ttu-id="7c429-424">Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="7c429-424">This property is inherited from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="7c429-425">Intervallo: 1 10000</span><span class="sxs-lookup"><span data-stu-id="7c429-425">Range: 1 10000</span></span>

</dd> <dt>

<span data-ttu-id="7c429-426">**WriteHardeningMethod**</span><span class="sxs-lookup"><span data-stu-id="7c429-426">**WriteHardeningMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c429-427">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c429-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c429-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c429-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c429-429">Indica il metodo di protezione avanzata delle Scritture supportato dal disco.</span><span class="sxs-lookup"><span data-stu-id="7c429-429">Indicates what write hardening method is supported by the disk.</span></span>

> [!Note]  
> <span data-ttu-id="7c429-430">Questa proprietà è stata aggiunta in Windows 10, versione 1703.</span><span class="sxs-lookup"><span data-stu-id="7c429-430">This property was added in Windows 10, version 1703.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="7c429-431">**Valore predefinito** (0)</span><span class="sxs-lookup"><span data-stu-id="7c429-431">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

<span data-ttu-id="7c429-432">**WriteCacheEnabled** (1)</span><span class="sxs-lookup"><span data-stu-id="7c429-432">**WriteCacheEnabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

<span data-ttu-id="7c429-433">**WriteCacheandFUAEnabled** (2)</span><span class="sxs-lookup"><span data-stu-id="7c429-433">**WriteCacheandFUAEnabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

<span data-ttu-id="7c429-434">**WriteCacheDisabled** (3)</span><span class="sxs-lookup"><span data-stu-id="7c429-434">**WriteCacheDisabled** (3)</span></span>


<span data-ttu-id="7c429-435"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7c429-435"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7c429-436">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c429-436">Requirements</span></span>



| <span data-ttu-id="7c429-437">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c429-437">Requirement</span></span> | <span data-ttu-id="7c429-438">Valore</span><span class="sxs-lookup"><span data-stu-id="7c429-438">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c429-439">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c429-439">Minimum supported client</span></span><br/> | <span data-ttu-id="7c429-440">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c429-440">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c429-441">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c429-441">Minimum supported server</span></span><br/> | <span data-ttu-id="7c429-442">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c429-442">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c429-443">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c429-443">Namespace</span></span><br/>                | <span data-ttu-id="7c429-444">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c429-444">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c429-445">MOF</span><span class="sxs-lookup"><span data-stu-id="7c429-445">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c429-446"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c429-446"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c429-447">DLL</span><span class="sxs-lookup"><span data-stu-id="7c429-447">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c429-448"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c429-448"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

