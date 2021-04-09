---
description: Rappresenta un'opzione di Fibre Channel virtuale.
ms.assetid: 4300747b-3ffc-4caf-8f0b-76cab6d2294e
title: Classe Msvm_VirtualFcSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualFcSwitch
- Msvm_VirtualFcSwitch.SetPowerState
- Msvm_VirtualFcSwitch.InstanceID
- Msvm_VirtualFcSwitch.Caption
- Msvm_VirtualFcSwitch.Description
- Msvm_VirtualFcSwitch.ElementName
- Msvm_VirtualFcSwitch.InstallDate
- Msvm_VirtualFcSwitch.OperationalStatus
- Msvm_VirtualFcSwitch.StatusDescriptions
- Msvm_VirtualFcSwitch.Status
- Msvm_VirtualFcSwitch.HealthState
- Msvm_VirtualFcSwitch.CommunicationStatus
- Msvm_VirtualFcSwitch.DetailedStatus
- Msvm_VirtualFcSwitch.OperatingStatus
- Msvm_VirtualFcSwitch.PrimaryStatus
- Msvm_VirtualFcSwitch.EnabledState
- Msvm_VirtualFcSwitch.OtherEnabledState
- Msvm_VirtualFcSwitch.RequestedState
- Msvm_VirtualFcSwitch.EnabledDefault
- Msvm_VirtualFcSwitch.TimeOfLastStateChange
- Msvm_VirtualFcSwitch.AvailableRequestedStates
- Msvm_VirtualFcSwitch.TransitioningToState
- Msvm_VirtualFcSwitch.CreationClassName
- Msvm_VirtualFcSwitch.Name
- Msvm_VirtualFcSwitch.PrimaryOwnerName
- Msvm_VirtualFcSwitch.PrimaryOwnerContact
- Msvm_VirtualFcSwitch.Roles
- Msvm_VirtualFcSwitch.NameFormat
- Msvm_VirtualFcSwitch.OtherIdentifyingInfo
- Msvm_VirtualFcSwitch.IdentifyingDescriptions
- Msvm_VirtualFcSwitch.Dedicated
- Msvm_VirtualFcSwitch.OtherDedicatedDescriptions
- Msvm_VirtualFcSwitch.ResetCapability
- Msvm_VirtualFcSwitch.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66c6b7a284a2751b1c9b664428a9c90db9f468a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128407"
---
# <a name="msvm_virtualfcswitch-class"></a><span data-ttu-id="86ace-103">\_Classe MSVM VirtualFcSwitch</span><span class="sxs-lookup"><span data-stu-id="86ace-103">Msvm\_VirtualFcSwitch class</span></span>

<span data-ttu-id="86ace-104">Rappresenta un'opzione di Fibre Channel virtuale.</span><span class="sxs-lookup"><span data-stu-id="86ace-104">Represents a virtual Fibre Channel switch.</span></span> <span data-ttu-id="86ace-105">Ogni opzione è associata a una porta Fibre Channel fisica a cui è possibile connettere molte porte Fibre Channel sintetiche.</span><span class="sxs-lookup"><span data-stu-id="86ace-105">Each switch is associated with one physical Fibre Channel port to which many synthetic Fibre Channel ports can be connected.</span></span> <span data-ttu-id="86ace-106">Il Commuter non è altamente configurabile e funge principalmente da segnaposto.</span><span class="sxs-lookup"><span data-stu-id="86ace-106">The switch itself is not highly configurable and acts mostly as a placeholder.</span></span>

<span data-ttu-id="86ace-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="86ace-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ace-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86ace-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualFcSwitch : CIM_ComputerSystem
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
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="86ace-109">Members</span><span class="sxs-lookup"><span data-stu-id="86ace-109">Members</span></span>

<span data-ttu-id="86ace-110">La **classe \_ VirtualFcSwitch di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="86ace-110">The **Msvm\_VirtualFcSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="86ace-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="86ace-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="86ace-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86ace-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="86ace-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="86ace-113">Methods</span></span>

