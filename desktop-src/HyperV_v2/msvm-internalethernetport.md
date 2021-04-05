---
description: Rappresenta una porta Ethernet interna (scheda di rete).
ms.assetid: 43277FA7-E040-49F2-A086-AF19B29D4F75
title: Classe Msvm_InternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InternalEthernetPort
- Msvm_InternalEthernetPort.SetPowerState
- Msvm_InternalEthernetPort.EnableDevice
- Msvm_InternalEthernetPort.OnlineDevice
- Msvm_InternalEthernetPort.QuiesceDevice
- Msvm_InternalEthernetPort.SaveProperties
- Msvm_InternalEthernetPort.RestoreProperties
- Msvm_InternalEthernetPort.InstanceID
- Msvm_InternalEthernetPort.Caption
- Msvm_InternalEthernetPort.Description
- Msvm_InternalEthernetPort.ElementName
- Msvm_InternalEthernetPort.InstallDate
- Msvm_InternalEthernetPort.Name
- Msvm_InternalEthernetPort.OperationalStatus
- Msvm_InternalEthernetPort.StatusDescriptions
- Msvm_InternalEthernetPort.Status
- Msvm_InternalEthernetPort.HealthState
- Msvm_InternalEthernetPort.CommunicationStatus
- Msvm_InternalEthernetPort.DetailedStatus
- Msvm_InternalEthernetPort.OperatingStatus
- Msvm_InternalEthernetPort.PrimaryStatus
- Msvm_InternalEthernetPort.EnabledState
- Msvm_InternalEthernetPort.OtherEnabledState
- Msvm_InternalEthernetPort.RequestedState
- Msvm_InternalEthernetPort.EnabledDefault
- Msvm_InternalEthernetPort.TimeOfLastStateChange
- Msvm_InternalEthernetPort.AvailableRequestedStates
- Msvm_InternalEthernetPort.TransitioningToState
- Msvm_InternalEthernetPort.SystemCreationClassName
- Msvm_InternalEthernetPort.SystemName
- Msvm_InternalEthernetPort.CreationClassName
- Msvm_InternalEthernetPort.DeviceID
- Msvm_InternalEthernetPort.PowerManagementSupported
- Msvm_InternalEthernetPort.PowerManagementCapabilities
- Msvm_InternalEthernetPort.Availability
- Msvm_InternalEthernetPort.StatusInfo
- Msvm_InternalEthernetPort.LastErrorCode
- Msvm_InternalEthernetPort.ErrorDescription
- Msvm_InternalEthernetPort.ErrorCleared
- Msvm_InternalEthernetPort.OtherIdentifyingInfo
- Msvm_InternalEthernetPort.PowerOnHours
- Msvm_InternalEthernetPort.TotalPowerOnHours
- Msvm_InternalEthernetPort.IdentifyingDescriptions
- Msvm_InternalEthernetPort.AdditionalAvailability
- Msvm_InternalEthernetPort.MaxQuiesceTime
- Msvm_InternalEthernetPort.MaxSpeed
- Msvm_InternalEthernetPort.RequestedSpeed
- Msvm_InternalEthernetPort.UsageRestriction
- Msvm_InternalEthernetPort.OtherPortType
- Msvm_InternalEthernetPort.Speed
- Msvm_InternalEthernetPort.OtherNetworkPortType
- Msvm_InternalEthernetPort.PortNumber
- Msvm_InternalEthernetPort.LinkTechnology
- Msvm_InternalEthernetPort.OtherLinkTechnology
- Msvm_InternalEthernetPort.PermanentAddress
- Msvm_InternalEthernetPort.FullDuplex
- Msvm_InternalEthernetPort.AutoSense
- Msvm_InternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_InternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_InternalEthernetPort.PortType
- Msvm_InternalEthernetPort.NetworkAddresses
- Msvm_InternalEthernetPort.MaxDataSize
- Msvm_InternalEthernetPort.Capabilities
- Msvm_InternalEthernetPort.CapabilityDescriptions
- Msvm_InternalEthernetPort.EnabledCapabilities
- Msvm_InternalEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a1441055fc7b86b97c69a40758236261b20f75c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752367"
---
# <a name="msvm_internalethernetport-class"></a><span data-ttu-id="ddac4-103">\_Classe MSVM InternalEthernetPort</span><span class="sxs-lookup"><span data-stu-id="ddac4-103">Msvm\_InternalEthernetPort class</span></span>

