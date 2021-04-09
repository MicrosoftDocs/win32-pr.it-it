---
description: Rappresenta una scheda di rete Wi-Fi fisica (802,11) che può essere associata a un commutire virtuale per fornire la connettività di rete esterna alle macchine virtuali.
ms.assetid: c6dae491-607c-4f17-aea9-162d910120c2
title: Classe Msvm_WiFiPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiPort
- Msvm_WiFiPort.RequestStateChange
- Msvm_WiFiPort.SetPowerState
- Msvm_WiFiPort.Reset
- Msvm_WiFiPort.EnableDevice
- Msvm_WiFiPort.OnlineDevice
- Msvm_WiFiPort.QuiesceDevice
- Msvm_WiFiPort.SaveProperties
- Msvm_WiFiPort.RestoreProperties
- Msvm_WiFiPort.InstanceID
- Msvm_WiFiPort.Caption
- Msvm_WiFiPort.Description
- Msvm_WiFiPort.ElementName
- Msvm_WiFiPort.InstallDate
- Msvm_WiFiPort.Name
- Msvm_WiFiPort.OperationalStatus
- Msvm_WiFiPort.StatusDescriptions
- Msvm_WiFiPort.Status
- Msvm_WiFiPort.HealthState
- Msvm_WiFiPort.CommunicationStatus
- Msvm_WiFiPort.DetailedStatus
- Msvm_WiFiPort.OperatingStatus
- Msvm_WiFiPort.PrimaryStatus
- Msvm_WiFiPort.EnabledState
- Msvm_WiFiPort.OtherEnabledState
- Msvm_WiFiPort.RequestedState
- Msvm_WiFiPort.EnabledDefault
- Msvm_WiFiPort.TimeOfLastStateChange
- Msvm_WiFiPort.AvailableRequestedStates
- Msvm_WiFiPort.TransitioningToState
- Msvm_WiFiPort.SystemCreationClassName
- Msvm_WiFiPort.SystemName
- Msvm_WiFiPort.CreationClassName
- Msvm_WiFiPort.DeviceID
- Msvm_WiFiPort.PowerManagementSupported
- Msvm_WiFiPort.PowerManagementCapabilities
- Msvm_WiFiPort.Availability
- Msvm_WiFiPort.StatusInfo
- Msvm_WiFiPort.LastErrorCode
- Msvm_WiFiPort.ErrorDescription
- Msvm_WiFiPort.ErrorCleared
- Msvm_WiFiPort.OtherIdentifyingInfo
- Msvm_WiFiPort.PowerOnHours
- Msvm_WiFiPort.TotalPowerOnHours
- Msvm_WiFiPort.IdentifyingDescriptions
- Msvm_WiFiPort.AdditionalAvailability
- Msvm_WiFiPort.MaxQuiesceTime
- Msvm_WiFiPort.Speed
- Msvm_WiFiPort.MaxSpeed
- Msvm_WiFiPort.RequestedSpeed
- Msvm_WiFiPort.UsageRestriction
- Msvm_WiFiPort.PortType
- Msvm_WiFiPort.OtherPortType
- Msvm_WiFiPort.OtherNetworkPortType
- Msvm_WiFiPort.PortNumber
- Msvm_WiFiPort.LinkTechnology
- Msvm_WiFiPort.OtherLinkTechnology
- Msvm_WiFiPort.PermanentAddress
- Msvm_WiFiPort.NetworkAddresses
- Msvm_WiFiPort.FullDuplex
- Msvm_WiFiPort.AutoSense
- Msvm_WiFiPort.SupportedMaximumTransmissionUnit
- Msvm_WiFiPort.ActiveMaximumTransmissionUnit
- Msvm_WiFiPort.IsBound
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47ec33236c55d281755b50449a8f33a56152a07a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968684"
---
# <a name="msvm_wifiport-class"></a><span data-ttu-id="df2c3-103">\_Classe MSVM WiFiPort</span><span class="sxs-lookup"><span data-stu-id="df2c3-103">Msvm\_WiFiPort class</span></span>

<span data-ttu-id="df2c3-104">Rappresenta una scheda di rete Wi-Fi fisica (802,11) che può essere associata a un commutire virtuale per fornire la connettività di rete esterna alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="df2c3-104">Represents a physical Wi-Fi (802.11) network adapter that can be bound to a virtual switch to provide external network connectivity to virtual machines.</span></span>

