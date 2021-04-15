---
description: Rappresenta lo stato del servizio heartbeat, che è responsabile del monitoraggio dello stato di una macchina virtuale segnalando un heartbeat a intervalli regolari.
ms.assetid: 72DB3CD9-B083-4483-BCCD-DC8C140DDBF4
title: Classe Msvm_HeartbeatComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HeartbeatComponent
- Msvm_HeartbeatComponent.SetPowerState
- Msvm_HeartbeatComponent.EnableDevice
- Msvm_HeartbeatComponent.OnlineDevice
- Msvm_HeartbeatComponent.QuiesceDevice
- Msvm_HeartbeatComponent.SaveProperties
- Msvm_HeartbeatComponent.RestoreProperties
- Msvm_HeartbeatComponent.InstanceID
- Msvm_HeartbeatComponent.Caption
- Msvm_HeartbeatComponent.Description
- Msvm_HeartbeatComponent.ElementName
- Msvm_HeartbeatComponent.InstallDate
- Msvm_HeartbeatComponent.Name
- Msvm_HeartbeatComponent.OperationalStatus
- Msvm_HeartbeatComponent.StatusDescriptions
- Msvm_HeartbeatComponent.Status
- Msvm_HeartbeatComponent.HealthState
- Msvm_HeartbeatComponent.CommunicationStatus
- Msvm_HeartbeatComponent.DetailedStatus
- Msvm_HeartbeatComponent.OperatingStatus
- Msvm_HeartbeatComponent.PrimaryStatus
- Msvm_HeartbeatComponent.EnabledState
- Msvm_HeartbeatComponent.OtherEnabledState
- Msvm_HeartbeatComponent.RequestedState
- Msvm_HeartbeatComponent.EnabledDefault
- Msvm_HeartbeatComponent.TimeOfLastStateChange
- Msvm_HeartbeatComponent.AvailableRequestedStates
- Msvm_HeartbeatComponent.TransitioningToState
- Msvm_HeartbeatComponent.SystemCreationClassName
- Msvm_HeartbeatComponent.SystemName
- Msvm_HeartbeatComponent.CreationClassName
- Msvm_HeartbeatComponent.DeviceID
- Msvm_HeartbeatComponent.PowerManagementSupported
- Msvm_HeartbeatComponent.PowerManagementCapabilities
- Msvm_HeartbeatComponent.Availability
- Msvm_HeartbeatComponent.StatusInfo
- Msvm_HeartbeatComponent.LastErrorCode
- Msvm_HeartbeatComponent.ErrorDescription
- Msvm_HeartbeatComponent.ErrorCleared
- Msvm_HeartbeatComponent.OtherIdentifyingInfo
- Msvm_HeartbeatComponent.PowerOnHours
- Msvm_HeartbeatComponent.TotalPowerOnHours
- Msvm_HeartbeatComponent.IdentifyingDescriptions
- Msvm_HeartbeatComponent.AdditionalAvailability
- Msvm_HeartbeatComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 61a3efaba52c2e592f405e1b95f1c62568a59229
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525230"
---
# <a name="msvm_heartbeatcomponent-class"></a><span data-ttu-id="e38a5-103">\_Classe MSVM HeartbeatComponent</span><span class="sxs-lookup"><span data-stu-id="e38a5-103">Msvm\_HeartbeatComponent class</span></span>

<span data-ttu-id="e38a5-104">Rappresenta lo stato del servizio heartbeat, che è responsabile del monitoraggio dello stato di una macchina virtuale segnalando un heartbeat a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="e38a5-104">Represents the state of the heartbeat service, which is responsible for monitoring the state of a virtual machine by reporting a heartbeat at regular intervals.</span></span>

