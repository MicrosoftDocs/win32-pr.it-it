---
description: Rappresenta lo stato configurato del componente dell'interfaccia del servizio Guest.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Classe Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306042"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a><span data-ttu-id="35c8c-103">\_Classe MSVM GuestServiceInterfaceComponentSettingData</span><span class="sxs-lookup"><span data-stu-id="35c8c-103">Msvm\_GuestServiceInterfaceComponentSettingData class</span></span>

<span data-ttu-id="35c8c-104">Rappresenta lo stato configurato del componente dell'interfaccia del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="35c8c-104">Represents the configured state of the guest service interface component.</span></span> <span data-ttu-id="35c8c-105">Questa classe deriva dalla classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .</span><span class="sxs-lookup"><span data-stu-id="35c8c-105">This class derives from the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class.</span></span>

<span data-ttu-id="35c8c-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="35c8c-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c8c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35c8c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a><span data-ttu-id="35c8c-108">Members</span><span class="sxs-lookup"><span data-stu-id="35c8c-108">Members</span></span>

<span data-ttu-id="35c8c-109">La **classe \_ GuestServiceInterfaceComponentSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35c8c-109">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="35c8c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35c8c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35c8c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35c8c-111">Properties</span></span>

<span data-ttu-id="35c8c-112">La **classe \_ GuestServiceInterfaceComponentSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="35c8c-112">The **Msvm\_GuestServiceInterfaceComponentSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35c8c-113">**Indirizzo**</span><span class="sxs-lookup"><span data-stu-id="35c8c-113">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-116">Indirizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c8c-116">The address of the resource.</span></span> <span data-ttu-id="35c8c-117">Ad esempio, l'indirizzo MAC di una porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="35c8c-117">For example, the MAC address of a Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-118">**AllocationUnits**</span><span class="sxs-lookup"><span data-stu-id="35c8c-118">**AllocationUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-121">Questa proprietà specifica le unità di allocazione utilizzate dalle proprietà di prenotazione e limite.</span><span class="sxs-lookup"><span data-stu-id="35c8c-121">This property specifies the units of allocation used by the Reservation and Limit properties.</span></span> <span data-ttu-id="35c8c-122">Ad esempio, quando ResourceType = Processor, AllocationUnits può essere impostato su MHz.</span><span class="sxs-lookup"><span data-stu-id="35c8c-122">For example, when ResourceType=Processor, AllocationUnits may be set to MHz.</span></span> <span data-ttu-id="35c8c-123">Quando ResourceType = Memory, AllocationUnits può essere impostato su MB</span><span class="sxs-lookup"><span data-stu-id="35c8c-123">When ResourceType=Memory, AllocationUnits may be set to MB</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-124">**AutomaticAllocation**</span><span class="sxs-lookup"><span data-stu-id="35c8c-124">**AutomaticAllocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-125">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="35c8c-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-127">Questa proprietà specifica se la risorsa verrà allocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="35c8c-127">This property specifies if the resource will be automatically allocated.</span></span> <span data-ttu-id="35c8c-128">Se, ad esempio, è impostato su true, quando il computer virtuale che lo utilizza è acceso, questa risorsa verrebbe allocata.</span><span class="sxs-lookup"><span data-stu-id="35c8c-128">For example when set to true, when the consuming virtual computer system is powered on, this resource would be allocated.</span></span> <span data-ttu-id="35c8c-129">Il valore false indica che la risorsa deve essere allocata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="35c8c-129">A value of false indicates the resource must be explicitly allocated.</span></span> <span data-ttu-id="35c8c-130">Ad esempio, l'impostazione può rappresentare supporti rimovibili (ovvero CDROM o floppy) in cui, in fase di accensione, il supporto non è presente.</span><span class="sxs-lookup"><span data-stu-id="35c8c-130">For example, the setting may represent removable media (that is, cdrom or floppy) where at power on time, the media is not present.</span></span> <span data-ttu-id="35c8c-131">Per allocare la risorsa è necessaria un'operazione esplicita.</span><span class="sxs-lookup"><span data-stu-id="35c8c-131">An explicit operation is required to allocate the resource.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-132">**AutomaticDeallocation**</span><span class="sxs-lookup"><span data-stu-id="35c8c-132">**AutomaticDeallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="35c8c-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-135">Questa proprietà specifica se la risorsa verrà deallocata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="35c8c-135">This property specifies if the resource will be automatically deallocated.</span></span> <span data-ttu-id="35c8c-136">Se, ad esempio, si imposta su true, quando il computer virtuale che lo utilizza è spento, questa risorsa verrebbe deallocata.</span><span class="sxs-lookup"><span data-stu-id="35c8c-136">For example, when set to true, when the consuming virtual computer system is powered off, this resource would be deallocated.</span></span> <span data-ttu-id="35c8c-137">Se impostata su false, la risorsa rimane allocata e deve essere deallocata in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="35c8c-137">When set to false, the resource will remain allocated and must be explicitly deallocated.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-138">**Connection**</span><span class="sxs-lookup"><span data-stu-id="35c8c-138">**Connection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-139">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="35c8c-139">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-141">Elemento a cui è connessa questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c8c-141">The thing to which this resource is connected.</span></span> <span data-ttu-id="35c8c-142">Ad esempio, una rete denominata o una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-142">For example, a named network or switch port.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-143">**ConsumerVisibility**</span><span class="sxs-lookup"><span data-stu-id="35c8c-143">**ConsumerVisibility**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35c8c-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-146">Descrive la visibilità dei consumer per la risorsa allocata.</span><span class="sxs-lookup"><span data-stu-id="35c8c-146">Describes the consumers visibility to the allocated resource.</span></span>



