---
description: Rappresenta una porta sull'opzione.
ms.assetid: a2637e53-6b28-41ad-bef9-d3a14b6cf727
title: Classe Msvm_EthernetSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPort
- Msvm_EthernetSwitchPort.SetPowerState
- Msvm_EthernetSwitchPort.EnableDevice
- Msvm_EthernetSwitchPort.OnlineDevice
- Msvm_EthernetSwitchPort.QuiesceDevice
- Msvm_EthernetSwitchPort.SaveProperties
- Msvm_EthernetSwitchPort.RestoreProperties
- Msvm_EthernetSwitchPort.InstanceID
- Msvm_EthernetSwitchPort.Caption
- Msvm_EthernetSwitchPort.Description
- Msvm_EthernetSwitchPort.ElementName
- Msvm_EthernetSwitchPort.InstallDate
- Msvm_EthernetSwitchPort.Name
- Msvm_EthernetSwitchPort.OperationalStatus
- Msvm_EthernetSwitchPort.StatusDescriptions
- Msvm_EthernetSwitchPort.Status
- Msvm_EthernetSwitchPort.HealthState
- Msvm_EthernetSwitchPort.CommunicationStatus
- Msvm_EthernetSwitchPort.DetailedStatus
- Msvm_EthernetSwitchPort.OperatingStatus
- Msvm_EthernetSwitchPort.PrimaryStatus
- Msvm_EthernetSwitchPort.EnabledState
- Msvm_EthernetSwitchPort.OtherEnabledState
- Msvm_EthernetSwitchPort.RequestedState
- Msvm_EthernetSwitchPort.EnabledDefault
- Msvm_EthernetSwitchPort.TimeOfLastStateChange
- Msvm_EthernetSwitchPort.AvailableRequestedStates
- Msvm_EthernetSwitchPort.TransitioningToState
- Msvm_EthernetSwitchPort.SystemCreationClassName
- Msvm_EthernetSwitchPort.SystemName
- Msvm_EthernetSwitchPort.CreationClassName
- Msvm_EthernetSwitchPort.DeviceID
- Msvm_EthernetSwitchPort.PowerManagementSupported
- Msvm_EthernetSwitchPort.PowerManagementCapabilities
- Msvm_EthernetSwitchPort.Availability
- Msvm_EthernetSwitchPort.StatusInfo
- Msvm_EthernetSwitchPort.LastErrorCode
- Msvm_EthernetSwitchPort.ErrorDescription
- Msvm_EthernetSwitchPort.ErrorCleared
- Msvm_EthernetSwitchPort.OtherIdentifyingInfo
- Msvm_EthernetSwitchPort.PowerOnHours
- Msvm_EthernetSwitchPort.TotalPowerOnHours
- Msvm_EthernetSwitchPort.IdentifyingDescriptions
- Msvm_EthernetSwitchPort.AdditionalAvailability
- Msvm_EthernetSwitchPort.MaxQuiesceTime
- Msvm_EthernetSwitchPort.Speed
- Msvm_EthernetSwitchPort.MaxSpeed
- Msvm_EthernetSwitchPort.RequestedSpeed
- Msvm_EthernetSwitchPort.UsageRestriction
- Msvm_EthernetSwitchPort.PortType
- Msvm_EthernetSwitchPort.OtherPortType
- Msvm_EthernetSwitchPort.OtherNetworkPortType
- Msvm_EthernetSwitchPort.PortNumber
- Msvm_EthernetSwitchPort.LinkTechnology
- Msvm_EthernetSwitchPort.OtherLinkTechnology
- Msvm_EthernetSwitchPort.PermanentAddress
- Msvm_EthernetSwitchPort.NetworkAddresses
- Msvm_EthernetSwitchPort.FullDuplex
- Msvm_EthernetSwitchPort.AutoSense
- Msvm_EthernetSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_EthernetSwitchPort.MaxDataSize
- Msvm_EthernetSwitchPort.Capabilities
- Msvm_EthernetSwitchPort.CapabilityDescriptions
- Msvm_EthernetSwitchPort.EnabledCapabilities
- Msvm_EthernetSwitchPort.OtherEnabledCapabilities
- Msvm_EthernetSwitchPort.VMQOffloadUsage
- Msvm_EthernetSwitchPort.IOVOffloadUsage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 76c43cbe8dd053808085346b1874781f354b20dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106320023"
---
# <a name="msvm_ethernetswitchport-class"></a><span data-ttu-id="2b6e8-103">\_Classe MSVM EthernetSwitchPort</span><span class="sxs-lookup"><span data-stu-id="2b6e8-103">Msvm\_EthernetSwitchPort class</span></span>

