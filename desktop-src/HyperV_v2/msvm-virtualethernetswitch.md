---
description: Rappresenta un Commuter Ethernet virtuale. Ogni Commuter dispone di molte porte diverse a cui è possibile collegare le schede di rete. Il Commuter non è altamente configurabile e funge principalmente da segnaposto.
ms.assetid: 9415477a-9423-40fa-a887-3a93da1374af
title: Classe Msvm_VirtualEthernetSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitch
- Msvm_VirtualEthernetSwitch.SetPowerState
- Msvm_VirtualEthernetSwitch.InstanceID
- Msvm_VirtualEthernetSwitch.Caption
- Msvm_VirtualEthernetSwitch.Description
- Msvm_VirtualEthernetSwitch.ElementName
- Msvm_VirtualEthernetSwitch.InstallDate
- Msvm_VirtualEthernetSwitch.OperationalStatus
- Msvm_VirtualEthernetSwitch.StatusDescriptions
- Msvm_VirtualEthernetSwitch.Status
- Msvm_VirtualEthernetSwitch.HealthState
- Msvm_VirtualEthernetSwitch.CommunicationStatus
- Msvm_VirtualEthernetSwitch.DetailedStatus
- Msvm_VirtualEthernetSwitch.OperatingStatus
- Msvm_VirtualEthernetSwitch.PrimaryStatus
- Msvm_VirtualEthernetSwitch.EnabledState
- Msvm_VirtualEthernetSwitch.OtherEnabledState
- Msvm_VirtualEthernetSwitch.RequestedState
- Msvm_VirtualEthernetSwitch.EnabledDefault
- Msvm_VirtualEthernetSwitch.TimeOfLastStateChange
- Msvm_VirtualEthernetSwitch.AvailableRequestedStates
- Msvm_VirtualEthernetSwitch.TransitioningToState
- Msvm_VirtualEthernetSwitch.CreationClassName
- Msvm_VirtualEthernetSwitch.Name
- Msvm_VirtualEthernetSwitch.PrimaryOwnerName
- Msvm_VirtualEthernetSwitch.PrimaryOwnerContact
- Msvm_VirtualEthernetSwitch.Roles
- Msvm_VirtualEthernetSwitch.NameFormat
- Msvm_VirtualEthernetSwitch.OtherIdentifyingInfo
- Msvm_VirtualEthernetSwitch.IdentifyingDescriptions
- Msvm_VirtualEthernetSwitch.Dedicated
- Msvm_VirtualEthernetSwitch.OtherDedicatedDescriptions
- Msvm_VirtualEthernetSwitch.ResetCapability
- Msvm_VirtualEthernetSwitch.PowerManagementCapabilities
- Msvm_VirtualEthernetSwitch.MaxVMQOffloads
- Msvm_VirtualEthernetSwitch.MaxIOVOffloads
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1cd916e24a6e34ed6a70002c4988f55810050c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883037"
---
# <a name="msvm_virtualethernetswitch-class"></a><span data-ttu-id="45620-105">\_Classe MSVM VirtualEthernetSwitch</span><span class="sxs-lookup"><span data-stu-id="45620-105">Msvm\_VirtualEthernetSwitch class</span></span>