<span data-ttu-id="86ace-114">La **classe \_ VirtualFcSwitch di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="86ace-114">The **Msvm\_VirtualFcSwitch** class has these methods.</span></span>



| <span data-ttu-id="86ace-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="86ace-115">Method</span></span>                                                                | <span data-ttu-id="86ace-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86ace-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="86ace-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="86ace-117">**RequestStateChange**</span></span>](msvm-virtualfcswitch-requeststatechange.md) | <span data-ttu-id="86ace-118">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="86ace-118">Requests a state change.</span></span><br/>      |
| <span data-ttu-id="86ace-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="86ace-119">**SetPowerState**</span></span>                                                     | <span data-ttu-id="86ace-120">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="86ace-120">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86ace-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86ace-121">Properties</span></span>

<span data-ttu-id="86ace-122">La **classe \_ VirtualFcSwitch di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="86ace-122">The **Msvm\_VirtualFcSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86ace-123">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="86ace-123">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-124">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-124">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-126">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="86ace-126">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="86ace-127">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="86ace-127">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="86ace-128">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="86ace-128">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="86ace-129">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="86ace-129">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="86ace-130">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86ace-130">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="86ace-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-131"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-132"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="86ace-133"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="86ace-134"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="86ace-135"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="86ace-136"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="86ace-137"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="86ace-138"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="86ace-139"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="86ace-140"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="86ace-141">)</span><span class="sxs-lookup"><span data-stu-id="86ace-141">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-142">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="86ace-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-145">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="86ace-145">A short description of the object.</span></span> <span data-ttu-id="86ace-146">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-147">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="86ace-147">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-148">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-148">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-149">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-150">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="86ace-150">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="86ace-151">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="86ace-151">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="86ace-152">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-152">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="86ace-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="86ace-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="86ace-154"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-155"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-156"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="86ace-157"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="86ace-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="86ace-159"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="86ace-160">)</span><span class="sxs-lookup"><span data-stu-id="86ace-160">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-161">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="86ace-161">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-164">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="86ace-164">The name of the class or subclass that is used in the creation of an instance.</span></span> <span data-ttu-id="86ace-165">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="86ace-165">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-166">**Dedicato**</span><span class="sxs-lookup"><span data-stu-id="86ace-166">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-167">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-169">Indica se il sistema informatico è un sistema speciale (dedicato a un particolare uso), rispetto a un sistema di uso generale.</span><span class="sxs-lookup"><span data-stu-id="86ace-169">Indicates whether the computer system is a special-purpose system (dedicated to a particular use), versus being a general-purpose system.</span></span> <span data-ttu-id="86ace-170">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su 0 (non dedicata).</span><span class="sxs-lookup"><span data-stu-id="86ace-170">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to 0 (Not Dedicated).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-171">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="86ace-171">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-174">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="86ace-174">A description of the object.</span></span> <span data-ttu-id="86ace-175">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-176">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="86ace-176">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-179">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="86ace-179">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="86ace-180">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="86ace-180">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="86ace-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-181">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="86ace-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="86ace-182"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="86ace-183"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-184"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-185"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="86ace-186"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="86ace-187"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="86ace-188"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="86ace-189"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="86ace-190">)</span><span class="sxs-lookup"><span data-stu-id="86ace-190">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-191">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="86ace-191">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-194">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="86ace-194">A display name for the object.</span></span> <span data-ttu-id="86ace-195">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-195">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-196">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="86ace-196">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-197">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-198">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-199">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-199">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="86ace-200">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="86ace-200">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="86ace-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-201"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-202"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="86ace-203"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-204">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="86ace-204">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-205">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-207">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-207">The enabled and disabled states of an element.</span></span> <span data-ttu-id="86ace-208">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="86ace-208">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="86ace-209">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="86ace-209">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-210">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="86ace-210">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-211">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-213">Specifica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-213">Specifies the current health of the element.</span></span> <span data-ttu-id="86ace-214">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="86ace-214">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="86ace-215">Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="86ace-215">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="86ace-216">La proprietà **EnabledState** può inoltre contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="86ace-216">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="86ace-217">Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).</span><span class="sxs-lookup"><span data-stu-id="86ace-217">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="86ace-218">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="86ace-219">Valore</span><span class="sxs-lookup"><span data-stu-id="86ace-219">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="86ace-220">Significato</span><span class="sxs-lookup"><span data-stu-id="86ace-220">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="86ace-221"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="86ace-221"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="86ace-222">L'elemento è completamente funzionante e funziona entro i normali parametri operativi e senza errori.</span><span class="sxs-lookup"><span data-stu-id="86ace-222">The element is fully functional and is operating within normal operational parameters and without error.</span></span><br/> |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="86ace-223"><dt>**Errore principale**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="86ace-223"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="86ace-224">Si è verificato un errore grave nell'elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-224">The element has suffered a major failure.</span></span><br/>                                                                |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="86ace-225"><dt>**Errore critico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="86ace-225"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="86ace-226">L'elemento è non funzionale e il ripristino potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="86ace-226">The element is nonfunctional and recovery might not be possible.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="86ace-227">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="86ace-227">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-228">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="86ace-228">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-230">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-230">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-231">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="86ace-231">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-232">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86ace-232">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-234">Data e ora di creazione della configurazione della macchina virtuale per una macchina virtuale, o **null**, per un sistema operativo di gestione.</span><span class="sxs-lookup"><span data-stu-id="86ace-234">The date and time the virtual machine configuration was created for a virtual machine, or **Null**, for a management operating system.</span></span> <span data-ttu-id="86ace-235">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-235">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-236">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="86ace-236">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-237">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-238">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ace-239">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="86ace-239">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="86ace-240">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="86ace-240">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="86ace-241">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-241">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-242">**Nome**</span><span class="sxs-lookup"><span data-stu-id="86ace-242">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-245">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="86ace-245">The label by which the object is known.</span></span> <span data-ttu-id="86ace-246">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system).</span><span class="sxs-lookup"><span data-stu-id="86ace-246">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-247">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="86ace-247">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-250">Stringa che identifica il modo in cui è stato generato il nome di sistema utilizzando l'euristica della sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="86ace-250">A string that identifies how the system name was generated, using the subclass heuristic.</span></span> <span data-ttu-id="86ace-251">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-251">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-252">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="86ace-252">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-253">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-253">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-255">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="86ace-255">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="86ace-256">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="86ace-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="86ace-257">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="86ace-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="86ace-258"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="86ace-259"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-260"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-261"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="86ace-262"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="86ace-263"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="86ace-264"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="86ace-265"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="86ace-266"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="86ace-267"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="86ace-268"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="86ace-269"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="86ace-270"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="86ace-271"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="86ace-272"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="86ace-273"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="86ace-274"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="86ace-275"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="86ace-276"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="86ace-277">)</span><span class="sxs-lookup"><span data-stu-id="86ace-277">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-278">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="86ace-278">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-279">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-279">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-281">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="86ace-281">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="86ace-282">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-282">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-283">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="86ace-283">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-284">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="86ace-284">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-286">Stringa che descrive come o perché il sistema è dedicato quando la matrice **dedicata** include il valore 2 (other).</span><span class="sxs-lookup"><span data-stu-id="86ace-286">A string that describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span> <span data-ttu-id="86ace-287">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-287">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-288">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="86ace-288">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-291">Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="86ace-291">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="86ace-292">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="86ace-292">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="86ace-293">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-293">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-294">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="86ace-294">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-295">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="86ace-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-296">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-297">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-297">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-298">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="86ace-298">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-299">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-299">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-300">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-301">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="86ace-301">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-302">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="86ace-302">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-303">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-305">Stringa che indica come è possibile raggiungere il proprietario del sistema primario (ad esempio, un numero di telefono o un indirizzo di posta elettronica).</span><span class="sxs-lookup"><span data-stu-id="86ace-305">A string that indicates how the primary system owner can be reached (for example, a phone number or an email address).</span></span> <span data-ttu-id="86ace-306">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-306">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-307">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="86ace-307">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-308">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-309">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-310">Nome del proprietario del sistema primario.</span><span class="sxs-lookup"><span data-stu-id="86ace-310">The name of the primary system owner.</span></span> <span data-ttu-id="86ace-311">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-311">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-312">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="86ace-312">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-313">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-315">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="86ace-315">Provides high level status information.</span></span> <span data-ttu-id="86ace-316">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="86ace-316">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="86ace-317">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="86ace-317">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="86ace-318">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-318">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="86ace-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="86ace-319"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="86ace-320"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="86ace-321"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="86ace-322"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="86ace-323"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="86ace-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="86ace-324"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="86ace-325">)</span><span class="sxs-lookup"><span data-stu-id="86ace-325">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="86ace-326">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="86ace-326">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-327">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-329">Ultimo stato richiesto o desiderato per l'elemento passato al metodo **RequestStateChange** oppure 12 (non applicabile) se non è in corso alcuna modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="86ace-329">The last requested or desired state for the element as passed to the **RequestStateChange** method, or 12 (Not Applicable) if no state change is in progress.</span></span> <span data-ttu-id="86ace-330">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="86ace-330">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="86ace-331">Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="86ace-331">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="86ace-332">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86ace-332">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-333">**ResetCapability**</span><span class="sxs-lookup"><span data-stu-id="86ace-333">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-334">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-334">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-335">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-336">Questa proprietà viene ereditata da [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span><span class="sxs-lookup"><span data-stu-id="86ace-336">This property is inherited from [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-337">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="86ace-337">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-338">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="86ace-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-340">Matrice di stringhe che descrivono i ruoli riprodotti dal sistema nell'ambiente Information Technology.</span><span class="sxs-lookup"><span data-stu-id="86ace-340">An array of strings that describe the roles the system plays in the information technology environment.</span></span> <span data-ttu-id="86ace-341">Questa proprietà viene ereditata [**dal \_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="86ace-341">This property is inherited from [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="86ace-342">**Status**</span><span class="sxs-lookup"><span data-stu-id="86ace-342">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-343">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="86ace-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-345">Stringa che specifica lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-345">A string that specifies the status of the element.</span></span> <span data-ttu-id="86ace-346">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-346">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-347">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="86ace-347">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-348">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="86ace-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="86ace-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86ace-350">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="86ace-350">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="86ace-351">Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="86ace-351">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="86ace-352">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="86ace-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-353">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="86ace-353">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-354">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="86ace-354">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-356">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="86ace-356">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="86ace-357">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86ace-357">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="86ace-358">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="86ace-358">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86ace-359">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="86ace-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="86ace-360">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86ace-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="86ace-361">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="86ace-361">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="86ace-362">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="86ace-362">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86ace-363">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86ace-363">Requirements</span></span>



| <span data-ttu-id="86ace-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ace-364">Requirement</span></span> | <span data-ttu-id="86ace-365">Valore</span><span class="sxs-lookup"><span data-stu-id="86ace-365">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ace-366">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86ace-366">Minimum supported client</span></span><br/> | <span data-ttu-id="86ace-367">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="86ace-367">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="86ace-368">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86ace-368">Minimum supported server</span></span><br/> | <span data-ttu-id="86ace-369">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="86ace-369">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86ace-370">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86ace-370">Namespace</span></span><br/>                | <span data-ttu-id="86ace-371">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="86ace-371">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="86ace-372">MOF</span><span class="sxs-lookup"><span data-stu-id="86ace-372">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86ace-373"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86ace-373"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="86ace-374">DLL</span><span class="sxs-lookup"><span data-stu-id="86ace-374">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ace-375"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="86ace-375"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

