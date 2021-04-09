---
description: Rappresenta una scheda Ethernet sintetica.
ms.assetid: B5CB86A9-015B-42E8-ADF4-2F61970D8437
title: Classe Msvm_SyntheticEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort
- Msvm_SyntheticEthernetPort.SetPowerState
- Msvm_SyntheticEthernetPort.EnableDevice
- Msvm_SyntheticEthernetPort.OnlineDevice
- Msvm_SyntheticEthernetPort.QuiesceDevice
- Msvm_SyntheticEthernetPort.SaveProperties
- Msvm_SyntheticEthernetPort.RestoreProperties
- Msvm_SyntheticEthernetPort.InstanceID
- Msvm_SyntheticEthernetPort.Caption
- Msvm_SyntheticEthernetPort.Description
- Msvm_SyntheticEthernetPort.ElementName
- Msvm_SyntheticEthernetPort.InstallDate
- Msvm_SyntheticEthernetPort.Name
- Msvm_SyntheticEthernetPort.OperationalStatus
- Msvm_SyntheticEthernetPort.StatusDescriptions
- Msvm_SyntheticEthernetPort.Status
- Msvm_SyntheticEthernetPort.HealthState
- Msvm_SyntheticEthernetPort.CommunicationStatus
- Msvm_SyntheticEthernetPort.DetailedStatus
- Msvm_SyntheticEthernetPort.OperatingStatus
- Msvm_SyntheticEthernetPort.PrimaryStatus
- Msvm_SyntheticEthernetPort.EnabledState
- Msvm_SyntheticEthernetPort.OtherEnabledState
- Msvm_SyntheticEthernetPort.RequestedState
- Msvm_SyntheticEthernetPort.EnabledDefault
- Msvm_SyntheticEthernetPort.TimeOfLastStateChange
- Msvm_SyntheticEthernetPort.AvailableRequestedStates
- Msvm_SyntheticEthernetPort.TransitioningToState
- Msvm_SyntheticEthernetPort.SystemCreationClassName
- Msvm_SyntheticEthernetPort.SystemName
- Msvm_SyntheticEthernetPort.CreationClassName
- Msvm_SyntheticEthernetPort.DeviceID
- Msvm_SyntheticEthernetPort.PowerManagementSupported
- Msvm_SyntheticEthernetPort.PowerManagementCapabilities
- Msvm_SyntheticEthernetPort.Availability
- Msvm_SyntheticEthernetPort.StatusInfo
- Msvm_SyntheticEthernetPort.LastErrorCode
- Msvm_SyntheticEthernetPort.ErrorDescription
- Msvm_SyntheticEthernetPort.ErrorCleared
- Msvm_SyntheticEthernetPort.OtherIdentifyingInfo
- Msvm_SyntheticEthernetPort.PowerOnHours
- Msvm_SyntheticEthernetPort.TotalPowerOnHours
- Msvm_SyntheticEthernetPort.IdentifyingDescriptions
- Msvm_SyntheticEthernetPort.AdditionalAvailability
- Msvm_SyntheticEthernetPort.MaxQuiesceTime
- Msvm_SyntheticEthernetPort.Speed
- Msvm_SyntheticEthernetPort.MaxSpeed
- Msvm_SyntheticEthernetPort.RequestedSpeed
- Msvm_SyntheticEthernetPort.UsageRestriction
- Msvm_SyntheticEthernetPort.PortType
- Msvm_SyntheticEthernetPort.OtherPortType
- Msvm_SyntheticEthernetPort.OtherNetworkPortType
- Msvm_SyntheticEthernetPort.PortNumber
- Msvm_SyntheticEthernetPort.LinkTechnology
- Msvm_SyntheticEthernetPort.OtherLinkTechnology
- Msvm_SyntheticEthernetPort.PermanentAddress
- Msvm_SyntheticEthernetPort.NetworkAddresses
- Msvm_SyntheticEthernetPort.FullDuplex
- Msvm_SyntheticEthernetPort.AutoSense
- Msvm_SyntheticEthernetPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticEthernetPort.MaxDataSize
- Msvm_SyntheticEthernetPort.Capabilities
- Msvm_SyntheticEthernetPort.CapabilityDescriptions
- Msvm_SyntheticEthernetPort.EnabledCapabilities
- Msvm_SyntheticEthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c8e2a8c2207e410878a4f5c498ea71a1ce67cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880518"
---
# <a name="msvm_syntheticethernetport-class"></a><span data-ttu-id="c4442-103">\_Classe MSVM SyntheticEthernetPort</span><span class="sxs-lookup"><span data-stu-id="c4442-103">Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="c4442-104">Rappresenta una scheda Ethernet sintetica.</span><span class="sxs-lookup"><span data-stu-id="c4442-104">Represents a synthetic Ethernet adapter.</span></span> <span data-ttu-id="c4442-105">Questa scheda è la scheda di rete preferita a causa delle prestazioni e delle modifiche apportate all'applicazione, mentre è in uso (configurazione a caldo).</span><span class="sxs-lookup"><span data-stu-id="c4442-105">This adapter is the preferred network adapter because of its performance and because changes to it can take effect right away, while it is in use (hot configurability).</span></span>

