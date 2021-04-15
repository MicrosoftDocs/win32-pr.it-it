---
description: Rappresenta una porta Ethernet esterna (scheda di rete).
ms.assetid: 70901587-641D-46F5-8A35-FEA483D336DE
title: Classe Msvm_ExternalEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalEthernetPort
- Msvm_ExternalEthernetPort.SetPowerState
- Msvm_ExternalEthernetPort.EnableDevice
- Msvm_ExternalEthernetPort.OnlineDevice
- Msvm_ExternalEthernetPort.QuiesceDevice
- Msvm_ExternalEthernetPort.SaveProperties
- Msvm_ExternalEthernetPort.RestoreProperties
- Msvm_ExternalEthernetPort.InstanceID
- Msvm_ExternalEthernetPort.Caption
- Msvm_ExternalEthernetPort.Description
- Msvm_ExternalEthernetPort.ElementName
- Msvm_ExternalEthernetPort.InstallDate
- Msvm_ExternalEthernetPort.Name
- Msvm_ExternalEthernetPort.OperationalStatus
- Msvm_ExternalEthernetPort.StatusDescriptions
- Msvm_ExternalEthernetPort.Status
- Msvm_ExternalEthernetPort.HealthState
- Msvm_ExternalEthernetPort.CommunicationStatus
- Msvm_ExternalEthernetPort.DetailedStatus
- Msvm_ExternalEthernetPort.OperatingStatus
- Msvm_ExternalEthernetPort.PrimaryStatus
- Msvm_ExternalEthernetPort.EnabledState
- Msvm_ExternalEthernetPort.OtherEnabledState
- Msvm_ExternalEthernetPort.RequestedState
- Msvm_ExternalEthernetPort.EnabledDefault
- Msvm_ExternalEthernetPort.TimeOfLastStateChange
- Msvm_ExternalEthernetPort.AvailableRequestedStates
- Msvm_ExternalEthernetPort.TransitioningToState
- Msvm_ExternalEthernetPort.SystemCreationClassName
- Msvm_ExternalEthernetPort.SystemName
- Msvm_ExternalEthernetPort.CreationClassName
- Msvm_ExternalEthernetPort.DeviceID
- Msvm_ExternalEthernetPort.PowerManagementSupported
- Msvm_ExternalEthernetPort.PowerManagementCapabilities
- Msvm_ExternalEthernetPort.Availability
- Msvm_ExternalEthernetPort.StatusInfo
- Msvm_ExternalEthernetPort.LastErrorCode
- Msvm_ExternalEthernetPort.ErrorDescription
- Msvm_ExternalEthernetPort.ErrorCleared
- Msvm_ExternalEthernetPort.OtherIdentifyingInfo
- Msvm_ExternalEthernetPort.PowerOnHours
- Msvm_ExternalEthernetPort.TotalPowerOnHours
- Msvm_ExternalEthernetPort.IdentifyingDescriptions
- Msvm_ExternalEthernetPort.AdditionalAvailability
- Msvm_ExternalEthernetPort.MaxQuiesceTime
- Msvm_ExternalEthernetPort.Speed
- Msvm_ExternalEthernetPort.MaxSpeed
- Msvm_ExternalEthernetPort.RequestedSpeed
- Msvm_ExternalEthernetPort.UsageRestriction
- Msvm_ExternalEthernetPort.PortType
- Msvm_ExternalEthernetPort.OtherPortType
- Msvm_ExternalEthernetPort.OtherNetworkPortType
- Msvm_ExternalEthernetPort.PortNumber
- Msvm_ExternalEthernetPort.LinkTechnology
- Msvm_ExternalEthernetPort.OtherLinkTechnology
- Msvm_ExternalEthernetPort.PermanentAddress
- Msvm_ExternalEthernetPort.NetworkAddresses
- Msvm_ExternalEthernetPort.FullDuplex
- Msvm_ExternalEthernetPort.AutoSense
- Msvm_ExternalEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalEthernetPort.MaxDataSize
- Msvm_ExternalEthernetPort.Capabilities
- Msvm_ExternalEthernetPort.CapabilityDescriptions
- Msvm_ExternalEthernetPort.EnabledCapabilities
- Msvm_ExternalEthernetPort.OtherEnabledCapabilities
- Msvm_ExternalEthernetPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 507c2235c1fda5f43ba025172e276b30e2f0aa85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526851"
---
# <a name="msvm_externalethernetport-class"></a><span data-ttu-id="57738-103">\_Classe MSVM ExternalEthernetPort</span><span class="sxs-lookup"><span data-stu-id="57738-103">Msvm\_ExternalEthernetPort class</span></span>

