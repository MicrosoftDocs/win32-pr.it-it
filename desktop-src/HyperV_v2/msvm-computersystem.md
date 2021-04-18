---
description: Rappresenta un sistema computer fisico o una macchina virtuale.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565740"
---
# <a name="msvm_computersystem-class"></a><span data-ttu-id="61a72-103">\_Classe MSVM ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="61a72-103">Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="61a72-104">Rappresenta un sistema computer fisico o una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-104">Represents a physical computer system or virtual machine.</span></span>

<span data-ttu-id="61a72-105">Per recuperare informazioni per VMMS, usare la classe [**\_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="61a72-105">To retrieve information for the VMMS, use the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="61a72-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="61a72-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a72-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61a72-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
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
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a><span data-ttu-id="61a72-108">Members</span><span class="sxs-lookup"><span data-stu-id="61a72-108">Members</span></span>

<span data-ttu-id="61a72-109">La **classe \_ ComputerSystem di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="61a72-109">The **Msvm\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="61a72-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="61a72-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="61a72-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61a72-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="61a72-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="61a72-112">Methods</span></span>

<span data-ttu-id="61a72-113">La **classe \_ ComputerSystem di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="61a72-113">The **Msvm\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="61a72-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="61a72-114">Method</span></span>                                                                                         | <span data-ttu-id="61a72-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61a72-115">Description</span></span>                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61a72-116">**InjectNonMaskableInterrupt**</span><span class="sxs-lookup"><span data-stu-id="61a72-116">**InjectNonMaskableInterrupt**</span></span>](injectnonmaskableinterrupt-msvm-computersystem.md)           | <span data-ttu-id="61a72-117">Inserisce un interrupt non mascherabile nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-117">Injects a non-maskable interrupt into the virtual machine.</span></span> <span data-ttu-id="61a72-118">Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-118">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="61a72-119">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="61a72-119">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                    |
| [<span data-ttu-id="61a72-120">**RequestReplicationStateChange**</span><span class="sxs-lookup"><span data-stu-id="61a72-120">**RequestReplicationStateChange**</span></span>](msvm-computersystem-requestreplicationstatechange.md)     | <span data-ttu-id="61a72-121">Richiede che lo stato di replica della macchina virtuale venga modificato in un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="61a72-121">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="61a72-122">Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-122">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="61a72-123">**RequestReplicationStateChangeEx**</span><span class="sxs-lookup"><span data-stu-id="61a72-123">**RequestReplicationStateChangeEx**</span></span>](msvm-requestreplicationstatechangeex-computersystem.md) | <span data-ttu-id="61a72-124">Richiede che lo stato di replica della macchina virtuale venga modificato in un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="61a72-124">Requests that the replication state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="61a72-125">Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-125">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/> <span data-ttu-id="61a72-126">**Windows 8.1:** Questo metodo non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="61a72-126">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="61a72-127">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="61a72-127">**RequestStateChange**</span></span>](requeststatechange-msvm-computersystem.md)                           | <span data-ttu-id="61a72-128">Richiede che lo stato della macchina virtuale venga modificato.</span><span class="sxs-lookup"><span data-stu-id="61a72-128">Requests that the state of the virtual machine be changed.</span></span> <span data-ttu-id="61a72-129">Questo metodo è supportato solo per le istanze della classe **MSVM \_ ComputerSystem** che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-129">This method is only supported for instances of the **Msvm\_ComputerSystem** class that represent a virtual machine.</span></span><br/>                                                                                                                                           |
| <span data-ttu-id="61a72-130">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="61a72-130">**SetPowerState**</span></span>                                                                              | <span data-ttu-id="61a72-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61a72-131">This method is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a><span data-ttu-id="61a72-132">Proprietà</span><span class="sxs-lookup"><span data-stu-id="61a72-132">Properties</span></span>

<span data-ttu-id="61a72-133">La **classe \_ ComputerSystem di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="61a72-133">The **Msvm\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61a72-134">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="61a72-134">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-135">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-137">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="61a72-137">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="61a72-138">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="61a72-138">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="61a72-139">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="61a72-139">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="61a72-140">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="61a72-140">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="61a72-141">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61a72-141">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="61a72-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-142"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-143"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="61a72-144"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="61a72-145"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="61a72-146"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="61a72-147"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="61a72-148"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="61a72-149"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="61a72-150"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="61a72-151"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="61a72-152">)</span><span class="sxs-lookup"><span data-stu-id="61a72-152">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61a72-153">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="61a72-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-154">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-156">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61a72-156">A short description of the object.</span></span> <span data-ttu-id="61a72-157">Questa proprietà viene ereditata dalla classe [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) e conterrà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-157">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class, and it will contain one of the following values.</span></span>