<span data-ttu-id="45620-106">Rappresenta un Commuter Ethernet virtuale.</span><span class="sxs-lookup"><span data-stu-id="45620-106">Represents a virtual Ethernet switch.</span></span> <span data-ttu-id="45620-107">Ogni Commuter dispone di molte porte diverse a cui è possibile collegare le schede di rete.</span><span class="sxs-lookup"><span data-stu-id="45620-107">Each switch has many different ports to which network adapters can be attached.</span></span> <span data-ttu-id="45620-108">Il Commuter non è altamente configurabile e funge principalmente da segnaposto.</span><span class="sxs-lookup"><span data-stu-id="45620-108">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="45620-109">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="45620-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45620-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45620-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitch : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Virtual Switch";
  string   Description = "Microsoft Virtual Switch";
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName = "Msvm_VirtualEthernetSwitch";
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 5;
  uint16   PowerManagementCapabilities[];
  uint32   MaxVMQOffloads;
  uint32   MaxIOVOffloads;
};
```

## <a name="members"></a><span data-ttu-id="45620-111">Members</span><span class="sxs-lookup"><span data-stu-id="45620-111">Members</span></span>

<span data-ttu-id="45620-112">La **classe \_ VirtualEthernetSwitch di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="45620-112">The **Msvm\_VirtualEthernetSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="45620-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="45620-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="45620-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45620-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45620-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="45620-115">Methods</span></span>

<span data-ttu-id="45620-116">La **classe \_ VirtualEthernetSwitch di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="45620-116">The **Msvm\_VirtualEthernetSwitch** class has these methods.</span></span>



| <span data-ttu-id="45620-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="45620-117">Method</span></span>                                                                      | <span data-ttu-id="45620-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45620-118">Description</span></span>                              |
|:----------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="45620-119">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="45620-119">**RequestStateChange**</span></span>](msvm-virtualethernetswitch-requeststatechange.md) | <span data-ttu-id="45620-120">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="45620-120">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="45620-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45620-121">**SetPowerState**</span></span>                                                           | <span data-ttu-id="45620-122">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="45620-122">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45620-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="45620-123">Properties</span></span>

<span data-ttu-id="45620-124">La **classe \_ VirtualEthernetSwitch di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="45620-124">The **Msvm\_VirtualEthernetSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45620-125">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="45620-125">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-126">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-126">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-128">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="45620-128">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="45620-129">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="45620-129">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="45620-130">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="45620-130">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="45620-131">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="45620-131">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="45620-132">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45620-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="45620-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-133"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-134"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="45620-135"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45620-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="45620-136"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45620-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="45620-137"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="45620-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="45620-138"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45620-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="45620-139"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45620-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="45620-140"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="45620-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="45620-141"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="45620-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="45620-142"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="45620-143">)</span><span class="sxs-lookup"><span data-stu-id="45620-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-144">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="45620-144">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-147">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="45620-147">A short description of the object.</span></span> <span data-ttu-id="45620-148">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Switch".</span><span class="sxs-lookup"><span data-stu-id="45620-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="45620-149">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="45620-149">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-150">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-152">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="45620-152">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="45620-153">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="45620-153">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45620-154">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-154">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45620-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="45620-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45620-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="45620-156"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45620-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-157"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-158"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="45620-159"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45620-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="45620-160"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45620-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="45620-161"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45620-162">)</span><span class="sxs-lookup"><span data-stu-id="45620-162">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-163">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45620-163">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-166">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="45620-166">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="45620-167">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="45620-167">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="45620-168">**Dedicato**</span><span class="sxs-lookup"><span data-stu-id="45620-168">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-169">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-171">Indica se il sistema informatico è un sistema speciale (dedicato a un particolare uso), rispetto a un sistema di uso generale.</span><span class="sxs-lookup"><span data-stu-id="45620-171">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="45620-172">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 0 (non dedicata).</span><span class="sxs-lookup"><span data-stu-id="45620-172">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="45620-173">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="45620-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-176">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="45620-176">A description of the object.</span></span> <span data-ttu-id="45620-177">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Virtual Switch".</span><span class="sxs-lookup"><span data-stu-id="45620-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch".</span></span>

</dd> <dt>

<span data-ttu-id="45620-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="45620-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-181">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="45620-181">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="45620-182">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="45620-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45620-183">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45620-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="45620-184"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45620-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="45620-185"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45620-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-186"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-187"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="45620-188"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45620-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="45620-189"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45620-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="45620-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45620-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="45620-191"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45620-192">)</span><span class="sxs-lookup"><span data-stu-id="45620-192">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-193">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="45620-193">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-196">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="45620-196">A display name for the object.</span></span> <span data-ttu-id="45620-197">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45620-197">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-198">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="45620-198">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-201">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-201">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="45620-202">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="45620-202">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="45620-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-203"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-204"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="45620-205"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-206">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="45620-206">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-209">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-209">The enabled and disabled states of an element.</span></span> <span data-ttu-id="45620-210">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="45620-210">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="45620-211">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="45620-211">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="45620-212">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="45620-212">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-215">Specifica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-215">Specifies the current health of the element.</span></span> <span data-ttu-id="45620-216">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="45620-216">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="45620-217">Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="45620-217">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="45620-218">La proprietà **EnabledState** può inoltre contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="45620-218">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="45620-219">Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).</span><span class="sxs-lookup"><span data-stu-id="45620-219">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="45620-220">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="45620-221">Valore</span><span class="sxs-lookup"><span data-stu-id="45620-221">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="45620-222">Significato</span><span class="sxs-lookup"><span data-stu-id="45620-222">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="45620-223"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="45620-223"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="45620-224">L'elemento è completamente funzionante e funziona entro i normali parametri operativi e senza errori.</span><span class="sxs-lookup"><span data-stu-id="45620-224">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="45620-225"><dt>**Errore principale**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="45620-225"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="45620-226">Si è verificato un errore grave nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-226">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="45620-227"><dt>**Errore critico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="45620-227"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="45620-228">L'elemento è non funzionale e il ripristino potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="45620-228">The element is nonfunctional, and recovery might not be possible.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="45620-229">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45620-229">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-230">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="45620-230">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-231">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-232">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-232">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-233">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45620-233">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-234">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45620-234">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45620-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-236">Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **null**, per un sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="45620-236">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="45620-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-238">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="45620-238">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45620-241">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="45620-241">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="45620-242">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="45620-242">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="45620-243">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45620-243">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-244">**MaxIOVOffloads**</span><span class="sxs-lookup"><span data-stu-id="45620-244">**MaxIOVOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-245">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45620-245">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45620-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-246">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-247">Il numero massimo di offload della funzione virtuale Single root IO Virtualization (SR-IOV) disponibili in questa opzione.</span><span class="sxs-lookup"><span data-stu-id="45620-247">The maximum number of single root IO virtualization (SR-IOV) virtual function offloads available on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="45620-248">**MaxVMQOffloads**</span><span class="sxs-lookup"><span data-stu-id="45620-248">**MaxVMQOffloads**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-249">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45620-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45620-250">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="45620-250">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="45620-251">Numero massimo di offload della coda della macchina virtuale (VMQ) consentiti per una porta in questa opzione.</span><span class="sxs-lookup"><span data-stu-id="45620-251">The maximum number of virtual machine queue (VMQ) offloads allowed for a port on this switch.</span></span>

</dd> <dt>

<span data-ttu-id="45620-252">**Nome**</span><span class="sxs-lookup"><span data-stu-id="45620-252">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-253">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-255">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="45620-255">The label by which the object is known.</span></span> <span data-ttu-id="45620-256">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su "*GUID*".</span><span class="sxs-lookup"><span data-stu-id="45620-256">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to "*GUID*".</span></span>

</dd> <dt>

<span data-ttu-id="45620-257">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="45620-257">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-258">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-259">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-260">Stringa che identifica il modo in cui è stato generato il nome di sistema utilizzando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="45620-260">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="45620-261">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-261">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-262">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="45620-262">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-263">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-263">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-264">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-264">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-265">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="45620-265">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="45620-266">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="45620-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45620-267">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45620-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="45620-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45620-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="45620-269"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45620-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-270"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-271"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="45620-272"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45620-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="45620-273"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45620-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="45620-274"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45620-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="45620-275"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="45620-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="45620-276"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45620-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="45620-277"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45620-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="45620-278"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="45620-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="45620-279"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="45620-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="45620-280"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="45620-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="45620-281"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="45620-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="45620-282"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="45620-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="45620-283"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="45620-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="45620-284"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="45620-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="45620-285"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45620-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="45620-286"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45620-287">)</span><span class="sxs-lookup"><span data-stu-id="45620-287">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-288">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="45620-288">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-289">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-289">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-291">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="45620-291">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="45620-292">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-293">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45620-293">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-294">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="45620-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-295">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-296">Stringa che descrive come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other).</span><span class="sxs-lookup"><span data-stu-id="45620-296">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="45620-297">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-298">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="45620-298">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-299">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-301">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="45620-301">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="45620-302">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="45620-302">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="45620-303">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-304">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="45620-304">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-305">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="45620-305">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-306">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-307">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-307">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-308">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="45620-308">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-309">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-309">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-310">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-311">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="45620-311">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45620-312">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="45620-312">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-315">Stringa che indica come è possibile raggiungere il proprietario del sistema primario (ad esempio, un numero di telefono o un indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="45620-315">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="45620-316">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-316">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-317">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="45620-317">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-318">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-319">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-320">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="45620-320">The name of the primary system owner.</span></span> <span data-ttu-id="45620-321">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-321">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-322">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="45620-322">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-323">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-323">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-325">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="45620-325">Provides high level status information.</span></span> <span data-ttu-id="45620-326">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="45620-326">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="45620-327">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="45620-327">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45620-328">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-328">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45620-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="45620-329"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45620-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="45620-330"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45620-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="45620-331"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45620-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="45620-332"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45620-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="45620-333"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45620-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="45620-334"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45620-335">)</span><span class="sxs-lookup"><span data-stu-id="45620-335">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45620-336">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="45620-336">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-337">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-338">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-339">Ultimo stato richiesto o desiderato per l'elemento passato al metodo **RequestStateChange** oppure 12 (non applicabile) se non è in corso alcuna modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="45620-339">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="45620-340">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="45620-340">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="45620-341">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="45620-341">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="45620-342">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45620-342">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45620-343">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="45620-343">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-346">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 5 (non implementato).</span><span class="sxs-lookup"><span data-stu-id="45620-346">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 5 (Not implemented).</span></span>

</dd> <dt>

<span data-ttu-id="45620-347">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="45620-347">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-348">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="45620-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-350">Matrice di stringhe che descrivono i ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="45620-350">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="45620-351">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="45620-351">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45620-352">**Status**</span><span class="sxs-lookup"><span data-stu-id="45620-352">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-353">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="45620-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45620-354">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-355">Stringa che specifica lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-355">A string that specifies the status of the element.</span></span> <span data-ttu-id="45620-356">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-356">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-357">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45620-357">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-358">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="45620-358">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45620-359">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45620-360">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="45620-360">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="45620-361">Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="45620-361">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="45620-362">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45620-362">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45620-363">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="45620-363">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-364">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45620-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45620-365">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-366">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="45620-366">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="45620-367">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45620-367">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45620-368">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="45620-368">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45620-369">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45620-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45620-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="45620-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45620-371">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="45620-371">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="45620-372">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45620-372">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45620-373">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45620-373">Requirements</span></span>



| <span data-ttu-id="45620-374">Requisito</span><span class="sxs-lookup"><span data-stu-id="45620-374">Requirement</span></span> | <span data-ttu-id="45620-375">Valore</span><span class="sxs-lookup"><span data-stu-id="45620-375">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45620-376">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45620-376">Minimum supported client</span></span><br/> | <span data-ttu-id="45620-377">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="45620-377">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45620-378">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45620-378">Minimum supported server</span></span><br/> | <span data-ttu-id="45620-379">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="45620-379">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45620-380">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="45620-380">Namespace</span></span><br/>                | <span data-ttu-id="45620-381">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="45620-381">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45620-382">MOF</span><span class="sxs-lookup"><span data-stu-id="45620-382">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45620-383"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45620-383"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45620-384">DLL</span><span class="sxs-lookup"><span data-stu-id="45620-384">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45620-385"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45620-385"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