<span data-ttu-id="57738-104">Rappresenta una porta Ethernet esterna (scheda di rete).</span><span class="sxs-lookup"><span data-stu-id="57738-104">Represents an external Ethernet port (network adapter).</span></span> <span data-ttu-id="57738-105">Questi tipi di porte Ethernet consentono alle macchine virtuali di accedere alla rete esterna.</span><span class="sxs-lookup"><span data-stu-id="57738-105">These types of Ethernet ports give virtual machines access to the external network.</span></span>

<span data-ttu-id="57738-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="57738-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57738-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57738-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption = "Ethernet Port";
  string   Description = "Microsoft External Ethernet Port";
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ExternalEthernetPort";
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
  string   AdditionalAvailability[];
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="57738-108">Members</span><span class="sxs-lookup"><span data-stu-id="57738-108">Members</span></span>

<span data-ttu-id="57738-109">La **classe \_ ExternalEthernetPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="57738-109">The **Msvm\_ExternalEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="57738-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="57738-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="57738-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57738-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="57738-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="57738-112">Methods</span></span>

<span data-ttu-id="57738-113">La **classe \_ ExternalEthernetPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="57738-113">The **Msvm\_ExternalEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="57738-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="57738-114">Method</span></span>                                                                     | <span data-ttu-id="57738-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57738-115">Description</span></span>                              |
|:---------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="57738-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="57738-116">**EnableDevice**</span></span>                                                           | <span data-ttu-id="57738-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="57738-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="57738-118">**OnlineDevice**</span></span>                                                           | <span data-ttu-id="57738-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="57738-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="57738-120">**QuiesceDevice**</span></span>                                                          | <span data-ttu-id="57738-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="57738-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="57738-122">**RequestStateChange**</span></span>](msvm-externalethernetport-requeststatechange.md) | <span data-ttu-id="57738-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="57738-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="57738-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="57738-124">**Reset**</span></span>](msvm-externalethernetport-reset.md)                           | <span data-ttu-id="57738-125">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="57738-125">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="57738-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="57738-126">**RestoreProperties**</span></span>                                                      | <span data-ttu-id="57738-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="57738-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="57738-128">**SaveProperties**</span></span>                                                         | <span data-ttu-id="57738-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="57738-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="57738-130">**SetPowerState**</span></span>                                                          | <span data-ttu-id="57738-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="57738-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="57738-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57738-132">Properties</span></span>

<span data-ttu-id="57738-133">La **classe \_ ExternalEthernetPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="57738-133">The **Msvm\_ExternalEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57738-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="57738-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-137">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="57738-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="57738-138">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="57738-138">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="57738-139">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="57738-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-141">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-143">Eventuali ulteriori disponibilità e stato del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="57738-143">Any additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="57738-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-145">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="57738-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57738-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57738-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-148">Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="57738-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="57738-149">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="57738-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-153">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57738-153">The primary availability and status of the device.</span></span> <span data-ttu-id="57738-154">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="57738-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-156">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-158">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="57738-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="57738-159">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="57738-160">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="57738-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="57738-161">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="57738-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="57738-162">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="57738-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="57738-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57738-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="57738-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57738-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="57738-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57738-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="57738-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="57738-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="57738-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="57738-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="57738-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="57738-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="57738-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="57738-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="57738-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="57738-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="57738-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="57738-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="57738-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="57738-173">)</span><span class="sxs-lookup"><span data-stu-id="57738-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="57738-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-177">Matrice che specifica le funzionalità della porta.</span><span class="sxs-lookup"><span data-stu-id="57738-177">An array that specifies the capabilities of the port.</span></span> <span data-ttu-id="57738-178">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="57738-178">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="57738-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="57738-179"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57738-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="57738-180"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57738-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="57738-181"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57738-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="57738-182"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57738-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="57738-183"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57738-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="57738-184"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-185">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="57738-185">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-186">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-188">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per le funzionalità della porta contenute nella matrice di **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="57738-188">An array of free-form strings that provides more detailed explanations for the port features that are contained in the **Capabilities** array.</span></span> <span data-ttu-id="57738-189">Ogni voce di questa matrice è correlata alla voce corrispondente nella matrice delle **funzionalità** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="57738-189">Each entry of this array is related to the corresponding entry in the **Capabilities** array that is located at the same index.</span></span> <span data-ttu-id="57738-190">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="57738-190">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-191">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="57738-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-194">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="57738-194">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="57738-195">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57738-195">A short description of the object.</span></span> <span data-ttu-id="57738-196">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="57738-196">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="57738-197">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="57738-197">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-198">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-200">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="57738-200">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="57738-201">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="57738-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="57738-202">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-203">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="57738-203">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-206">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="57738-206">The scoping system's creation class name.</span></span> <span data-ttu-id="57738-207">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ ExternalEthernetPort".</span><span class="sxs-lookup"><span data-stu-id="57738-207">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ExternalEthernetPort".</span></span>