| <span data-ttu-id="61a72-158">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-158">Value</span></span>                                                                                                | <span data-ttu-id="61a72-159">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-159">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="61a72-160"><dt>"Macchina virtuale"</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-160"><dt>"Virtual Machine"</dt></span></span> </dl>         | <span data-ttu-id="61a72-161">L'istanza rappresenta una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-161">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="61a72-162"><dt>"Host computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-162"><dt>"Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="61a72-163">L'istanza rappresenta il computer host.</span><span class="sxs-lookup"><span data-stu-id="61a72-163">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="61a72-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="61a72-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-165">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-167">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="61a72-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="61a72-168">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="61a72-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="61a72-169">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-170">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="61a72-170">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-171">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-173">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="61a72-173">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="61a72-174">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="61a72-174">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="61a72-175">**Dedicato**</span><span class="sxs-lookup"><span data-stu-id="61a72-175">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-176">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-176">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-177">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-178">Indica se il sistema informatico è un sistema speciale (dedicato a un particolare uso), rispetto a un sistema di uso generale.</span><span class="sxs-lookup"><span data-stu-id="61a72-178">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="61a72-179">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 0 (non dedicata).</span><span class="sxs-lookup"><span data-stu-id="61a72-179">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-180">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="61a72-180">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-183">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="61a72-183">A description of the object.</span></span> <span data-ttu-id="61a72-184">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e conterrà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-184">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it will contain one of the following values.</span></span>



| <span data-ttu-id="61a72-185">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-185">Value</span></span>                                                                                                          | <span data-ttu-id="61a72-186">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-186">Meaning</span></span>                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="61a72-187"><dt>"Microsoft Virtual computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-187"><dt>"Microsoft Virtual Computer System"</dt></span></span> </dl> | <span data-ttu-id="61a72-188">L'istanza rappresenta una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-188">The instance represents a virtual machine.</span></span><br/>    |
| <dl> <span data-ttu-id="61a72-189"><dt>"Microsoft hosting computer System"</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-189"><dt>"Microsoft Hosting Computer System"</dt></span></span> </dl> | <span data-ttu-id="61a72-190">L'istanza rappresenta il computer host.</span><span class="sxs-lookup"><span data-stu-id="61a72-190">The instance represents the hosting computer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="61a72-191">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="61a72-191">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-192">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-194">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="61a72-194">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="61a72-195">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="61a72-195">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="61a72-196">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-196">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-197">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="61a72-197">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-198">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-200">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61a72-200">A display name for the object.</span></span> <span data-ttu-id="61a72-201">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata sul nome visualizzato del computer per una macchina virtuale o sul nome NetBIOS del sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="61a72-201">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to the display name of the computer for a virtual machine or the NetBIOS name of the management operating system.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="61a72-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-205">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="61a72-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="61a72-206">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="61a72-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-207"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-208"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="61a72-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="61a72-209"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="61a72-210">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="61a72-210">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-213">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="61a72-213">The enabled and disabled states of an element.</span></span> <span data-ttu-id="61a72-214">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="61a72-214">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="61a72-215">Questa proprietà viene ereditata dalla classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è impostata su 2 (Enabled) per un computer fisico o su uno dei valori seguenti per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-215">This property is inherited from the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class, and it is set to 2 (Enabled) for a physical computer or one of the following values for a virtual machine.</span></span> <span data-ttu-id="61a72-216">Per una visualizzazione grafica di questi Stati, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="61a72-216">For a graphical view of these states, see Remarks.</span></span>



| <span data-ttu-id="61a72-217">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-217">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="61a72-218">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-218">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="61a72-219"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-219"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="61a72-220">Non è stato possibile determinare lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="61a72-220">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="61a72-221"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-221"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="61a72-222"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-222"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="61a72-223">L'elemento è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="61a72-223">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="61a72-224"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-224"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="61a72-225">L'elemento è disattivato.</span><span class="sxs-lookup"><span data-stu-id="61a72-225">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="61a72-226"><dt>**Chiusura**</dt> di <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-226"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="61a72-227">L'elemento è in corso di passaggio a uno stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="61a72-227">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="61a72-228"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-228"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="61a72-229">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="61a72-229">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="61a72-230"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-230"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="61a72-231">L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="61a72-231">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="61a72-232"><dt>**Nel test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-232"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="61a72-233">L'elemento si trova in uno stato di test.</span><span class="sxs-lookup"><span data-stu-id="61a72-233">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="61a72-234"><dt>**Posticipato**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-234"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="61a72-235">È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.</span><span class="sxs-lookup"><span data-stu-id="61a72-235">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="61a72-236"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-236"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="61a72-237">L'elemento è abilitato ma in modalità con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="61a72-237">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="61a72-238">Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato.</span><span class="sxs-lookup"><span data-stu-id="61a72-238">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="61a72-239">Tutte le altre richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="61a72-239">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="61a72-240"><dt>**A partire**</dt> da <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-240"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="61a72-241">L'elemento è in corso di attivazione dello stato abilitato (2).</span><span class="sxs-lookup"><span data-stu-id="61a72-241">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="61a72-242">Le nuove richieste vengono accodate.</span><span class="sxs-lookup"><span data-stu-id="61a72-242">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="61a72-243">**EnhancedSessionModeState**</span><span class="sxs-lookup"><span data-stu-id="61a72-243">**EnhancedSessionModeState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-246">Specifica lo stato corrente della modalità sessione avanzata nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-246">Specifies the current state of enhanced session mode on the virtual machine.</span></span>

