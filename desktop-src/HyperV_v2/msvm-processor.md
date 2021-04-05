---
description: Rappresenta il processore virtuale in una macchina virtuale.
ms.assetid: 4BA91C44-0F85-42D1-A8B5-147E1D532FB5
title: Classe Msvm_Processor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Processor
- Msvm_Processor.SetPowerState
- Msvm_Processor.EnableDevice
- Msvm_Processor.OnlineDevice
- Msvm_Processor.QuiesceDevice
- Msvm_Processor.SaveProperties
- Msvm_Processor.RestoreProperties
- Msvm_Processor.InstanceID
- Msvm_Processor.Caption
- Msvm_Processor.Description
- Msvm_Processor.ElementName
- Msvm_Processor.InstallDate
- Msvm_Processor.Name
- Msvm_Processor.OperationalStatus
- Msvm_Processor.StatusDescriptions
- Msvm_Processor.Status
- Msvm_Processor.HealthState
- Msvm_Processor.CommunicationStatus
- Msvm_Processor.DetailedStatus
- Msvm_Processor.OperatingStatus
- Msvm_Processor.PrimaryStatus
- Msvm_Processor.EnabledState
- Msvm_Processor.OtherEnabledState
- Msvm_Processor.RequestedState
- Msvm_Processor.EnabledDefault
- Msvm_Processor.TimeOfLastStateChange
- Msvm_Processor.AvailableRequestedStates
- Msvm_Processor.TransitioningToState
- Msvm_Processor.SystemCreationClassName
- Msvm_Processor.SystemName
- Msvm_Processor.CreationClassName
- Msvm_Processor.DeviceID
- Msvm_Processor.PowerManagementSupported
- Msvm_Processor.PowerManagementCapabilities
- Msvm_Processor.Availability
- Msvm_Processor.StatusInfo
- Msvm_Processor.LastErrorCode
- Msvm_Processor.ErrorDescription
- Msvm_Processor.ErrorCleared
- Msvm_Processor.OtherIdentifyingInfo
- Msvm_Processor.PowerOnHours
- Msvm_Processor.TotalPowerOnHours
- Msvm_Processor.IdentifyingDescriptions
- Msvm_Processor.AdditionalAvailability
- Msvm_Processor.MaxQuiesceTime
- Msvm_Processor.Role
- Msvm_Processor.Family
- Msvm_Processor.OtherFamilyDescription
- Msvm_Processor.UpgradeMethod
- Msvm_Processor.MaxClockSpeed
- Msvm_Processor.CurrentClockSpeed
- Msvm_Processor.DataWidth
- Msvm_Processor.AddressWidth
- Msvm_Processor.LoadPercentage
- Msvm_Processor.Stepping
- Msvm_Processor.UniqueID
- Msvm_Processor.CPUStatus
- Msvm_Processor.ExternalBusClockSpeed
- Msvm_Processor.LoadPercentageHistory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 14ed1e2bbb9e15f89376234da8981faffb1a6809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882173"
---
# <a name="msvm_processor-class"></a><span data-ttu-id="da5aa-103">\_Classe processore MSVM</span><span class="sxs-lookup"><span data-stu-id="da5aa-103">Msvm\_Processor class</span></span>

<span data-ttu-id="da5aa-104">Rappresenta il processore virtuale in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-104">Represents the virtual processor in a virtual machine.</span></span>

