---
description: Rappresenta una macchina virtuale pianificata.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318312"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="e1e0d-103">\_Classe MSVM PlannedComputerSystem</span><span class="sxs-lookup"><span data-stu-id="e1e0d-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="e1e0d-104">Rappresenta una macchina virtuale pianificata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="e1e0d-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1e0d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1e0d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="e1e0d-107">Members</span><span class="sxs-lookup"><span data-stu-id="e1e0d-107">Members</span></span>

<span data-ttu-id="e1e0d-108">La **classe \_ PlannedComputerSystem di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e1e0d-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="e1e0d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e1e0d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e1e0d-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1e0d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e1e0d-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e1e0d-111">Methods</span></span>

<span data-ttu-id="e1e0d-112">La **classe \_ PlannedComputerSystem di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="e1e0d-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e1e0d-113">Method</span></span>                                                                      | <span data-ttu-id="e1e0d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1e0d-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1e0d-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="e1e0d-116">Richiede che lo stato del sistema pianificato venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="e1e0d-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="e1e0d-118">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="e1e0d-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e1e0d-119">Properties</span></span>

<span data-ttu-id="e1e0d-120">La **classe \_ PlannedComputerSystem di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1e0d-121">**AssignedNumaNodeList**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-122">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-124">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="e1e0d-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-125">Matrice di nodi NUMA (non-Uniform Memory Access) attualmente assegnati alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-129">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e1e0d-130">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="e1e0d-131">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e1e0d-132">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e1e0d-133">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e1e0d-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="e1e0d-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e1e0d-144">)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1e0d-145">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-148">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-148">A short description of the object.</span></span> <span data-ttu-id="e1e0d-149">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "macchina virtuale pianificata".</span><span class="sxs-lookup"><span data-stu-id="e1e0d-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-153">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e1e0d-154">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1e0d-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-159">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-160">Indica il nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="e1e0d-161">Se utilizzata con le altre proprietà chiave di questa classe, questa proprietà consente di identificare in modo univoco tutte le istanze di questa classe e le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="e1e0d-162">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-163">**Dedicato**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-164">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-166">Matrice di valori che indica gli scopi a cui è dedicato il sistema pianificato, se presente, e la funzionalità fornita.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="e1e0d-167">Ad esempio, è possibile specificare che il sistema è dedicato a "Print" (valore = 11) o funge da "hub" (valore = 8).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="e1e0d-168">È anche possibile indicare più scopi.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="e1e0d-169">Ad esempio, si tratta di un sistema per utilizzo generico che indica "non dedicato" (valore = 0) ma che ospita anche "stampa" (valore = 11) o "dispositivo utente mobile" (valore = 17) servizi.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="e1e0d-170">Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="e1e0d-171">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="e1e0d-172">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="e1e0d-173"><dt>**Non dedicato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e1e0d-174"><dt>**Sconosciuto**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e1e0d-175"><dt>**Altro**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="e1e0d-176"><dt>**Archiviazione**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="e1e0d-177"><dt>**Router**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="e1e0d-178"><dt>**Switch**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="e1e0d-179"><dt>**Switch di livello 3**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="e1e0d-180"><dt>**Switch ufficio centrale**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="e1e0d-181"><dt>**Hub**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="e1e0d-182"><dt>**Accesso al server**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="e1e0d-183"><dt>**Firewall**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="e1e0d-184"><dt>**Stampa**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="e1e0d-185"><dt>**I/O**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="e1e0d-186"><dt>**Caching Web**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="e1e0d-187"><dt>**Gestione**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="e1e0d-188">Indica che questa istanza è dedicata all'hosting del software di gestione del sistema.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="e1e0d-189"><dt>**Blocca server**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="e1e0d-190"><dt>**File server**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="e1e0d-191"><dt>**Dispositivo utente mobile**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="e1e0d-192">Un esempio di dispositivo utente mobile dedicato è un telefono cellulare o uno scanner di codice a barre in un negozio che comunica tramite frequenza radio.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="e1e0d-193">Questi sistemi sono molto limitati in funzionalità e programmabilità e non sono considerati piattaforme di elaborazione per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="e1e0d-194">In alternativa, un esempio di sistema mobile che è generico (ovvero, non è dedicato) è un computer portatile.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="e1e0d-195">Sebbene sia limitato nella programmabilità, è possibile scaricare il nuovo software e la relativa funzionalità espanso dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="e1e0d-196"><dt>**Repeater**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="e1e0d-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="e1e0d-198"><dt>**Gateway**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="e1e0d-199"><dt>**Virtualizzatore archiviazione**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="e1e0d-200"><dt>**Libreria multimediale**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="e1e0d-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="e1e0d-202"><dt>**Server principale**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="e1e0d-203"><dt>**NAS autonomo**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="e1e0d-204"><dt>**UPS**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="e1e0d-205"><dt>**Telefono IP**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="e1e0d-206"><dt>**Controller di gestione**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="e1e0d-207">Indica che questa istanza rappresenta hardware specializzato dedicato alla gestione dei sistemi, ovvero un controller di gestione (BMC) o un processore di servizi di battiscopa.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="e1e0d-208">L'ambito di gestione di un controller di gestione è in genere un singolo sistema gestito in cui è contenuto.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="e1e0d-209"><dt>**Gestione chassis**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="e1e0d-210">Indica che questa istanza rappresenta un sistema dedicato alla gestione di uno chassis del pannello e dei relativi dispositivi contenuti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="e1e0d-211">Questo valore verrebbe utilizzato per rappresentare un controller di scaffale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="e1e0d-212">Uno chassis Manager è un punto di aggregazione per la gestione e può basarsi su controller di gestione subordinati per la gestione di parti costituenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="e1e0d-213"><dt>**Controller RAID basato su host**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="e1e0d-214">Indica che questa istanza rappresenta un controller di archiviazione RAID contenuto in un computer host.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="e1e0d-215"><dt>**Enclosure del dispositivo di archiviazione**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="e1e0d-216">Indica che questa istanza rappresenta un'enclosure che contiene dispositivi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="e1e0d-217"><dt>**Desktop**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="e1e0d-218"><dt>**Portatile**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="e1e0d-219"><dt>**Libreria di nastri virtuale**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="e1e0d-220">Emulazione di una libreria di nastri da parte di un sistema di libreria virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="e1e0d-221"><dt>**Sistema di libreria virtuale**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="e1e0d-222">Usa l'archiviazione su disco per emulare le librerie di nastri.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="e1e0d-223"><dt>**PC di rete/Thin Client**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="e1e0d-224"><dt>**Switch FC**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="e1e0d-225">Indica che questa istanza è dedicata al cambio di frame Fibre Channel di livello 2.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="e1e0d-226"><dt>**Switch Ethernet**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="e1e0d-227">Indica che questa istanza è dedicata al cambio di frame Ethernet di livello 2.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="e1e0d-228"><dt>**DMTF riservato**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="e1e0d-229">32568 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="e1e0d-230">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-231">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-233">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-233">A description of the object.</span></span> <span data-ttu-id="e1e0d-234">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "macchina virtuale pianificata Microsoft".</span><span class="sxs-lookup"><span data-stu-id="e1e0d-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-236">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-238">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e1e0d-239">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1e0d-240">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-242">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-243">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-244">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-244">A display name for the object.</span></span> <span data-ttu-id="e1e0d-245">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-246">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-249">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e1e0d-250">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). i possibili valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="e1e0d-251">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e1e0d-252">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e1e0d-253"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e1e0d-254">Il sistema è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e1e0d-255"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e1e0d-256">Il sistema è abilitato, ma non è in linea.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-256">The system is enabled, but offline.</span></span> <span data-ttu-id="e1e0d-257">Tutte le nuove richieste verranno eliminate.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1e0d-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-259">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-261">Specifica lo stato abilitato del sistema pianificato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="e1e0d-262">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="e1e0d-263">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e1e0d-264">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e1e0d-265"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e1e0d-266">Il sistema è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e1e0d-267"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e1e0d-268">Il sistema è abilitato, ma non è in linea.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-268">The system is enabled, but offline.</span></span> <span data-ttu-id="e1e0d-269">Tutte le nuove richieste verranno eliminate.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1e0d-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-271">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-272">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-273">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-273">The current health of the element.</span></span> <span data-ttu-id="e1e0d-274">Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e1e0d-275">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e1e0d-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="e1e0d-277">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-277">Value</span></span>                                                                        | <span data-ttu-id="e1e0d-278">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="e1e0d-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="e1e0d-280">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1e0d-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-282">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-283">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-284">Matrice di stringhe che forniscono spiegazioni e dettagli dietro le voci della matrice **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="e1e0d-285">Ogni voce di questa matrice è correlata alla voce in **OtherIdentifyingInfo** che si trova nello stesso indice.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="e1e0d-286">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-288">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-289">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-290">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e1e0d-291">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-293">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-294">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-295">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-296">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e1e0d-297">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-298">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-301">Qualificatori: **chiave**, **override**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-302">Il nome ereditato funge da chiave di un'istanza di sistema in un ambiente aziendale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="e1e0d-303">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-304">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-305">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-307">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-308">Identifica il modo in cui è stato generato il nome di sistema, usando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="e1e0d-309">L'oggetto di sistema e i relativi derivati sono oggetti di primo livello di CIM.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="e1e0d-310">Forniscono l'ambito per numerosi componenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="e1e0d-311">È necessario disporre di chiavi di sistema univoche.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-311">Having unique system keys is required.</span></span> <span data-ttu-id="e1e0d-312">È possibile definire un'euristica nelle singole sottoclassi di sistema per tentare di generare sempre la stessa chiave del nome di sistema.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="e1e0d-313">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-314">**OnTimeInMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-315">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-317">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi")</span><span class="sxs-lookup"><span data-stu-id="e1e0d-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-318">Tempo totale, in millisecondi, dall'ultima volta in cui la macchina virtuale è stata attivata, reimpostata o ripristinata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="e1e0d-319">Questa volta esclude l'ora in cui la macchina virtuale è in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-320">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-321">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-323">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e1e0d-324">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1e0d-325">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-327">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-329">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-329">The current statuses of the object.</span></span> <span data-ttu-id="e1e0d-330">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-332">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-334">Stringa che descrive come o perché il sistema è dedicato quando la matrice dedicata include il valore 2, ovvero "altro".</span><span class="sxs-lookup"><span data-stu-id="e1e0d-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="e1e0d-335">Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-336">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-337">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-339">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="e1e0d-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="e1e0d-340">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e1e0d-341">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-343">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-345">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-346">Contiene dati aggiuntivi, oltre alle informazioni sul nome del sistema, che possono essere usati per identificare un ComputerSystem.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="e1e0d-347">Un esempio è quello di contenere il nome Fibre Channel universale (WWN) di un nodo.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="e1e0d-348">Se solo il nome del Fibre Channel è disponibile ed è univoco (in grado di essere usato come chiave di sistema), questa proprietà sarà **null** e WWN diventerebbe la chiave di sistema, i dati inseriti nella proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="e1e0d-349">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-350">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-351">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-353">Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-354">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-355">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-356">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-357">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-358">Stringa che fornisce informazioni sul modo in cui il proprietario del sistema primario può essere raggiunto, ad esempio numero di telefono, indirizzo di posta elettronica e così via.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="e1e0d-359">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-360">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-361">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-362">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-363">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e1e0d-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-364">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-364">The name of the primary system owner.</span></span> <span data-ttu-id="e1e0d-365">Il proprietario del sistema è l'utente principale del sistema.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="e1e0d-366">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-367">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-368">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-369">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-370">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-370">Provides high level status information.</span></span> <span data-ttu-id="e1e0d-371">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e1e0d-372">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e1e0d-373">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-375">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-376">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-377">Identificatore del processo in cui è in esecuzione la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="e1e0d-378">Questo valore può essere utilizzato per identificare in modo univoco l'istanza di Vmwp.exe nel sistema che esegue la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-380">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-382">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="e1e0d-383">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="e1e0d-384">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="e1e0d-385">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="e1e0d-386">In tal caso, viene utilizzato il valore 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="e1e0d-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="e1e0d-387">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="e1e0d-388">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-388">Value</span></span>                                                                         | <span data-ttu-id="e1e0d-389">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e1e0d-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e1e0d-391">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1e0d-392">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-393">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-394">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-395">Specifica le funzionalità di reimpostazione del computer.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="e1e0d-396">Questa proprietà viene ereditata dalla classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="e1e0d-397">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="e1e0d-398">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="e1e0d-399"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e1e0d-400"><dt>**Sconosciuto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e1e0d-401"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="e1e0d-402">La reimpostazione dell'hardware non è consentita.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e1e0d-403"><dt>**Abilitato**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="e1e0d-404">Il sistema del computer può essere reimpostato utilizzando l'hardware (ad esempio, i pulsanti Power e reset).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="e1e0d-405"><dt> **Non implementato**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="e1e0d-406">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-407">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-408">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-409">Matrice di stringhe che specifica i ruoli definiti dall'amministratore che questo sistema riproduce nell'ambiente gestito.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="e1e0d-410">Esempi potrebbero essere "Building 8 Server di stampa" o "directory utente Boise".</span><span class="sxs-lookup"><span data-stu-id="e1e0d-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="e1e0d-411">Un singolo sistema può eseguire più ruoli.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="e1e0d-412">La visualizzazione strumentazione dei ruoli di un sistema viene definita creando un'istanza di una sottoclasse specifica di System o dalle proprietà in una sottoclasse oppure entrambe.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="e1e0d-413">Ad esempio, lo scopo di un ComputerSystem viene definito usando le proprietà **Dedicated** e **OtherDedicatedDescription** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="e1e0d-414">Questa proprietà viene ereditata dalla classe di [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-415">**Status**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-416">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-418">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-419">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-420">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-422">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e1e0d-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e1e0d-423">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "il servizio è in esecuzione normalmente".</span><span class="sxs-lookup"><span data-stu-id="e1e0d-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-424">**TimeOfLastConfigurationChange**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-425">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-426">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-427">Data e ora dell'Ultima modifica del file di configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="e1e0d-428">Il file di configurazione viene modificato durante determinate operazioni della macchina virtuale, nonché quando vengono aggiunte, modificate o rimosse le impostazioni della macchina virtuale o del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-429">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-430">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-432">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e1e0d-433">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e1e0d-434">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1e0d-435">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1e0d-436">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e1e0d-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1e0d-437">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e1e0d-438">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1e0d-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="e1e0d-439">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="e1e0d-440">Significato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="e1e0d-441"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="e1e0d-442"><dt>**Abilitato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e1e0d-443"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="e1e0d-444"><dt>**Arresta**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="e1e0d-445"><dt>**Nessuna modifica**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="e1e0d-446">Non è in corso alcuna transizione.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="e1e0d-447"><dt>**Offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="e1e0d-448"><dt>**Test**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="e1e0d-449"><dt>**Rinvia**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="e1e0d-450"><dt>**Mettere in stato**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="e1e0d-451"><dt>**Riavvio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="e1e0d-452"><dt>**Reimposta**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e1e0d-453"><dt>**Non applicabile**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="e1e0d-454">L'implementazione non supporta la rappresentazione delle transizioni in corso.</span><span class="sxs-lookup"><span data-stu-id="e1e0d-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="e1e0d-455"><dt> **DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1e0d-456">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1e0d-456">Requirements</span></span>



| <span data-ttu-id="e1e0d-457">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1e0d-457">Requirement</span></span> | <span data-ttu-id="e1e0d-458">Valore</span><span class="sxs-lookup"><span data-stu-id="e1e0d-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e0d-459">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-459">Minimum supported client</span></span><br/> | <span data-ttu-id="e1e0d-460">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e1e0d-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e1e0d-461">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1e0d-461">Minimum supported server</span></span><br/> | <span data-ttu-id="e1e0d-462">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e1e0d-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1e0d-463">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e1e0d-463">Namespace</span></span><br/>                | <span data-ttu-id="e1e0d-464">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e1e0d-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e1e0d-465">MOF</span><span class="sxs-lookup"><span data-stu-id="e1e0d-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1e0d-466"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1e0d-467">DLL</span><span class="sxs-lookup"><span data-stu-id="e1e0d-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1e0d-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e1e0d-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e1e0d-469">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1e0d-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1e0d-470">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="e1e0d-471">**\_VirtualSystemManagementService MSVM. Metodo ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="e1e0d-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

