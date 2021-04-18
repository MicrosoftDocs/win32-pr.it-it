---
description: Rappresenta una scheda Ethernet emulata.
ms.assetid: 8E990C76-7D48-42B0-BB4D-C4C07B1C482A
title: Classe Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort
- Msvm_EmulatedEthernetPort.SetPowerState
- Msvm_EmulatedEthernetPort.EnableDevice
- Msvm_EmulatedEthernetPort.OnlineDevice
- Msvm_EmulatedEthernetPort.QuiesceDevice
- Msvm_EmulatedEthernetPort.SaveProperties
- Msvm_EmulatedEthernetPort.RestoreProperties
- Msvm_EmulatedEthernetPort.InstanceID
- Msvm_EmulatedEthernetPort.Caption
- Msvm_EmulatedEthernetPort.Description
- Msvm_EmulatedEthernetPort.ElementName
- Msvm_EmulatedEthernetPort.InstallDate
- Msvm_EmulatedEthernetPort.Name
- Msvm_EmulatedEthernetPort.OperationalStatus
- Msvm_EmulatedEthernetPort.StatusDescriptions
- Msvm_EmulatedEthernetPort.Status
- Msvm_EmulatedEthernetPort.HealthState
- Msvm_EmulatedEthernetPort.CommunicationStatus
- Msvm_EmulatedEthernetPort.DetailedStatus
- Msvm_EmulatedEthernetPort.OperatingStatus
- Msvm_EmulatedEthernetPort.PrimaryStatus
- Msvm_EmulatedEthernetPort.EnabledState
- Msvm_EmulatedEthernetPort.OtherEnabledState
- Msvm_EmulatedEthernetPort.RequestedState
- Msvm_EmulatedEthernetPort.EnabledDefault
- Msvm_EmulatedEthernetPort.TimeOfLastStateChange
- Msvm_EmulatedEthernetPort.AvailableRequestedStates
- Msvm_EmulatedEthernetPort.TransitioningToState
- Msvm_EmulatedEthernetPort.SystemCreationClassName
- Msvm_EmulatedEthernetPort.SystemName
- Msvm_EmulatedEthernetPort.CreationClassName
- Msvm_EmulatedEthernetPort.DeviceID
- Msvm_EmulatedEthernetPort.PowerManagementSupported
- Msvm_EmulatedEthernetPort.PowerManagementCapabilities
- Msvm_EmulatedEthernetPort.Availability
- Msvm_EmulatedEthernetPort.StatusInfo
- Msvm_EmulatedEthernetPort.LastErrorCode
- Msvm_EmulatedEthernetPort.ErrorDescription
- Msvm_EmulatedEthernetPort.ErrorCleared
- Msvm_EmulatedEthernetPort.OtherIdentifyingInfo
- Msvm_EmulatedEthernetPort.PowerOnHours
- Msvm_EmulatedEthernetPort.TotalPowerOnHours
- Msvm_EmulatedEthernetPort.IdentifyingDescriptions
- Msvm_EmulatedEthernetPort.AdditionalAvailability
- Msvm_EmulatedEthernetPort.MaxQuiesceTime
- Msvm_EmulatedEthernetPort.Speed
- Msvm_EmulatedEthernetPort.MaxSpeed
- Msvm_EmulatedEthernetPort.RequestedSpeed
- Msvm_EmulatedEthernetPort.UsageRestriction
- Msvm_EmulatedEthernetPort.PortType
- Msvm_EmulatedEthernetPort.OtherPortType
- Msvm_EmulatedEthernetPort.OtherNetworkPortType
- Msvm_EmulatedEthernetPort.PortNumber
- Msvm_EmulatedEthernetPort.LinkTechnology
- Msvm_EmulatedEthernetPort.OtherLinkTechnology
- Msvm_EmulatedEthernetPort.PermanentAddress
- Msvm_EmulatedEthernetPort.NetworkAddresses
- Msvm_EmulatedEthernetPort.FullDuplex
- Msvm_EmulatedEthernetPort.AutoSense
- Msvm_EmulatedEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_EmulatedEthernetPort.MaxDataSize
- Msvm_EmulatedEthernetPort.Capabilities
- Msvm_EmulatedEthernetPort.CapabilityDescriptions
- Msvm_EmulatedEthernetPort.EnabledCapabilities
- Msvm_EmulatedEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ec13ae369f6d5e3d884f74c96d7df27c2f5fa97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309504"
---
# <a name="msvm_emulatedethernetport-class"></a><span data-ttu-id="7c29b-103">\_Classe MSVM EmulatedEthernetPort</span><span class="sxs-lookup"><span data-stu-id="7c29b-103">Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="7c29b-104">Rappresenta una scheda Ethernet emulata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-104">Represents an emulated Ethernet adapter.</span></span> <span data-ttu-id="7c29b-105">Questa scheda viene utilizzata quando una macchina virtuale non è in grado di eseguire la porta Ethernet sintetica quando nel guest non è installato alcun circuito integrato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-105">This adapter is used when a virtual machine is not capable of running the synthetic Ethernet port when no integrated circuits are installed in the guest.</span></span>