</dd> <dt>

<span data-ttu-id="57738-208">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="57738-208">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-211">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="57738-211">A description of the object.</span></span> <span data-ttu-id="57738-212">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft External Ethernet Port".</span><span class="sxs-lookup"><span data-stu-id="57738-212">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft External Ethernet Port".</span></span>

</dd> <dt>

<span data-ttu-id="57738-213">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="57738-213">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-214">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-214">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-216">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="57738-216">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="57738-217">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="57738-217">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="57738-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-219">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="57738-219">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-222">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="57738-222">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="57738-223">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="57738-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="57738-224">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="57738-224">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-227">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57738-227">A display name for the object.</span></span> <span data-ttu-id="57738-228">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="57738-228">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-229">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="57738-229">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-230">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-230">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-232">Specifica quali funzionalità sono abilitate dall'elenco di tutte le funzionalità supportate nell'array delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="57738-232">Specifies which capabilities are enabled from the list of all supported capabilities in the **Capabilities** array.</span></span> <span data-ttu-id="57738-233">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="57738-233">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

<dl> <dt>

<span data-ttu-id="57738-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="57738-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57738-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="57738-235"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57738-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="57738-236"><span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>**AlertOnLan** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57738-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="57738-237"><span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>**WakeOnLan** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57738-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="57738-238"><span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>**FailOver** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57738-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**Loadbalancing** (5)</span><span class="sxs-lookup"><span data-stu-id="57738-239"><span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>**LoadBalancing** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-240">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="57738-240">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-241">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-241">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-243">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="57738-243">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="57738-244">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="57738-244">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="57738-245">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="57738-245">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-246">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-246">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-248">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="57738-248">The enabled and disabled states of an element.</span></span> <span data-ttu-id="57738-249">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="57738-249">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="57738-250">Ad esempio, l'arresto (4) e l'avvio di (10) sono stati temporanei tra l'abilitazione e la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="57738-250">For example, shutting down (4) and starting (10) are transient states between enabled and disabled.</span></span> <span data-ttu-id="57738-251">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-251">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="57738-252">Valore</span><span class="sxs-lookup"><span data-stu-id="57738-252">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="57738-253">Significato</span><span class="sxs-lookup"><span data-stu-id="57738-253">Meaning</span></span>                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="57738-254"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57738-254"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 |                                                                                                                                                                                                             |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="57738-255"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="57738-255"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                             |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="57738-256"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="57738-256"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="57738-257">L'elemento è o potrebbe eseguire comandi, elaborerà tutti i comandi in coda e accoda le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="57738-257">The element is or could be executing commands, will process any queued commands, and queues new requests.</span></span><br/>                                                                                        |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="57738-258"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="57738-258"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="57738-259">L'elemento non esegue i comandi e rilascia tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="57738-259">The element will not execute commands and will drop any new requests.</span></span><br/>                                                                                                                            |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="57738-260"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="57738-260"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="57738-261">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="57738-261">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                      |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="57738-262"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="57738-262"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="57738-263">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="57738-263">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                          |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="57738-264"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="57738-264"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="57738-265">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="57738-265">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                     |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="57738-266"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="57738-266"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="57738-267">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="57738-267">The element is in a test state.</span></span><br/>                                                                                                                                                                  |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="57738-268"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="57738-268"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="57738-269">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="57738-269">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                    |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="57738-270"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="57738-270"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="57738-271">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="57738-271">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="57738-272">Il comportamento dell'elemento è simile allo stato Enabled, ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="57738-272">The behavior of the element is similar to the Enabled state, but it processes only a restricted set of commands.</span></span> <span data-ttu-id="57738-273">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="57738-273">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="57738-274"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="57738-274"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="57738-275">L'elemento sta per passare a uno stato abilitato.</span><span class="sxs-lookup"><span data-stu-id="57738-275">The element is in the process of going to an Enabled state.</span></span> <span data-ttu-id="57738-276">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="57738-276">New requests are queued.</span></span><br/>                                                                                                             |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="57738-277"><dt>**DMTF riservato**</dt> <dt>11 32767</dt></span><span class="sxs-lookup"><span data-stu-id="57738-277"><dt>**DMTF Reserved**</dt> <dt>11 32767</dt></span></span> </dl>                  | <span data-ttu-id="57738-278">Riservato.</span><span class="sxs-lookup"><span data-stu-id="57738-278">Reserved.</span></span><br/>                                                                                                                                                                                        |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <span data-ttu-id="57738-279"><dt>**Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="57738-279"><dt>**Vendor Reserved**</dt> <dt>32768 65535</dt></span></span> </dl>       | <span data-ttu-id="57738-280">Riservato.</span><span class="sxs-lookup"><span data-stu-id="57738-280">Reserved.</span></span><br/>                                                                                                                                                                                        |



 