<span data-ttu-id="61a72-247">Il provider WMI Hyper-V genera un' [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) ogni volta che viene modificato il **EnhancedSessionModeState** della classe **MSVM \_ ComputerSystem** .</span><span class="sxs-lookup"><span data-stu-id="61a72-247">The Hyper-V WMI provider raises an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) each time the **EnhancedSessionModeState** of the **Msvm\_ComputerSystem** class changes.</span></span> <span data-ttu-id="61a72-248">Se una sessione vmconnection attiva riceve un **\_ \_ InstanceModificationEvent**, tenta di passare alla modalità sessione avanzata se l'utente ha abilitato tale impostazione.</span><span class="sxs-lookup"><span data-stu-id="61a72-248">If an active vmconnection session receives an **\_\_InstanceModificationEvent**, it attempts to switch to enhanced session mode if the user enabled that setting.</span></span>

<span data-ttu-id="61a72-249">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="61a72-249">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="61a72-250">**EnhancedSessionModeState** può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="61a72-250">**EnhancedSessionModeState** can be one of these values:</span></span>

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span data-ttu-id="61a72-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Consentito e disponibile** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-251"><span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Allowed and available** (2)</span></span>


</dt> <dd>

<span data-ttu-id="61a72-252">La modalità avanzata è consentita e disponibile nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-252">Enhanced mode is allowed and available on the virtual machine.</span></span>

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span data-ttu-id="61a72-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Non consentito** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-253"><span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Not allowed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="61a72-254">La modalità avanzata non è consentita nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-254">Enhanced mode is not allowed on the virtual machine.</span></span>

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span data-ttu-id="61a72-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Consentito ma non disponibile** (6)</span><span class="sxs-lookup"><span data-stu-id="61a72-255"><span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Allowed but not available** (6)</span></span>


</dt> <dd>

<span data-ttu-id="61a72-256">La modalità avanzata è consentita e non è attualmente disponibile nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-256">Enhanced mode is allowed and but not currently available on the virtual machine.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-257">**FailedOverReplicationType**</span><span class="sxs-lookup"><span data-stu-id="61a72-257">**FailedOverReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-258">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-260">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="61a72-260">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-261">Tipo di punto dati di ripristino applicato durante l'operazione di failover.</span><span class="sxs-lookup"><span data-stu-id="61a72-261">The type of recovery data point that was applied during the failover operation.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-262">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-262">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="61a72-263">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="61a72-263">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="61a72-264">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="61a72-264">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="61a72-265">**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="61a72-265">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="61a72-266">**Coerente** con l'applicazione (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-266">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="61a72-267">**Pianificato** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-267">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-268">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="61a72-268">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-269">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-271">Specifica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="61a72-271">Specifies the current health of the element.</span></span> <span data-ttu-id="61a72-272">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-272">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="61a72-273">Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="61a72-273">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="61a72-274">La proprietà **EnabledState** può inoltre contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="61a72-274">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="61a72-275">Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).</span><span class="sxs-lookup"><span data-stu-id="61a72-275">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="61a72-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="61a72-277">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-277">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="61a72-278">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-278">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="61a72-279"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-279"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="61a72-280">La macchina virtuale è completamente funzionante e funziona entro i normali parametri operativi e senza errori.</span><span class="sxs-lookup"><span data-stu-id="61a72-280">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="61a72-281"><dt>**Errore principale**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-281"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="61a72-282">Si è verificato un errore grave della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-282">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="61a72-283">Questo valore viene usato quando lo spazio su disco di uno o più dischi che contengono i VHD della macchina virtuale è insufficiente e la macchina virtuale è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-283">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="61a72-284"><dt>**Errore critico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-284"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="61a72-285">L'elemento è non funzionale e il ripristino potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="61a72-285">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="61a72-286">Questo può indicare che il processo di lavoro della macchina virtuale (Vmwp.exe) non risponde alle richieste di controllo o informazioni oppure che uno o più dischi che contengono i dischi rigidi virtuali per la macchina virtuale hanno spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="61a72-286">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="61a72-287">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="61a72-287">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-288">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="61a72-288">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-290">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-290">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-291">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="61a72-291">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-292">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-292">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-294">Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **null**, per un sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="61a72-294">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="61a72-295">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-295">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-296">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61a72-296">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-297">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-298">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-299">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="61a72-299">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="61a72-300">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="61a72-300">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="61a72-301">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-301">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="61a72-302">In Windows 8 esiste una singola istanza di [**ReplicationSettingData**](msvm-replicationsettingdata.md) per ogni sistema di computer o macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-302">In Windows 8, there is a single instance of [**ReplicationSettingData**](msvm-replicationsettingdata.md) for every computer system or virtual machine.</span></span> <span data-ttu-id="61a72-303">Per Windows 8.1, una macchina virtuale di ripristino dispone di due istanze di **ReplicationSettingData**.</span><span class="sxs-lookup"><span data-stu-id="61a72-303">For Windows 8.1, a recovery virtual machine has two instances of **ReplicationSettingData**.</span></span> <span data-ttu-id="61a72-304">Questa modifica distingue e associa i dati all'impostazione con la relazione di replica.</span><span class="sxs-lookup"><span data-stu-id="61a72-304">This change differentiates and associates setting data with replication relationship.</span></span>