<span data-ttu-id="c4442-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c4442-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4442-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4442-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticEthernetPort : CIM_EthernetPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
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
  uint16   AdditionalAvailability[] = 6;
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
};
```

## <a name="members"></a><span data-ttu-id="c4442-108">Members</span><span class="sxs-lookup"><span data-stu-id="c4442-108">Members</span></span>

<span data-ttu-id="c4442-109">La **classe \_ SyntheticEthernetPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c4442-109">The **Msvm\_SyntheticEthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="c4442-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4442-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c4442-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4442-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c4442-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4442-112">Methods</span></span>

<span data-ttu-id="c4442-113">La **classe \_ SyntheticEthernetPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c4442-113">The **Msvm\_SyntheticEthernetPort** class has these methods.</span></span>



| <span data-ttu-id="c4442-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="c4442-114">Method</span></span>                                                                      | <span data-ttu-id="c4442-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4442-115">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="c4442-116">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="c4442-116">**EnableDevice**</span></span>                                                            | <span data-ttu-id="c4442-117">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-117">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4442-118">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="c4442-118">**OnlineDevice**</span></span>                                                            | <span data-ttu-id="c4442-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4442-120">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="c4442-120">**QuiesceDevice**</span></span>                                                           | <span data-ttu-id="c4442-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-121">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="c4442-122">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c4442-122">**RequestStateChange**</span></span>](msvm-syntheticethernetport-requeststatechange.md) | <span data-ttu-id="c4442-123">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="c4442-123">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="c4442-124">**Reset**</span><span class="sxs-lookup"><span data-stu-id="c4442-124">**Reset**</span></span>](msvm-syntheticethernetport-reset.md)                           | <span data-ttu-id="c4442-125">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4442-125">Resets the device.</span></span><br/>            |
| <span data-ttu-id="c4442-126">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="c4442-126">**RestoreProperties**</span></span>                                                       | <span data-ttu-id="c4442-127">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-127">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4442-128">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="c4442-128">**SaveProperties**</span></span>                                                          | <span data-ttu-id="c4442-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="c4442-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c4442-130">**SetPowerState**</span></span>                                                           | <span data-ttu-id="c4442-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="c4442-131">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c4442-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c4442-132">Properties</span></span>

<span data-ttu-id="c4442-133">La **classe \_ SyntheticEthernetPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4442-133">The **Msvm\_SyntheticEthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4442-134">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c4442-134">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-137">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="c4442-137">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c4442-138">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata.</span><span class="sxs-lookup"><span data-stu-id="c4442-138">The active or negotiated maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="c4442-139">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-139">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-140">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="c4442-140">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-141">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-143">Disponibilità e stato aggiuntive del dispositivo, oltre a quello specificato nella proprietà **Availability** .</span><span class="sxs-lookup"><span data-stu-id="c4442-143">Additional availability and status of the device, beyond that specified in the **Availability** property.</span></span> <span data-ttu-id="c4442-144">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="c4442-144">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-145">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="c4442-145">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-146">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4442-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-148">Indica se la porta di rete è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="c4442-148">Indicates whether the network port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="c4442-149">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-149">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-150">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="c4442-150">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-153">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4442-153">The primary availability and status of the device.</span></span> <span data-ttu-id="c4442-154">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c4442-154">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c4442-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-156">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-158">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="c4442-158">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="c4442-159">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-159">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="c4442-160">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="c4442-160">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="c4442-161">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="c4442-161">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="c4442-162">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-162">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="c4442-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="c4442-163"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="c4442-164"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="c4442-165"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="c4442-166"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="c4442-167"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="c4442-168"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="c4442-169"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="c4442-170"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="c4442-171"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c4442-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="c4442-172"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c4442-173">)</span><span class="sxs-lookup"><span data-stu-id="c4442-173">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4442-174">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c4442-174">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-175">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-177">Funzionalità della porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c4442-177">The capabilities of the Ethernet port.</span></span> <span data-ttu-id="c4442-178">Ad esempio, il dispositivo potrebbe supportare AlertOnLan, WakeOnLan, bilanciamento del carico o FailOver.</span><span class="sxs-lookup"><span data-stu-id="c4442-178">For example, the device might support AlertOnLan, WakeOnLan, Load Balancing, or FailOver.</span></span> <span data-ttu-id="c4442-179">Se sono elencate le funzionalità di failover o bilanciamento del carico, è necessario definire anche un SpareGroup (failover) o ExtraCapacityGroup (bilanciamento del carico) per descrivere completamente la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c4442-179">If failover or load balancing capabilities are listed, a SpareGroup (failover) or ExtraCapacityGroup (load balancing) should also be defined to completely describe the capability.</span></span> <span data-ttu-id="c4442-180">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-180">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-181">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c4442-181">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-182">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-182">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-184">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità di EthernetPort indicate nella matrice di proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c4442-184">An array of free-form strings that provides more detailed explanations for any of the EthernetPort features that are indicated in the **Capabilities** property array.</span></span> <span data-ttu-id="c4442-185">Si noti che ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **capabilities** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="c4442-185">Note, each entry of this array is related to the entry in the **Capabilities** property array that is located at the same index.</span></span> <span data-ttu-id="c4442-186">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-186">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-187">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="c4442-187">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-190">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c4442-190">A short description of the object.</span></span> <span data-ttu-id="c4442-191">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-191">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-192">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c4442-192">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-193">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-195">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="c4442-195">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c4442-196">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="c4442-196">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4442-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-198">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4442-198">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-201">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c4442-201">The name of the class or the subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="c4442-202">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c4442-202">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-203">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c4442-203">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-204">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-206">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="c4442-206">A description of the object.</span></span> <span data-ttu-id="c4442-207">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-207">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-208">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c4442-208">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-209">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-209">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-211">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="c4442-211">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c4442-212">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="c4442-212">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4442-213">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-213">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-214">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c4442-214">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-215">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-217">Un indirizzo o altre informazioni di identificazione utilizzate per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c4442-217">An address or other identifying information used to uniquely name the logical device.</span></span> <span data-ttu-id="c4442-218">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c4442-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-219">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c4442-219">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-222">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c4442-222">A display name for the object.</span></span> <span data-ttu-id="c4442-223">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-223">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-224">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c4442-224">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-225">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-225">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-227">Funzionalità abilitate dall'elenco di tutti quelli supportati, definiti nella matrice di proprietà **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c4442-227">The capabilities that are enabled from the list of all supported ones, which are defined in the **Capabilities** property array.</span></span> <span data-ttu-id="c4442-228">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-228">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-229">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c4442-229">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-230">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-232">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-232">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c4442-233">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-233">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c4442-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-235">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-237">Stati abilitati e disabilitati di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-237">The enabled and disabled states of this element.</span></span> <span data-ttu-id="c4442-238">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-238">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-239">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="c4442-239">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-240">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4442-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-242">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-243">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c4442-243">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-244">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-246">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-246">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-247">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="c4442-247">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-248">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4442-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-250">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="c4442-250">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="c4442-251">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-251">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-252">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c4442-252">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-255">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-255">The current health of the element.</span></span> <span data-ttu-id="c4442-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-257">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c4442-257">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-258">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-258">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-260">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="c4442-260">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="c4442-261">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-261">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-262">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c4442-262">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-263">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4442-263">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-265">Data di aggiunta della porta Ethernet alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c4442-265">The date the Ethernet port was added to the virtual machine.</span></span> <span data-ttu-id="c4442-266">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-266">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-267">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c4442-267">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-268">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-269">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-270">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="c4442-270">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c4442-271">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="c4442-271">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c4442-272">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-272">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-273">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="c4442-273">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-274">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4442-274">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-275">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-276">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-276">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-277">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c4442-277">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-278">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-278">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-280">Enumerazione dei tipi di collegamenti.</span><span class="sxs-lookup"><span data-stu-id="c4442-280">An enumeration of the types of links.</span></span> <span data-ttu-id="c4442-281">Quando è impostata su 1 (other), la proprietà correlata **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="c4442-281">When set to 1 (Other), the related property **OtherLinkTechnology** contains a string description of the type of link.</span></span> <span data-ttu-id="c4442-282">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-282">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="c4442-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="c4442-283"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c4442-284">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="c4442-284">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-285">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4442-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-286">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-286">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-287">Dimensione massima del campo INFO (non MAC) che verrà ricevuto o trasmesso.</span><span class="sxs-lookup"><span data-stu-id="c4442-287">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span> <span data-ttu-id="c4442-288">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="c4442-288">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-289">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="c4442-289">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-290">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-290">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-291">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-292">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-292">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-293">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="c4442-293">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-294">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-294">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-296">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="c4442-296">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c4442-297">Larghezza di banda massima della porta in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c4442-297">The maximum bandwidth of the port in bits per second.</span></span> <span data-ttu-id="c4442-298">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-298">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-299">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c4442-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-302">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="c4442-302">A display name for the object.</span></span> <span data-ttu-id="c4442-303">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-303">This property is inherited from [**CIM\_ManagedSystemElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-304">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="c4442-304">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-305">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-307">Indirizzi MAC Ethernet/802.3 formattati come dodici cifre esadecimali, ad esempio "010203040506", con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico (il bit dell'indirizzo del gruppo viene trovato nel bit di ordine inferiore del primo carattere della stringa).</span><span class="sxs-lookup"><span data-stu-id="c4442-307">Ethernet/802.3 MAC addresses formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order (the Group address bit is found in the low order bit of the first character of the string).</span></span> <span data-ttu-id="c4442-308">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-308">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-309">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c4442-309">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-310">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-312">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="c4442-312">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c4442-313">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="c4442-313">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4442-314">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-314">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-315">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c4442-315">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-316">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-316">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-317">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-318">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-318">The current status of the element.</span></span> <span data-ttu-id="c4442-319">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="c4442-319">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-320">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c4442-320">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-321">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-321">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-323">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità abilitate specificate come "altro".</span><span class="sxs-lookup"><span data-stu-id="c4442-323">An array of free-form strings that provides more detailed explanations for any of the enabled capabilities that are specified as "Other".</span></span> <span data-ttu-id="c4442-324">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-324">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-325">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c4442-325">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-326">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-328">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c4442-328">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="c4442-329">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-330">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="c4442-330">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-331">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-331">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-333">Tutti i dati, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="c4442-333">Any data, in addition to device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="c4442-334">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-334">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-335">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="c4442-335">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-338">Valore stringa che descrive **LinkTechnology** quando è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c4442-338">A string value that describes **LinkTechnology** when it is set to 1 (Other).</span></span> <span data-ttu-id="c4442-339">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-339">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-340">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="c4442-340">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-343">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) e viene impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="c4442-343">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport) and is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-344">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="c4442-344">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-345">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-347">Tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="c4442-347">The type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="c4442-348">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-348">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-349">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="c4442-349">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-352">Indirizzo di rete hardcoded nella porta.</span><span class="sxs-lookup"><span data-stu-id="c4442-352">The network address that is hardcoded into the port.</span></span> <span data-ttu-id="c4442-353">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="c4442-353">This hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="c4442-354">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="c4442-354">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="c4442-355">Se non esiste alcun indirizzo hardcoded per la scheda di rete, la proprietà **PermanentAddress** deve essere lasciata vuota.</span><span class="sxs-lookup"><span data-stu-id="c4442-355">The **PermanentAddress** property should be left blank if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="c4442-356">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-356">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-357">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="c4442-357">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-358">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-360">Le porte di rete spesso sono numerate in relazione a un modulo logico o a un elemento di rete.</span><span class="sxs-lookup"><span data-stu-id="c4442-360">Network ports are often numbered relative to either a logical module or a network element.</span></span> <span data-ttu-id="c4442-361">Questo valore è 1 per le NIC emulate, 0 per tutti gli altri.</span><span class="sxs-lookup"><span data-stu-id="c4442-361">This value is 1 for emulated NICs, 0 for all others.</span></span> <span data-ttu-id="c4442-362">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-362">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-363">**PortType**</span><span class="sxs-lookup"><span data-stu-id="c4442-363">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-364">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-366">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="c4442-366">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="c4442-367">Quando è impostata su 1 (other), la proprietà correlata **OtherPortType** contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="c4442-367">When set to 1 (Other), the related property **OtherPortType** contains a string description of the type of port.</span></span> <span data-ttu-id="c4442-368">Questa proprietà viene ereditata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span><span class="sxs-lookup"><span data-stu-id="c4442-368">This property is inherited from [**CIM\_EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-369">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c4442-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-372">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-372">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-373">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="c4442-373">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-374">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="c4442-374">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-375">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-376">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-376">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-377">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c4442-377">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-378">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-378">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-379">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-380">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-380">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-381">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c4442-381">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-382">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-383">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-384">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="c4442-384">Provides high level status information.</span></span> <span data-ttu-id="c4442-385">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="c4442-385">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="c4442-386">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="c4442-386">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c4442-387">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-388">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="c4442-388">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-389">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-389">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-391">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="c4442-391">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c4442-392">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c4442-392">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c4442-393">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="c4442-393">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="c4442-394">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-394">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-395">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c4442-395">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-396">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-398">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="c4442-398">The last requested or desired state for the management service.</span></span> <span data-ttu-id="c4442-399">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-399">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-400">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="c4442-400">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-401">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-401">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-403">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="c4442-403">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="c4442-404">Larghezza di banda corrente della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c4442-404">The current bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="c4442-405">Per le porte che variano a seconda della larghezza di banda o per quelle in cui non è possibile effettuare una stima accurata, questa proprietà deve contenere la larghezza di banda nominale.</span><span class="sxs-lookup"><span data-stu-id="c4442-405">For ports that vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span> <span data-ttu-id="c4442-406">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-406">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-407">**Status**</span><span class="sxs-lookup"><span data-stu-id="c4442-407">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-408">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-409">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-410">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-410">The current status of the element.</span></span> <span data-ttu-id="c4442-411">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-411">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-412">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c4442-412">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-413">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="c4442-413">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c4442-414">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-415">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="c4442-415">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c4442-416">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="c4442-416">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-417">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c4442-417">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-418">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-419">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-420">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-421">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="c4442-421">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-422">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-422">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4442-424">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="c4442-424">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="c4442-425">Unità di trasmissione massima (MTU) che può essere supportata.</span><span class="sxs-lookup"><span data-stu-id="c4442-425">The maximum transmission unit (MTU) that can be supported.</span></span> <span data-ttu-id="c4442-426">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="c4442-426">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-427">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c4442-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-428">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-430">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="c4442-430">The creation class name of the scoping system.</span></span> <span data-ttu-id="c4442-431">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c4442-431">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-432">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c4442-432">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-433">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="c4442-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-435">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="c4442-435">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="c4442-436">Questa proprietà conterrà l'ID della macchina virtuale in formato **GUID** .</span><span class="sxs-lookup"><span data-stu-id="c4442-436">This property will contain the virtual machine ID in **GUID** form.</span></span> <span data-ttu-id="c4442-437">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="c4442-437">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-438">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c4442-438">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-439">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c4442-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-441">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="c4442-441">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c4442-442">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-442">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-443">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="c4442-443">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-444">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c4442-444">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-446">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="c4442-446">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="c4442-447">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c4442-447">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-448">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-448">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-450">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c4442-450">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c4442-451">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-451">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c4442-452">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="c4442-452">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4442-453">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c4442-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c4442-454">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c4442-454">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4442-455">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="c4442-455">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="c4442-456">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="c4442-456">If there is no restriction on the use of the port, then the value should be set to 4 (Not Restricted).</span></span> <span data-ttu-id="c4442-457">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4442-457">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4442-458">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4442-458">Remarks</span></span>

<span data-ttu-id="c4442-459">L'accesso alla **classe \_ SyntheticEthernetPort di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="c4442-459">Access to the **Msvm\_SyntheticEthernetPort** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c4442-460">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c4442-460">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c4442-461">Esempio</span><span class="sxs-lookup"><span data-stu-id="c4442-461">Examples</span></span>

<span data-ttu-id="c4442-462">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c4442-462">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4442-463">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4442-463">Requirements</span></span>



| <span data-ttu-id="c4442-464">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4442-464">Requirement</span></span> | <span data-ttu-id="c4442-465">Valore</span><span class="sxs-lookup"><span data-stu-id="c4442-465">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4442-466">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4442-466">Minimum supported client</span></span><br/> | <span data-ttu-id="c4442-467">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c4442-467">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4442-468">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4442-468">Minimum supported server</span></span><br/> | <span data-ttu-id="c4442-469">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c4442-469">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4442-470">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c4442-470">Namespace</span></span><br/>                | <span data-ttu-id="c4442-471">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c4442-471">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4442-472">MOF</span><span class="sxs-lookup"><span data-stu-id="c4442-472">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4442-473"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4442-473"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4442-474">DLL</span><span class="sxs-lookup"><span data-stu-id="c4442-474">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4442-475"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4442-475"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4442-476">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4442-476">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4442-477">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="c4442-477">**CIM\_EthernetPort**</span></span>](cim-ethernetport.md)
</dt> <dt>

[<span data-ttu-id="c4442-478">**\_ETHERNETPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="c4442-478">**CIM\_EthernetPort**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)
</dt> </dl>

 