<span data-ttu-id="da5aa-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="da5aa-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da5aa-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da5aa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Processor : CIM_Processor
{
  string   InstanceID;
  string   Caption = "Processor";
  string   Description = " A logical processor of the hypervisor running on the host computer system.";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 2;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_Processor";
  string   DeviceID = "Microsoft:GUID\device specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  string   Role = "Central Processor";
  uint16   Family;
  string   OtherFamilyDescription;
  uint16   UpgradeMethod;
  uint32   MaxClockSpeed;
  uint32   CurrentClockSpeed;
  uint16   DataWidth;
  uint16   AddressWidth;
  uint16   LoadPercentage;
  string   Stepping;
  string   UniqueID;
  uint16   CPUStatus;
  uint32   ExternalBusClockSpeed;
  uint16   LoadPercentageHistory[];
};
```

## <a name="members"></a><span data-ttu-id="da5aa-107">Members</span><span class="sxs-lookup"><span data-stu-id="da5aa-107">Members</span></span>

<span data-ttu-id="da5aa-108">La classe del **\_ processore MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="da5aa-108">The **Msvm\_Processor** class has these types of members:</span></span>

-   [<span data-ttu-id="da5aa-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="da5aa-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="da5aa-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da5aa-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="da5aa-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="da5aa-111">Methods</span></span>

<span data-ttu-id="da5aa-112">La classe del **\_ processore MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="da5aa-112">The **Msvm\_Processor** class has these methods.</span></span>



| <span data-ttu-id="da5aa-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="da5aa-113">Method</span></span>                                                          | <span data-ttu-id="da5aa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da5aa-114">Description</span></span>                              |
|:----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="da5aa-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="da5aa-115">**EnableDevice**</span></span>                                                | <span data-ttu-id="da5aa-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="da5aa-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="da5aa-117">**OnlineDevice**</span></span>                                                | <span data-ttu-id="da5aa-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="da5aa-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="da5aa-119">**QuiesceDevice**</span></span>                                               | <span data-ttu-id="da5aa-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="da5aa-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="da5aa-121">**RequestStateChange**</span></span>](msvm-processor-requeststatechange.md) | <span data-ttu-id="da5aa-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="da5aa-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="da5aa-123">**Reset**</span></span>](msvm-processor-reset.md)                           | <span data-ttu-id="da5aa-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="da5aa-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="da5aa-125">**RestoreProperties**</span></span>                                           | <span data-ttu-id="da5aa-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="da5aa-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="da5aa-127">**SaveProperties**</span></span>                                              | <span data-ttu-id="da5aa-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="da5aa-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="da5aa-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="da5aa-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="da5aa-131">Properties</span></span>

<span data-ttu-id="da5aa-132">La classe del **\_ processore MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="da5aa-132">The **Msvm\_Processor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da5aa-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="da5aa-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-136">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="da5aa-136">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="da5aa-137">La proprietà **Availability** indica lo stato primario e la disponibilità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-137">The **Availability** property denotes the primary status and availability of the device.</span></span> <span data-ttu-id="da5aa-138">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="da5aa-138">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-139">**AddressWidth**</span><span class="sxs-lookup"><span data-stu-id="da5aa-139">**AddressWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-140">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-142">Larghezza dell'indirizzo del processore, in bit.</span><span class="sxs-lookup"><span data-stu-id="da5aa-142">The processor address width, in bits.</span></span> <span data-ttu-id="da5aa-143">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e il valore è 32 o 64, a seconda delle caratteristiche della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-143">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-144">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="da5aa-144">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-147">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-147">The primary availability and status of the device.</span></span> <span data-ttu-id="da5aa-148">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-148">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-149">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="da5aa-149">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-150">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-152">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="da5aa-152">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="da5aa-153">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="da5aa-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-154">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="da5aa-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-157">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="da5aa-157">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-158">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da5aa-158">A short description of the object.</span></span> <span data-ttu-id="da5aa-159">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-160">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-160">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-163">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="da5aa-163">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="da5aa-164">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-164">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da5aa-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-165">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="da5aa-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="da5aa-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="da5aa-167"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="da5aa-168"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="da5aa-169"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="da5aa-170"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="da5aa-171"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="da5aa-172"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="da5aa-173">)</span><span class="sxs-lookup"><span data-stu-id="da5aa-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da5aa-174">**CPUStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-174">**CPUStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-175">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-175">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-177">Stato corrente del processore.</span><span class="sxs-lookup"><span data-stu-id="da5aa-177">The current status of the processor.</span></span> <span data-ttu-id="da5aa-178">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-178">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da5aa-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-182">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="da5aa-182">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-183">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="da5aa-183">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="da5aa-184">Se utilizzata con altre proprietà chiave della classe, questa proprietà consente di identificare in modo univoco tutte le istanze della classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="da5aa-184">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="da5aa-185">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="da5aa-185">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-186">**CurrentClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="da5aa-186">**CurrentClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-187">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5aa-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-189">Velocità massima del processore fisico, prendendo in considerazione la capacità del processore virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-189">The maximum speed of the physical processor, taking into account the capacity for the virtual processor.</span></span> <span data-ttu-id="da5aa-190">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-190">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-191">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="da5aa-191">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-194">Larghezza dei dati del processore, in bit.</span><span class="sxs-lookup"><span data-stu-id="da5aa-194">The processor data width, in bits.</span></span> <span data-ttu-id="da5aa-195">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor)e il valore è 32 o 64, a seconda delle caratteristiche della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-195">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and the value is either 32 or 64, depending on the characteristics of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-196">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="da5aa-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-199">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="da5aa-199">A description of the object.</span></span> <span data-ttu-id="da5aa-200">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-204">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="da5aa-205">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da5aa-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="da5aa-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="da5aa-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="da5aa-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="da5aa-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="da5aa-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="da5aa-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="da5aa-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="da5aa-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="da5aa-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="da5aa-215">)</span><span class="sxs-lookup"><span data-stu-id="da5aa-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da5aa-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="da5aa-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-219">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="da5aa-219">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="da5aa-220">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID* \\ *Device Specific Data*".</span><span class="sxs-lookup"><span data-stu-id="da5aa-220">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-221">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="da5aa-221">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-224">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da5aa-224">A display name for the object.</span></span> <span data-ttu-id="da5aa-225">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-226">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="da5aa-226">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-227">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-229">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="da5aa-229">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="da5aa-230">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5aa-230">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-231">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-231">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-232">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-234">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="da5aa-234">The enabled and disabled states of an element.</span></span> <span data-ttu-id="da5aa-235">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5aa-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-236">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="da5aa-236">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-237">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="da5aa-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-239">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-239">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="da5aa-240">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-240">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-241">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="da5aa-241">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-244">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="da5aa-244">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="da5aa-245">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-246">**ExternalBusClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="da5aa-246">**ExternalBusClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-247">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5aa-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-249">Velocità di clock del bus esterno del processore fisico sottostante.</span><span class="sxs-lookup"><span data-stu-id="da5aa-249">The external bus clock speed of the underlying physical processor.</span></span> <span data-ttu-id="da5aa-250">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-250">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-251">**Famiglia**</span><span class="sxs-lookup"><span data-stu-id="da5aa-251">**Family**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-252">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-254">La famiglia di processori del processore fisico sottostante.</span><span class="sxs-lookup"><span data-stu-id="da5aa-254">The processor family of the underlying physical processor.</span></span> <span data-ttu-id="da5aa-255">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-255">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-259">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="da5aa-259">The current health of the element.</span></span> <span data-ttu-id="da5aa-260">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="da5aa-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-262">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="da5aa-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-264">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice [**OtherIdentifyingInfo**](msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="da5aa-264">An array of free-form strings that provide explanations and details behind the entries in the [**OtherIdentifyingInfo**](msvm-keyboard.md) array.</span></span> <span data-ttu-id="da5aa-265">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="da5aa-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="da5aa-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-267">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da5aa-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-269">Data e ora di creazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-269">The date and time when the virtual machine was created.</span></span> <span data-ttu-id="da5aa-270">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="da5aa-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-274">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="da5aa-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-275">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="da5aa-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="da5aa-276">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="da5aa-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-278">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5aa-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-280">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="da5aa-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="da5aa-281">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-282">**LoadPercentage**</span><span class="sxs-lookup"><span data-stu-id="da5aa-282">**LoadPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-285">Percentuale corrente della potenza di elaborazione totale utilizzata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-285">The current percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="da5aa-286">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-286">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-287">**LoadPercentageHistory**</span><span class="sxs-lookup"><span data-stu-id="da5aa-287">**LoadPercentageHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-288">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-288">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-290">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="da5aa-290">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-291">Cronologia registrata della percentuale della potenza di elaborazione totale utilizzata dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-291">The recorded history of percentage of the total processing power being consumed by the virtual machine.</span></span> <span data-ttu-id="da5aa-292">Si tratta di una matrice contenente esempi.</span><span class="sxs-lookup"><span data-stu-id="da5aa-292">This is an array containing samples.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-293">**MaxClockSpeed**</span><span class="sxs-lookup"><span data-stu-id="da5aa-293">**MaxClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-294">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="da5aa-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-296">Velocità di clock massima, in megahertz, del processore virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-296">The maximum clock speed, in megahertz, of the virtual processor.</span></span> <span data-ttu-id="da5aa-297">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-297">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-298">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="da5aa-298">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-299">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da5aa-299">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-301">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-301">This property has been deprecated.</span></span> <span data-ttu-id="da5aa-302">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-302">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-303">**Nome**</span><span class="sxs-lookup"><span data-stu-id="da5aa-303">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-304">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-306">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="da5aa-306">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-307">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="da5aa-307">The label by which the object is known.</span></span> <span data-ttu-id="da5aa-308">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="da5aa-308">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="da5aa-309">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-310">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-310">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-311">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-311">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-313">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="da5aa-313">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="da5aa-314">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-314">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da5aa-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="da5aa-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="da5aa-316"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="da5aa-317"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="da5aa-318"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="da5aa-319"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="da5aa-320"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="da5aa-321"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="da5aa-322"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="da5aa-323"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="da5aa-324"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="da5aa-325"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="da5aa-326"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="da5aa-327"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="da5aa-328"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="da5aa-329"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="da5aa-330"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="da5aa-331"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="da5aa-332"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="da5aa-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="da5aa-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="da5aa-335">)</span><span class="sxs-lookup"><span data-stu-id="da5aa-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da5aa-336">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-336">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-337">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-339">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="da5aa-339">The current status of the element.</span></span> <span data-ttu-id="da5aa-340">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-341">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-341">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-344">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="da5aa-344">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="da5aa-345">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="da5aa-345">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="da5aa-346">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5aa-346">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-347">**OtherFamilyDescription**</span><span class="sxs-lookup"><span data-stu-id="da5aa-347">**OtherFamilyDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-350">Descrizione del tipo di famiglia del processore.</span><span class="sxs-lookup"><span data-stu-id="da5aa-350">A description of the processor family type.</span></span> <span data-ttu-id="da5aa-351">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="da5aa-351">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-352">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="da5aa-352">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-353">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="da5aa-353">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-355">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="da5aa-355">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="da5aa-356">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="da5aa-356">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-357">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="da5aa-357">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-358">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-358">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-360">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-360">The power management capabilities of the device.</span></span> <span data-ttu-id="da5aa-361">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-362">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="da5aa-362">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-363">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="da5aa-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-365">Indica se il risparmio energia è supportato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-365">Indicates whether power management is supported on the device.</span></span> <span data-ttu-id="da5aa-366">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-367">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="da5aa-367">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-368">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da5aa-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-370">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="da5aa-370">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="da5aa-371">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-371">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-372">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="da5aa-372">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-373">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-375">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="da5aa-375">Provides high level status information.</span></span> <span data-ttu-id="da5aa-376">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="da5aa-376">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="da5aa-377">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-377">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="da5aa-378">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-378">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="da5aa-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="da5aa-379"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="da5aa-380"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="da5aa-381"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="da5aa-382"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="da5aa-383"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="da5aa-384"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="da5aa-385">)</span><span class="sxs-lookup"><span data-stu-id="da5aa-385">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="da5aa-386">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-386">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-387">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-389">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="da5aa-389">The last requested or desired state for the element.</span></span> <span data-ttu-id="da5aa-390">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5aa-390">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-391">**Ruolo**</span><span class="sxs-lookup"><span data-stu-id="da5aa-391">**Role**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-392">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-393">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-394">Stringa che descrive il ruolo del processore.</span><span class="sxs-lookup"><span data-stu-id="da5aa-394">A string that describes the role of the processor.</span></span> <span data-ttu-id="da5aa-395">Ad esempio, "Central Processor" o "Math Processor".</span><span class="sxs-lookup"><span data-stu-id="da5aa-395">For example, "Central Processor" or "Math Processor".</span></span> <span data-ttu-id="da5aa-396">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-396">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-397">**Status**</span><span class="sxs-lookup"><span data-stu-id="da5aa-397">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-398">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-400">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="da5aa-400">The current status of the object.</span></span> <span data-ttu-id="da5aa-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-402">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="da5aa-402">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-403">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="da5aa-403">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-405">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="da5aa-405">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="da5aa-406">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="da5aa-406">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-407">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="da5aa-407">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-408">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-408">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-410">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="da5aa-410">The current state of the logical device.</span></span> <span data-ttu-id="da5aa-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-412">**Esecuzione di istruzioni**</span><span class="sxs-lookup"><span data-stu-id="da5aa-412">**Stepping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-413">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-415">Livello di revisione del processore all'interno della famiglia di processori del processore fisico sottostante.</span><span class="sxs-lookup"><span data-stu-id="da5aa-415">The revision level of the processor within the processor family of the underlying physical processor.</span></span> <span data-ttu-id="da5aa-416">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-416">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-417">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="da5aa-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-418">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-420">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="da5aa-420">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-421">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="da5aa-421">The creation class name of the scoping system.</span></span> <span data-ttu-id="da5aa-422">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="da5aa-422">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="da5aa-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-424">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-425">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-426">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="da5aa-426">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-427">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="da5aa-427">The name of the scoping system.</span></span> <span data-ttu-id="da5aa-428">Questo valore corrisponde al valore della proprietà [**Name**](msvm-computersystem.md) della classe **MSVM \_ ComputerSystem** per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="da5aa-428">This value corresponds to the value of the [**Name**](msvm-computersystem.md) property of the **Msvm\_ComputerSystem** class for the scoping virtual machine.</span></span> <span data-ttu-id="da5aa-429">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="da5aa-429">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-430">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="da5aa-430">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-431">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="da5aa-431">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-433">Data o ora in cui è stato modificato lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="da5aa-433">The date or time at which the virtual machine's state was changed.</span></span> <span data-ttu-id="da5aa-434">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="da5aa-434">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="da5aa-435">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-435">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="da5aa-436">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="da5aa-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-437">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="da5aa-437">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-438">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="da5aa-438">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-439">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-440">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-440">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="da5aa-441">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-441">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-442">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="da5aa-442">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-443">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-444">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-445">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="da5aa-445">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="da5aa-446">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="da5aa-446">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-447">**UniqueID**</span><span class="sxs-lookup"><span data-stu-id="da5aa-447">**UniqueID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="da5aa-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-450">Identificatore univoco globale per il processore.</span><span class="sxs-lookup"><span data-stu-id="da5aa-450">A globally unique identifier for the processor.</span></span> <span data-ttu-id="da5aa-451">Questo identificatore può essere univoco solo all'interno di una famiglia di processori.</span><span class="sxs-lookup"><span data-stu-id="da5aa-451">This identifier can only be unique within a processor family.</span></span> <span data-ttu-id="da5aa-452">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="da5aa-452">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="da5aa-453">**UpgradeMethod**</span><span class="sxs-lookup"><span data-stu-id="da5aa-453">**UpgradeMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da5aa-454">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="da5aa-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="da5aa-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="da5aa-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="da5aa-456">Informazioni sul socket della CPU, che includono i dati su come aggiornare il processore (se sono supportati gli aggiornamenti).</span><span class="sxs-lookup"><span data-stu-id="da5aa-456">The CPU socket information, which includes data on how to upgrade the processor (if upgrades are supported).</span></span> <span data-ttu-id="da5aa-457">Questa proprietà viene ereditata [**dal \_ processore CIM**](/windows/desktop/CIMWin32Prov/cim-processor).</span><span class="sxs-lookup"><span data-stu-id="da5aa-457">This property is inherited from [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da5aa-458">Commenti</span><span class="sxs-lookup"><span data-stu-id="da5aa-458">Remarks</span></span>

<span data-ttu-id="da5aa-459">L'accesso alla classe del **\_ processore MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="da5aa-459">Access to the **Msvm\_Processor** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="da5aa-460">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="da5aa-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="da5aa-461">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da5aa-461">Requirements</span></span>



| <span data-ttu-id="da5aa-462">Requisito</span><span class="sxs-lookup"><span data-stu-id="da5aa-462">Requirement</span></span> | <span data-ttu-id="da5aa-463">Valore</span><span class="sxs-lookup"><span data-stu-id="da5aa-463">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da5aa-464">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da5aa-464">Minimum supported client</span></span><br/> | <span data-ttu-id="da5aa-465">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="da5aa-465">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="da5aa-466">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da5aa-466">Minimum supported server</span></span><br/> | <span data-ttu-id="da5aa-467">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="da5aa-467">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="da5aa-468">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="da5aa-468">Namespace</span></span><br/>                | <span data-ttu-id="da5aa-469">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="da5aa-469">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="da5aa-470">MOF</span><span class="sxs-lookup"><span data-stu-id="da5aa-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da5aa-471"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da5aa-471"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="da5aa-472">DLL</span><span class="sxs-lookup"><span data-stu-id="da5aa-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da5aa-473"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="da5aa-473"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="da5aa-474">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da5aa-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da5aa-475">**\_Processore CIM**</span><span class="sxs-lookup"><span data-stu-id="da5aa-475">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dt>

[<span data-ttu-id="da5aa-476">**\_Processore CIM**</span><span class="sxs-lookup"><span data-stu-id="da5aa-476">**CIM\_Processor**</span></span>](/windows/desktop/CIMWin32Prov/cim-processor)
</dt> <dt>

[<span data-ttu-id="da5aa-477">Classi del processore</span><span class="sxs-lookup"><span data-stu-id="da5aa-477">Processor Classes</span></span>](processor-classes.md)
</dt> </dl>

 