| <span data-ttu-id="61a72-305">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="61a72-305">Property name</span></span>  | <span data-ttu-id="61a72-306">Valore di Windows 8</span><span class="sxs-lookup"><span data-stu-id="61a72-306">Windows 8 value</span></span>               | <span data-ttu-id="61a72-307">Valore Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="61a72-307">Windows 8.1 value</span></span>                          |
|----------------|-------------------------------|--------------------------------------------|
| <span data-ttu-id="61a72-308">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="61a72-308">**InstanceID**</span></span> | <span data-ttu-id="61a72-309">Microsoft: <vmguid> \\ HVR</span><span class="sxs-lookup"><span data-stu-id="61a72-309">Microsoft:<vmguid>\\HVR</span></span> | <span data-ttu-id="61a72-310">Microsoft: <vmguid> \\ HVR \\<0/1></span><span class="sxs-lookup"><span data-stu-id="61a72-310">Microsoft:<vmguid>\\HVR\\<0/1></span></span> |



 

<span data-ttu-id="61a72-311">Nel valore Windows 8.1 0 indica primario e 1 indica la replica estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-311">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="61a72-312">Per ulteriori informazioni sulla replica estesa, vedere [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).</span><span class="sxs-lookup"><span data-stu-id="61a72-312">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-313">**LastApplicationConsistentReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-313">**LastApplicationConsistentReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-314">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-314">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-315">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-316">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="61a72-316">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-317">Ora in cui è stata ricevuta l'ultima replica coerente con l'applicazione per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-317">The time at which the last application-consistent replication was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-318">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-318">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="61a72-319">**LastReplicationTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-319">**LastReplicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-320">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-320">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-321">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-322">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span><span class="sxs-lookup"><span data-stu-id="61a72-322">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-323">Ora di ricezione dell'ultima replica durante il ripristino per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-323">The time at which the last replication is received on recovery for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-324">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-324">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

</dd> <dt>

<span data-ttu-id="61a72-325">**LastReplicationType**</span><span class="sxs-lookup"><span data-stu-id="61a72-325">**LastReplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-326">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-328">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span><span class="sxs-lookup"><span data-stu-id="61a72-328">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-329">Tipo dell'ultima replica ricevuta per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-329">The type of the last replication that was received for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-330">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-330">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="61a72-331">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="61a72-331">Possible values are:</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="61a72-332">**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="61a72-332">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="61a72-333">**Normale** (1)</span><span class="sxs-lookup"><span data-stu-id="61a72-333">**Regular** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="61a72-334">**Coerente** con l'applicazione (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-334">**Application consistent** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