<span data-ttu-id="df2c3-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="df2c3-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df2c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df2c3-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiPort : CIM_WiFiPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
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
  boolean  IsBound;
};
```

## <a name="members"></a><span data-ttu-id="df2c3-107">Members</span><span class="sxs-lookup"><span data-stu-id="df2c3-107">Members</span></span>

<span data-ttu-id="df2c3-108">La **classe \_ WiFiPort di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="df2c3-108">The **Msvm\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="df2c3-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="df2c3-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="df2c3-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df2c3-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="df2c3-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="df2c3-111">Methods</span></span>

<span data-ttu-id="df2c3-112">La **classe \_ WiFiPort di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="df2c3-112">The **Msvm\_WiFiPort** class has these methods.</span></span>



| <span data-ttu-id="df2c3-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="df2c3-113">Method</span></span>                 | <span data-ttu-id="df2c3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df2c3-114">Description</span></span>                              |
|:-----------------------|:-----------------------------------------|
| <span data-ttu-id="df2c3-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="df2c3-115">**EnableDevice**</span></span>       | <span data-ttu-id="df2c3-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="df2c3-117">**OnlineDevice**</span></span>       | <span data-ttu-id="df2c3-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="df2c3-119">**QuiesceDevice**</span></span>      | <span data-ttu-id="df2c3-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="df2c3-121">**RequestStateChange**</span></span> | <span data-ttu-id="df2c3-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-122">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-123">**Reimpostazione**</span><span class="sxs-lookup"><span data-stu-id="df2c3-123">**Reset**</span></span>              | <span data-ttu-id="df2c3-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-124">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="df2c3-125">**RestoreProperties**</span></span>  | <span data-ttu-id="df2c3-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="df2c3-127">**SaveProperties**</span></span>     | <span data-ttu-id="df2c3-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="df2c3-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-129">**SetPowerState**</span></span>      | <span data-ttu-id="df2c3-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="df2c3-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="df2c3-131">Properties</span></span>

<span data-ttu-id="df2c3-132">La **classe \_ WiFiPort di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="df2c3-132">The **Msvm\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df2c3-133">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="df2c3-133">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-136">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="df2c3-136">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-137">Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="df2c3-137">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="df2c3-138">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-138">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-139">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="df2c3-139">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-140">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-142">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-142">Any additional availability and status of the device.</span></span> <span data-ttu-id="df2c3-143">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-143">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-144">**Rilevamento automatico**</span><span class="sxs-lookup"><span data-stu-id="df2c3-144">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-145">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="df2c3-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-147">Indica se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-147">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="df2c3-148">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-148">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-149">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="df2c3-149">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-152">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-152">The primary availability and status of the device.</span></span> <span data-ttu-id="df2c3-153">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-153">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-154">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="df2c3-154">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-155">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-155">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-157">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-157">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="df2c3-158">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-158">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="df2c3-159">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="df2c3-159">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="df2c3-160">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="df2c3-160">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="df2c3-161">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="df2c3-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="df2c3-162"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="df2c3-163"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="df2c3-164"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="df2c3-165"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="df2c3-166"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="df2c3-167"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="df2c3-168"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="df2c3-169"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="df2c3-170"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="df2c3-171"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="df2c3-172">)</span><span class="sxs-lookup"><span data-stu-id="df2c3-172">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df2c3-173">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="df2c3-173">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-176">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-176">A short description of the object.</span></span> <span data-ttu-id="df2c3-177">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="df2c3-177">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-178">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="df2c3-178">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-181">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="df2c3-181">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="df2c3-182">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df2c3-183">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-184">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df2c3-184">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-187">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="df2c3-187">The scoping system's creation class name.</span></span> <span data-ttu-id="df2c3-188">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-188">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-189">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="df2c3-189">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-192">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="df2c3-192">A description of the object.</span></span> <span data-ttu-id="df2c3-193">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-193">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-194">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="df2c3-194">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-195">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-195">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-197">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-197">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="df2c3-198">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-198">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df2c3-199">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-199">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-200">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="df2c3-200">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-201">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-203">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="df2c3-203">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="df2c3-204">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-204">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-205">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="df2c3-205">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-208">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-208">A display name for the object.</span></span> <span data-ttu-id="df2c3-209">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-209">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-210">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="df2c3-210">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-213">Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-213">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="df2c3-214">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-214">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-215">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-215">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-216">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-216">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-218">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-218">The enabled and disabled states of an element.</span></span> <span data-ttu-id="df2c3-219">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="df2c3-219">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="df2c3-220">Valore</span><span class="sxs-lookup"><span data-stu-id="df2c3-220">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="df2c3-221">Significato</span><span class="sxs-lookup"><span data-stu-id="df2c3-221">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="df2c3-222"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="df2c3-223">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="df2c3-223">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="df2c3-224"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="df2c3-225">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-225">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="df2c3-226">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="df2c3-226">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-227">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="df2c3-227">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-229">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-229">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="df2c3-230">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-231">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="df2c3-231">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-234">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="df2c3-234">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="df2c3-235">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-235">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-236">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="df2c3-236">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-237">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="df2c3-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-239">Indica se la porta funziona in modalità full duplex.</span><span class="sxs-lookup"><span data-stu-id="df2c3-239">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="df2c3-240">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-240">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-241">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-241">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-242">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-242">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-244">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-244">The current health of the element.</span></span> <span data-ttu-id="df2c3-245">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-246">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df2c3-246">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-247">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="df2c3-247">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-249">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="df2c3-249">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="df2c3-250">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-251">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="df2c3-251">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-252">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df2c3-252">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-254">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-254">The date and time when the object was installed.</span></span> <span data-ttu-id="df2c3-255">Questa proprietà non richiede un valore per indicare che l'oggetto è installato.</span><span class="sxs-lookup"><span data-stu-id="df2c3-255">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="df2c3-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-257">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="df2c3-257">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-260">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="df2c3-260">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-261">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="df2c3-261">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="df2c3-262">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-262">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-263">**Con associazione**</span><span class="sxs-lookup"><span data-stu-id="df2c3-263">**IsBound**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-264">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="df2c3-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-266">Specifica se la porta Wi-Fi è associata all'architettura di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df2c3-266">Specifies if the Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <span data-ttu-id="df2c3-267">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="df2c3-267">This will be one of the following values.</span></span>



| <span data-ttu-id="df2c3-268">Valore</span><span class="sxs-lookup"><span data-stu-id="df2c3-268">Value</span></span>                                                                                                                                                        | <span data-ttu-id="df2c3-269">Significato</span><span class="sxs-lookup"><span data-stu-id="df2c3-269">Meaning</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="True"></span><span id="true"></span><span id="TRUE"></span><dl> <span data-ttu-id="df2c3-270"><dt>**Vero**</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-270"><dt>**True**</dt></span></span> </dl>     | <span data-ttu-id="df2c3-271">La porta Wi-Fi è associata all'architettura di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df2c3-271">The Wi-Fi port is bound to the virtual machine networking architecture.</span></span> <br/>     |
| <span id="False"></span><span id="false"></span><span id="FALSE"></span><dl> <span data-ttu-id="df2c3-272"><dt>**False**</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-272"><dt>**False**</dt></span></span> </dl> | <span data-ttu-id="df2c3-273">La porta Wi-Fi non è associata all'architettura di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="df2c3-273">The Wi-Fi port is not bound to the virtual machine networking architecture.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="df2c3-274">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="df2c3-274">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-275">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="df2c3-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-277">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="df2c3-277">The last error code reported by the logical device.</span></span> <span data-ttu-id="df2c3-278">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-278">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-279">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="df2c3-279">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-280">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-282">Specifica il tipo di tecnologia di collegamento per la porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-282">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="df2c3-283">Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-283">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="df2c3-284">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-284">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="df2c3-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="df2c3-285"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="df2c3-286"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="df2c3-287"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="df2c3-288"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="df2c3-289"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="df2c3-290"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="df2c3-291"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="df2c3-292"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="df2c3-293"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (9)</span><span class="sxs-lookup"><span data-stu-id="df2c3-294"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="df2c3-295"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN wireless** (11)</span><span class="sxs-lookup"><span data-stu-id="df2c3-296"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df2c3-297">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="df2c3-297">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-298">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-298">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-300">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-300">This property has been deprecated.</span></span> <span data-ttu-id="df2c3-301">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-302">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="df2c3-302">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-303">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-303">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-305">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="df2c3-305">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-306">Larghezza di banda massima della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-306">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="df2c3-307">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-307">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-308">**Nome**</span><span class="sxs-lookup"><span data-stu-id="df2c3-308">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-309">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-311">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-311">The label by which the object is known.</span></span> <span data-ttu-id="df2c3-312">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-313">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="df2c3-313">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-314">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="df2c3-314">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-316">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="df2c3-316">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-317">Matrice di stringhe che contengono gli indirizzi MAC per la porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-317">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="df2c3-318">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-318">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-319">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="df2c3-319">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-320">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-320">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-322">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="df2c3-322">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="df2c3-323">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-323">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df2c3-324">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-324">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-325">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="df2c3-325">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-326">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-326">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-328">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-328">The current statuses of the object.</span></span> <span data-ttu-id="df2c3-329">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-329">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-330">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-330">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-331">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-333">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="df2c3-333">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="df2c3-334">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="df2c3-334">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="df2c3-335">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-335">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-336">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="df2c3-336">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-337">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="df2c3-337">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-339">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="df2c3-339">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="df2c3-340">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-340">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-341">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="df2c3-341">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-342">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-344">Valore stringa che descrive **LinkTechnology** quando è impostato su 1, (other).</span><span class="sxs-lookup"><span data-stu-id="df2c3-344">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="df2c3-345">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-345">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-346">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="df2c3-346">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-347">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-349">L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** .</span><span class="sxs-lookup"><span data-stu-id="df2c3-349">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="df2c3-350">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-350">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-351">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="df2c3-351">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-352">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-354">Descrive il tipo di modulo, quando **portType** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="df2c3-354">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="df2c3-355">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-355">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-356">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="df2c3-356">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-357">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-359">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="df2c3-359">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-360">Indirizzo di rete hardcoded in una porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-360">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="df2c3-361">Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software.</span><span class="sxs-lookup"><span data-stu-id="df2c3-361">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="df2c3-362">Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-362">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="df2c3-363">Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="df2c3-363">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="df2c3-364">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-364">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-365">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="df2c3-365">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-366">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-368">Il numero della porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-368">The port number.</span></span> <span data-ttu-id="df2c3-369">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-369">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-370">**PortType**</span><span class="sxs-lookup"><span data-stu-id="df2c3-370">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-371">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-373">Modalità specifica attualmente abilitata per la porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-373">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="df2c3-374">Quando è impostata su 1 (other), la proprietà **OtherPortType** correlata contiene una descrizione di stringa del tipo di porta.</span><span class="sxs-lookup"><span data-stu-id="df2c3-374">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="df2c3-375">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-375">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="df2c3-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="df2c3-376"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="df2c3-377"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 rame 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="df2c3-378"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="df2c3-379"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="df2c3-380"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="df2c3-381"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="df2c3-382"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="df2c3-383"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="df2c3-384"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 fibre 100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="df2c3-385"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="df2c3-386"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="df2c3-387"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="df2c3-388"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="df2c3-389"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="df2c3-390"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="df2c3-391"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="df2c3-392"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="df2c3-393"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="df2c3-394"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="df2c3-395"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)</span><span class="sxs-lookup"><span data-stu-id="df2c3-396"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (16000.65535)</span><span class="sxs-lookup"><span data-stu-id="df2c3-397"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="df2c3-398">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df2c3-398">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-399">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-399">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-401">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-401">The power management capabilities of the device.</span></span> <span data-ttu-id="df2c3-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-403">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="df2c3-403">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-404">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="df2c3-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-406">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="df2c3-406">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="df2c3-407">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-407">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-408">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="df2c3-408">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-409">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-411">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="df2c3-411">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="df2c3-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-413">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="df2c3-413">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-414">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-416">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="df2c3-416">Provides high level status information.</span></span> <span data-ttu-id="df2c3-417">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="df2c3-417">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="df2c3-418">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-418">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="df2c3-419">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-419">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-420">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="df2c3-420">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-421">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-422">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="df2c3-422">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-423">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="df2c3-423">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-424">Larghezza di banda richiesta della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-424">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="df2c3-425">La larghezza di banda effettiva viene segnalata nella proprietà **velocità** .</span><span class="sxs-lookup"><span data-stu-id="df2c3-425">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="df2c3-426">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-426">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-427">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-427">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-428">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-428">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-430">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-430">The last requested or desired state for the element.</span></span> <span data-ttu-id="df2c3-431">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-432">**Velocità**</span><span class="sxs-lookup"><span data-stu-id="df2c3-432">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-433">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-435">Qualificatori: **unità** ("bit al secondo")</span><span class="sxs-lookup"><span data-stu-id="df2c3-435">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-436">Larghezza di banda della porta, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="df2c3-436">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="df2c3-437">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-437">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-438">**Status**</span><span class="sxs-lookup"><span data-stu-id="df2c3-438">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-439">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-441">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="df2c3-441">The current status of the object.</span></span> <span data-ttu-id="df2c3-442">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-442">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-443">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="df2c3-443">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-444">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="df2c3-444">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-445">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-445">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-446">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="df2c3-446">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="df2c3-447">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="df2c3-447">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-448">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="df2c3-448">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-449">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-450">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-451">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="df2c3-451">The current state of the logical device.</span></span> <span data-ttu-id="df2c3-452">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-452">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-453">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="df2c3-453">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-454">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-454">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-455">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-456">Qualificatori: **unità** ("byte")</span><span class="sxs-lookup"><span data-stu-id="df2c3-456">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-457">Unità di trasmissione massima (MTU) che può essere supportata, in byte.</span><span class="sxs-lookup"><span data-stu-id="df2c3-457">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="df2c3-458">Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="df2c3-458">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-459">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="df2c3-459">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-460">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-461">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-461">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-462">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="df2c3-462">The scoping system's creation class name.</span></span> <span data-ttu-id="df2c3-463">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-463">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-464">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="df2c3-464">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-465">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="df2c3-465">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-466">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-466">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-467">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="df2c3-467">The scoping system's name.</span></span> <span data-ttu-id="df2c3-468">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-468">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-469">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="df2c3-469">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-470">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="df2c3-470">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-471">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-472">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="df2c3-472">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="df2c3-473">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-473">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-474">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="df2c3-474">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-475">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="df2c3-475">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-476">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-477">Il numero totale di ore in cui il dispositivo è stato acceso.</span><span class="sxs-lookup"><span data-stu-id="df2c3-477">The total number of hours that this device has been powered on.</span></span> <span data-ttu-id="df2c3-478">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="df2c3-478">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-479">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="df2c3-479">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-480">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-482">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="df2c3-482">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="df2c3-483">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="df2c3-483">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="df2c3-484">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="df2c3-484">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df2c3-485">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df2c3-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-486">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="df2c3-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df2c3-487">In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="df2c3-487">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="df2c3-488">Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host.</span><span class="sxs-lookup"><span data-stu-id="df2c3-488">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="df2c3-489">Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni).</span><span class="sxs-lookup"><span data-stu-id="df2c3-489">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="df2c3-490">Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="df2c3-490">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="df2c3-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="df2c3-491"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="df2c3-492"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="df2c3-493"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="df2c3-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Senza restrizioni** (4)</span><span class="sxs-lookup"><span data-stu-id="df2c3-494"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df2c3-495">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df2c3-495">Requirements</span></span>



| <span data-ttu-id="df2c3-496">Requisito</span><span class="sxs-lookup"><span data-stu-id="df2c3-496">Requirement</span></span> | <span data-ttu-id="df2c3-497">Valore</span><span class="sxs-lookup"><span data-stu-id="df2c3-497">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df2c3-498">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df2c3-498">Minimum supported client</span></span><br/> | <span data-ttu-id="df2c3-499">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="df2c3-499">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="df2c3-500">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df2c3-500">Minimum supported server</span></span><br/> | <span data-ttu-id="df2c3-501">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="df2c3-501">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="df2c3-502">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="df2c3-502">Namespace</span></span><br/>                | <span data-ttu-id="df2c3-503">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="df2c3-503">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="df2c3-504">MOF</span><span class="sxs-lookup"><span data-stu-id="df2c3-504">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df2c3-505"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-505"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df2c3-506">DLL</span><span class="sxs-lookup"><span data-stu-id="df2c3-506">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df2c3-507"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df2c3-507"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