> [!Note]  
> <span data-ttu-id="7c29b-106">Questa classe non è disponibile per le macchine virtuali di seconda generazione.</span><span class="sxs-lookup"><span data-stu-id="7c29b-106">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="7c29b-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7c29b-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c29b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c29b-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EmulatedEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Emulated Ethernet Port";
  string   ElementName = "Legacy Network Adapter";
  datetime InstallDate;
  string   Name = "Ethernet Port";
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
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
  string   CreationClassName = "Msvm_EmulatedEthernetPort";
  string   DeviceID = "Microsoft:GUID\device-specific data";
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   Speed = 1000000000;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  uint16   PortType = 1;
  string   OtherPortType = "Virtual Ethernet";
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  string   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="7c29b-109">Members</span><span class="sxs-lookup"><span data-stu-id="7c29b-109">Members</span></span>

<span data-ttu-id="7c29b-110">La **classe \_ EmulatedEthernetPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7c29b-110">The **Msvm\_EmulatedEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="7c29b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7c29b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7c29b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c29b-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7c29b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="7c29b-113">Methods</span></span>

<span data-ttu-id="7c29b-114">La **classe \_ EmulatedEthernetPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7c29b-114">The **Msvm\_EmulatedEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="7c29b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="7c29b-115">Method</span></span>                                                                     | <span data-ttu-id="7c29b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c29b-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="7c29b-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="7c29b-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="7c29b-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7c29b-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="7c29b-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="7c29b-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7c29b-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="7c29b-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="7c29b-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="7c29b-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7c29b-123">**RequestStateChange**</span></span>](msvm-emulatedethernetport-requeststatechange.md) | <span data-ttu-id="7c29b-124">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="7c29b-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7c29b-125">**Reset**</span></span>](msvm-emulatedethernetport-reset.md)                           | <span data-ttu-id="7c29b-126">Reimposta il dispositivo emulato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-126">Resets the emulated device.</span></span><br/>   |
| <span data-ttu-id="7c29b-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="7c29b-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="7c29b-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7c29b-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="7c29b-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="7c29b-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="7c29b-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="7c29b-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7c29b-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7c29b-133">Properties</span></span>