<span data-ttu-id="ddac4-104">Rappresenta una porta Ethernet interna (scheda di rete).</span><span class="sxs-lookup"><span data-stu-id="ddac4-104">Represents an internal Ethernet port (network adapter).</span></span> <span data-ttu-id="ddac4-105">Questo tipo di porta Ethernet consente alle macchine virtuali di accedere al server di virtualizzazione che esegue il software di rete.</span><span class="sxs-lookup"><span data-stu-id="ddac4-105">This type of Ethernet port gives virtual machines access to the virtualization server running the networking software.</span></span> <span data-ttu-id="ddac4-106">Le schede di rete interne consentono di instradare o filtrare il traffico di rete delle macchine virtuali prima di uscire dal sistema fisico.</span><span class="sxs-lookup"><span data-stu-id="ddac4-106">The internal network adapters allow the virtual machines network traffic to be routed or filtered before leaving the physical system.</span></span>

<span data-ttu-id="ddac4-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ddac4-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddac4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddac4-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft Internal Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
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
  string   CreationClassName = "Msvm_InternalEthernetPort";
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
  uint16   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint64   MaxSpeed = 1000000000;
  uint64   RequestedSpeed = 1000000000;
  uint16   UsageRestriction = 4;
  string   OtherPortType;
  uint64   Speed;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 2;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  boolean  FullDuplex = True;
  boolean  AutoSense = True;
  uint64   SupportedMaximumTransmissionUnit = 1500;
  uint64   ActiveMaximumTransmissionUnit = 1500;
  uint16   PortType;
  string   NetworkAddresses[];
  uint32   MaxDataSize = 1500;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  uint16   EnabledCapabilities[];
  string   OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="ddac4-109">Members</span><span class="sxs-lookup"><span data-stu-id="ddac4-109">Members</span></span>

<span data-ttu-id="ddac4-110">La **classe \_ InternalEthernetPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ddac4-110">The **Msvm\_InternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ddac4-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddac4-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ddac4-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ddac4-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ddac4-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="ddac4-113">Methods</span></span>

<span data-ttu-id="ddac4-114">La **classe \_ InternalEthernetPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ddac4-114">The **Msvm\_InternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="ddac4-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="ddac4-115">Method</span></span>                                                                     | <span data-ttu-id="ddac4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddac4-116">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="ddac4-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="ddac4-117">**EnableDevice**</span></span>                                                           | <span data-ttu-id="ddac4-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ddac4-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="ddac4-119">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="ddac4-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ddac4-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="ddac4-121">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="ddac4-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="ddac4-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="ddac4-123">**RequestStateChange**</span></span>](msvm-internalethernetport-requeststatechange.md) | <span data-ttu-id="ddac4-124">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="ddac4-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="ddac4-125">**Reset**</span></span>](msvm-internalethernetport-reset.md)                           | <span data-ttu-id="ddac4-126">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="ddac4-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="ddac4-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="ddac4-127">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="ddac4-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ddac4-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="ddac4-129">**SaveProperties**</span></span>                                                         | <span data-ttu-id="ddac4-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="ddac4-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-131">**SetPowerState**</span></span>                                                          | <span data-ttu-id="ddac4-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ddac4-133">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ddac4-133">Properties</span></span>

