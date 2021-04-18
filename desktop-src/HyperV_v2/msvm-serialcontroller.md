---
description: Rappresenta le funzionalità e la gestione del controller seriale.
ms.assetid: 0F4DCF98-8EE4-4005-ADD5-BA23CB4CBE82
title: Classe Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController
- Msvm_SerialController.SetPowerState
- Msvm_SerialController.EnableDevice
- Msvm_SerialController.OnlineDevice
- Msvm_SerialController.QuiesceDevice
- Msvm_SerialController.SaveProperties
- Msvm_SerialController.RestoreProperties
- Msvm_SerialController.InstanceID
- Msvm_SerialController.Caption
- Msvm_SerialController.Description
- Msvm_SerialController.ElementName
- Msvm_SerialController.InstallDate
- Msvm_SerialController.Name
- Msvm_SerialController.OperationalStatus
- Msvm_SerialController.StatusDescriptions
- Msvm_SerialController.Status
- Msvm_SerialController.HealthState
- Msvm_SerialController.CommunicationStatus
- Msvm_SerialController.DetailedStatus
- Msvm_SerialController.OperatingStatus
- Msvm_SerialController.PrimaryStatus
- Msvm_SerialController.EnabledState
- Msvm_SerialController.OtherEnabledState
- Msvm_SerialController.RequestedState
- Msvm_SerialController.EnabledDefault
- Msvm_SerialController.TimeOfLastStateChange
- Msvm_SerialController.AvailableRequestedStates
- Msvm_SerialController.TransitioningToState
- Msvm_SerialController.SystemCreationClassName
- Msvm_SerialController.SystemName
- Msvm_SerialController.CreationClassName
- Msvm_SerialController.DeviceID
- Msvm_SerialController.PowerManagementSupported
- Msvm_SerialController.PowerManagementCapabilities
- Msvm_SerialController.Availability
- Msvm_SerialController.StatusInfo
- Msvm_SerialController.LastErrorCode
- Msvm_SerialController.ErrorDescription
- Msvm_SerialController.ErrorCleared
- Msvm_SerialController.OtherIdentifyingInfo
- Msvm_SerialController.PowerOnHours
- Msvm_SerialController.TotalPowerOnHours
- Msvm_SerialController.IdentifyingDescriptions
- Msvm_SerialController.AdditionalAvailability
- Msvm_SerialController.MaxQuiesceTime
- Msvm_SerialController.TimeOfLastReset
- Msvm_SerialController.ProtocolSupported
- Msvm_SerialController.MaxNumberControlled
- Msvm_SerialController.ProtocolDescription
- Msvm_SerialController.Capabilities
- Msvm_SerialController.CapabilityDescriptions
- Msvm_SerialController.MaxBaudRate
- Msvm_SerialController.Security
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3f1bbc9dabe078751d58875745a789895cb4c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308210"
---
# <a name="msvm_serialcontroller-class"></a><span data-ttu-id="cd9ce-103">\_Classe MSVM controller seriale</span><span class="sxs-lookup"><span data-stu-id="cd9ce-103">Msvm\_SerialController class</span></span>

<span data-ttu-id="cd9ce-104">Rappresenta le funzionalità e la gestione del controller seriale.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-104">Represents the capabilities and management of the serial controller.</span></span> <span data-ttu-id="cd9ce-105">I controller seriale sono dispositivi logici che sono sempre presenti in una macchina virtuale e pertanto non vengono allocati tramite un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-105">Serial controllers are logical devices that are always present in a virtual machine, and thus are not allocated through a resource pool.</span></span> <span data-ttu-id="cd9ce-106">Un'istanza del controller seriale è sempre presente in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-106">One serial controller instance is always present in a virtual machine.</span></span> <span data-ttu-id="cd9ce-107">I controller seriali hanno un numero fisso di istanze di porte.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-107">Serial controllers have a fixed number of port instances.</span></span> <span data-ttu-id="cd9ce-108">Questa implementazione supporta due porte per controller.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-108">This implementation supports two ports per controller.</span></span>