<span data-ttu-id="61a72-335">**Pianificato** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-335">**Planned** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-336">**LastSuccessfulBackupTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-336">**LastSuccessfulBackupTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-337">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-337">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-339">Ora di completamento dell'ultimo backup riuscito per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-339">The time at which the last successful backup has completed for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-340">**Nome**</span><span class="sxs-lookup"><span data-stu-id="61a72-340">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-341">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-343">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="61a72-343">The label by which the object is known.</span></span> <span data-ttu-id="61a72-344">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="61a72-344">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="61a72-345">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="61a72-345">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-346">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-348">Stringa che identifica il modo in cui è stato generato il nome di sistema utilizzando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="61a72-348">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="61a72-349">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-349">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-350">**NumberOfNumaNodes**</span><span class="sxs-lookup"><span data-stu-id="61a72-350">**NumberOfNumaNodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-351">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-353">Numero di nodi NUMA (non-Uniform Memory Access) del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="61a72-353">The number of nonuniform memory access (NUMA) nodes of the computer system.</span></span> <span data-ttu-id="61a72-354">Quando **MSVM \_ ComputerSystem** rappresenta il computer host, questa proprietà contiene il numero di nodi NUMA fisici.</span><span class="sxs-lookup"><span data-stu-id="61a72-354">When **Msvm\_ComputerSystem** represents the hosting computer system, this property contains the count of physical NUMA nodes.</span></span> <span data-ttu-id="61a72-355">Quando **MSVM \_ ComputerSystem** rappresenta una macchina virtuale, questa proprietà contiene il numero di nodi NUMA virtuali presentati al sistema operativo guest tramite la tabella di affinità risorse di sistema ACPI (SRAT).</span><span class="sxs-lookup"><span data-stu-id="61a72-355">When **Msvm\_ComputerSystem** represents a virtual machine, this property contains the number of virtual NUMA nodes that are presented to the guest operating system through the ACPI System Resource Affinity Table (SRAT).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-356">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="61a72-356">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-357">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="61a72-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-359">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="61a72-359">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-360">Per la macchina virtuale, questa proprietà indica l'intervallo di tempo, in millisecondi, dall'ultima volta in cui è stato attivato, reimpostato o ripristinato il computer.</span><span class="sxs-lookup"><span data-stu-id="61a72-360">For the virtual machine, this property indicates the time, in milliseconds, since the machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="61a72-361">Questa volta esclude l'ora in cui la macchina virtuale è in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="61a72-361">This time excludes the time the virtual machine was in the paused state.</span></span> <span data-ttu-id="61a72-362">Per il sistema operativo di gestione, questa proprietà è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-362">For the management operating system, this property is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-363">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="61a72-363">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-364">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-364">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-366">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="61a72-366">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="61a72-367">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="61a72-367">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="61a72-368">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-368">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-369">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="61a72-369">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-370">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-372">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61a72-372">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="61a72-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="61a72-374">Il valore in corrispondenza dell'indice zero (0) corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-374">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="61a72-375">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-375">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="61a72-376">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-376">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="61a72-377"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-377"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="61a72-378">La macchina virtuale è funzionante e funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="61a72-378">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="61a72-379"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-379"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="61a72-380">La macchina virtuale è solo parzialmente funzionante.</span><span class="sxs-lookup"><span data-stu-id="61a72-380">The virtual machine is only partially functional.</span></span> <span data-ttu-id="61a72-381">Ciò indica che non è possibile accedere alla risorsa di archiviazione che contiene la configurazione.</span><span class="sxs-lookup"><span data-stu-id="61a72-381">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="61a72-382">Una macchina virtuale in questo stato può essere disattivata o eliminata.</span><span class="sxs-lookup"><span data-stu-id="61a72-382">A virtual machine in this state can only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="61a72-383"><dt>**Errore predittivo**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-383"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="61a72-384">La macchina virtuale è funzionante, ma potrebbe non riuscire in futuro.</span><span class="sxs-lookup"><span data-stu-id="61a72-384">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="61a72-385">Ciò indica che lo spazio disponibile nello spazio di archiviazione che contiene il disco rigido virtuale della macchina virtuale è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="61a72-385">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="61a72-386">La macchina virtuale verrà sospesa se non viene reso disponibile più spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="61a72-386">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="61a72-387"><dt>**Arrestato**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-387"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="61a72-388">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61a72-388">This value is not supported.</span></span> <span data-ttu-id="61a72-389">Se la macchina virtuale viene arrestata, il valore della proprietà **EnabledState** sarà 3 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="61a72-389">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="61a72-390"><dt>**Nel servizio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-390"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="61a72-391">La macchina virtuale sta elaborando una richiesta.</span><span class="sxs-lookup"><span data-stu-id="61a72-391">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="61a72-392"><dt>15</dt> <dt>**inattivo**</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-392"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="61a72-393">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="61a72-393">This value is not supported.</span></span> <span data-ttu-id="61a72-394">Se la macchina virtuale viene sospesa o sospesa, la proprietà **EnabledState** avrà il valore 32769 (Suspended) o 32768 (Paused).</span><span class="sxs-lookup"><span data-stu-id="61a72-394">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="61a72-395">Il valore in corrispondenza dell'indice uno (1) è facoltativo e contiene informazioni sullo stato secondario.</span><span class="sxs-lookup"><span data-stu-id="61a72-395">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="61a72-396">Un client deve usare lo stato primario da index zero (0) per determinare se una nuova richiesta può essere rilasciata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-396">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="61a72-397">Se **OperationalStatus** \[ 0 \] è 2 (OK), l'operazione indicata da **OperationalStatus** \[ 1 \] può essere interrotta.</span><span class="sxs-lookup"><span data-stu-id="61a72-397">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="61a72-398">Il valore in **OperationalStatus** \[ 1 \] è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-398">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="61a72-399">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-399">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="61a72-400">Significato</span><span class="sxs-lookup"><span data-stu-id="61a72-400">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="61a72-401"><dt>**Creazione dello Snapshot**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-401"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="61a72-402">È in corso la creazione di uno snapshot per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-402">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="61a72-403"><dt>**Applicazione dello Snapshot**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-403"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="61a72-404">È in corso l'applicazione di uno snapshot alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-404">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="61a72-405"><dt>**Eliminazione dello Snapshot**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-405"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="61a72-406">È in corso l'eliminazione di uno snapshot dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-406">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="61a72-407"><dt>**In attesa dell'avvio**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-407"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="61a72-408">La macchina virtuale verrà avviata dopo che è trascorso il ritardo di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="61a72-408">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="61a72-409"><dt>**Unione di dischi**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-409"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="61a72-410">I dischi rigidi virtuali degli snapshot eliminati in precedenza vengono uniti.</span><span class="sxs-lookup"><span data-stu-id="61a72-410">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="61a72-411"><dt>**Esportazione della macchina virtuale**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-411"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="61a72-412">È in corso l'esportazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-412">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="61a72-413"><dt>**Migrazione della macchina virtuale**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-413"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="61a72-414">È in corso la migrazione della macchina virtuale da un computer fisico a un altro.</span><span class="sxs-lookup"><span data-stu-id="61a72-414">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="61a72-415">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="61a72-415">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-416">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="61a72-416">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-418">Stringa che descrive come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other).</span><span class="sxs-lookup"><span data-stu-id="61a72-418">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="61a72-419">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-419">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-420">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="61a72-420">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-421">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-422">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-423">Stato abilitato o disabilitato della macchina virtuale quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="61a72-423">The enabled or disabled state of the virtual machine when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="61a72-424">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="61a72-424">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="61a72-425">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-425">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-426">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="61a72-426">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-427">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="61a72-427">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-428">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-429">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-429">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-430">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="61a72-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-431">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-432">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-433">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="61a72-433">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-434">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="61a72-434">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-435">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-435">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-437">Stringa che indica come è possibile raggiungere il proprietario del sistema primario (ad esempio, un numero di telefono o un indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="61a72-437">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="61a72-438">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-438">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-439">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="61a72-439">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-440">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-442">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="61a72-442">The name of the primary system owner.</span></span> <span data-ttu-id="61a72-443">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-443">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-444">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="61a72-444">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-445">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-445">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-447">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="61a72-447">Provides high level status information.</span></span> <span data-ttu-id="61a72-448">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-448">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="61a72-449">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="61a72-449">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="61a72-450">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-450">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-451">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="61a72-451">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-452">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61a72-452">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-453">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-454">Identificatore del processo in cui è in esecuzione la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-454">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="61a72-455">Questo valore può essere utilizzato per identificare in modo univoco l'istanza di Vmwp.exe nel sistema che esegue la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-455">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-456">**ReplicationHealth**</span><span class="sxs-lookup"><span data-stu-id="61a72-456">**ReplicationHealth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-457">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-458">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-459">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span><span class="sxs-lookup"><span data-stu-id="61a72-459">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-460">Stato di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-460">The replication health for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-461">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-461">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="61a72-462">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="61a72-462">Possible values are:</span></span>

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="61a72-463">**Non applicabile** (0)</span><span class="sxs-lookup"><span data-stu-id="61a72-463">**Not applicable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