<span data-ttu-id="7c29b-134">La **classe \_ EmulatedEthernetPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7c29b-134">The **Msvm\_EmulatedEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c29b-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="7c29b-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-136">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-138">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="7c29b-139">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 1500.</span><span class="sxs-lookup"><span data-stu-id="7c29b-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="7c29b-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-143">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="7c29b-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="7c29b-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-145">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="7c29b-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c29b-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-148">Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="7c29b-149">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="7c29b-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="7c29b-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-153">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-153">The primary availability and status of the device.</span></span> <span data-ttu-id="7c29b-154">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c29b-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7c29b-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-156">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-158">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="7c29b-159">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c29b-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="7c29b-160">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="7c29b-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="7c29b-161">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="7c29b-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="7c29b-162">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7c29b-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7c29b-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7c29b-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7c29b-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="7c29b-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7c29b-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="7c29b-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="7c29b-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="7c29b-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="7c29b-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="7c29b-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="7c29b-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7c29b-173">)</span><span class="sxs-lookup"><span data-stu-id="7c29b-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7c29b-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="7c29b-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-177">Funzionalità della porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7c29b-177">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="7c29b-178">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-179">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7c29b-179">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-180">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-180">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-182">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità della porta Ethernet indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-182">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="7c29b-183">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="7c29b-183">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="7c29b-184">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-184">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-185">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7c29b-185">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-188">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c29b-188">A short description of the object.</span></span> <span data-ttu-id="7c29b-189">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="7c29b-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-190">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7c29b-190">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-193">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="7c29b-193">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7c29b-194">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-194">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7c29b-195">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-196">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7c29b-196">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-199">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7c29b-199">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="7c29b-200">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="7c29b-200">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="7c29b-201">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ EmulatedEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="7c29b-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EmulatedEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-202">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7c29b-202">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-205">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7c29b-205">A description of the object.</span></span> <span data-ttu-id="7c29b-206">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Emulated Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="7c29b-206">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Emulated Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-207">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7c29b-207">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-210">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-210">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7c29b-211">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-211">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7c29b-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-213">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7c29b-213">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-214">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-216">Un indirizzo o altre informazioni di identificazione utilizzate per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7c29b-216">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="7c29b-217">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*GUID* \\ *Device-Specific Data*".</span><span class="sxs-lookup"><span data-stu-id="7c29b-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-218">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7c29b-218">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-221">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c29b-221">A display name for the object.</span></span> <span data-ttu-id="7c29b-222">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Legacy Network Adapter".</span><span class="sxs-lookup"><span data-stu-id="7c29b-222">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Legacy Network Adapter".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-223">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7c29b-223">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-224">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-224">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-226">Funzionalità abilitate dall'elenco di tutti quelli supportati, definiti nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-226">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="7c29b-227">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-227">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-228">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7c29b-228">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-229">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-230">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-231">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-231">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7c29b-232">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su 2 ("Enabled").</span><span class="sxs-lookup"><span data-stu-id="7c29b-232">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 ("Enabled").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-233">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-233">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-234">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-234">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-236">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-236">The enabled and disabled states of an element.</span></span> <span data-ttu-id="7c29b-237">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 5 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="7c29b-237">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-238">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="7c29b-238">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-239">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c29b-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-241">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-241">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="7c29b-242">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7c29b-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-246">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="7c29b-246">A string that provides more information about the error recorded in **LastErrorCode**, and information on any corrective actions that can be taken.</span></span> <span data-ttu-id="7c29b-247">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-247">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-248">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="7c29b-248">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-249">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c29b-249">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-251">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="7c29b-251">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="7c29b-252">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="7c29b-252">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-253">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-253">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-254">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-256">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-256">The current health of the element.</span></span> <span data-ttu-id="7c29b-257">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7c29b-257">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7c29b-258">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 ("OK").</span><span class="sxs-lookup"><span data-stu-id="7c29b-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-259">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7c29b-259">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-260">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-260">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-262">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-262">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="7c29b-263">Ogni voce di questa matrice è correlata alla voce in **OtherIdentifyingInfo** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="7c29b-263">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="7c29b-264">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-264">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7c29b-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-266">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c29b-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-268">Valore **DateTime** che indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-268">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="7c29b-269">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-269">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="7c29b-270">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7c29b-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-274">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7c29b-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-275">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7c29b-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7c29b-276">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="7c29b-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-278">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c29b-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-280">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7c29b-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="7c29b-281">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-282">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="7c29b-282">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-283">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-283">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-285">Tipi di collegamenti.</span><span class="sxs-lookup"><span data-stu-id="7c29b-285">The types of links.</span></span> <span data-ttu-id="7c29b-286">Quando è impostato su 1 ("altro"), la proprietà correlata **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-286">When set to 1 ("Other"), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="7c29b-287">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) ed è sempre impostata su 2 ("Ethernet").</span><span class="sxs-lookup"><span data-stu-id="7c29b-287">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is always set to 2 ("Ethernet").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-288">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="7c29b-288">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-289">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7c29b-289">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-291">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="7c29b-291">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="7c29b-292">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)ed è sempre impostata su 1500.</span><span class="sxs-lookup"><span data-stu-id="7c29b-292">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-293">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="7c29b-293">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-294">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-296">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-296">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-297">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="7c29b-297">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-298">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-300">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-300">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="7c29b-301">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))ed è sempre impostata su 1 miliardo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-301">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-302">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7c29b-302">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-305">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7c29b-305">The label by which the object is known.</span></span> <span data-ttu-id="7c29b-306">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="7c29b-306">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="7c29b-307">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="7c29b-307">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-308">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="7c29b-308">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-309">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-309">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-311">Indirizzi MAC Ethernet/802.3, formattati come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC nell'ordine dei bit canonico (il bit dell'indirizzo del gruppo viene trovato nel bit di ordine inferiore del primo carattere della stringa).</span><span class="sxs-lookup"><span data-stu-id="7c29b-311">The Ethernet/802.3 MAC addresses, formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="7c29b-312">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-312">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-313">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7c29b-313">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-314">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-314">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-316">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-316">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7c29b-317">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7c29b-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-319">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7c29b-319">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-320">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-320">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-322">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-322">The current statuses of the element.</span></span> <span data-ttu-id="7c29b-323">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 2 ("OK").</span><span class="sxs-lookup"><span data-stu-id="7c29b-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-324">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7c29b-324">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-325">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-325">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-327">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità abilitate specificate come "altro".</span><span class="sxs-lookup"><span data-stu-id="7c29b-327">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="7c29b-328">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-328">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-329">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-329">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-330">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-332">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="7c29b-332">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7c29b-333">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="7c29b-333">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7c29b-334">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-335">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="7c29b-335">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-336">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-336">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-338">Tutti i dati, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7c29b-338">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="7c29b-339">Ad esempio, è possibile usare questa proprietà per conservare il nome visualizzato del sistema operativo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-339">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="7c29b-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="7c29b-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-344">Valore stringa che descrive **LinkTechnology** quando è impostato su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="7c29b-344">A string value that describes **LinkTechnology** when it is set to 1 ("Other").</span></span> <span data-ttu-id="7c29b-345">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="7c29b-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-349">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e viene impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7c29b-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-350">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="7c29b-350">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-353">Tipo di modulo, quando **portType** è impostato su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="7c29b-353">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="7c29b-354">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ed è sempre impostata su "Virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="7c29b-354">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-355">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="7c29b-355">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-358">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="7c29b-358">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="7c29b-359">Questo indirizzo può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="7c29b-359">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="7c29b-360">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-360">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="7c29b-361">Questa operazione deve essere lasciata vuota se per la scheda di rete non esiste alcun indirizzo hardcoded.</span><span class="sxs-lookup"><span data-stu-id="7c29b-361">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="7c29b-362">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="7c29b-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-363">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="7c29b-363">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-364">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-366">Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete.</span><span class="sxs-lookup"><span data-stu-id="7c29b-366">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="7c29b-367">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="7c29b-367">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="7c29b-368">Valore</span><span class="sxs-lookup"><span data-stu-id="7c29b-368">Value</span></span>                                                                        | <span data-ttu-id="7c29b-369">Significato</span><span class="sxs-lookup"><span data-stu-id="7c29b-369">Meaning</span></span>                             |
|------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="7c29b-370"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c29b-370"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7c29b-371">SCHEDA di interfaccia di rete non emulata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-371">The NIC is not emulated.</span></span><br/> |
| <dl> <span data-ttu-id="7c29b-372"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7c29b-372"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7c29b-373">La scheda di interfaccia di rete è emulata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-373">The NIC is emulated.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="7c29b-374">**PortType**</span><span class="sxs-lookup"><span data-stu-id="7c29b-374">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-375">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-377">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="7c29b-377">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="7c29b-378">Quando è impostato su 1 ("altro"), la proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="7c29b-378">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="7c29b-379">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)ed è sempre impostata su 1 ("other").</span><span class="sxs-lookup"><span data-stu-id="7c29b-379">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1 ("Other").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-380">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="7c29b-380">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-381">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-381">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-383">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-383">The power management capabilities of the device.</span></span> <span data-ttu-id="7c29b-384">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-384">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-385">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="7c29b-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-386">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7c29b-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-388">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="7c29b-388">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="7c29b-389">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-389">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-390">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7c29b-390">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-391">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-393">Il numero di ore consecutive in cui il dispositivo è stato alimentato, dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="7c29b-393">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="7c29b-394">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-394">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-395">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7c29b-395">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-396">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-398">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="7c29b-398">Provides high level status information.</span></span> <span data-ttu-id="7c29b-399">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7c29b-399">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="7c29b-400">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-400">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7c29b-401">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7c29b-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-402">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="7c29b-402">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-403">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-405">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-405">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="7c29b-406">La larghezza di banda effettiva viene segnalata in LogicalPort. Speed.</span><span class="sxs-lookup"><span data-stu-id="7c29b-406">The actual bandwidth is reported in LogicalPort.Speed.</span></span> <span data-ttu-id="7c29b-407">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))ed è sempre impostata su 1 miliardo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-408">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-408">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-409">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-411">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="7c29b-411">The last requested or desired state for the management service.</span></span> <span data-ttu-id="7c29b-412">Quando **EnabledState** è impostato su 5 ("non applicabile"), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-412">When **EnabledState** is set to 5 ("Not Applicable"), then this property has no meaning.</span></span> <span data-ttu-id="7c29b-413">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="7c29b-413">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 ("Not Applicable").</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-414">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="7c29b-414">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-415">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7c29b-415">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-417">Larghezza di banda corrente della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-417">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="7c29b-418">Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="7c29b-418">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="7c29b-419">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 1 miliardo.</span><span class="sxs-lookup"><span data-stu-id="7c29b-419">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1000000000.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-420">**Status**</span><span class="sxs-lookup"><span data-stu-id="7c29b-420">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-423">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-424">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7c29b-424">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-425">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7c29b-425">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-427">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-427">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7c29b-428">Le voci in questa matrice sono correlate a quelle nello stesso indice di matrice in **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="7c29b-428">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="7c29b-429">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="7c29b-429">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-430">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7c29b-430">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-431">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-433">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="7c29b-433">The state of the logical device.</span></span> <span data-ttu-id="7c29b-434">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-435">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="7c29b-435">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-436">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-438">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="7c29b-438">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-439">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="7c29b-439">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="7c29b-440">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)ed è sempre impostata su 1500.</span><span class="sxs-lookup"><span data-stu-id="7c29b-440">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-441">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7c29b-441">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-442">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-443">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-444">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="7c29b-444">The creation class name of the scoping system.</span></span> <span data-ttu-id="7c29b-445">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="7c29b-445">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-446">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7c29b-446">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-447">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7c29b-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-448">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-449">ID della macchina virtuale in formato **GUID** .</span><span class="sxs-lookup"><span data-stu-id="7c29b-449">The virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="7c29b-450">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="7c29b-450">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-451">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7c29b-451">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-452">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7c29b-452">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-454">Data o ora dell'Ultima modifica apportata al **EnabledState** dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7c29b-454">The date or time when the **EnabledState** of the element last changed.</span></span> <span data-ttu-id="7c29b-455">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="7c29b-455">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="7c29b-456">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-456">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="7c29b-457">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-457">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-458">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="7c29b-458">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-459">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-461">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="7c29b-461">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="7c29b-462">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-463">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7c29b-463">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-464">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-464">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-466">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7c29b-466">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7c29b-467">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7c29b-467">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="7c29b-468">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="7c29b-468">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c29b-469">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7c29b-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7c29b-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7c29b-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c29b-471">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="7c29b-471">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="7c29b-472">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 ("non limitato").</span><span class="sxs-lookup"><span data-stu-id="7c29b-472">If there is no restriction on the use of the port, then the value should be set to 4 ("Not Restricted").</span></span> <span data-ttu-id="7c29b-473">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) ed è sempre impostata su 4 ("non limitato").</span><span class="sxs-lookup"><span data-stu-id="7c29b-473">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) and is always set to 4 ("Not Restricted").</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c29b-474">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c29b-474">Remarks</span></span>