| <span data-ttu-id="35c8c-147">Valore</span><span class="sxs-lookup"><span data-stu-id="35c8c-147">Value</span></span>                                                                                                                                                                                                                                                                  | <span data-ttu-id="35c8c-148">Significato</span><span class="sxs-lookup"><span data-stu-id="35c8c-148">Meaning</span></span>                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="35c8c-149"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-149"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                            | <span data-ttu-id="35c8c-150">Sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="35c8c-150">Unknown.</span></span><br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <span data-ttu-id="35c8c-151"><dt>**Passato-a**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-151"><dt>**Passed-Through**</dt> <dt>2</dt></span></span> </dl>                | <span data-ttu-id="35c8c-152">La risorsa host o sottostante viene utilizzata e passata al consumer, possibilmente utilizzando il partizionamento.</span><span class="sxs-lookup"><span data-stu-id="35c8c-152">The underlying or host resource is utilized and passed through to the consumer, possibly using partitioning.</span></span> <span data-ttu-id="35c8c-153">Nella proprietà DeviceID deve essere presente almeno un elemento.</span><span class="sxs-lookup"><span data-stu-id="35c8c-153">At least one item shall be present in the DeviceID property.</span></span><br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <span data-ttu-id="35c8c-154"><dt>**Virtualizzato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-154"><dt>**Virtualized**</dt> <dt>3</dt></span></span> </dl>                            | <span data-ttu-id="35c8c-155">La risorsa è virtualizzata e non può essere mappata direttamente a una risorsa host o sottostante.</span><span class="sxs-lookup"><span data-stu-id="35c8c-155">The resource is virtualized and may not map directly to an underlying/host resource.</span></span> <span data-ttu-id="35c8c-156">Alcune implementazioni possono supportare un'assegnazione specifica per le risorse virtualizzate, nel qual caso le risorse host vengono esposte tramite la proprietà DeviceID.</span><span class="sxs-lookup"><span data-stu-id="35c8c-156">Some implementations may support specific assignment for virtualized resources, in which case the host resource(s) are exposed using the DeviceID property.</span></span><br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <span data-ttu-id="35c8c-157"><dt>**Non rappresentato**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-157"><dt>**Not represented**</dt> <dt>4</dt></span></span> </dl>            | <span data-ttu-id="35c8c-158">Una rappresentazione della risorsa non esiste nel contesto del consumer di risorse.</span><span class="sxs-lookup"><span data-stu-id="35c8c-158">A representation of the resource does not exist within the context of the resource consumer.</span></span><br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="35c8c-159"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-159"><dt>**DMTF reserved**</dt> <dt>..</dt></span></span> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="35c8c-160">32767 <dt>**riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-160"><dt>**Vendor Reserved**</dt> <dt>32767..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="35c8c-161">**DefaultEnabledStatePolicy**</span><span class="sxs-lookup"><span data-stu-id="35c8c-161">**DefaultEnabledStatePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-162">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35c8c-162">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-164">Per impostazione predefinita, gli stati abilitati e disabilitati dei servizi di comunicazione Guest.</span><span class="sxs-lookup"><span data-stu-id="35c8c-164">The enabled and disabled states of guest communication services by default.</span></span>

