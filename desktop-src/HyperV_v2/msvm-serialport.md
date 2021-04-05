---
description: Rappresenta una porta seriale associata al controller seriale.
ms.assetid: 856823A5-7481-453A-8476-1CDAB1D84123
title: Classe Msvm_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPort
- Msvm_SerialPort.SetPowerState
- Msvm_SerialPort.EnableDevice
- Msvm_SerialPort.OnlineDevice
- Msvm_SerialPort.QuiesceDevice
- Msvm_SerialPort.SaveProperties
- Msvm_SerialPort.RestoreProperties
- Msvm_SerialPort.InstanceID
- Msvm_SerialPort.Caption
- Msvm_SerialPort.Description
- Msvm_SerialPort.ElementName
- Msvm_SerialPort.InstallDate
- Msvm_SerialPort.Name
- Msvm_SerialPort.OperationalStatus
- Msvm_SerialPort.StatusDescriptions
- Msvm_SerialPort.Status
- Msvm_SerialPort.HealthState
- Msvm_SerialPort.CommunicationStatus
- Msvm_SerialPort.DetailedStatus
- Msvm_SerialPort.OperatingStatus
- Msvm_SerialPort.PrimaryStatus
- Msvm_SerialPort.EnabledState
- Msvm_SerialPort.OtherEnabledState
- Msvm_SerialPort.RequestedState
- Msvm_SerialPort.EnabledDefault
- Msvm_SerialPort.TimeOfLastStateChange
- Msvm_SerialPort.AvailableRequestedStates
- Msvm_SerialPort.TransitioningToState
- Msvm_SerialPort.SystemCreationClassName
- Msvm_SerialPort.SystemName
- Msvm_SerialPort.CreationClassName
- Msvm_SerialPort.DeviceID
- Msvm_SerialPort.PowerManagementSupported
- Msvm_SerialPort.PowerManagementCapabilities
- Msvm_SerialPort.Availability
- Msvm_SerialPort.StatusInfo
- Msvm_SerialPort.LastErrorCode
- Msvm_SerialPort.ErrorDescription
- Msvm_SerialPort.ErrorCleared
- Msvm_SerialPort.OtherIdentifyingInfo
- Msvm_SerialPort.PowerOnHours
- Msvm_SerialPort.TotalPowerOnHours
- Msvm_SerialPort.IdentifyingDescriptions
- Msvm_SerialPort.AdditionalAvailability
- Msvm_SerialPort.MaxQuiesceTime
- Msvm_SerialPort.Speed
- Msvm_SerialPort.MaxSpeed
- Msvm_SerialPort.RequestedSpeed
- Msvm_SerialPort.UsageRestriction
- Msvm_SerialPort.PortType
- Msvm_SerialPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc9ff5e1ce4b0a750866a9957c0cffc4bc8501e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882158"
---
# <a name="msvm_serialport-class"></a><span data-ttu-id="5293e-103">\_Classe SerialPort MSVM</span><span class="sxs-lookup"><span data-stu-id="5293e-103">Msvm\_SerialPort class</span></span>

<span data-ttu-id="5293e-104">Rappresenta una porta seriale associata al controller seriale.</span><span class="sxs-lookup"><span data-stu-id="5293e-104">Represents a serial port associated with the serial controller.</span></span>