<span data-ttu-id="ddac4-134">La **classe \_ InternalEthernetPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ddac4-134">The **Msvm\_InternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddac4-135">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ddac4-135">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-136">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-136">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-138">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="ddac4-139">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="ddac4-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-143">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="ddac4-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ddac4-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-145">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="ddac4-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddac4-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-148">Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="ddac4-149">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="ddac4-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-153">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-153">The primary availability and status of the device.</span></span> <span data-ttu-id="ddac4-154">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="ddac4-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-156">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-158">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="ddac4-159">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ddac4-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="ddac4-160">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="ddac4-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="ddac4-161">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="ddac4-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="ddac4-162">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-163">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="ddac4-163">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-164">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-166">Funzionalità della porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="ddac4-166">Capabilities of the Ethernet port.</span></span> <span data-ttu-id="ddac4-167">Se sono elencate le funzionalità di failover o bilanciamento del carico, è necessario definire anche un [**\_ SpareGroup CIM**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) o [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (bilanciamento del carico) per descrivere completamente la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ddac4-167">If failover or load balancing capabilities are listed, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="ddac4-168">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-168">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="ddac4-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ddac4-169"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ddac4-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="ddac4-171"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="ddac4-172"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="ddac4-173"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="ddac4-174"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddac4-175">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ddac4-175">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-176">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-176">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-178">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità della porta Ethernet indicate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-178">An array of free-form strings that provides more detailed explanations for any of the Ethernet port features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="ddac4-179">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="ddac4-179">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="ddac4-180">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-181">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="ddac4-181">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-184">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddac4-184">A short description of the object.</span></span> <span data-ttu-id="ddac4-185">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-185">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-186">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="ddac4-186">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-187">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-188">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-189">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="ddac4-189">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ddac4-190">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddac4-191">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-192">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddac4-192">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-195">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="ddac4-195">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="ddac4-196">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="ddac4-196">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="ddac4-197">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ddac4-197">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-198">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="ddac4-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-201">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="ddac4-201">A description of the object.</span></span> <span data-ttu-id="ddac4-202">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-202">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-203">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ddac4-203">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-204">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-206">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-206">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ddac4-207">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-207">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddac4-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-209">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="ddac4-209">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-212">Un indirizzo o altre informazioni di identificazione utilizzate per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddac4-212">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="ddac4-213">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific Data*".</span><span class="sxs-lookup"><span data-stu-id="ddac4-213">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-214">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ddac4-214">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-216">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="ddac4-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-217">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddac4-217">A display name for the object.</span></span> <span data-ttu-id="ddac4-218">Questa proprietà consente a ogni istanza di definire un nome visualizzato oltre alle relative proprietà chiave, dati di identità e informazioni sulla descrizione.</span><span class="sxs-lookup"><span data-stu-id="ddac4-218">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="ddac4-219">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e viene generata in base alla scheda di interfaccia di rete presente nell'host.</span><span class="sxs-lookup"><span data-stu-id="ddac4-219">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) and is generated based on the NIC present in the host.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-220">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ddac4-220">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-221">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-221">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-223">Specifica quali funzionalità sono abilitate dall'elenco di tutti quelli supportati, definiti nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-223">Specifies which capabilities are enabled from the list of all supported ones, which are defined in the **Capabilities** array.</span></span> <span data-ttu-id="ddac4-224">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-224">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="ddac4-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ddac4-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ddac4-226"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="ddac4-227"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="ddac4-228"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="ddac4-229"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="ddac4-230"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddac4-231">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="ddac4-231">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-232">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-232">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-234">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-234">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ddac4-235">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-235">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-236">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-236">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-237">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-239">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-239">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ddac4-240">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-240">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-241">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="ddac4-241">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-242">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddac4-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-244">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-244">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="ddac4-245">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-245">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-246">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="ddac4-246">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-249">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="ddac4-249">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="ddac4-250">Questa proprietà viene ereditata dalla proprietà [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) property and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-251">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="ddac4-251">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-252">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddac4-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-254">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="ddac4-254">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="ddac4-255">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-255">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-256">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-256">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-259">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-259">The current health of the element.</span></span> <span data-ttu-id="ddac4-260">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="ddac4-260">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ddac4-261">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-262">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ddac4-262">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-263">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-263">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-265">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-265">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="ddac4-266">Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **OtherIdentifyingInfo** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="ddac4-266">Each entry of this array is related to the entry in the **OtherIdentifyingInfo** property array that is located at the same index.</span></span> <span data-ttu-id="ddac4-267">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-267">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ddac4-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-269">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddac4-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-271">Valore **DateTime** che indica quando l'oggetto è stato installato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-271">A **datetime** value that indicates when the object was installed.</span></span> <span data-ttu-id="ddac4-272">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-272">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="ddac4-273">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-274">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ddac4-274">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-275">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-277">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="ddac4-277">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-278">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ddac4-278">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ddac4-279">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-279">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-280">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="ddac4-280">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-281">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddac4-281">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-283">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddac4-283">The last error code reported by the logical device.</span></span> <span data-ttu-id="ddac4-284">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-284">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-285">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ddac4-285">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-286">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-288">Tipi di collegamenti.</span><span class="sxs-lookup"><span data-stu-id="ddac4-288">The types of links.</span></span> <span data-ttu-id="ddac4-289">Quando è impostata su 1 (other), la proprietà correlata **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-289">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="ddac4-290">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-290">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="ddac4-291">Valore</span><span class="sxs-lookup"><span data-stu-id="ddac4-291">Value</span></span>                                                                        | <span data-ttu-id="ddac4-292">Significato</span><span class="sxs-lookup"><span data-stu-id="ddac4-292">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="ddac4-293"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ddac4-293"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ddac4-294">Ethernet</span><span class="sxs-lookup"><span data-stu-id="ddac4-294">Ethernet</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ddac4-295">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="ddac4-295">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-296">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ddac4-296">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-298">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="ddac4-298">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="ddac4-299">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-299">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-300">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="ddac4-300">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-301">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-303">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-303">This property has been deprecated.</span></span> <span data-ttu-id="ddac4-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-305">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="ddac4-305">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-306">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-306">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-308">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-308">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ddac4-309">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-309">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-310">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ddac4-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-311">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-312">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-313">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="ddac4-313">The label by which the object is known.</span></span> <span data-ttu-id="ddac4-314">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="ddac4-314">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="ddac4-315">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-316">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="ddac4-316">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-317">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-317">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-318">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-319">Gli indirizzi MAC Ethernet/802.3 formattati come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico (il bit dell'indirizzo del gruppo viene trovato nel bit di ordine inferiore del primo carattere della stringa). Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-319">The Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="ddac4-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-321">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-323">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ddac4-324">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddac4-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ddac4-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-327">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-329">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-329">The current statuses of the element.</span></span> <span data-ttu-id="ddac4-330">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-331">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ddac4-331">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-332">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-334">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità abilitata specificata come 1 (other).</span><span class="sxs-lookup"><span data-stu-id="ddac4-334">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other).</span></span> <span data-ttu-id="ddac4-335">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-335">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-339">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="ddac4-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other.) This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="ddac4-340">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="ddac4-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-342">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-344">Tutti i dati, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddac4-344">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="ddac4-345">Ad esempio, è possibile usare questa proprietà per conservare il nome visualizzato del sistema operativo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-345">For example, you could use this property to hold the operating system's display name for the device.</span></span> <span data-ttu-id="ddac4-346">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-346">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-347">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="ddac4-347">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-350">Valore stringa che descrive la proprietà **LinkTechnology** quando è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="ddac4-350">A string value that describes the **LinkTechnology** property when it is set to 1 (Other).</span></span> <span data-ttu-id="ddac4-351">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-351">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-352">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="ddac4-352">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-355">Questa proprietà è deprecata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-355">This property is deprecated.</span></span> <span data-ttu-id="ddac4-356">Utilizzare la proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-356">Use the **PortType** property.</span></span> <span data-ttu-id="ddac4-357">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-357">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<span data-ttu-id="ddac4-358">Deprecated Description: tipo di modulo, quando la proprietà **portType** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="ddac4-358">Deprecated description: The type of module, when the **PortType** property is set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-359">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="ddac4-359">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-362">Tipo di modulo, quando la proprietà **portType** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="ddac4-362">The type of module, when the **PortType** property is set to 1 (Other).</span></span> <span data-ttu-id="ddac4-363">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ddac4-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)) .</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-364">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="ddac4-364">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-367">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="ddac4-367">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="ddac4-368">Questo indirizzo può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="ddac4-368">This address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="ddac4-369">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-369">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="ddac4-370">Questa operazione deve essere lasciata vuota se per la scheda di rete non esiste alcun indirizzo hardcoded.</span><span class="sxs-lookup"><span data-stu-id="ddac4-370">This should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="ddac4-371">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-371">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-372">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="ddac4-372">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-373">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-374">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-375">Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete.</span><span class="sxs-lookup"><span data-stu-id="ddac4-375">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="ddac4-376">Questo valore è 1 per le NIC emulate, 0 per tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="ddac4-376">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="ddac4-377">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-377">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-378">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ddac4-378">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-379">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-381">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="ddac4-381">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="ddac4-382">Quando è impostata su 1 (other), la proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="ddac4-382">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="ddac4-383">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-383">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="ddac4-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="ddac4-384"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="ddac4-385"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="ddac4-386"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="ddac4-387"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="ddac4-388"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="ddac4-389"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="ddac4-390"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="ddac4-391"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="ddac4-392"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="ddac4-393"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="ddac4-394"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="ddac4-395"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="ddac4-396"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="ddac4-397"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="ddac4-398"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="ddac4-399"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="ddac4-400"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="ddac4-401"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="ddac4-402"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="ddac4-403"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="ddac4-404"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="ddac4-405"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ddac4-406">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="ddac4-406">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-407">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-407">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-409">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-409">The power management capabilities of the device.</span></span> <span data-ttu-id="ddac4-410">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-410">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-411">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="ddac4-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-412">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="ddac4-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-414">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="ddac4-414">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="ddac4-415">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-415">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-416">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ddac4-416">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-417">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-417">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-419">Il numero di ore consecutive in cui il dispositivo è stato alimentato, dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="ddac4-419">The number of consecutive hours that this device has been powered, since its last power cycle.</span></span> <span data-ttu-id="ddac4-420">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-421">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="ddac4-421">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-422">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-424">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="ddac4-424">Provides high level status information.</span></span> <span data-ttu-id="ddac4-425">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="ddac4-425">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="ddac4-426">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-426">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ddac4-427">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-427">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-428">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="ddac4-428">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-429">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-429">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-430">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-431">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-431">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="ddac4-432">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-432">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="ddac4-433">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-433">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-434">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-434">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-435">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-437">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="ddac4-437">The last requested or desired state for the management service.</span></span> <span data-ttu-id="ddac4-438">Quando la proprietà **EnabledState** è impostata su 5 (non applicabile), questa proprietà non ha alcun significato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-438">When the **EnabledState** property is set to 5 (Not Applicable), then this property has no meaning.</span></span> <span data-ttu-id="ddac4-439">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-439">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-440">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="ddac4-440">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-441">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-441">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-442">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-442">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-443">Qualificatori: **override**, **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="ddac4-443">Qualifiers: **Override**, **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-444">Larghezza di banda corrente della porta in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="ddac4-444">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="ddac4-445">Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="ddac4-445">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="ddac4-446">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-446">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-447">**Status**</span><span class="sxs-lookup"><span data-stu-id="ddac4-447">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-448">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-450">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ddac4-450">The current status of the object.</span></span> <span data-ttu-id="ddac4-451">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-451">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-452">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ddac4-452">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-453">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="ddac4-453">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-455">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ddac4-455">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ddac4-456">Le voci in questa matrice sono correlate a quelle nello stesso indice di matrice in **OperationalStatus**.</span><span class="sxs-lookup"><span data-stu-id="ddac4-456">Entries in this array are correlated with those at the same array index in **OperationalStatus**.</span></span> <span data-ttu-id="ddac4-457">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ddac4-457">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-458">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="ddac4-458">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-459">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-459">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-461">Stato del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ddac4-461">The state of the logical device.</span></span> <span data-ttu-id="ddac4-462">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-463">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="ddac4-463">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-464">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ddac4-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-466">Unità di trasmissione massima (MTU) che può essere supportata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-466">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="ddac4-467">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="ddac4-467">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-468">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ddac4-468">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-469">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-471">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ddac4-471">The scoping system's creation class name.</span></span> <span data-ttu-id="ddac4-472">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non è supportata</span><span class="sxs-lookup"><span data-stu-id="ddac4-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not supported</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ddac4-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-474">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="ddac4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-476">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="ddac4-476">The name of the scoping system.</span></span> <span data-ttu-id="ddac4-477">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="ddac4-477">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-478">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="ddac4-478">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-479">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ddac4-479">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-480">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-481">Data o ora dell'Ultima modifica apportata alla proprietà **EnabledState** dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="ddac4-481">The date or time when the **EnabledState** property of the element last changed.</span></span> <span data-ttu-id="ddac4-482">Se lo stato dell'elemento non è stato modificato e questa proprietà è popolata, deve essere impostata su un valore di intervallo 0.</span><span class="sxs-lookup"><span data-stu-id="ddac4-482">If the state of the element has not changed and this property is populated, then it must be set to a 0 interval value.</span></span> <span data-ttu-id="ddac4-483">Se è stata richiesta una modifica di stato, ma è stata rifiutata o non ancora elaborata, la proprietà non deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-483">If a state change was requested, but rejected or not yet processed, the property must not be updated.</span></span> <span data-ttu-id="ddac4-484">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-484">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-485">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="ddac4-485">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-486">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-487">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-488">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="ddac4-488">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="ddac4-489">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-489">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-490">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="ddac4-490">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-491">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-491">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-492">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-493">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ddac4-493">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ddac4-494">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="ddac4-494">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ddac4-495">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="ddac4-495">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddac4-496">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ddac4-496">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ddac4-497">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ddac4-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ddac4-498">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="ddac4-498">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="ddac4-499">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ddac4-499">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>