</dd> <dt>

<span data-ttu-id="57738-281">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="57738-281">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-282">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57738-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57738-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-284">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="57738-284">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="57738-285">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-285">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-286">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="57738-286">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-287">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-288">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-289">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="57738-289">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="57738-290">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-290">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-291">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="57738-291">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-292">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57738-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57738-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-294">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="57738-294">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="57738-295">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-295">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-296">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="57738-296">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-297">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-297">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-299">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="57738-299">The current health of the element.</span></span> <span data-ttu-id="57738-300">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="57738-300">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="57738-301">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="57738-301">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="57738-302">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="57738-302">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="57738-303">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="57738-303">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-304">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-304">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-306">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="57738-306">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="57738-307">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-307">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="57738-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-309">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57738-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57738-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-311">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57738-311">The date and time when the object was installed.</span></span> <span data-ttu-id="57738-312">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="57738-312">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="57738-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-313">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-314">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="57738-314">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-315">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-317">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="57738-317">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="57738-318">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="57738-318">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="57738-319">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="57738-319">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-320">**Con associazione**</span><span class="sxs-lookup"><span data-stu-id="57738-320">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-321">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57738-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57738-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-323">Se questa proprietà è impostata su **true**, questa porta Ethernet può essere connessa ai commutatori e pertanto può fornire connettività a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="57738-323">If this property is **True**, then this Ethernet port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="57738-324">Se questa proprietà è **false**, questa porta Ethernet non viene usata dall'architettura di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="57738-324">If this property is **False**, then this Ethernet port is not being used by the virtual machine networking architecture.</span></span>

</dd> <dt>

<span data-ttu-id="57738-325">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="57738-325">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-326">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57738-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57738-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-328">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="57738-328">The last error code reported by the logical device.</span></span> <span data-ttu-id="57738-329">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-329">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-330">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="57738-330">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-333">Specifica il tipo di tecnologia di collegamento per la porta.</span><span class="sxs-lookup"><span data-stu-id="57738-333">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="57738-334">Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="57738-334">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="57738-335">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-335">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="57738-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="57738-336"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57738-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="57738-337"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57738-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="57738-338"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57738-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="57738-339"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57738-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="57738-340"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="57738-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="57738-341"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="57738-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="57738-342"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="57738-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="57738-343"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="57738-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="57738-344"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="57738-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (9)</span><span class="sxs-lookup"><span data-stu-id="57738-345"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="57738-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="57738-346"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="57738-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**LAN wireless** (11)</span><span class="sxs-lookup"><span data-stu-id="57738-347"><span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>**Wireless LAN** (11)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-348">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="57738-348">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-349">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57738-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57738-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-351">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="57738-351">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="57738-352">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)ed è sempre impostata su 1500.</span><span class="sxs-lookup"><span data-stu-id="57738-352">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is always set to 1500.</span></span>

</dd> <dt>