<span data-ttu-id="61a72-464">**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="61a72-464">**Ok** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="61a72-465">**Avviso** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-465">**Warning** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="61a72-466">**Critico** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-466">**Critical** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-467">**ReplicationMode**</span><span class="sxs-lookup"><span data-stu-id="61a72-467">**ReplicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-468">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-468">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-469">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-470">Specifica la modalità di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-470">Specifies the replication mode for the virtual machine.</span></span> <span data-ttu-id="61a72-471">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="61a72-471">This will be one of the following values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="61a72-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)</span><span class="sxs-lookup"><span data-stu-id="61a72-472"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="61a72-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primario** (1)</span><span class="sxs-lookup"><span data-stu-id="61a72-473"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span data-ttu-id="61a72-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-474"><span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Replica** (2)</span></span>


</dt> <dd>

<span data-ttu-id="61a72-475">Ripristino</span><span class="sxs-lookup"><span data-stu-id="61a72-475">Recovery</span></span>

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span data-ttu-id="61a72-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Replica di test** (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-476"><span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Test Replica** (3)</span></span>


</dt> <dd>

<span data-ttu-id="61a72-477">Replica</span><span class="sxs-lookup"><span data-stu-id="61a72-477">Replica</span></span>

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span data-ttu-id="61a72-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Replica estesa** (4)</span><span class="sxs-lookup"><span data-stu-id="61a72-478"><span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Extended Replica** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-479">**ReplicationState**</span><span class="sxs-lookup"><span data-stu-id="61a72-479">**ReplicationState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-480">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-480">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-482">Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span><span class="sxs-lookup"><span data-stu-id="61a72-482">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-483">Stato di replica per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-483">The replication state for the virtual machine.</span></span>