<span data-ttu-id="2b6e8-104">Rappresenta una porta sull'opzione.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-104">Represents a port on the switch.</span></span>

<span data-ttu-id="2b6e8-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6e8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b6e8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Switch Port";
  string   Description = "Microsoft Virtual Ethernet Switch Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string   SystemName;
  string   CreationClassName = "Msvm_EthernetSwitchPort";
  string   DeviceID;
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
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint32   MaxDataSize;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
  uint32   VMQOffloadUsage;
  uint32   IOVOffloadUsage;
};
```

## <a name="members"></a><span data-ttu-id="2b6e8-107">Members</span><span class="sxs-lookup"><span data-stu-id="2b6e8-107">Members</span></span>

<span data-ttu-id="2b6e8-108">La **classe \_ EthernetSwitchPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2b6e8-108">The **Msvm\_EthernetSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2b6e8-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b6e8-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b6e8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b6e8-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b6e8-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2b6e8-111">Methods</span></span>

<span data-ttu-id="2b6e8-112">La **classe \_ EthernetSwitchPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-112">The **Msvm\_EthernetSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="2b6e8-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="2b6e8-113">Method</span></span>                                                                   | <span data-ttu-id="2b6e8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6e8-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="2b6e8-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="2b6e8-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2b6e8-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="2b6e8-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2b6e8-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="2b6e8-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="2b6e8-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-121">**RequestStateChange**</span></span>](msvm-ethernetswitchport-requeststatechange.md) | <span data-ttu-id="2b6e8-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="2b6e8-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-123">**Reset**</span></span>](msvm-ethernetswitchport-reset.md)                           | <span data-ttu-id="2b6e8-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="2b6e8-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="2b6e8-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2b6e8-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="2b6e8-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="2b6e8-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="2b6e8-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2b6e8-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2b6e8-131">Properties</span></span>

<span data-ttu-id="2b6e8-132">La **classe \_ EthernetSwitchPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-132">The **Msvm\_EthernetSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-136">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="2b6e8-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-137">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="2b6e8-138">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-140">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-142">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="2b6e8-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-144">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-147">Indica se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="2b6e8-148">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-149">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-152">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-152">The primary availability and status of the device.</span></span> <span data-ttu-id="2b6e8-153">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-155">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-157">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="2b6e8-158">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="2b6e8-159">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="2b6e8-160">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="2b6e8-161">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="2b6e8-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="2b6e8-172">)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-173">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-173">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-174">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-174">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-176">Matrice che specifica le funzionalità della porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-176">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="2b6e8-177">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-177">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-178"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-179"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-180"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-181"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-182"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-183"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-184">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-185">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-187">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per le funzionalità della porta contenute nella matrice di **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-187">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="2b6e8-188">Ogni voce di questa matrice è correlata alla voce corrispondente nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-188">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="2b6e8-189">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-189">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-190">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-193">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-193">A short description of the object.</span></span> <span data-ttu-id="2b6e8-194">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "Ethernet Switch Port".</span><span class="sxs-lookup"><span data-stu-id="2b6e8-194">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it is always set to "Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-195">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-195">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-198">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-198">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="2b6e8-199">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-199">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b6e8-200">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-200">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-201">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-201">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-204">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-204">The scoping system's creation class name.</span></span> <span data-ttu-id="2b6e8-205">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="2b6e8-205">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-206">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-206">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-207">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-209">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-209">A description of the object.</span></span> <span data-ttu-id="2b6e8-210">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Virtual Ethernet Switch Port".</span><span class="sxs-lookup"><span data-stu-id="2b6e8-210">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Ethernet Switch Port".</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-211">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-211">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-212">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-213">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-214">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-214">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="2b6e8-215">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-215">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b6e8-216">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-216">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-217">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-217">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-218">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-220">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-220">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="2b6e8-221">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-221">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-222">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-222">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-223">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-225">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-225">A display name for the object.</span></span> <span data-ttu-id="2b6e8-226">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-227">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-227">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-228">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-228">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-230">Specifica quali funzionalità sono abilitate dall'elenco di tutte le funzionalità supportate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-230">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="2b6e8-231">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-231">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-233"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-234"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-235"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-236"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-237"><span id="LoadBalancing_"></span><span id="loadbalancing_"></span><span id="LOADBALANCING_"></span>**LoadBalancing** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-241">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-241">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="2b6e8-242">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-243">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-243">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-246">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-246">The enabled and disabled states of an element.</span></span> <span data-ttu-id="2b6e8-247">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-247">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="2b6e8-248">Valore</span><span class="sxs-lookup"><span data-stu-id="2b6e8-248">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="2b6e8-249">Significato</span><span class="sxs-lookup"><span data-stu-id="2b6e8-249">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="2b6e8-250"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e8-250"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="2b6e8-251">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-251">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="2b6e8-252"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e8-252"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2b6e8-253">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-253">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2b6e8-254">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-254">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-255">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-255">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-257">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-257">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="2b6e8-258">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-258">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-259">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-259">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-261">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-262">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-262">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="2b6e8-263">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-263">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-264">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-264">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-265">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-265">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-266">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-267">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-267">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="2b6e8-268">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-268">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-269">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-269">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-270">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-270">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-271">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-271">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-272">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-272">The current health of the element.</span></span> <span data-ttu-id="2b6e8-273">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-274">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-274">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-275">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-275">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-277">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-277">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="2b6e8-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-279">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-279">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-280">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-280">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-282">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-282">The date and time when the object was installed.</span></span> <span data-ttu-id="2b6e8-283">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-283">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="2b6e8-284">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-285">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-285">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-286">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-288">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-288">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-289">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-289">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2b6e8-290">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-290">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-291">**IOVOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-291">**IOVOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-294">Utilizzo corrente di offload di I/O Virtualization (IOV) su questa porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-294">The current I/O virtualization (IOV) offload usage on this port.</span></span> <span data-ttu-id="2b6e8-295">L'utilizzo è la quantità di risorse IOV in uso sulla porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-295">The usage is the amount of IOV resources in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-296">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-296">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-297">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-299">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-299">The last error code reported by the logical device.</span></span> <span data-ttu-id="2b6e8-300">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-300">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-301">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-301">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-302">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-304">Specifica il tipo di tecnologia di collegamento per la porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-304">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="2b6e8-305">Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-305">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="2b6e8-306">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-306">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-308"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-309"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-310"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-311"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-312"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-313"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-314"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-315"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (9)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-316"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-317"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN wireless** (11)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-318"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-319">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-319">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-320">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-322">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-322">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="2b6e8-323">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)ed è sempre impostata su 1500.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-323">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-324">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-324">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-325">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-325">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-326">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-327">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-327">This property has been deprecated.</span></span> <span data-ttu-id="2b6e8-328">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-328">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-329">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-329">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-330">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-330">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-331">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-332">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="2b6e8-332">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-333">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-333">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2b6e8-334">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-334">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-335">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-335">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-338">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-338">The label by which the object is known.</span></span> <span data-ttu-id="2b6e8-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-340">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-340">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-341">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-343">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-343">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-344">Matrice di stringhe che contengono gli indirizzi MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-344">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="2b6e8-345">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-346">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-346">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-347">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-347">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-349">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-349">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="2b6e8-350">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-350">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b6e8-351">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-351">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-352">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-352">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-353">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-355">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-355">The current statuses of the object.</span></span> <span data-ttu-id="2b6e8-356">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-357">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-357">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-358">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-360">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità abilitata specificata come 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-360">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="2b6e8-361">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-361">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-362">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-362">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-363">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-364">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-365">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-365">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="2b6e8-366">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-366">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="2b6e8-367">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-368">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-368">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-369">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-371">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-371">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="2b6e8-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-373">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-373">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-374">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-376">Valore stringa che descrive **LinkTechnology** quando è impostato su 1, (other).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-376">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="2b6e8-377">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-378">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-378">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-381">L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-381">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="2b6e8-382">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-382">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-383">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-383">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-384">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-386">Descrive il tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-386">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="2b6e8-387">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-387">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-388">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-388">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-389">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-391">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-391">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-392">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-392">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="2b6e8-393">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-393">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="2b6e8-394">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-394">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="2b6e8-395">Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-395">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="2b6e8-396">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-396">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-397">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-397">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-398">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-398">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-399">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-400">Il numero della porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-400">The port number.</span></span> <span data-ttu-id="2b6e8-401">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-401">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-402">**PortType**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-402">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-403">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-404">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-405">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-405">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="2b6e8-406">Quando è impostata su 1 (other), la proprietà **OtherPortType** correlata contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-406">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="2b6e8-407">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-407">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-408"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-409"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-410"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-411"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-412"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-413"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-414"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-415"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-416"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-417"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-418"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-419"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-420"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-421"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-422"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-423"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-424"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-425"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-426"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-427"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-428"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-429"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-431">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-433">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-433">The power management capabilities of the device.</span></span> <span data-ttu-id="2b6e8-434">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-434">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-435">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-436">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-437">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-438">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-438">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="2b6e8-439">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-439">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-440">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-440">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-441">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-443">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-443">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="2b6e8-444">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-444">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-445">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-445">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-446">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-447">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-448">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-448">Provides high level status information.</span></span> <span data-ttu-id="2b6e8-449">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-449">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="2b6e8-450">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-450">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="2b6e8-451">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-452">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-452">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-453">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-453">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-454">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-454">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-455">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="2b6e8-455">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-456">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-456">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2b6e8-457">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-457">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="2b6e8-458">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-458">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-459">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-459">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-460">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-460">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-462">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-462">The last requested or desired state for the element.</span></span> <span data-ttu-id="2b6e8-463">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-463">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-464">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-464">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-465">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-465">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-466">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-467">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="2b6e8-467">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-468">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-468">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="2b6e8-469">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-469">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-470">**Status**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-470">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-471">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-472">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-473">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-473">The current status of the object.</span></span> <span data-ttu-id="2b6e8-474">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-474">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-475">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-475">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-476">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-476">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-477">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-478">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="2b6e8-478">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="2b6e8-479">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-480">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-480">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-481">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-481">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-483">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-483">The current state of the logical device.</span></span> <span data-ttu-id="2b6e8-484">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-485">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-485">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-486">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-488">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="2b6e8-488">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-489">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-489">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="2b6e8-490">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-490">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-491">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-491">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-492">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-493">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-493">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-494">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-494">The scoping system's creation class name.</span></span> <span data-ttu-id="2b6e8-495">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="2b6e8-495">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-497">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-498">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-499">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-499">The scoping system's name.</span></span> <span data-ttu-id="2b6e8-500">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-500">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-501">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-501">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-502">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-502">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-504">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-504">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="2b6e8-505">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-505">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-506">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-506">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-507">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-507">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-508">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-509">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-509">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="2b6e8-510">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-510">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-511">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-511">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-512">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-512">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-513">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-513">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-514">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-514">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="2b6e8-515">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-515">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2b6e8-516">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-516">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-517">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-517">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-518">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-519">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-519">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="2b6e8-520">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-520">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="2b6e8-521">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-521">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="2b6e8-522">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2b6e8-522">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="2b6e8-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-523"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-524"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-525"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="2b6e8-526"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2b6e8-527">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-527">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b6e8-528">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b6e8-528">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2b6e8-529">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2b6e8-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b6e8-530">L'utilizzo della coda di macchine virtuali (VMQ) corrente su questa porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-530">The current virtual machine queue (VMQ) offloading usage on this port.</span></span> <span data-ttu-id="2b6e8-531">L'utilizzo è la quantità di risorse VMQ in uso sulla porta.</span><span class="sxs-lookup"><span data-stu-id="2b6e8-531">The usage is the amount of VMQ resources in use on the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b6e8-532">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b6e8-532">Requirements</span></span>



| <span data-ttu-id="2b6e8-533">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b6e8-533">Requirement</span></span> | <span data-ttu-id="2b6e8-534">Valore</span><span class="sxs-lookup"><span data-stu-id="2b6e8-534">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6e8-535">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b6e8-535">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6e8-536">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2b6e8-536">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2b6e8-537">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b6e8-537">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6e8-538">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2b6e8-538">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b6e8-539">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2b6e8-539">Namespace</span></span><br/>                | <span data-ttu-id="2b6e8-540">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2b6e8-540">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2b6e8-541">MOF</span><span class="sxs-lookup"><span data-stu-id="2b6e8-541">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b6e8-542"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e8-542"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b6e8-543">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6e8-543">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b6e8-544"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b6e8-544"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

