---
description: Rappresenta un controller IDE.
ms.assetid: DFD4D90E-CA91-42B3-AC88-9E9D26089C36
title: Classe Msvm_IDEController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_IDEController
- Msvm_IDEController.SetPowerState
- Msvm_IDEController.EnableDevice
- Msvm_IDEController.OnlineDevice
- Msvm_IDEController.QuiesceDevice
- Msvm_IDEController.SaveProperties
- Msvm_IDEController.RestoreProperties
- Msvm_IDEController.InstanceID
- Msvm_IDEController.Caption
- Msvm_IDEController.Description
- Msvm_IDEController.ElementName
- Msvm_IDEController.InstallDate
- Msvm_IDEController.Name
- Msvm_IDEController.OperationalStatus
- Msvm_IDEController.StatusDescriptions
- Msvm_IDEController.Status
- Msvm_IDEController.HealthState
- Msvm_IDEController.CommunicationStatus
- Msvm_IDEController.DetailedStatus
- Msvm_IDEController.OperatingStatus
- Msvm_IDEController.PrimaryStatus
- Msvm_IDEController.EnabledState
- Msvm_IDEController.OtherEnabledState
- Msvm_IDEController.RequestedState
- Msvm_IDEController.EnabledDefault
- Msvm_IDEController.TimeOfLastStateChange
- Msvm_IDEController.AvailableRequestedStates
- Msvm_IDEController.TransitioningToState
- Msvm_IDEController.SystemCreationClassName
- Msvm_IDEController.SystemName
- Msvm_IDEController.CreationClassName
- Msvm_IDEController.DeviceID
- Msvm_IDEController.PowerManagementSupported
- Msvm_IDEController.PowerManagementCapabilities
- Msvm_IDEController.Availability
- Msvm_IDEController.StatusInfo
- Msvm_IDEController.LastErrorCode
- Msvm_IDEController.ErrorDescription
- Msvm_IDEController.ErrorCleared
- Msvm_IDEController.OtherIdentifyingInfo
- Msvm_IDEController.PowerOnHours
- Msvm_IDEController.TotalPowerOnHours
- Msvm_IDEController.IdentifyingDescriptions
- Msvm_IDEController.AdditionalAvailability
- Msvm_IDEController.MaxQuiesceTime
- Msvm_IDEController.TimeOfLastReset
- Msvm_IDEController.ProtocolSupported
- Msvm_IDEController.MaxNumberControlled
- Msvm_IDEController.ProtocolDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 25da1bddfa029ca5a6892006283e322d91a328a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307898"
---
# <a name="msvm_idecontroller-class"></a><span data-ttu-id="09054-103">\_Classe MSVM IDECONTROLLER</span><span class="sxs-lookup"><span data-stu-id="09054-103">Msvm\_IDEController class</span></span>

<span data-ttu-id="09054-104">Rappresenta un controller IDE.</span><span class="sxs-lookup"><span data-stu-id="09054-104">Represents an IDE controller.</span></span> <span data-ttu-id="09054-105">Questa classe può supportare fino a quattro unità collegate al controller.</span><span class="sxs-lookup"><span data-stu-id="09054-105">This class can support up to four drives attached to the controller.</span></span> <span data-ttu-id="09054-106">Il controller IDE è fisso nella macchina virtuale e pertanto non è associato a un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="09054-106">The IDE controller is fixed in the virtual machine and therefore does not have a resource pool associated with it.</span></span>

> [!Note]  
> <span data-ttu-id="09054-107">Questa classe non è disponibile per le macchine virtuali di seconda generazione.</span><span class="sxs-lookup"><span data-stu-id="09054-107">This class is not available to generation 2 virtual machines.</span></span>

 