<span data-ttu-id="35c8c-165">Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="35c8c-165">This is a read-only property, but it can be changed using the [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="35c8c-166">Aggiunto in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="35c8c-166">Added in Windows 10.</span></span>

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="35c8c-167">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="35c8c-167">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="35c8c-168">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="35c8c-168">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35c8c-169">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="35c8c-169">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-170">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-172">Nome visualizzato per questa istanza di SettingData.</span><span class="sxs-lookup"><span data-stu-id="35c8c-172">The display name for this instance of SettingData.</span></span> <span data-ttu-id="35c8c-173">Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="35c8c-173">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="35c8c-174">Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="35c8c-174">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-175">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="35c8c-175">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-176">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35c8c-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-178">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="35c8c-178">The enabled and disabled states of an element.</span></span>

<span data-ttu-id="35c8c-179">Si tratta di una proprietà di sola lettura, ma può essere modificata usando il metodo [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (o [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 o versione successiva) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="35c8c-179">This is a read-only property, but it can be changed by using the [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) method (or [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 or later) of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="35c8c-180">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="35c8c-180">Valid values are:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="35c8c-181">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="35c8c-181">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="35c8c-182">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="35c8c-182">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35c8c-183">**HostResource**</span><span class="sxs-lookup"><span data-stu-id="35c8c-183">**HostResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-184">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="35c8c-184">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-186">Questa proprietà espone un'assegnazione specifica a un host o a risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="35c8c-186">This property exposes specific assignment to host or underlying resources.</span></span> <span data-ttu-id="35c8c-187">Le istanze incorporate devono contenere solo proprietà chiave e essere considerate come percorsi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="35c8c-187">The embedded instances shall contain only key properties and be treated as Object Paths.</span></span> <span data-ttu-id="35c8c-188">Se la risorsa virtuale può essere pianificata su una serie di risorse sottostanti, questa proprietà deve rimanere **null**.</span><span class="sxs-lookup"><span data-stu-id="35c8c-188">If the virtual resource may be scheduled on a number of underlying resources, this property should remain **NULL**.</span></span> <span data-ttu-id="35c8c-189">In tal caso, è possibile usare le associazioni DeviceAllocatedFromPool o ResourceAllocationFromPool per determinare il pool di risorse host in cui la risorsa virtuale può essere pianificata.</span><span class="sxs-lookup"><span data-stu-id="35c8c-189">In that case, the DeviceAllocatedFromPool or ResourceAllocationFromPool associations may be used to determine the pool of host resources on which this virtual resource may be scheduled.</span></span> <span data-ttu-id="35c8c-190">Se viene utilizzata un'assegnazione specifica, tutte le risorse sottostanti utilizzate da questa risorsa virtuale verranno elencate in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="35c8c-190">If specific assignment is utilized, all underlying resources used by this virtual resource shall be listed in this array.</span></span> <span data-ttu-id="35c8c-191">In genere, la matrice conterrà un elemento, tuttavia per le allocazioni di aggregazione, ad esempio più processori, è possibile specificare più risorse host.</span><span class="sxs-lookup"><span data-stu-id="35c8c-191">Typically, the array will contain one item, however for aggregate allocations, such as multiple processors, multiple host resources may be specified.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-192">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35c8c-192">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-195">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="35c8c-195">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-196">All'interno dell'ambito dello spazio dei nomi di creazione di istanze, InstanceID indica in modo opaco e univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="35c8c-196">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="35c8c-197">Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID*:*localizzato* in cui *OrgID* e *LocalId* sono separati da due punti (:) e dove *OrgID* deve includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità di business da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="35c8c-197">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="35c8c-198">(Questo requisito è simile a *SchemaName* \_ Struttura *ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="35c8c-198">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="35c8c-199">Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono comparire tra *OrgID* e *localizzato*.</span><span class="sxs-lookup"><span data-stu-id="35c8c-199">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="35c8c-200">*Localizzato* viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="35c8c-200">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="35c8c-201">Se non viene utilizzato l'algoritmo "preferito" precedente, l'entità di definizione deve garantire che l'ID istanza risultante non venga riutilizzato in tutte le InstanceID generate da questo o da altri provider per lo spazio dei nomi di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="35c8c-201">If the above "preferred" algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="35c8c-202">Per le istanze definite da DMTF, è necessario usare l'algoritmo "preferenziale" con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="35c8c-202">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-203">**Limite**</span><span class="sxs-lookup"><span data-stu-id="35c8c-203">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-204">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35c8c-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-206">Questa proprietà specifica il limite superiore o la quantità massima di risorse che verrà concessa per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-206">This property specifies the upper bound, or maximum amount of resource that will be granted for this allocation.</span></span> <span data-ttu-id="35c8c-207">Ad esempio, un sistema che supporta il paging della memoria può supportare l'impostazione del limite di un'allocazione di memoria inferiore a quella del VirtualQuantity, forzando così il paging per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-207">For example, a system which supports memory paging may support setting the Limit of a Memory allocation below that of the VirtualQuantity, thus forcing paging to occur for this allocation.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-208">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="35c8c-208">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-209">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35c8c-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-211">Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti.</span><span class="sxs-lookup"><span data-stu-id="35c8c-211">Specifies how this resource maps to underlying resources.</span></span> <span data-ttu-id="35c8c-212">Se la matrice HostResource contiene voci, questa proprietà riflette il modo in cui viene eseguito il mapping della risorsa a tali risorse specifiche.</span><span class="sxs-lookup"><span data-stu-id="35c8c-212">If the HostResource array contains any entries, this property reflects how the resource maps to those specific resources.</span></span>

<dl> <dt>

<span data-ttu-id="35c8c-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="35c8c-213"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="35c8c-214"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (2)</span><span class="sxs-lookup"><span data-stu-id="35c8c-215"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinità Soft** (3)</span><span class="sxs-lookup"><span data-stu-id="35c8c-216"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinità hardware** (4)</span><span class="sxs-lookup"><span data-stu-id="35c8c-217"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="35c8c-218"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="35c8c-219"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35c8c-220">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="35c8c-220">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-223">Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e ResourceType ha il valore "other".</span><span class="sxs-lookup"><span data-stu-id="35c8c-223">A string that describes the resource type when a well defined value is not available and ResourceType has the value "Other".</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-224">**Parent**</span><span class="sxs-lookup"><span data-stu-id="35c8c-224">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-227">Elemento padre della risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c8c-227">The Parent of the resource.</span></span> <span data-ttu-id="35c8c-228">Ad esempio, un controller per l'allocazione corrente.</span><span class="sxs-lookup"><span data-stu-id="35c8c-228">For example, a controller for the current allocation.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-229">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="35c8c-229">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-230">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-232">Questa proprietà specifica il ResourcePool da cui la risorsa è attualmente allocata o il ResourcePool da cui verrà allocata la risorsa quando si verifica l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-232">This property specifies which ResourcePool the resource is currently allocated from, or which ResourcePool the resource will be allocated from when the allocation occurs.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-233">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="35c8c-233">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-234">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35c8c-234">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-236">Questa proprietà specifica la quantità di risorse garantita per l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-236">This property specifies the amount of resource guaranteed to be available for this allocation.</span></span> <span data-ttu-id="35c8c-237">Nel sistema che supporta l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione per impedire che un'allocazione venga accettata, impedendo così l'esaurimento delle risorse.</span><span class="sxs-lookup"><span data-stu-id="35c8c-237">On system which support over-commitment of resources, this value is typically used for admission control to prevent an an allocation from being accepted thus preventing resource depletion.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-238">**ResourceSubType**</span><span class="sxs-lookup"><span data-stu-id="35c8c-238">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35c8c-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-241">Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c8c-241">A string describing an implementation specific sub-type for this resource.</span></span> <span data-ttu-id="35c8c-242">Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="35c8c-242">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-243">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="35c8c-243">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35c8c-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-246">Tipo di risorsa rappresentata da questa impostazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="35c8c-246">The type of resource this allocation setting represents.</span></span>

<dl> <dt>

<span data-ttu-id="35c8c-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="35c8c-247"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span><span class="sxs-lookup"><span data-stu-id="35c8c-248"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)</span><span class="sxs-lookup"><span data-stu-id="35c8c-249"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="35c8c-250"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="35c8c-251"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)</span><span class="sxs-lookup"><span data-stu-id="35c8c-252"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)</span><span class="sxs-lookup"><span data-stu-id="35c8c-253"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="35c8c-254"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="35c8c-255"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="35c8c-256"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)</span><span class="sxs-lookup"><span data-stu-id="35c8c-257"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)</span><span class="sxs-lookup"><span data-stu-id="35c8c-258"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)</span><span class="sxs-lookup"><span data-stu-id="35c8c-259"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)</span><span class="sxs-lookup"><span data-stu-id="35c8c-260"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)</span><span class="sxs-lookup"><span data-stu-id="35c8c-261"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="35c8c-262"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (17)</span><span class="sxs-lookup"><span data-stu-id="35c8c-263"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (17)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (18)</span><span class="sxs-lookup"><span data-stu-id="35c8c-264"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (18)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (19)</span><span class="sxs-lookup"><span data-stu-id="35c8c-265"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (19)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (20)</span><span class="sxs-lookup"><span data-stu-id="35c8c-266"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (20)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (21)</span><span class="sxs-lookup"><span data-stu-id="35c8c-267"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)</span><span class="sxs-lookup"><span data-stu-id="35c8c-268"><span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disk** (22)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Nastro** (23)</span><span class="sxs-lookup"><span data-stu-id="35c8c-269"><span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Tape** (23)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (24)</span><span class="sxs-lookup"><span data-stu-id="35c8c-270"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (24)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controller FireWire** (25)</span><span class="sxs-lookup"><span data-stu-id="35c8c-271"><span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)</span><span class="sxs-lookup"><span data-stu-id="35c8c-272"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)</span><span class="sxs-lookup"><span data-stu-id="35c8c-273"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)</span><span class="sxs-lookup"><span data-stu-id="35c8c-274"><span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Power Supply** (28)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)</span><span class="sxs-lookup"><span data-stu-id="35c8c-275"><span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Cooling Device** (29)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="35c8c-276"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="35c8c-277"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35c8c-278">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="35c8c-278">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-279">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35c8c-279">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-281">Questa proprietà specifica la quantità di risorse presentate al consumer.</span><span class="sxs-lookup"><span data-stu-id="35c8c-281">This property specifies the quantity of resources presented to the consumer.</span></span> <span data-ttu-id="35c8c-282">Ad esempio, quando ResourceType = Processor, questa proprietà riflette il numero di processori discreti presentati al sistema del computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="35c8c-282">For example, when ResourceType=Processor, this property would reflect the number of discrete Processors presented to the virtual computer system.</span></span> <span data-ttu-id="35c8c-283">Quando ResourceType = Memory, questa proprietà può riflettere il numero di MB restituiti al sistema del computer virtuale.</span><span class="sxs-lookup"><span data-stu-id="35c8c-283">When ResourceType=Memory, this property could reflect the number of MB reported to the virtual computer system.</span></span>

</dd> <dt>

<span data-ttu-id="35c8c-284">**Weight**</span><span class="sxs-lookup"><span data-stu-id="35c8c-284">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c8c-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35c8c-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35c8c-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35c8c-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35c8c-287">Questa proprietà specifica una priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso ResourcePool.</span><span class="sxs-lookup"><span data-stu-id="35c8c-287">This property specifies a relative priority for this allocation in relation to other allocations from the same ResourcePool.</span></span> <span data-ttu-id="35c8c-288">Questa proprietà non dispone di unità di misura ed è pertinente solo se confrontata con altre allocazioni che competono per le stesse risorse host.</span><span class="sxs-lookup"><span data-stu-id="35c8c-288">This property has no unit of measure, and is only relevant when compared to other allocations competing for the same host resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35c8c-289">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35c8c-289">Requirements</span></span>



| <span data-ttu-id="35c8c-290">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c8c-290">Requirement</span></span> | <span data-ttu-id="35c8c-291">Valore</span><span class="sxs-lookup"><span data-stu-id="35c8c-291">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c8c-292">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35c8c-292">Minimum supported client</span></span><br/> | <span data-ttu-id="35c8c-293">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35c8c-293">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="35c8c-294">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35c8c-294">Minimum supported server</span></span><br/> | <span data-ttu-id="35c8c-295">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35c8c-295">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="35c8c-296">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35c8c-296">Namespace</span></span><br/>                | <span data-ttu-id="35c8c-297">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="35c8c-297">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="35c8c-298">MOF</span><span class="sxs-lookup"><span data-stu-id="35c8c-298">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35c8c-299"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-299"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35c8c-300">DLL</span><span class="sxs-lookup"><span data-stu-id="35c8c-300">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c8c-301"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35c8c-301"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35c8c-302">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35c8c-302">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c8c-303">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="35c8c-303">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="35c8c-304">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="35c8c-304">**CIM\_ResourceAllocationSettingData**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