<span data-ttu-id="e38a5-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e38a5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e38a5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e38a5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HeartbeatComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Heartbeat";
  string   Description = "Microsoft Heartbeat Service";
  string   ElementName = "Heartbeat";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
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
  uint16   EnabledDefault = 7;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_HeartbeatComponent";
  string   DeviceID = "Microsoft:VMGUID\GUID";
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
};
```

## <a name="members"></a><span data-ttu-id="e38a5-107">Members</span><span class="sxs-lookup"><span data-stu-id="e38a5-107">Members</span></span>

<span data-ttu-id="e38a5-108">La **classe \_ HeartbeatComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e38a5-108">The **Msvm\_HeartbeatComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e38a5-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e38a5-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e38a5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e38a5-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e38a5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e38a5-111">Methods</span></span>

<span data-ttu-id="e38a5-112">La **classe \_ HeartbeatComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e38a5-112">The **Msvm\_HeartbeatComponent** class has these methods.</span></span>



| <span data-ttu-id="e38a5-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e38a5-113">Method</span></span>                                                                   | <span data-ttu-id="e38a5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e38a5-114">Description</span></span>                              |
|:-------------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="e38a5-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="e38a5-115">**EnableDevice**</span></span>                                                         | <span data-ttu-id="e38a5-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-116">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e38a5-117">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="e38a5-117">**OnlineDevice**</span></span>                                                         | <span data-ttu-id="e38a5-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e38a5-119">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="e38a5-119">**QuiesceDevice**</span></span>                                                        | <span data-ttu-id="e38a5-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-120">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="e38a5-121">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e38a5-121">**RequestStateChange**</span></span>](msvm-heartbeatcomponent-requeststatechange.md) | <span data-ttu-id="e38a5-122">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-122">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="e38a5-123">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e38a5-123">**Reset**</span></span>](msvm-heartbeatcomponent-reset.md)                           | <span data-ttu-id="e38a5-124">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="e38a5-124">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="e38a5-125">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="e38a5-125">**RestoreProperties**</span></span>                                                    | <span data-ttu-id="e38a5-126">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-126">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e38a5-127">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="e38a5-127">**SaveProperties**</span></span>                                                       | <span data-ttu-id="e38a5-128">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="e38a5-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-129">**SetPowerState**</span></span>                                                        | <span data-ttu-id="e38a5-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-130">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e38a5-131">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e38a5-131">Properties</span></span>

<span data-ttu-id="e38a5-132">La **classe \_ HeartbeatComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e38a5-132">The **Msvm\_HeartbeatComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e38a5-133">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="e38a5-133">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-134">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-136">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e38a5-136">Any additional availability and status of the device.</span></span> <span data-ttu-id="e38a5-137">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su 6 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e38a5-137">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to 6 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-138">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="e38a5-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-139">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-141">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e38a5-141">The primary availability and status of the device.</span></span> <span data-ttu-id="e38a5-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-143">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e38a5-143">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-144">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-144">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-146">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-146">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e38a5-147">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e38a5-147">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="e38a5-148">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-148">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e38a5-149">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-149">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e38a5-150">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e38a5-150">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e38a5-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e38a5-151"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e38a5-152"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="e38a5-153"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e38a5-154"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e38a5-155"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="e38a5-156"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="e38a5-157"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="e38a5-158"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="e38a5-159"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="e38a5-160"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e38a5-161">)</span><span class="sxs-lookup"><span data-stu-id="e38a5-161">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e38a5-162">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e38a5-162">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-165">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e38a5-165">A short description of the object.</span></span> <span data-ttu-id="e38a5-166">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ed è sempre impostata su "heartbeat".</span><span class="sxs-lookup"><span data-stu-id="e38a5-166">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-167">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e38a5-167">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-168">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-170">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="e38a5-170">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e38a5-171">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-171">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e38a5-172">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-172">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-173">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e38a5-173">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-176">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e38a5-176">The scoping system's creation class name.</span></span> <span data-ttu-id="e38a5-177">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ HeartbeatComponent".</span><span class="sxs-lookup"><span data-stu-id="e38a5-177">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_HeartbeatComponent".</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-178">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e38a5-178">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-179">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-181">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e38a5-181">A description of the object.</span></span> <span data-ttu-id="e38a5-182">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft heartbeat Service".</span><span class="sxs-lookup"><span data-stu-id="e38a5-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Heartbeat Service".</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-183">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e38a5-183">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-186">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-186">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e38a5-187">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-187">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e38a5-188">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-188">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-189">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="e38a5-189">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-190">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-192">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e38a5-192">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="e38a5-193">Questa proprietà viene ereditata [**da CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*VMGUID* \\ *GUID*", dove *VMGUID* è la proprietà **Name** del [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associato a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e38a5-193">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-194">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e38a5-194">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-195">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-196">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-197">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e38a5-197">A display name for the object.</span></span> <span data-ttu-id="e38a5-198">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "heartbeat".</span><span class="sxs-lookup"><span data-stu-id="e38a5-198">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Heartbeat".</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-199">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e38a5-199">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-200">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-200">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-201">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-202">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 7 (nessuna impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="e38a5-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 7 (No Default).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-203">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-203">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-204">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-206">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-206">The enabled and disabled states of an element.</span></span> <span data-ttu-id="e38a5-207">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e38a5-207">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>



| <span data-ttu-id="e38a5-208">Valore</span><span class="sxs-lookup"><span data-stu-id="e38a5-208">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="e38a5-209">Significato</span><span class="sxs-lookup"><span data-stu-id="e38a5-209">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e38a5-210"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e38a5-210"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="e38a5-211">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e38a5-211">The element is running.</span></span><br/>    |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e38a5-212"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e38a5-212"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e38a5-213">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-213">The element is turned off.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e38a5-214">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="e38a5-214">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-215">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e38a5-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-217">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-217">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="e38a5-218">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-218">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-219">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="e38a5-219">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-220">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-221">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-222">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="e38a5-222">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="e38a5-223">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-223">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-224">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-224">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-225">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-227">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-227">The current health of the element.</span></span> <span data-ttu-id="e38a5-228">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="e38a5-228">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e38a5-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-230">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e38a5-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-232">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e38a5-232">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="e38a5-233">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-233">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e38a5-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-235">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e38a5-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-237">Data e ora in cui il servizio di integrazione è stato installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e38a5-237">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="e38a5-238">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-238">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-239">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e38a5-239">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-240">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-241">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-242">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="e38a5-242">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-243">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e38a5-243">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e38a5-244">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-244">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-245">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="e38a5-245">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-246">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e38a5-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-248">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e38a5-248">The last error code reported by the logical device.</span></span> <span data-ttu-id="e38a5-249">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-249">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-250">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="e38a5-250">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-251">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e38a5-251">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-253">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-253">This property has been deprecated.</span></span> <span data-ttu-id="e38a5-254">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-254">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e38a5-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-258">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e38a5-258">The label by which the object is known.</span></span> <span data-ttu-id="e38a5-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-260">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e38a5-260">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-261">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-261">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-263">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e38a5-263">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e38a5-264">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-264">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e38a5-265">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-265">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-266">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e38a5-266">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-267">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-267">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-269">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e38a5-269">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-270">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-270">The current status of the element.</span></span> <span data-ttu-id="e38a5-271">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e38a5-272">Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="e38a5-272">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e38a5-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="e38a5-273"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-274">Il servizio funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-274">The service is operating normally.</span></span> <span data-ttu-id="e38a5-275">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="e38a5-275">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e38a5-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)</span><span class="sxs-lookup"><span data-stu-id="e38a5-276"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-277">Il servizio funziona normalmente, ma il servizio Guest ha negoziato una versione del protocollo di comunicazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="e38a5-277">The service is operating normally, but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="e38a5-278">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="e38a5-278">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span data-ttu-id="e38a5-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (7)</span><span class="sxs-lookup"><span data-stu-id="e38a5-279"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-280">Il Guest non supporta una versione del protocollo compatibile.</span><span class="sxs-lookup"><span data-stu-id="e38a5-280">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="e38a5-281">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="e38a5-281">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span>

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e38a5-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)</span><span class="sxs-lookup"><span data-stu-id="e38a5-282"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (12)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-283">Il servizio Guest non è installato o non è stato ancora contattato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-283">The guest service is not installed or has not yet been contacted.</span></span>

</dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span data-ttu-id="e38a5-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)</span><span class="sxs-lookup"><span data-stu-id="e38a5-284"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (13)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-285">Il servizio Guest non risponde più normalmente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-285">The guest service is no longer responding normally.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="e38a5-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>In **pausa** (15)</span><span class="sxs-lookup"><span data-stu-id="e38a5-286"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (15)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-287">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="e38a5-287">The virtual machine is paused.</span></span>

</dd> </dl>

<span data-ttu-id="e38a5-288">Il  \[ valore della \] proprietà OperationalStatus 1 indica i valori dello stato dell'applicazione Uniti.</span><span class="sxs-lookup"><span data-stu-id="e38a5-288">The **OperationalStatus**\[1\] property value indicates the coalesced application state values.</span></span> <span data-ttu-id="e38a5-289">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e38a5-289">This will be one of the following values.</span></span>

> [!Note]  
> <span data-ttu-id="e38a5-290">Lo stato di un'applicazione viene impostato sulla macchina virtuale utilizzando il metodo [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) .</span><span class="sxs-lookup"><span data-stu-id="e38a5-290">The state for an application is set on the virtual machine by using the [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md) method.</span></span>

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e38a5-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span><span class="sxs-lookup"><span data-stu-id="e38a5-291"><span id="OK"></span><span id="ok"></span>**OK** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-292">Le applicazioni in esecuzione all'interno della macchina virtuale funzionano normalmente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-292">The applications running inside the virtual machine are operating normally.</span></span>

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span data-ttu-id="e38a5-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Mancata corrispondenza del protocollo** (32775)</span><span class="sxs-lookup"><span data-stu-id="e38a5-293"><span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Protocol Mismatch** (32775)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-294">Il Guest e i componenti host eseguono versioni diverse del protocollo.</span><span class="sxs-lookup"><span data-stu-id="e38a5-294">The guest and the host components are running different protocol versions.</span></span>

</dd> <dt>

<span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>

<span data-ttu-id="e38a5-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Stato critico applicazione** (32782)</span><span class="sxs-lookup"><span data-stu-id="e38a5-295"><span id="Application_Critical_State"></span><span id="application_critical_state"></span><span id="APPLICATION_CRITICAL_STATE"></span>**Application Critical State** (32782)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-296">Una o più applicazioni all'interno della macchina virtuale si trovano in uno stato critico.</span><span class="sxs-lookup"><span data-stu-id="e38a5-296">One or more of the applications inside the virtual machine are in a critical state.</span></span>

</dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span data-ttu-id="e38a5-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout della comunicazione** (32783)</span><span class="sxs-lookup"><span data-stu-id="e38a5-297"><span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Communication Timed Out** (32783)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-298">Timeout durante l'attesa di una risposta dal componente Guest.</span><span class="sxs-lookup"><span data-stu-id="e38a5-298">Timed out waiting for a response from the guest component.</span></span>

</dd> <dt>

<span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>

<span data-ttu-id="e38a5-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Comunicazione non riuscita** (32784)</span><span class="sxs-lookup"><span data-stu-id="e38a5-299"><span id="Communication_Failed"></span><span id="communication_failed"></span><span id="COMMUNICATION_FAILED"></span>**Communication Failed** (32784)</span></span>


</dt> <dd>

<span data-ttu-id="e38a5-300">Non è stato possibile comunicare con il componente Guest.</span><span class="sxs-lookup"><span data-stu-id="e38a5-300">Failed to communicate with the guest component.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e38a5-301">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-301">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-302">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-304">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e38a5-304">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="e38a5-305">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e38a5-305">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="e38a5-306">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e38a5-306">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-307">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e38a5-307">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-308">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e38a5-308">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-310">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e38a5-310">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="e38a5-311">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e38a5-311">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-312">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e38a5-312">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-313">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-313">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-315">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e38a5-315">The power management capabilities of the device.</span></span> <span data-ttu-id="e38a5-316">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-316">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-317">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="e38a5-317">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-318">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e38a5-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-320">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="e38a5-320">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="e38a5-321">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-322">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e38a5-322">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-323">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e38a5-323">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-325">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="e38a5-325">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="e38a5-326">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-326">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-327">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e38a5-327">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-328">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-328">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-330">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="e38a5-330">Provides high level status information.</span></span> <span data-ttu-id="e38a5-331">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e38a5-331">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e38a5-332">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-332">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e38a5-333">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-333">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-334">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-334">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-335">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-336">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-337">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-337">The last requested or desired state for the element.</span></span> <span data-ttu-id="e38a5-338">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e38a5-338">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-339">**Status**</span><span class="sxs-lookup"><span data-stu-id="e38a5-339">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-340">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-341">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-342">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e38a5-342">The current status of the object.</span></span> <span data-ttu-id="e38a5-343">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-343">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-344">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e38a5-344">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-345">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e38a5-345">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-347">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e38a5-347">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e38a5-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e38a5-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-349">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="e38a5-349">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-350">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-350">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-352">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="e38a5-352">The current state of the logical device.</span></span> <span data-ttu-id="e38a5-353">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-354">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e38a5-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-356">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-357">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e38a5-357">The scoping system's creation class name.</span></span> <span data-ttu-id="e38a5-358">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="e38a5-358">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e38a5-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-360">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e38a5-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-362">Nome del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="e38a5-362">The scoping system's name.</span></span> <span data-ttu-id="e38a5-363">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) e è il nome del [**\_ ComputerSystem MSVM**](msvm-computersystem.md) associato a questo servizio heartbeat.</span><span class="sxs-lookup"><span data-stu-id="e38a5-363">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is the name of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) that is associated with this heartbeat service.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-364">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e38a5-364">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-365">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e38a5-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-367">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e38a5-367">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e38a5-368">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e38a5-368">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-369">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="e38a5-369">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-370">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e38a5-370">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-372">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="e38a5-372">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="e38a5-373">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-373">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e38a5-374">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e38a5-374">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e38a5-375">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e38a5-375">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e38a5-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e38a5-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e38a5-377">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e38a5-377">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e38a5-378">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e38a5-378">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e38a5-379">Commenti</span><span class="sxs-lookup"><span data-stu-id="e38a5-379">Remarks</span></span>

<span data-ttu-id="e38a5-380">L'accesso alla **classe \_ HeartbeatComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="e38a5-380">Access to the **Msvm\_HeartbeatComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="e38a5-381">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="e38a5-381">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="e38a5-382">Esempio</span><span class="sxs-lookup"><span data-stu-id="e38a5-382">Examples</span></span>

<span data-ttu-id="e38a5-383">L'esempio C# seguente consente di ottenere lo stato di integrità dell'applicazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e38a5-383">The following C# sample obtains the application health status of a virtual machine.</span></span> <span data-ttu-id="e38a5-384">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="e38a5-384">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e38a5-385">Per funzionare correttamente, il codice seguente deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="e38a5-385">To function correctly, the following code must be run with Administrator privileges.</span></span>

 


```CSharp
private UInt16 OperationalStatusOk = 2;
private UInt16 OperationalStatusApplicationCriticalState = 32782;