<span data-ttu-id="57738-353">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="57738-353">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-354">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-356">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="57738-356">This property has been deprecated.</span></span> <span data-ttu-id="57738-357">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-357">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-358">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="57738-358">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-359">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-359">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-361">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="57738-361">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="57738-362">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="57738-362">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="57738-363">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-363">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57738-364">**Nome**</span><span class="sxs-lookup"><span data-stu-id="57738-364">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-367">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="57738-367">The label by which the object is known.</span></span> <span data-ttu-id="57738-368">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-369">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="57738-369">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-370">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-370">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-372">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="57738-372">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="57738-373">Matrice di stringhe che contengono gli indirizzi MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="57738-373">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="57738-374">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-374">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-375">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="57738-375">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-378">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="57738-378">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="57738-379">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="57738-379">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="57738-380">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-380">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-381">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="57738-381">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-382">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-382">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-384">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57738-384">The current statuses of the object.</span></span> <span data-ttu-id="57738-385">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="57738-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="57738-386">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="57738-386">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-387">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-388">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-389">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per qualsiasi funzionalità abilitata specificata come 1 (other). Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="57738-389">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as 1 (Other.) This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-390">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="57738-390">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-391">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-392">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-393">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="57738-393">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="57738-394">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="57738-394">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="57738-395">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57738-396">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="57738-396">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-397">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-398">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-399">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="57738-399">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="57738-400">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-400">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-401">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="57738-401">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-402">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-403">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-403">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-404">Valore stringa che descrive **LinkTechnology** quando è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="57738-404">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="57738-405">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-405">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-406">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="57738-406">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-407">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-409">L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="57738-409">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="57738-410">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-410">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-411">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="57738-411">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-412">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-413">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-414">Tipo di modulo, quando **portType** è impostato su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="57738-414">The type of module, when **PortType** is set to 1 ("Other").</span></span> <span data-ttu-id="57738-415">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-415">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57738-416">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="57738-416">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-417">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-418">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-419">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="57738-419">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="57738-420">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="57738-420">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="57738-421">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="57738-421">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="57738-422">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="57738-422">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="57738-423">Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="57738-423">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="57738-424">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-424">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-425">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="57738-425">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-426">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-426">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-427">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-427">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-428">Il numero della porta.</span><span class="sxs-lookup"><span data-stu-id="57738-428">The port number.</span></span> <span data-ttu-id="57738-429">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-429">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-430">**PortType**</span><span class="sxs-lookup"><span data-stu-id="57738-430">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-431">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-431">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-433">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="57738-433">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="57738-434">Quando è impostato su 1 ("altro"), la proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="57738-434">When set to 1 ("Other"), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="57738-435">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="57738-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="57738-436"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57738-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="57738-437"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="57738-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="57738-438"><span id="__50_Copper_10BaseT"></span><span id="__50_copper_10baset"></span><span id="__50_COPPER_10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="57738-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="57738-439"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="57738-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="57738-440"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="57738-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="57738-441"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="57738-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="57738-442"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="57738-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="57738-443"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="57738-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="57738-444"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="57738-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="57738-445"><span id="__100_Fibre_100Base-FX"></span><span id="__100_fibre_100base-fx"></span><span id="__100_FIBRE_100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="57738-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="57738-446"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="57738-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="57738-447"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="57738-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="57738-448"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="57738-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="57738-449"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="57738-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="57738-450"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="57738-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="57738-451"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="57738-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="57738-452"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="57738-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="57738-453"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="57738-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="57738-454"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="57738-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="57738-455"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="57738-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="57738-456"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="57738-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (16000 65535)</span><span class="sxs-lookup"><span data-stu-id="57738-457"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-458">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="57738-458">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-459">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-459">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-460">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-460">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-461">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57738-461">The power management capabilities of the device.</span></span> <span data-ttu-id="57738-462">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-462">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-463">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="57738-463">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-464">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="57738-464">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="57738-465">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-466">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="57738-466">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="57738-467">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-467">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-468">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="57738-468">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-469">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-469">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-471">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="57738-471">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="57738-472">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-472">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-473">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="57738-473">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-474">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-474">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-475">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-476">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="57738-476">Provides high level status information.</span></span> <span data-ttu-id="57738-477">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="57738-477">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="57738-478">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="57738-478">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="57738-479">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-479">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="57738-480">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="57738-480">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-481">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-482">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-483">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="57738-483">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="57738-484">Larghezza di banda richiesta per la porta in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="57738-484">The requested bandwidth of the port in bits per second.</span></span> <span data-ttu-id="57738-485">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="57738-485">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="57738-486">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-486">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57738-487">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="57738-487">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-488">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-488">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-490">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="57738-490">The last requested or desired state for the element.</span></span> <span data-ttu-id="57738-491">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="57738-491">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="57738-492">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="57738-492">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-493">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-493">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-494">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-495">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="57738-495">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="57738-496">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="57738-496">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="57738-497">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-497">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="57738-498">**Status**</span><span class="sxs-lookup"><span data-stu-id="57738-498">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-499">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-500">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-501">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="57738-501">The current status of the object.</span></span> <span data-ttu-id="57738-502">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="57738-502">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="57738-503">OK</span><span class="sxs-lookup"><span data-stu-id="57738-503">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="57738-504"><span id="OK"></span><span id="ok"></span>**Ok**</span><span class="sxs-lookup"><span data-stu-id="57738-504"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="57738-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore**</span><span class="sxs-lookup"><span data-stu-id="57738-505"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="57738-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradato**</span><span class="sxs-lookup"><span data-stu-id="57738-506"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="57738-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="57738-507"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="57738-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Errore di prede**</span><span class="sxs-lookup"><span data-stu-id="57738-508"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="57738-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio**</span><span class="sxs-lookup"><span data-stu-id="57738-509"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="57738-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto**</span><span class="sxs-lookup"><span data-stu-id="57738-510"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="57738-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio**</span><span class="sxs-lookup"><span data-stu-id="57738-511"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="57738-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato**</span><span class="sxs-lookup"><span data-stu-id="57738-512"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="57738-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**Non ripristino**</span><span class="sxs-lookup"><span data-stu-id="57738-513"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="57738-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto**</span><span class="sxs-lookup"><span data-stu-id="57738-514"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="57738-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Comunicazione persa**</span><span class="sxs-lookup"><span data-stu-id="57738-515"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="57738-516">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="57738-516">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-517">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="57738-517">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="57738-518">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-519">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="57738-519">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="57738-520">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="57738-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="57738-521">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="57738-521">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-522">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-522">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-523">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-523">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-524">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="57738-524">The current state of the logical device.</span></span> <span data-ttu-id="57738-525">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-525">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-526">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="57738-526">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-527">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-527">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-528">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57738-529">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="57738-529">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="57738-530">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="57738-530">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="57738-531">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="57738-531">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="57738-532">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="57738-532">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-533">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-533">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-534">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-535">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="57738-535">The scoping system's creation class name.</span></span> <span data-ttu-id="57738-536">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="57738-536">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="57738-537">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="57738-537">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-538">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="57738-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57738-539">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-539">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-540">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="57738-540">The name of the scoping system.</span></span> <span data-ttu-id="57738-541">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="57738-541">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="57738-542">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="57738-542">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-543">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57738-543">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57738-544">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-544">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-545">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="57738-545">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="57738-546">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="57738-546">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="57738-547">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="57738-547">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-548">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57738-548">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57738-549">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-550">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="57738-550">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="57738-551">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-551">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-552">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="57738-552">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-553">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-553">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-554">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-554">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-555">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="57738-555">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="57738-556">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="57738-556">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57738-557">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="57738-557">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57738-558">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57738-558">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57738-559">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="57738-559">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57738-560">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="57738-560">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="57738-561">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="57738-561">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="57738-562">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su "senza restrizioni".</span><span class="sxs-lookup"><span data-stu-id="57738-562">If there is no restriction on the use of the port, then the value should be set to "Not restricted".</span></span> <span data-ttu-id="57738-563">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="57738-563">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="57738-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="57738-564"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="57738-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="57738-565"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="57738-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="57738-566"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="57738-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="57738-567"><span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>**Not restricted** (4)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57738-568">Commenti</span><span class="sxs-lookup"><span data-stu-id="57738-568">Remarks</span></span>