> [!Note]  
> <span data-ttu-id="cd9ce-109">I controller seriali sono facoltativi nelle [macchine virtuali di seconda generazione](virtualization-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-109">Serial controllers are optional in [generation 2 virtual machines](virtualization-glossary.md).</span></span>

 

<span data-ttu-id="cd9ce-110">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-110">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9ce-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd9ce-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialController : CIM_SerialController
{
  string   InstanceID;
  string   Caption = "Serial Controller";
  string   Description = "Microsoft Virtual Serial Controller";
  string   ElementName = "Serial Controller";
  datetime InstallDate;
  string   Name = "Serial Controller";
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
  string   CreationClassName = "Msvm_SerialController";
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
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 26;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription;
  uint16   Capabilities[] = { 5 };
  string   CapabilityDescriptions[] = { "16550 compatible" };
  uint32   MaxBaudRate = 115200;
  uint16   Security = 3;
};
```

## <a name="members"></a><span data-ttu-id="cd9ce-112">Members</span><span class="sxs-lookup"><span data-stu-id="cd9ce-112">Members</span></span>

<span data-ttu-id="cd9ce-113">La **classe \_ controller seriale di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cd9ce-113">The **Msvm\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="cd9ce-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd9ce-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cd9ce-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd9ce-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cd9ce-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="cd9ce-116">Methods</span></span>

<span data-ttu-id="cd9ce-117">La **classe \_ controller seriale di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-117">The **Msvm\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="cd9ce-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="cd9ce-118">Method</span></span>                                                                 | <span data-ttu-id="cd9ce-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd9ce-119">Description</span></span>                              |
|:-----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="cd9ce-120">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-120">**EnableDevice**</span></span>                                                       | <span data-ttu-id="cd9ce-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd9ce-122">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-122">**OnlineDevice**</span></span>                                                       | <span data-ttu-id="cd9ce-123">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-123">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd9ce-124">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-124">**QuiesceDevice**</span></span>                                                      | <span data-ttu-id="cd9ce-125">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-125">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="cd9ce-126">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-126">**RequestStateChange**</span></span>](msvm-serialcontroller-requeststatechange.md) | <span data-ttu-id="cd9ce-127">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-127">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="cd9ce-128">**Reset**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-128">**Reset**</span></span>](msvm-serialcontroller-reset.md)                           | <span data-ttu-id="cd9ce-129">Reimposta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-129">Resets the device.</span></span><br/>            |
| <span data-ttu-id="cd9ce-130">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-130">**RestoreProperties**</span></span>                                                  | <span data-ttu-id="cd9ce-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd9ce-132">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-132">**SaveProperties**</span></span>                                                     | <span data-ttu-id="cd9ce-133">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-133">This method is not supported.</span></span><br/> |
| <span data-ttu-id="cd9ce-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-134">**SetPowerState**</span></span>                                                      | <span data-ttu-id="cd9ce-135">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-135">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cd9ce-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cd9ce-136">Properties</span></span>

<span data-ttu-id="cd9ce-137">La **classe \_ controller seriale di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-137">The **Msvm\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd9ce-138">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-138">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-139">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-139">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-141">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-141">Any additional availability and status of the device.</span></span> <span data-ttu-id="cd9ce-142">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-142">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cd9ce-143">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-143">Value</span></span>                                                                            | <span data-ttu-id="cd9ce-144">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-144">Meaning</span></span>                   |
|----------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cd9ce-145"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-145"><dt>{ 6 }</dt></span></span> </dl> |                           |
| <dl> <span data-ttu-id="cd9ce-146"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-146"><dt>6</dt></span></span> </dl>     | <span data-ttu-id="cd9ce-147">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="cd9ce-147">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-148">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-148">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-149">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-151">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-151">The primary availability and status of the device.</span></span> <span data-ttu-id="cd9ce-152">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-152">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>



| <span data-ttu-id="cd9ce-153">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-153">Value</span></span>                                                                        | <span data-ttu-id="cd9ce-154">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-154">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cd9ce-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-155"><dt>6</dt></span></span> </dl> | <span data-ttu-id="cd9ce-156">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="cd9ce-156">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-157">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-157">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-158">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-160">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-160">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="cd9ce-161">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-161">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-163">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-165">Il buffering e altre funzionalità del controller seriale che potrebbero essere intrinseci nell'hardware del chip.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-165">The buffering and other capabilities of the serial controller that might be inherent in the chip hardware.</span></span> <span data-ttu-id="cd9ce-166">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-166">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-167">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-167">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-168">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-168">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-170">Matrice di stringhe in formato libero che fornisce spiegazioni più dettagliate per tutte le funzionalità del controller seriale indicate nella matrice delle **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-170">An array of free-form strings that provides more detailed explanations for any of the serial controller features that are indicated in the **Capabilities** array.</span></span> <span data-ttu-id="cd9ce-171">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-171">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-172">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-175">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-175">A short description of the object.</span></span> <span data-ttu-id="cd9ce-176">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-176">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-177">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-177">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-178">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-180">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-180">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="cd9ce-181">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-181">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd9ce-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd9ce-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-185"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-186"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-187"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd9ce-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd9ce-190">)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd9ce-191">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-191">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-194">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-194">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="cd9ce-195">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-195">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-196">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-196">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-197">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-199">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-199">A description of the object.</span></span> <span data-ttu-id="cd9ce-200">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-200">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-201">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-201">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-202">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-204">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-204">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="cd9ce-205">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-205">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd9ce-206">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-206">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd9ce-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-207"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-208"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-209"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-210"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-211"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-212"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-213"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd9ce-214"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd9ce-215">)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-215">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd9ce-216">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-216">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-219">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su "Microsoft: *<GUID>* ".</span><span class="sxs-lookup"><span data-stu-id="cd9ce-219">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to "Microsoft:*<GUID>*".</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-220">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-220">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-223">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-223">A display name for the object.</span></span> <span data-ttu-id="cd9ce-224">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-224">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-225">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-225">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-226">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-228">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-228">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="cd9ce-229">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-229">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cd9ce-230">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-230">Value</span></span>                                                                        | <span data-ttu-id="cd9ce-231">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-231">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="cd9ce-232"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-232"><dt>2</dt></span></span> </dl> | <span data-ttu-id="cd9ce-233">Abilitato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-233">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-234">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-234">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-235">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-236">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-237">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-237">The enabled and disabled states of an element.</span></span> <span data-ttu-id="cd9ce-238">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-238">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="cd9ce-239">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-239">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cd9ce-240">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-240">Value</span></span>                                                                        | <span data-ttu-id="cd9ce-241">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-241">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cd9ce-242"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-242"><dt>5</dt></span></span> </dl> | <span data-ttu-id="cd9ce-243">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="cd9ce-243">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-244">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-244">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-245">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-247">Indica se l'errore riportato nella proprietà **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-247">Indicates whether the error reported in the **LastErrorCode** property is now cleared.</span></span> <span data-ttu-id="cd9ce-248">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-248">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-249">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-249">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-250">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-251">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-252">Stringa che fornisce ulteriori informazioni sull'errore registrato nella proprietà **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-252">A string that provides more information about the error recorded in the **LastErrorCode** property and information about any corrective actions that may be taken.</span></span> <span data-ttu-id="cd9ce-253">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-253">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-254">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-254">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-255">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-256">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-257">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-257">The current health of the element.</span></span> <span data-ttu-id="cd9ce-258">Questa operazione esprime l'integrità dell'elemento, ma non necessariamente quello dei sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-258">This expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="cd9ce-259">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-259">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="cd9ce-260">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-261">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-261">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-262">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-264">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-264">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="cd9ce-265">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-265">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-266">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-266">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-267">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-267">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-269">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-269">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="cd9ce-270">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-270">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-271">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-271">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-272">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-274">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-274">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-275">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-275">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="cd9ce-276">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-277">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-277">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-278">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-280">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-280">The last error code reported by the logical device.</span></span> <span data-ttu-id="cd9ce-281">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-281">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-282">**MaxBaudRate**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-282">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-283">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-284">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-285">Velocità in baud massima, in bit al secondo, supportata dal controller seriale.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-285">The maximum baud rate, in bits per second, that is supported by the serial controller.</span></span> <span data-ttu-id="cd9ce-286">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-286">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-287">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-288">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-290">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-290">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="cd9ce-291">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-291">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="cd9ce-292">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-292">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="cd9ce-293">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-293">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-294">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-294">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-295">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-295">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-297">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-297">This property has been deprecated.</span></span> <span data-ttu-id="cd9ce-298">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-298">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-299">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-299">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-300">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-301">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-302">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-302">The label by which the object is known.</span></span> <span data-ttu-id="cd9ce-303">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-303">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-304">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-304">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-305">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-307">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-307">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="cd9ce-308">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-308">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd9ce-309">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-309">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd9ce-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-311"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-312"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-313"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-314"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-315"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-316"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-317"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-318"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-319"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-320"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-321"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-322"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-323"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-324"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-325"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-326"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-327"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd9ce-328"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd9ce-329">)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-329">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd9ce-330">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-330">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-331">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-333">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-333">The current statuses of the object.</span></span> <span data-ttu-id="cd9ce-334">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-334">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-335">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-335">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-338">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-338">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="cd9ce-339">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-339">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="cd9ce-340">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-340">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-342">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-344">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-344">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="cd9ce-345">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-345">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-346">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-347">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-348">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-349">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-349">The power management capabilities of the device.</span></span> <span data-ttu-id="cd9ce-350">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-350">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-351">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-351">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-352">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-353">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-354">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-354">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="cd9ce-355">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-355">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-356">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-356">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-357">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-357">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-358">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-359">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-359">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="cd9ce-360">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-360">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-361">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-361">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-362">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-364">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-364">Provides high level status information.</span></span> <span data-ttu-id="cd9ce-365">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-365">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="cd9ce-366">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-366">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="cd9ce-367">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="cd9ce-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-368"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-369"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-370"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-371"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-372"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="cd9ce-373"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="cd9ce-374">)</span><span class="sxs-lookup"><span data-stu-id="cd9ce-374">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cd9ce-375">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-375">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-376">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-378">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-378">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="cd9ce-379">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-379">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-380">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-380">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-381">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-381">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-383">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-383">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="cd9ce-384">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-384">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="cd9ce-385">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-385">Value</span></span>                                                                         | <span data-ttu-id="cd9ce-386">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-386">Meaning</span></span>             |
|-------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="cd9ce-387"><dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-387"><dt>26</dt></span></span> </dl> | <span data-ttu-id="cd9ce-388">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="cd9ce-388">IEEE-488</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-389">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-389">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-390">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-392">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-392">The last requested or desired state for the element.</span></span> <span data-ttu-id="cd9ce-393">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-393">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="cd9ce-394">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-394">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="cd9ce-395">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-395">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="cd9ce-396">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-396">Value</span></span>                                                                         | <span data-ttu-id="cd9ce-397">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-397">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="cd9ce-398"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-398"><dt>12</dt></span></span> </dl> | <span data-ttu-id="cd9ce-399">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="cd9ce-399">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-400">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-400">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-401">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-401">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-403">Sicurezza operativa per il controller.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-403">The operational security for the controller.</span></span> <span data-ttu-id="cd9ce-404">Questa proprietà viene ereditata da [**CIM \_ controller seriale**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-404">This property is inherited from [**CIM\_SerialController**](/windows/desktop/CIMWin32Prov/cim-serialcontroller).</span></span>



| <span data-ttu-id="cd9ce-405">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-405">Value</span></span>                                                                        | <span data-ttu-id="cd9ce-406">Significato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-406">Meaning</span></span>         |
|------------------------------------------------------------------------------|-----------------|
| <dl> <span data-ttu-id="cd9ce-407"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-407"><dt>3</dt></span></span> </dl> | <span data-ttu-id="cd9ce-408">nessuno</span><span class="sxs-lookup"><span data-stu-id="cd9ce-408">None</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="cd9ce-409">**Status**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-409">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-410">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-412">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-412">The current status of the object.</span></span> <span data-ttu-id="cd9ce-413">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-413">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-414">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-414">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-415">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-415">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-416">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-417">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="cd9ce-417">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="cd9ce-418">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-419">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-419">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-420">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-420">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-422">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-422">The current state of the logical device.</span></span> <span data-ttu-id="cd9ce-423">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-423">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-424">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-424">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-425">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-425">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-427">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-427">The scoping system's creation class name.</span></span> <span data-ttu-id="cd9ce-428">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-428">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-429">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-429">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-430">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-432">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-432">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="cd9ce-433">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-433">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-434">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-434">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-435">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-435">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-437">Data e ora dell'ultima accensione del controller.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-437">The last time the controller was powered on.</span></span> <span data-ttu-id="cd9ce-438">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-438">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-439">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-439">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-440">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-441">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-442">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-442">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="cd9ce-443">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-443">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-444">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-444">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-445">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-446">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-447">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-447">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="cd9ce-448">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-448">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cd9ce-449">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-449">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd9ce-450">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-450">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cd9ce-451">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cd9ce-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cd9ce-452">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-452">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="cd9ce-453">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-453">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd9ce-454">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd9ce-454">Remarks</span></span>

<span data-ttu-id="cd9ce-455">L'accesso alla **classe \_ controller seriale di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="cd9ce-455">Access to the **Msvm\_SerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cd9ce-456">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cd9ce-456">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9ce-457">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd9ce-457">Requirements</span></span>



| <span data-ttu-id="cd9ce-458">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd9ce-458">Requirement</span></span> | <span data-ttu-id="cd9ce-459">Valore</span><span class="sxs-lookup"><span data-stu-id="cd9ce-459">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9ce-460">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-460">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9ce-461">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd9ce-461">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd9ce-462">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd9ce-462">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9ce-463">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd9ce-463">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd9ce-464">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cd9ce-464">Namespace</span></span><br/>                | <span data-ttu-id="cd9ce-465">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd9ce-465">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd9ce-466">MOF</span><span class="sxs-lookup"><span data-stu-id="cd9ce-466">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd9ce-467"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-467"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd9ce-468">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9ce-468">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd9ce-469"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd9ce-469"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd9ce-470">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd9ce-470">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9ce-471">**\_Controller seriale CIM**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-471">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="cd9ce-472">**\_Controller seriale CIM**</span><span class="sxs-lookup"><span data-stu-id="cd9ce-472">**CIM\_SerialController**</span></span>](/windows/desktop/CIMWin32Prov/cim-serialcontroller)
</dt> <dt>

[<span data-ttu-id="cd9ce-473">Classi di dispositivi seriali</span><span class="sxs-lookup"><span data-stu-id="cd9ce-473">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