/// <summary>
/// Gets the applications status in the VM.
/// </summary>
/// <param name="hostMachine">The hostname of the machine on which
/// the VM is running.</param>
/// <param name="vmName">The VM name.</param>
public
void
GetAppHealthStatus(
    string hostMachine,
    string vmName
    )
{
    ManagementScope scope = new ManagementScope(
        @"\\" + hostMachine + @"\root\virtualization\v2", null);

    ManagementObject heartBeatComponent = null;

    // Get the VM object and its heart beat component.
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
    using (ManagementObjectCollection heartBeatCollection =
        vm.GetRelated("Msvm_HeartbeatComponent", "Msvm_SystemDevice",
            null, null, null, null, false, null))
    {
        foreach (ManagementObject element in heartBeatCollection)
        {
            heartBeatComponent = element;
            break;
        }
    }

    if (heartBeatComponent == null)
    {
        Console.WriteLine("The VM is not running.");
        return;
    }

    using (heartBeatComponent)
    {
        UInt16[] operationalStatus = (UInt16[])heartBeatComponent["OperationalStatus"];
        UInt16 vmStatus = operationalStatus[0];

        if (vmStatus != OperationalStatusOk)
        {
            Console.WriteLine("The VM heartbeat status is not OK");
            return;
        }

        if (operationalStatus.Length != 2)
        {
            Console.WriteLine("The required Integration Components are not running " +
                "or not installed.");
            return;
        }

        UInt16 appStatus = operationalStatus[1];
        if (appStatus == OperationalStatusOk)
        {
            Console.WriteLine("The VM applications health status: OK");
        }
        else if (appStatus == OperationalStatusApplicationCriticalState)
        {
            Console.WriteLine("The VM applications health status: Critical");
        }
        else
        {
            throw new ManagementException("Unknown application health status");
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="e38a5-386">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e38a5-386">Requirements</span></span>



| <span data-ttu-id="e38a5-387">Requisito</span><span class="sxs-lookup"><span data-stu-id="e38a5-387">Requirement</span></span> | <span data-ttu-id="e38a5-388">Valore</span><span class="sxs-lookup"><span data-stu-id="e38a5-388">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e38a5-389">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e38a5-389">Minimum supported client</span></span><br/> | <span data-ttu-id="e38a5-390">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e38a5-390">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e38a5-391">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e38a5-391">Minimum supported server</span></span><br/> | <span data-ttu-id="e38a5-392">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e38a5-392">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e38a5-393">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e38a5-393">Namespace</span></span><br/>                | <span data-ttu-id="e38a5-394">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e38a5-394">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e38a5-395">MOF</span><span class="sxs-lookup"><span data-stu-id="e38a5-395">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e38a5-396"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e38a5-396"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e38a5-397">DLL</span><span class="sxs-lookup"><span data-stu-id="e38a5-397">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e38a5-398"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e38a5-398"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e38a5-399">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e38a5-399">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e38a5-400">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e38a5-400">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="e38a5-401">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="e38a5-401">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> <dt>

[<span data-ttu-id="e38a5-402">**\_HeartbeatComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="e38a5-402">**Msvm\_HeartbeatComponent**</span></span>](/previous-versions/windows/desktop/virtual/msvm-heartbeatcomponent)
</dt> </dl>

 