| <span data-ttu-id="ddac4-500">Valore</span><span class="sxs-lookup"><span data-stu-id="ddac4-500">Value</span></span>                                                                        | <span data-ttu-id="ddac4-501">Significato</span><span class="sxs-lookup"><span data-stu-id="ddac4-501">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ddac4-502"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ddac4-502"><dt>4</dt></span></span> </dl> | <span data-ttu-id="ddac4-503">Senza restrizioni</span><span class="sxs-lookup"><span data-stu-id="ddac4-503">Not Restricted</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddac4-504">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddac4-504">Remarks</span></span>

<span data-ttu-id="ddac4-505">L'accesso alla **classe \_ InternalEthernetPort di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="ddac4-505">Access to the **Msvm\_InternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ddac4-506">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ddac4-506">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ddac4-507">Esempio</span><span class="sxs-lookup"><span data-stu-id="ddac4-507">Examples</span></span>

<span data-ttu-id="ddac4-508">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ddac4-508">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddac4-509">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddac4-509">Requirements</span></span>



| <span data-ttu-id="ddac4-510">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddac4-510">Requirement</span></span> | <span data-ttu-id="ddac4-511">Valore</span><span class="sxs-lookup"><span data-stu-id="ddac4-511">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddac4-512">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddac4-512">Minimum supported client</span></span><br/> | <span data-ttu-id="ddac4-513">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ddac4-513">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ddac4-514">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddac4-514">Minimum supported server</span></span><br/> | <span data-ttu-id="ddac4-515">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ddac4-515">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ddac4-516">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ddac4-516">Namespace</span></span><br/>                | <span data-ttu-id="ddac4-517">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ddac4-517">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ddac4-518">MOF</span><span class="sxs-lookup"><span data-stu-id="ddac4-518">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddac4-519"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddac4-519"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddac4-520">DLL</span><span class="sxs-lookup"><span data-stu-id="ddac4-520">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddac4-521"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ddac4-521"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ddac4-522">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddac4-522">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddac4-523">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ddac4-523">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="ddac4-524">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ddac4-524">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

