---
description: Rappresenta lo stato del servizio di arresto, che fornisce un meccanismo per arrestare il sistema operativo della macchina virtuale dalle interfacce di gestione nel sistema host.
ms.assetid: E9BBB08C-A3FE-4226-A2CF-458706E759D6
title: Classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent
- Msvm_ShutdownComponent.EnableDevice
- Msvm_ShutdownComponent.OnlineDevice
- Msvm_ShutdownComponent.QuiesceDevice
- Msvm_ShutdownComponent.RestoreProperties
- Msvm_ShutdownComponent.SaveProperties
- Msvm_ShutdownComponent.SetPowerState
- Msvm_ShutdownComponent.InstanceID
- Msvm_ShutdownComponent.Caption
- Msvm_ShutdownComponent.Description
- Msvm_ShutdownComponent.ElementName
- Msvm_ShutdownComponent.InstallDate
- Msvm_ShutdownComponent.Name
- Msvm_ShutdownComponent.OperationalStatus
- Msvm_ShutdownComponent.StatusDescriptions
- Msvm_ShutdownComponent.Status
- Msvm_ShutdownComponent.HealthState
- Msvm_ShutdownComponent.CommunicationStatus
- Msvm_ShutdownComponent.DetailedStatus
- Msvm_ShutdownComponent.OperatingStatus
- Msvm_ShutdownComponent.PrimaryStatus
- Msvm_ShutdownComponent.EnabledState
- Msvm_ShutdownComponent.OtherEnabledState
- Msvm_ShutdownComponent.RequestedState
- Msvm_ShutdownComponent.EnabledDefault
- Msvm_ShutdownComponent.TimeOfLastStateChange
- Msvm_ShutdownComponent.AvailableRequestedStates
- Msvm_ShutdownComponent.TransitioningToState
- Msvm_ShutdownComponent.SystemCreationClassName
- Msvm_ShutdownComponent.SystemName
- Msvm_ShutdownComponent.CreationClassName
- Msvm_ShutdownComponent.DeviceID
- Msvm_ShutdownComponent.PowerManagementSupported
- Msvm_ShutdownComponent.PowerManagementCapabilities
- Msvm_ShutdownComponent.Availability
- Msvm_ShutdownComponent.StatusInfo
- Msvm_ShutdownComponent.LastErrorCode
- Msvm_ShutdownComponent.ErrorDescription
- Msvm_ShutdownComponent.ErrorCleared
- Msvm_ShutdownComponent.OtherIdentifyingInfo
- Msvm_ShutdownComponent.PowerOnHours
- Msvm_ShutdownComponent.TotalPowerOnHours
- Msvm_ShutdownComponent.IdentifyingDescriptions
- Msvm_ShutdownComponent.AdditionalAvailability
- Msvm_ShutdownComponent.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 49729568a1625b3df723b1b5b88cc1044b41e715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049706"
---
# <a name="msvm_shutdowncomponent-class"></a><span data-ttu-id="8f234-103">\_Classe MSVM ShutdownComponent</span><span class="sxs-lookup"><span data-stu-id="8f234-103">Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="8f234-104">Rappresenta lo stato del servizio di arresto, che fornisce un meccanismo per arrestare il sistema operativo della macchina virtuale dalle interfacce di gestione nel sistema host.</span><span class="sxs-lookup"><span data-stu-id="8f234-104">Represents the state of the shutdown service, which provides a mechanism to shut down the operating system of the virtual machine from the management interfaces on the host system.</span></span>