> [!Note]  
> <span data-ttu-id="61a72-484">Questa proprietà è deprecata a partire da Windows 8.1; usare invece la proprietà con lo stesso nome nella classe [**\_ ReplicationRelationship di MSVM**](msvm-replicationrelationship.md) per ottenere il valore per la relazione primaria o estesa.</span><span class="sxs-lookup"><span data-stu-id="61a72-484">This property is deprecated starting with Windows 8.1; instead, use the property of the same name in the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to get the value for the primary or extended relationship.</span></span>

 

<span data-ttu-id="61a72-485">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="61a72-485">Possible values are:</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="61a72-486">**Disabilitato** (0)</span><span class="sxs-lookup"><span data-stu-id="61a72-486">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span data-ttu-id="61a72-487">**Pronto per la replica** (1)</span><span class="sxs-lookup"><span data-stu-id="61a72-487">**Ready for replication** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span data-ttu-id="61a72-488">**In attesa del completamento della replica iniziale** (2)</span><span class="sxs-lookup"><span data-stu-id="61a72-488">**Waiting to complete initial replication** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span data-ttu-id="61a72-489">**Replica** in corso (3)</span><span class="sxs-lookup"><span data-stu-id="61a72-489">**Replicating** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span data-ttu-id="61a72-490">**Replica sincronizzata completata** (4)</span><span class="sxs-lookup"><span data-stu-id="61a72-490">**Synced replication complete** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span data-ttu-id="61a72-491">**Ripristino** (5)</span><span class="sxs-lookup"><span data-stu-id="61a72-491">**Recovered** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span data-ttu-id="61a72-492">**Commit eseguito** (6)</span><span class="sxs-lookup"><span data-stu-id="61a72-492">**Committed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span data-ttu-id="61a72-493">**Sospeso** (7)</span><span class="sxs-lookup"><span data-stu-id="61a72-493">**Suspended** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="61a72-494">**Critico** (8)</span><span class="sxs-lookup"><span data-stu-id="61a72-494">**Critical** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span data-ttu-id="61a72-495">**In attesa dell'avvio della risincronizzazione** (9)</span><span class="sxs-lookup"><span data-stu-id="61a72-495">**Waiting to start resynchronization** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span data-ttu-id="61a72-496">**Risincronizzazione** (10)</span><span class="sxs-lookup"><span data-stu-id="61a72-496">**Resynchronizing** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span data-ttu-id="61a72-497">**Risincronizzazione sospesa** (11)</span><span class="sxs-lookup"><span data-stu-id="61a72-497">**Resynchronization suspended** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span data-ttu-id="61a72-498">**Failover in corso** (12)</span><span class="sxs-lookup"><span data-stu-id="61a72-498">**Failover in progress** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span data-ttu-id="61a72-499">**Failback in corso** (13)</span><span class="sxs-lookup"><span data-stu-id="61a72-499">**Failback in progress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span data-ttu-id="61a72-500">**Failback completato** (14)</span><span class="sxs-lookup"><span data-stu-id="61a72-500">**Failback complete** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="61a72-501">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="61a72-501">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-502">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-503">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-504">Ultimo stato richiesto o desiderato per la macchina virtuale passato al metodo [**RequestStateChange**](requeststatechange-msvm-computersystem.md) oppure 12 (non applicabile) se non è in corso alcuna modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="61a72-504">The last requested or desired state for the virtual machine as passed to the [**RequestStateChange**](requeststatechange-msvm-computersystem.md) method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="61a72-505">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="61a72-505">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="61a72-506">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="61a72-506">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="61a72-507">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61a72-507">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-508">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="61a72-508">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-509">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-509">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-510">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-511">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="61a72-511">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-512">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="61a72-512">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-513">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="61a72-513">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-514">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-515">Matrice di stringhe che descrivono i ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="61a72-515">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="61a72-516">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="61a72-516">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-517">**Status**</span><span class="sxs-lookup"><span data-stu-id="61a72-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-518">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="61a72-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-519">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-520">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="61a72-520">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-521">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="61a72-521">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-522">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="61a72-522">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="61a72-523">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61a72-524">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="61a72-524">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="61a72-525">Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="61a72-525">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="61a72-526">Se ad esempio 11 (in servizio) è il valore assegnato a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] può contenere una spiegazione del motivo per cui la macchina virtuale sta elaborando una richiesta.</span><span class="sxs-lookup"><span data-stu-id="61a72-526">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="61a72-527">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="61a72-527">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-528">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="61a72-528">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-529">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-530">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-531">Data e ora dell'Ultima modifica del file di configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61a72-531">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="61a72-532">Il file di configurazione viene modificato durante determinate operazioni della macchina virtuale, nonché quando vengono aggiunte, modificate o rimosse le impostazioni della macchina virtuale o del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61a72-532">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="61a72-533">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="61a72-533">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-534">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="61a72-534">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-535">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-536">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="61a72-536">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="61a72-537">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="61a72-537">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="61a72-538">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="61a72-538">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61a72-539">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="61a72-539">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="61a72-540">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="61a72-540">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61a72-541">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="61a72-541">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="61a72-542">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="61a72-542">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61a72-543">Commenti</span><span class="sxs-lookup"><span data-stu-id="61a72-543">Remarks</span></span>