<span data-ttu-id="7c29b-475">L'accesso alla **classe \_ EmulatedEthernetPort di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="7c29b-475">Access to the **Msvm\_EmulatedEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7c29b-476">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7c29b-476">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7c29b-477">Esempio</span><span class="sxs-lookup"><span data-stu-id="7c29b-477">Examples</span></span>

<span data-ttu-id="7c29b-478">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7c29b-478">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c29b-479">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c29b-479">Requirements</span></span>



| <span data-ttu-id="7c29b-480">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c29b-480">Requirement</span></span> | <span data-ttu-id="7c29b-481">Valore</span><span class="sxs-lookup"><span data-stu-id="7c29b-481">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c29b-482">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c29b-482">Minimum supported client</span></span><br/> | <span data-ttu-id="7c29b-483">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7c29b-483">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7c29b-484">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c29b-484">Minimum supported server</span></span><br/> | <span data-ttu-id="7c29b-485">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7c29b-485">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c29b-486">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c29b-486">Namespace</span></span><br/>                | <span data-ttu-id="7c29b-487">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7c29b-487">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7c29b-488">MOF</span><span class="sxs-lookup"><span data-stu-id="7c29b-488">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c29b-489"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c29b-489"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c29b-490">DLL</span><span class="sxs-lookup"><span data-stu-id="7c29b-490">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c29b-491"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7c29b-491"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7c29b-492">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c29b-492">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c29b-493">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="7c29b-493">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="7c29b-494">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="7c29b-494">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