<span data-ttu-id="8f234-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8f234-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f234-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f234-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ShutdownComponent : CIM_LogicalDevice
{
  string   InstanceID;
  string   Caption = "Shutdown";
  string   Description = "Microsoft Shutdown Service";
  string   ElementName = "Shutdown";
  datetime InstallDate;
  string   Name = "Shutdown";
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
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
  string   CreationClassName = "Msvm_ShutdownComponent";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
};
```

## <a name="members"></a><span data-ttu-id="8f234-107">Members</span><span class="sxs-lookup"><span data-stu-id="8f234-107">Members</span></span>

<span data-ttu-id="8f234-108">La **classe \_ ShutdownComponent di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8f234-108">The **Msvm\_ShutdownComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="8f234-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f234-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="8f234-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f234-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8f234-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f234-111">Methods</span></span>

<span data-ttu-id="8f234-112">La **classe \_ ShutdownComponent di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="8f234-112">The **Msvm\_ShutdownComponent** class has these methods.</span></span>



| <span data-ttu-id="8f234-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="8f234-113">Method</span></span>                                                                  | <span data-ttu-id="8f234-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f234-114">Description</span></span>                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f234-115">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="8f234-115">**EnableDevice**</span></span>                                                        | <span data-ttu-id="8f234-116">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-116">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="8f234-117">**InitiateReboot**</span><span class="sxs-lookup"><span data-stu-id="8f234-117">**InitiateReboot**</span></span>](msvm-shutdowncomponent-initiatereboot.md)         | <span data-ttu-id="8f234-118">Avvia un'operazione di riavvio del sistema operativo sulla macchina virtuale figlio associata.</span><span class="sxs-lookup"><span data-stu-id="8f234-118">Initiates an operating system reboot operation on the associated child virtual machine.</span></span><br/> |
| [<span data-ttu-id="8f234-119">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="8f234-119">**InitiateShutdown**</span></span>](msvm-shutdowncomponent-initiateshutdown.md)     | <span data-ttu-id="8f234-120">Avvia un'operazione di arresto del sistema operativo sulla macchina virtuale figlio associata.</span><span class="sxs-lookup"><span data-stu-id="8f234-120">Initiates an operating system shutdown operation on associated child virtual machine.</span></span><br/>   |
| <span data-ttu-id="8f234-121">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="8f234-121">**OnlineDevice**</span></span>                                                        | <span data-ttu-id="8f234-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-122">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="8f234-123">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="8f234-123">**QuiesceDevice**</span></span>                                                       | <span data-ttu-id="8f234-124">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-124">This method is not supported.</span></span><br/>                                                           |
| [<span data-ttu-id="8f234-125">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="8f234-125">**RequestStateChange**</span></span>](msvm-shutdowncomponent-requeststatechange.md) | <span data-ttu-id="8f234-126">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="8f234-126">Requests a state change.</span></span><br/>                                                                |
| [<span data-ttu-id="8f234-127">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8f234-127">**Reset**</span></span>](msvm-shutdowncomponent-reset.md)                           | <span data-ttu-id="8f234-128">Reimposta il componente.</span><span class="sxs-lookup"><span data-stu-id="8f234-128">Resets the component.</span></span><br/>                                                                   |
| <span data-ttu-id="8f234-129">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="8f234-129">**RestoreProperties**</span></span>                                                   | <span data-ttu-id="8f234-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-130">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="8f234-131">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="8f234-131">**SaveProperties**</span></span>                                                      | <span data-ttu-id="8f234-132">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-132">This method is not supported.</span></span><br/>                                                           |
| <span data-ttu-id="8f234-133">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8f234-133">**SetPowerState**</span></span>                                                       | <span data-ttu-id="8f234-134">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="8f234-134">This method is not supported.</span></span><br/>                                                           |



 

### <a name="properties"></a><span data-ttu-id="8f234-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f234-135">Properties</span></span>

<span data-ttu-id="8f234-136">La **classe \_ ShutdownComponent di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8f234-136">The **Msvm\_ShutdownComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f234-137">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="8f234-137">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-138">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-138">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-140">Disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f234-140">Additional availability and status of the device.</span></span> <span data-ttu-id="8f234-141">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8f234-141">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="8f234-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-142">Value</span></span>                                                                        | <span data-ttu-id="8f234-143">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-143">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8f234-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-144"><dt>6</dt></span></span> </dl> | <span data-ttu-id="8f234-145">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8f234-145">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f234-146">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="8f234-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-149">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f234-149">The primary availability and status of the device.</span></span> <span data-ttu-id="8f234-150">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-150">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>



| <span data-ttu-id="8f234-151">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-151">Value</span></span>                                                                        | <span data-ttu-id="8f234-152">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-152">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8f234-153"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-153"><dt>6</dt></span></span> </dl> | <span data-ttu-id="8f234-154">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8f234-154">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f234-155">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="8f234-155">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-156">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-156">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-158">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="8f234-158">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="8f234-159">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-159">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-160">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="8f234-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-163">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f234-163">A short description of the object.</span></span> <span data-ttu-id="8f234-164">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8f234-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-168">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="8f234-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8f234-169">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8f234-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8f234-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8f234-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8f234-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="8f234-172"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="8f234-173"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="8f234-174"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="8f234-175"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8f234-176"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8f234-177"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8f234-178">)</span><span class="sxs-lookup"><span data-stu-id="8f234-178">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f234-179">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f234-179">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-180">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-181">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-182">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8f234-182">The scoping system's creation class name.</span></span> <span data-ttu-id="8f234-183">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8f234-183">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-184">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="8f234-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-187">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="8f234-187">A description of the object.</span></span> <span data-ttu-id="8f234-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8f234-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-192">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="8f234-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8f234-193">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8f234-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8f234-194">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8f234-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="8f234-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="8f234-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="8f234-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="8f234-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="8f234-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="8f234-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8f234-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8f234-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8f234-203">)</span><span class="sxs-lookup"><span data-stu-id="8f234-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f234-204">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8f234-204">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-205">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-207">Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco a LogicalDevice.</span><span class="sxs-lookup"><span data-stu-id="8f234-207">An address or other identifying information to uniquely name the LogicalDevice.</span></span> <span data-ttu-id="8f234-208">Questa proprietà viene ereditata [**da CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft:*VMGUID* \\ *GUID*", dove *VMGUID* è la proprietà **Name** dell'istanza [**MSVM \_ ComputerSystem**](msvm-computersystem.md) associata a questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f234-208">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*VMGUID*\\*GUID*" where *VMGUID* is the **Name** property of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) instance associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-209">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8f234-209">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-212">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f234-212">A display name for the object.</span></span> <span data-ttu-id="8f234-213">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-213">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-214">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="8f234-214">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-215">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-215">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-217">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f234-217">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="8f234-218">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-218">Value</span></span>                                                                        | <span data-ttu-id="8f234-219">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-219">Meaning</span></span>               |
|------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="8f234-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-220"><dt>7</dt></span></span> </dl> | <span data-ttu-id="8f234-221">Nessun valore predefinito</span><span class="sxs-lookup"><span data-stu-id="8f234-221">No Default</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f234-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="8f234-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-225">Stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f234-225">The enabled state of the element.</span></span> <span data-ttu-id="8f234-226">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e viene impostata su 2 (Enabled) o 3 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="8f234-226">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is either set to 2 (Enabled) or 3 (Disabled).</span></span>



| <span data-ttu-id="8f234-227">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-227">Value</span></span>                                                                        | <span data-ttu-id="8f234-228">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-228">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="8f234-229"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-229"><dt>2</dt></span></span> </dl> | <span data-ttu-id="8f234-230">Abilitato</span><span class="sxs-lookup"><span data-stu-id="8f234-230">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="8f234-231"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-231"><dt>3</dt></span></span> </dl> | <span data-ttu-id="8f234-232">Disabled</span><span class="sxs-lookup"><span data-stu-id="8f234-232">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f234-233">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="8f234-233">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-234">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f234-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-236">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="8f234-236">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="8f234-237">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-237">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-238">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8f234-238">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-241">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="8f234-241">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="8f234-242">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-242">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-243">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8f234-243">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-244">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-244">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-245">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-246">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f234-246">The current health of the element.</span></span> <span data-ttu-id="8f234-247">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="8f234-247">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="8f234-248">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-248">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-249">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8f234-249">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-250">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8f234-250">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-252">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="8f234-252">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="8f234-253">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-254">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8f234-254">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-255">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f234-255">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-257">Data e ora in cui il servizio di integrazione è stato installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8f234-257">The date and time that the integration service was installed into the virtual machine.</span></span> <span data-ttu-id="8f234-258">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-258">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-259">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8f234-259">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8f234-262">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="8f234-262">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8f234-263">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="8f234-263">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8f234-264">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-264">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-265">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="8f234-265">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-266">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8f234-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-267">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-268">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8f234-268">The last error code reported by the logical device.</span></span> <span data-ttu-id="8f234-269">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-269">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-270">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="8f234-270">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-271">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f234-271">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-273">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="8f234-273">This property has been deprecated.</span></span> <span data-ttu-id="8f234-274">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8f234-274">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-275">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8f234-275">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-276">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-277">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-278">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="8f234-278">The label by which the object is known.</span></span> <span data-ttu-id="8f234-279">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-279">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-280">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8f234-280">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-281">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-283">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8f234-283">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8f234-284">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8f234-284">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8f234-285">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-285">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8f234-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8f234-286"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="8f234-287"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="8f234-288"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="8f234-289"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="8f234-290"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="8f234-291"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="8f234-292"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="8f234-293"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="8f234-294"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="8f234-295"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="8f234-296"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="8f234-297"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="8f234-298"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="8f234-299"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="8f234-300"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="8f234-301"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="8f234-302"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8f234-303"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8f234-304"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8f234-305">)</span><span class="sxs-lookup"><span data-stu-id="8f234-305">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f234-306">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8f234-306">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-307">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-307">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-309">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f234-309">The current status of the element.</span></span> <span data-ttu-id="8f234-310">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-310">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="8f234-311">Di seguito sono riportati i valori possibili per il valore della proprietà **OperationalStatus** \[ 0 \] .</span><span class="sxs-lookup"><span data-stu-id="8f234-311">The following are the possible values for the **OperationalStatus**\[0\] property value.</span></span>



| <span data-ttu-id="8f234-312">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-312">Value</span></span>                                                                                                                                                                                                                                                                               | <span data-ttu-id="8f234-313">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-313">Meaning</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="8f234-314"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-314"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                                  | <span data-ttu-id="8f234-315">Il servizio funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="8f234-315">The service is operating normally.</span></span> <span data-ttu-id="8f234-316">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f234-316">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                                               |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="8f234-317"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-317"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                                     | <span data-ttu-id="8f234-318">Il servizio funziona normalmente, ma il servizio Guest ha negoziato una versione del protocollo di comunicazione compatibile.</span><span class="sxs-lookup"><span data-stu-id="8f234-318">The service is operating normally but the guest service negotiated a compatible communications protocol version.</span></span> <span data-ttu-id="8f234-319">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f234-319">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/> |
| <span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span><dl> <span data-ttu-id="8f234-320"><dt>**Errore irreversibile**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-320"><dt>**Non-Recoverable Error**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="8f234-321">Il Guest non supporta una versione del protocollo compatibile.</span><span class="sxs-lookup"><span data-stu-id="8f234-321">The guest does not support a compatible protocol version.</span></span> <span data-ttu-id="8f234-322">I  \[ valori delle \] proprietà OperationalStatus 1 e **StatusDescriptions** \[ 1 \] possono contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="8f234-322">The **OperationalStatus**\[1\] and **StatusDescriptions**\[1\] property values may contain more information.</span></span><br/>                                                        |
| <span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dl> <span data-ttu-id="8f234-323"><dt>**Nessun contatto**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-323"><dt>**No Contact**</dt> <dt>12</dt></span></span> </dl>                                            | <span data-ttu-id="8f234-324">Il servizio Guest non è installato o non è stato ancora contattato.</span><span class="sxs-lookup"><span data-stu-id="8f234-324">The guest service is not installed or has not yet been contacted.</span></span><br/>                                                                                                                                                             |
| <span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span><dl> <span data-ttu-id="8f234-325"><dt>**Perdita di comunicazione**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-325"><dt>**Lost Communication**</dt> <dt>13</dt></span></span> </dl>            | <span data-ttu-id="8f234-326">Il servizio Guest non risponde più normalmente.</span><span class="sxs-lookup"><span data-stu-id="8f234-326">The guest service is no longer responding normally.</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8f234-327">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="8f234-327">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-328">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-329">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-329">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-330">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="8f234-330">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="8f234-331">Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="8f234-331">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="8f234-332">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f234-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-333">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="8f234-333">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-334">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8f234-334">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-336">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8f234-336">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="8f234-337">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="8f234-337">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) and is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-338">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="8f234-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-339">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-341">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f234-341">The power management capabilities of the device.</span></span> <span data-ttu-id="8f234-342">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-342">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-343">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="8f234-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-344">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="8f234-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-346">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="8f234-346">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="8f234-347">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-347">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-348">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8f234-348">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-349">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f234-349">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-350">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-351">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="8f234-351">The number of consecutive hours that this Device has been powered on since its last power cycle.</span></span> <span data-ttu-id="8f234-352">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-352">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-353">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8f234-353">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-354">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-354">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-356">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="8f234-356">Provides high level status information.</span></span> <span data-ttu-id="8f234-357">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="8f234-357">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="8f234-358">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="8f234-358">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8f234-359">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-359">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="8f234-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="8f234-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="8f234-361"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="8f234-362"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="8f234-363"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="8f234-364"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8f234-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="8f234-365"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="8f234-366">)</span><span class="sxs-lookup"><span data-stu-id="8f234-366">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8f234-367">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="8f234-367">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-368">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-370">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f234-370">The last requested or desired state for the element.</span></span> <span data-ttu-id="8f234-371">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="8f234-371">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="8f234-372">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="8f234-372">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="8f234-373">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="8f234-373">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="8f234-374">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-374">Value</span></span>                                                                         | <span data-ttu-id="8f234-375">Significato</span><span class="sxs-lookup"><span data-stu-id="8f234-375">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="8f234-376"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-376"><dt>12</dt></span></span> </dl> | <span data-ttu-id="8f234-377">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="8f234-377">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8f234-378">**Status**</span><span class="sxs-lookup"><span data-stu-id="8f234-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-379">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-380">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-381">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8f234-381">The current status of the object.</span></span> <span data-ttu-id="8f234-382">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-382">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) but is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-383">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8f234-383">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-384">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="8f234-384">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8f234-385">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-386">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="8f234-386">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="8f234-387">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8f234-387">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-388">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8f234-388">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-389">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-390">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-391">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="8f234-391">The current state of the logical device.</span></span> <span data-ttu-id="8f234-392">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-392">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-393">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8f234-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-394">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-395">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-396">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="8f234-396">The scoping system's creation class name.</span></span> <span data-ttu-id="8f234-397">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8f234-397">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-398">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8f234-398">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-399">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="8f234-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-400">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-401">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="8f234-401">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="8f234-402">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="8f234-402">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="8f234-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-404">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8f234-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-405">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-406">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="8f234-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="8f234-407">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f234-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8f234-408">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="8f234-408">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-409">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8f234-409">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-410">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-411">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="8f234-411">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="8f234-412">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f234-413">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="8f234-413">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f234-414">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8f234-414">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8f234-415">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f234-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f234-416">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8f234-416">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="8f234-417">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8f234-417">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f234-418">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f234-418">Remarks</span></span>

<span data-ttu-id="8f234-419">L'accesso alla **classe \_ ShutdownComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="8f234-419">Access to the **Msvm\_ShutdownComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8f234-420">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8f234-420">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f234-421">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f234-421">Requirements</span></span>



| <span data-ttu-id="8f234-422">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f234-422">Requirement</span></span> | <span data-ttu-id="8f234-423">Valore</span><span class="sxs-lookup"><span data-stu-id="8f234-423">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f234-424">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f234-424">Minimum supported client</span></span><br/> | <span data-ttu-id="8f234-425">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8f234-425">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8f234-426">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f234-426">Minimum supported server</span></span><br/> | <span data-ttu-id="8f234-427">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8f234-427">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f234-428">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f234-428">Namespace</span></span><br/>                | <span data-ttu-id="8f234-429">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8f234-429">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8f234-430">MOF</span><span class="sxs-lookup"><span data-stu-id="8f234-430">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f234-431"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-431"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f234-432">DLL</span><span class="sxs-lookup"><span data-stu-id="8f234-432">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f234-433"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8f234-433"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8f234-434">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f234-434">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f234-435">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8f234-435">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="8f234-436">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="8f234-436">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