<span data-ttu-id="09054-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="09054-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="09054-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09054-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_IDEController : CIM_IDEController
{
  string   InstanceID;
  string   Caption;
  string   Description = "Microsoft Virtual IDE Controller";
  string   ElementName;
  datetime InstallDate;
  string   Name;
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
  string   CreationClassName = "Msvm_IDEController";
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
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 37;
  uint32   MaxNumberControlled = 2;
  string   ProtocolDescription = "IDE";
};
```

## <a name="members"></a><span data-ttu-id="09054-110">Members</span><span class="sxs-lookup"><span data-stu-id="09054-110">Members</span></span>

<span data-ttu-id="09054-111">La **classe \_ IDECONTROLLER di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="09054-111">The **Msvm\_IDEController** class has these types of members:</span></span>

-   [<span data-ttu-id="09054-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="09054-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="09054-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09054-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="09054-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="09054-114">Methods</span></span>

<span data-ttu-id="09054-115">La **classe \_ IDECONTROLLER di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="09054-115">The **Msvm\_IDEController** class has these methods.</span></span>



| <span data-ttu-id="09054-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="09054-116">Method</span></span>                                                              | <span data-ttu-id="09054-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09054-117">Description</span></span>                              |
|:--------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="09054-118">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="09054-118">**EnableDevice**</span></span>                                                    | <span data-ttu-id="09054-119">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-119">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09054-120">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="09054-120">**OnlineDevice**</span></span>                                                    | <span data-ttu-id="09054-121">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-121">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09054-122">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="09054-122">**QuiesceDevice**</span></span>                                                   | <span data-ttu-id="09054-123">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-123">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="09054-124">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="09054-124">**RequestStateChange**</span></span>](msvm-idecontroller-requeststatechange.md) | <span data-ttu-id="09054-125">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="09054-125">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="09054-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="09054-126">**Reset**</span></span>](msvm-idecontroller-reset.md)                           | <span data-ttu-id="09054-127">Reimposta il dispositivo virtuale.</span><span class="sxs-lookup"><span data-stu-id="09054-127">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="09054-128">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="09054-128">**RestoreProperties**</span></span>                                               | <span data-ttu-id="09054-129">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-129">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09054-130">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="09054-130">**SaveProperties**</span></span>                                                  | <span data-ttu-id="09054-131">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-131">This method is not supported.</span></span><br/> |
| <span data-ttu-id="09054-132">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="09054-132">**SetPowerState**</span></span>                                                   | <span data-ttu-id="09054-133">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="09054-133">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="09054-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="09054-134">Properties</span></span>

<span data-ttu-id="09054-135">La **classe \_ IDECONTROLLER di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="09054-135">The **Msvm\_IDEController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09054-136">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="09054-136">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-137">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-137">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-139">Eventuali disponibilità e stato aggiuntive del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09054-139">Any additional availability and status of the device.</span></span> <span data-ttu-id="09054-140">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="09054-140">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09054-141">**Disponibilità**</span><span class="sxs-lookup"><span data-stu-id="09054-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-142">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-144">Disponibilità e stato primari del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09054-144">The primary availability and status of the device.</span></span> <span data-ttu-id="09054-145">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="09054-145">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09054-146">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="09054-146">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-147">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-147">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-149">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="09054-149">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="09054-150">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="09054-150">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="09054-151">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="09054-151">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="09054-152">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="09054-152">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="09054-153">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-153">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-154">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="09054-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-157">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09054-157">A short description of the object.</span></span> <span data-ttu-id="09054-158">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09054-158">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="09054-159">Valore</span><span class="sxs-lookup"><span data-stu-id="09054-159">Value</span></span>                                                                                         | <span data-ttu-id="09054-160">Significato</span><span class="sxs-lookup"><span data-stu-id="09054-160">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="09054-161"><dt>"Controller IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="09054-161"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="09054-162">L'istanza rappresenta il controller primario.</span><span class="sxs-lookup"><span data-stu-id="09054-162">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="09054-163"><dt>"Controller IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="09054-163"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="09054-164">L'istanza rappresenta il controller secondario.</span><span class="sxs-lookup"><span data-stu-id="09054-164">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09054-165">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="09054-165">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-168">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="09054-168">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="09054-169">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="09054-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09054-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-171">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09054-171">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-174">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="09054-174">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="09054-175">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="09054-175">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09054-176">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="09054-176">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-179">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="09054-179">A description of the object.</span></span> <span data-ttu-id="09054-180">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09054-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-181">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="09054-181">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-182">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-184">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="09054-184">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="09054-185">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="09054-185">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09054-186">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-186">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-187">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="09054-187">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-188">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-190">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".</span><span class="sxs-lookup"><span data-stu-id="09054-190">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to "Microsoft:*GUID*\\*device-specific-data*".</span></span>

</dd> <dt>

<span data-ttu-id="09054-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="09054-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-194">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09054-194">A display name for the object.</span></span> <span data-ttu-id="09054-195">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09054-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>



| <span data-ttu-id="09054-196">Valore</span><span class="sxs-lookup"><span data-stu-id="09054-196">Value</span></span>                                                                                         | <span data-ttu-id="09054-197">Significato</span><span class="sxs-lookup"><span data-stu-id="09054-197">Meaning</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="09054-198"><dt>"Controller IDE 0"</dt></span><span class="sxs-lookup"><span data-stu-id="09054-198"><dt>"IDE Controller 0"</dt></span></span> </dl> | <span data-ttu-id="09054-199">L'istanza rappresenta il controller primario.</span><span class="sxs-lookup"><span data-stu-id="09054-199">The instance represents the primary controller.</span></span><br/>   |
| <dl> <span data-ttu-id="09054-200"><dt>"Controller IDE 1"</dt></span><span class="sxs-lookup"><span data-stu-id="09054-200"><dt>"IDE Controller 1"</dt></span></span> </dl> | <span data-ttu-id="09054-201">L'istanza rappresenta il controller secondario.</span><span class="sxs-lookup"><span data-stu-id="09054-201">The instance represents the secondary controller.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09054-202">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="09054-202">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-203">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-205">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="09054-205">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="09054-206">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-207">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="09054-207">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-208">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-210">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="09054-210">The enabled and disabled states of an element.</span></span> <span data-ttu-id="09054-211">Può inoltre indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="09054-211">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="09054-212">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-212">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-213">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="09054-213">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-214">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="09054-214">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09054-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-216">Indica se l'errore segnalato in **LastErrorCode** è ora cancellato.</span><span class="sxs-lookup"><span data-stu-id="09054-216">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="09054-217">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-217">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-218">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="09054-218">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-219">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-221">Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="09054-221">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="09054-222">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-222">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-223">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="09054-223">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-224">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-226">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="09054-226">The current health of the element.</span></span> <span data-ttu-id="09054-227">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="09054-227">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="09054-228">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="09054-228">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="09054-229">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-230">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="09054-230">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-231">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="09054-231">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-233">Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="09054-233">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="09054-234">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-234">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-235">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="09054-235">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-236">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09054-236">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09054-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-238">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09054-238">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="09054-239">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-239">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-240">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="09054-240">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09054-243">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="09054-243">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="09054-244">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="09054-244">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="09054-245">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="09054-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-246">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="09054-246">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-247">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09054-247">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09054-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-249">Ultimo codice di errore segnalato dal dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="09054-249">The last error code reported by the logical device.</span></span> <span data-ttu-id="09054-250">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-250">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-251">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="09054-251">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-252">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09054-252">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="09054-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-254">Numero massimo di entità indirizzabili direttamente supportate da questo controller.</span><span class="sxs-lookup"><span data-stu-id="09054-254">The maximum number of directly addressable entities that are supported by this controller.</span></span> <span data-ttu-id="09054-255">Se il numero è sconosciuto o illimitato, è necessario utilizzare il valore 0.</span><span class="sxs-lookup"><span data-stu-id="09054-255">A value of 0 should be used if the number is unknown or unlimited.</span></span> <span data-ttu-id="09054-256">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="09054-256">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="09054-257">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="09054-257">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="09054-258">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="09054-258">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-259">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09054-259">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09054-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-261">La proprietà è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="09054-261">This property has been deprecated.</span></span> <span data-ttu-id="09054-262">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-262">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-263">**Nome**</span><span class="sxs-lookup"><span data-stu-id="09054-263">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-264">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-265">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-265">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-266">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="09054-266">The label by which the object is known.</span></span> <span data-ttu-id="09054-267">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="09054-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="09054-268">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="09054-268">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-269">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-271">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="09054-271">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="09054-272">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="09054-272">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09054-273">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-274">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="09054-274">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-275">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-275">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-276">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-277">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09054-277">The current statuses of the object.</span></span> <span data-ttu-id="09054-278">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-278">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-279">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="09054-279">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-280">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-281">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-282">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="09054-282">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="09054-283">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="09054-283">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="09054-284">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-284">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-285">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="09054-285">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-286">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="09054-286">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-287">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-288">Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="09054-288">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="09054-289">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="09054-289">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), and it is set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="09054-290">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="09054-290">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-291">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-291">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-293">Funzionalità di risparmio energia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="09054-293">The power management capabilities of the device.</span></span> <span data-ttu-id="09054-294">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-294">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-295">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="09054-295">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-296">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="09054-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="09054-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-298">Indica se il dispositivo può essere gestito da energia elettrica.</span><span class="sxs-lookup"><span data-stu-id="09054-298">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="09054-299">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-299">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-300">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="09054-300">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-301">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09054-301">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09054-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-303">Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione.</span><span class="sxs-lookup"><span data-stu-id="09054-303">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="09054-304">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-304">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-305">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="09054-305">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-306">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-308">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="09054-308">Provides high level status information.</span></span> <span data-ttu-id="09054-309">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="09054-309">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="09054-310">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="09054-310">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="09054-311">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-311">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-312">**ProtocolDescription**</span><span class="sxs-lookup"><span data-stu-id="09054-312">**ProtocolDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-315">Stringa che fornisce ulteriori informazioni correlate al protocollo supportato dal controller.</span><span class="sxs-lookup"><span data-stu-id="09054-315">A string that provides more information that is related to the protocol supported by the controller.</span></span> <span data-ttu-id="09054-316">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="09054-316">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="09054-317">**ProtocolSupported**</span><span class="sxs-lookup"><span data-stu-id="09054-317">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-318">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-318">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-320">Protocollo usato dal controller per accedere ai dispositivi controllati.</span><span class="sxs-lookup"><span data-stu-id="09054-320">The protocol used by the controller to access controlled devices.</span></span> <span data-ttu-id="09054-321">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="09054-321">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>



| <span data-ttu-id="09054-322">Valore</span><span class="sxs-lookup"><span data-stu-id="09054-322">Value</span></span>                                                                         | <span data-ttu-id="09054-323">Significato</span><span class="sxs-lookup"><span data-stu-id="09054-323">Meaning</span></span>        |
|-------------------------------------------------------------------------------|----------------|
| <dl> <span data-ttu-id="09054-324"><dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="09054-324"><dt>37</dt></span></span> </dl> | <span data-ttu-id="09054-325">IDE</span><span class="sxs-lookup"><span data-stu-id="09054-325">IDE</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09054-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="09054-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-327">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-329">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="09054-329">The last requested or desired state for the element.</span></span> <span data-ttu-id="09054-330">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="09054-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="09054-331">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="09054-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="09054-332">Una particolare istanza di un elemento logico abilitato potrebbe non supportare **RequestedStateChange**.</span><span class="sxs-lookup"><span data-stu-id="09054-332">A particular instance of an enabled logical element might not support **RequestedStateChange**.</span></span> <span data-ttu-id="09054-333">In tal caso, viene utilizzato il valore 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="09054-333">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="09054-334">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-334">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-335">**Status**</span><span class="sxs-lookup"><span data-stu-id="09054-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-336">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-337">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-338">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="09054-338">The current status of the object.</span></span> <span data-ttu-id="09054-339">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-339">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-340">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="09054-340">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-341">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="09054-341">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="09054-342">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-342">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-343">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="09054-343">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="09054-344">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="09054-344">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="09054-345">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="09054-345">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-346">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-347">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-348">Stato corrente del dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="09054-348">The current state of the logical device.</span></span> <span data-ttu-id="09054-349">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-349">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-350">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="09054-350">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-351">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-353">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="09054-353">The scoping system's creation class name.</span></span> <span data-ttu-id="09054-354">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="09054-354">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09054-355">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="09054-355">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="09054-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="09054-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-358">Identificatore univoco per la macchina virtuale di ambito.</span><span class="sxs-lookup"><span data-stu-id="09054-358">The unique identifier for the scoping virtual machine.</span></span> <span data-ttu-id="09054-359">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="09054-359">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="09054-360">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="09054-360">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-361">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09054-361">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09054-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-363">Ora dell'ultima accensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="09054-363">The last time the virtual machine was powered on.</span></span> <span data-ttu-id="09054-364">Questa proprietà viene ereditata [**dal \_ controller CIM**](/windows/desktop/CIMWin32Prov/cim-controller).</span><span class="sxs-lookup"><span data-stu-id="09054-364">This property is inherited from [**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller).</span></span>

</dd> <dt>

<span data-ttu-id="09054-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="09054-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-366">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="09054-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="09054-367">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-368">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="09054-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="09054-369">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="09054-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="09054-370">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="09054-370">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-371">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09054-371">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09054-372">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-373">Il numero totale di ore in cui il dispositivo è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="09054-373">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="09054-374">Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-374">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="09054-375">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="09054-375">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09054-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09054-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09054-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="09054-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09054-378">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="09054-378">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="09054-379">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="09054-379">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09054-380">Commenti</span><span class="sxs-lookup"><span data-stu-id="09054-380">Remarks</span></span>

<span data-ttu-id="09054-381">L'accesso alla **classe \_ IDECONTROLLER di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="09054-381">Access to the **Msvm\_IDEController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="09054-382">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="09054-382">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="09054-383">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09054-383">Requirements</span></span>



| <span data-ttu-id="09054-384">Requisito</span><span class="sxs-lookup"><span data-stu-id="09054-384">Requirement</span></span> | <span data-ttu-id="09054-385">Valore</span><span class="sxs-lookup"><span data-stu-id="09054-385">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09054-386">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09054-386">Minimum supported client</span></span><br/> | <span data-ttu-id="09054-387">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="09054-387">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09054-388">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09054-388">Minimum supported server</span></span><br/> | <span data-ttu-id="09054-389">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="09054-389">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09054-390">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="09054-390">Namespace</span></span><br/>                | <span data-ttu-id="09054-391">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="09054-391">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09054-392">MOF</span><span class="sxs-lookup"><span data-stu-id="09054-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09054-393"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09054-393"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09054-394">DLL</span><span class="sxs-lookup"><span data-stu-id="09054-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09054-395"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09054-395"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09054-396">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09054-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09054-397">**\_IDECONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="09054-397">**CIM\_IDEController**</span></span>](cim-idecontroller.md)
</dt> <dt>

<span data-ttu-id="09054-398">[**\_IDECONTROLLER CIM**](/previous-versions//cc136863(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09054-398">[**CIM\_IDEController**](/previous-versions//cc136863(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="09054-399">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="09054-399">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