<span data-ttu-id="57738-569">L'accesso alla **classe \_ ExternalEthernetPort di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="57738-569">Access to the **Msvm\_ExternalEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="57738-570">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="57738-570">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="57738-571">Esempio</span><span class="sxs-lookup"><span data-stu-id="57738-571">Examples</span></span>

<span data-ttu-id="57738-572">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="57738-572">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57738-573">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57738-573">Requirements</span></span>



| <span data-ttu-id="57738-574">Requisito</span><span class="sxs-lookup"><span data-stu-id="57738-574">Requirement</span></span> | <span data-ttu-id="57738-575">Valore</span><span class="sxs-lookup"><span data-stu-id="57738-575">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57738-576">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57738-576">Minimum supported client</span></span><br/> | <span data-ttu-id="57738-577">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57738-577">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57738-578">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57738-578">Minimum supported server</span></span><br/> | <span data-ttu-id="57738-579">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57738-579">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57738-580">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="57738-580">Namespace</span></span><br/>                | <span data-ttu-id="57738-581">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="57738-581">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57738-582">MOF</span><span class="sxs-lookup"><span data-stu-id="57738-582">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57738-583"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57738-583"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57738-584">DLL</span><span class="sxs-lookup"><span data-stu-id="57738-584">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57738-585"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57738-585"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57738-586">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57738-586">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57738-587">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="57738-587">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="57738-588">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="57738-588">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