<span data-ttu-id="61a72-544">Nella figura seguente vengono mostrati i valori **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="61a72-544">The following illustration shows the **EnabledState** values.</span></span>

![diagramma di stato per i valori EnabledState per Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

<span data-ttu-id="61a72-546">Quando viene modificata una proprietà della classe **MSVM \_ ComputerSystem** , il provider WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) che descrive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="61a72-546">When a property of the **Msvm\_ComputerSystem** class changes, the WMI provider indicates an [**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) event that describes the changes.</span></span> <span data-ttu-id="61a72-547">Lo stato precedente è contenuto nella proprietà **PreviousInstance** e il nuovo stato è contenuto nella proprietà **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="61a72-547">The previous state is contained in the **PreviousInstance** property, and the new state is contained in the **TargetInstance** property.</span></span> <span data-ttu-id="61a72-548">Questo evento è asincrono. al momento dell'elaborazione dell'evento **\_ \_ InstanceModificationEvent** , è possibile che la proprietà **TargetInstance** non rifletta lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="61a72-548">This event is asynchronous; by the time the **\_\_InstanceModificationEvent** event is processed, the **TargetInstance** property may not reflect the current state.</span></span>

<span data-ttu-id="61a72-549">L'accesso alla **classe \_ ComputerSystem di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="61a72-549">Access to the **Msvm\_ComputerSystem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="61a72-550">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="61a72-550">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="61a72-551">Esempio</span><span class="sxs-lookup"><span data-stu-id="61a72-551">Examples</span></span>

<span data-ttu-id="61a72-552">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="61a72-552">See [Querying Networking Objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61a72-553">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61a72-553">Requirements</span></span>



| <span data-ttu-id="61a72-554">Requisito</span><span class="sxs-lookup"><span data-stu-id="61a72-554">Requirement</span></span> | <span data-ttu-id="61a72-555">Valore</span><span class="sxs-lookup"><span data-stu-id="61a72-555">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a72-556">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a72-556">Minimum supported client</span></span><br/> | <span data-ttu-id="61a72-557">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61a72-557">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="61a72-558">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61a72-558">Minimum supported server</span></span><br/> | <span data-ttu-id="61a72-559">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61a72-559">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61a72-560">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="61a72-560">Namespace</span></span><br/>                | <span data-ttu-id="61a72-561">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="61a72-561">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="61a72-562">MOF</span><span class="sxs-lookup"><span data-stu-id="61a72-562">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61a72-563"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-563"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61a72-564">DLL</span><span class="sxs-lookup"><span data-stu-id="61a72-564">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61a72-565"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61a72-565"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61a72-566">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61a72-566">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a72-567">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="61a72-567">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="61a72-568">**\_\_InstanceModificationEvent**</span><span class="sxs-lookup"><span data-stu-id="61a72-568">**\_\_InstanceModificationEvent**</span></span>](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[<span data-ttu-id="61a72-569">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="61a72-569">**CIM\_ComputerSystem**</span></span>](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[<span data-ttu-id="61a72-570">**MSVM \_ ComputerSystem (V1)**</span><span class="sxs-lookup"><span data-stu-id="61a72-570">**Msvm\_ComputerSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[<span data-ttu-id="61a72-571">Classi di sistema virtuali</span><span class="sxs-lookup"><span data-stu-id="61a72-571">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