<span data-ttu-id="5293e-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5293e-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5293e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5293e-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPort : CIM_LogicalPort
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual Serial Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_SerialPort";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint64   Speed = 115200;
  uint32   MaxSpeed = 115200;
  uint64   RequestedSpeed = 115200;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Serial Port";
};
```

## <a name="members"></a><span data-ttu-id="5293e-107">Members</span><span class="sxs-lookup"><span data-stu-id="5293e-107">Members</span></span>

<span data-ttu-id="5293e-108">La **classe \_ SerialPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5293e-108">The **Msvm\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="5293e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5293e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5293e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5293e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5293e-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="5293e-111">Methods</span></span>

<span data-ttu-id="5293e-112">La **classe \_ SerialPort MSVM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5293e-112">The **Msvm\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="5293e-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="5293e-113">Method</span></span>                                                           | <span data-ttu-id="5293e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5293e-114">Description</span></span>                              |
|:-----------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="5293e-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="5293e-115">**EnableDevice**</span></span>                                                 | <span data-ttu-id="5293e-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5293e-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="5293e-117">**OnlineDevice**</span></span>                                                 | <span data-ttu-id="5293e-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5293e-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="5293e-119">**QuiesceDevice**</span></span>                                                | <span data-ttu-id="5293e-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="5293e-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="5293e-121">**RequestStateChange**</span></span>](msvm-serialport-requeststatechange.md) | <span data-ttu-id="5293e-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="5293e-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="5293e-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5293e-123">**Reset**</span></span>](msvm-serialport-reset.md)                           | <span data-ttu-id="5293e-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="5293e-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="5293e-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="5293e-125">**RestoreProperties**</span></span>                                            | <span data-ttu-id="5293e-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5293e-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="5293e-127">**SaveProperties**</span></span>                                               | <span data-ttu-id="5293e-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="5293e-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="5293e-129">**SetPowerState**</span></span>                                                | <span data-ttu-id="5293e-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5293e-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5293e-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5293e-131">Properties</span></span>

<span data-ttu-id="5293e-132">La **classe \_ SerialPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5293e-132">The **Msvm\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5293e-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="5293e-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5293e-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="5293e-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5293e-138">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-138">Value</span></span>                                                                            | <span data-ttu-id="5293e-139">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-139">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5293e-140"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-140"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="5293e-141"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-141"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="5293e-142">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="5293e-142">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-143">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="5293e-143">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-144">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-146">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5293e-146">The primary availability and status of the device.</span></span> <span data-ttu-id="5293e-147">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-147">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="5293e-148">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-148">Value</span></span>                                                                        | <span data-ttu-id="5293e-149">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-149">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5293e-150"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-150"><dt>6</dt></span></span> </dl> | <span data-ttu-id="5293e-151">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="5293e-151">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-152">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="5293e-152">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-153">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-155">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="5293e-155">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="5293e-156">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-156">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-157">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5293e-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-160">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5293e-160">A short description of the object.</span></span> <span data-ttu-id="5293e-161">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="5293e-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-165">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="5293e-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5293e-166">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5293e-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5293e-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5293e-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5293e-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="5293e-169"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="5293e-170"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="5293e-171"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="5293e-172"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5293e-173"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5293e-174"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5293e-175">)</span><span class="sxs-lookup"><span data-stu-id="5293e-175">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5293e-176">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5293e-176">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-179">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="5293e-179">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5293e-180">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-180">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-181">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5293e-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-184">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="5293e-184">A description of the object.</span></span> <span data-ttu-id="5293e-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-186">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5293e-186">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-189">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="5293e-189">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5293e-190">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5293e-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5293e-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5293e-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="5293e-192"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="5293e-193"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="5293e-194"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="5293e-195"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="5293e-196"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="5293e-197"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5293e-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5293e-199"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5293e-200">)</span><span class="sxs-lookup"><span data-stu-id="5293e-200">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5293e-201">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5293e-201">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-204">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*", in cui *i dati specifici del dispositivo* sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="5293e-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*", where *device-specific-data* is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5293e-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-208">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5293e-208">A display name for the object.</span></span> <span data-ttu-id="5293e-209">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="5293e-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-213">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="5293e-213">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="5293e-214">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5293e-215">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-215">Value</span></span>                                                                        | <span data-ttu-id="5293e-216">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-216">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="5293e-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="5293e-218">Abilitato</span><span class="sxs-lookup"><span data-stu-id="5293e-218">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-219">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="5293e-219">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-220">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-220">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-222">Stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5293e-222">The enabled state of the element.</span></span> <span data-ttu-id="5293e-223">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="5293e-223">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="5293e-224">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-224">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5293e-225">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-225">Value</span></span>                                                                        | <span data-ttu-id="5293e-226">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-226">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5293e-227"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-227"><dt>5</dt></span></span> </dl> | <span data-ttu-id="5293e-228">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="5293e-228">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-229">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="5293e-229">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-230">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5293e-230">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-232">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="5293e-232">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="5293e-233">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-234">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="5293e-234">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-237">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="5293e-237">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="5293e-238">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-238">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-239">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5293e-239">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-240">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-240">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-242">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5293e-242">The current health of the element.</span></span> <span data-ttu-id="5293e-243">Questa operazione esprime l'integrità dell'elemento, ma non necessariamente quello dei sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="5293e-243">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="5293e-244">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="5293e-244">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="5293e-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5293e-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-247">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5293e-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-249">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="5293e-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="5293e-250">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5293e-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5293e-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-252">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5293e-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-254">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5293e-254">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="5293e-255">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-256">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5293e-256">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5293e-259">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="5293e-259">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5293e-260">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="5293e-260">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5293e-261">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-261">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-262">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5293e-262">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-263">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5293e-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-265">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5293e-265">The last error code reported by the logical device.</span></span> <span data-ttu-id="5293e-266">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-266">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-267">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="5293e-267">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-268">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5293e-268">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-270">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="5293e-270">This property has been deprecated.</span></span> <span data-ttu-id="5293e-271">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-271">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-272">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="5293e-272">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-273">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5293e-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-275">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5293e-275">The maximum bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="5293e-276">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-276">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-277">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5293e-277">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-280">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5293e-280">The label by which the object is known.</span></span> <span data-ttu-id="5293e-281">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="5293e-281">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-282">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="5293e-282">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-285">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5293e-285">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5293e-286">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5293e-286">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5293e-287">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-287">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5293e-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5293e-288"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="5293e-289"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="5293e-290"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="5293e-291"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="5293e-292"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="5293e-293"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="5293e-294"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="5293e-295"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="5293e-296"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="5293e-297"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="5293e-298"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="5293e-299"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="5293e-300"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="5293e-301"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="5293e-302"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="5293e-303"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="5293e-304"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5293e-305"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5293e-306"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5293e-307">)</span><span class="sxs-lookup"><span data-stu-id="5293e-307">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5293e-308">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5293e-308">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-309">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-311">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5293e-311">The current statuses of the object.</span></span> <span data-ttu-id="5293e-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-313">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="5293e-313">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-314">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-316">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="5293e-316">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="5293e-317">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="5293e-317">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="5293e-318">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-318">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-319">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5293e-319">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-320">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5293e-320">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-322">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5293e-322">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="5293e-323">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5293e-323">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-324">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="5293e-324">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-325">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-327">Tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="5293e-327">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="5293e-328">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-328">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-329">**PortType**</span><span class="sxs-lookup"><span data-stu-id="5293e-329">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-330">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-330">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-332">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-332">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="5293e-333">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-333">Value</span></span>                                                                        | <span data-ttu-id="5293e-334">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-334">Meaning</span></span>          |
|------------------------------------------------------------------------------|------------------|
| <dl> <span data-ttu-id="5293e-335"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-335"><dt>1</dt></span></span> </dl> | <span data-ttu-id="5293e-336">Altro</span><span class="sxs-lookup"><span data-stu-id="5293e-336">Other</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-337">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="5293e-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-338">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-340">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5293e-340">The power management capabilities of the device.</span></span> <span data-ttu-id="5293e-341">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-341">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-342">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="5293e-342">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-343">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5293e-343">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-345">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="5293e-345">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="5293e-346">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-347">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5293e-347">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-348">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5293e-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-350">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="5293e-350">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="5293e-351">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-351">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-352">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="5293e-352">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-353">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-353">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-355">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="5293e-355">Provides high level status information.</span></span> <span data-ttu-id="5293e-356">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="5293e-356">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="5293e-357">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="5293e-357">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5293e-358">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-358">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="5293e-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5293e-359"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="5293e-360"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="5293e-361"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="5293e-362"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5293e-363"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5293e-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="5293e-364"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="5293e-365">)</span><span class="sxs-lookup"><span data-stu-id="5293e-365">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5293e-366">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="5293e-366">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-367">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5293e-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-368">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-369">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5293e-369">The requested bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="5293e-370">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-370">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-371">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="5293e-371">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-372">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-373">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-374">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="5293e-374">The last requested or desired state for the element.</span></span> <span data-ttu-id="5293e-375">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="5293e-375">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="5293e-376">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="5293e-376">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="5293e-377">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-377">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="5293e-378">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-378">Value</span></span>                                                                         | <span data-ttu-id="5293e-379">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-379">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5293e-380"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-380"><dt>12</dt></span></span> </dl> | <span data-ttu-id="5293e-381">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="5293e-381">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5293e-382">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="5293e-382">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-383">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5293e-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-385">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="5293e-385">The bandwidth of the port, in bits-per-second.</span></span> <span data-ttu-id="5293e-386">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-386">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-387">**Status**</span><span class="sxs-lookup"><span data-stu-id="5293e-387">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-388">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-389">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-390">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5293e-390">The current status of the object.</span></span> <span data-ttu-id="5293e-391">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-391">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-392">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="5293e-392">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-393">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5293e-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5293e-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-395">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="5293e-395">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="5293e-396">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5293e-396">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-397">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="5293e-397">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-398">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-400">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="5293e-400">The current state of the logical device.</span></span> <span data-ttu-id="5293e-401">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-401">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-402">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5293e-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-403">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-405">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="5293e-405">The scoping system's creation class name.</span></span> <span data-ttu-id="5293e-406">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-406">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5293e-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5293e-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-410">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="5293e-410">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="5293e-411">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="5293e-411">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="5293e-412">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="5293e-412">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-413">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5293e-413">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-415">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5293e-415">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="5293e-416">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="5293e-416">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-417">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="5293e-417">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-418">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5293e-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-420">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="5293e-420">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="5293e-421">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-421">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-422">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="5293e-422">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-423">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-423">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-424">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-425">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5293e-425">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="5293e-426">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5293e-426">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5293e-427">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="5293e-427">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5293e-428">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5293e-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5293e-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5293e-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5293e-430">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="5293e-430">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="5293e-431">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="5293e-431">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="5293e-432">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="5293e-432">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="5293e-433">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5293e-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="5293e-434">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-434">Value</span></span>                                                                        | <span data-ttu-id="5293e-435">Significato</span><span class="sxs-lookup"><span data-stu-id="5293e-435">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="5293e-436"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-436"><dt>4</dt></span></span> </dl> | <span data-ttu-id="5293e-437">Senza restrizioni</span><span class="sxs-lookup"><span data-stu-id="5293e-437">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5293e-438">Commenti</span><span class="sxs-lookup"><span data-stu-id="5293e-438">Remarks</span></span>

<span data-ttu-id="5293e-439">L'accesso alla **classe \_ SerialPort MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="5293e-439">Access to the **Msvm\_SerialPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5293e-440">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5293e-440">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="5293e-441">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5293e-441">Requirements</span></span>



| <span data-ttu-id="5293e-442">Requisito</span><span class="sxs-lookup"><span data-stu-id="5293e-442">Requirement</span></span> | <span data-ttu-id="5293e-443">Valore</span><span class="sxs-lookup"><span data-stu-id="5293e-443">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5293e-444">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5293e-444">Minimum supported client</span></span><br/> | <span data-ttu-id="5293e-445">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5293e-445">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5293e-446">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5293e-446">Minimum supported server</span></span><br/> | <span data-ttu-id="5293e-447">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5293e-447">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5293e-448">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5293e-448">Namespace</span></span><br/>                | <span data-ttu-id="5293e-449">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5293e-449">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5293e-450">MOF</span><span class="sxs-lookup"><span data-stu-id="5293e-450">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5293e-451"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-451"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5293e-452">DLL</span><span class="sxs-lookup"><span data-stu-id="5293e-452">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5293e-453"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5293e-453"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5293e-454">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5293e-454">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5293e-455">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="5293e-455">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> <dt>

<span data-ttu-id="5293e-456">[**\_LOGICALPORT CIM**](/previous-versions//cc136869(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5293e-456">[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5293e-457">Classi di dispositivi seriali</span><span class="sxs-lookup"><span data-stu-id="5293e-457">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

