---
description: Rappresenta l'endpoint VLAN di una porta di commutazione.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Classe Msvm_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5606e18fd1327f17feaac07570e5bf8c0c8eb59d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305976"
---
# <a name="msvm_vlanendpoint-class"></a><span data-ttu-id="9e70c-103">\_Classe MSVM VLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="9e70c-103">Msvm\_VLANEndpoint class</span></span>

<span data-ttu-id="9e70c-104">Rappresenta l'endpoint VLAN di una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="9e70c-104">Represents the VLAN endpoint of a switch port.</span></span> <span data-ttu-id="9e70c-105">La configurazione di questo endpoint cambierà il modo in cui la porta del commutatore invia i pacchetti VLAN tramite il commutatore.</span><span class="sxs-lookup"><span data-stu-id="9e70c-105">The configuration of this endpoint will change the way the switch port sends VLAN packets through the switch.</span></span>

<span data-ttu-id="9e70c-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9e70c-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e70c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e70c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
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
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a><span data-ttu-id="9e70c-108">Members</span><span class="sxs-lookup"><span data-stu-id="9e70c-108">Members</span></span>

<span data-ttu-id="9e70c-109">La **classe \_ VLANEndpoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9e70c-109">The **Msvm\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="9e70c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e70c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9e70c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e70c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9e70c-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="9e70c-112">Methods</span></span>

<span data-ttu-id="9e70c-113">La **classe \_ VLANEndpoint di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="9e70c-113">The **Msvm\_VLANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="9e70c-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="9e70c-114">Method</span></span>                                                             | <span data-ttu-id="9e70c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e70c-115">Description</span></span>                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="9e70c-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="9e70c-116">**RequestStateChange**</span></span>](msvm-vlanendpoint-requeststatechange.md) | <span data-ttu-id="9e70c-117">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="9e70c-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9e70c-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9e70c-118">Properties</span></span>

<span data-ttu-id="9e70c-119">La **classe \_ VLANEndpoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9e70c-119">The **Msvm\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9e70c-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="9e70c-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-121">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-123">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="9e70c-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="9e70c-124">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9e70c-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="9e70c-125">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="9e70c-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="9e70c-126">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="9e70c-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="9e70c-127">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9e70c-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="9e70c-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="9e70c-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9e70c-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="9e70c-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="9e70c-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="9e70c-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="9e70c-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="9e70c-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="9e70c-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="9e70c-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="9e70c-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="9e70c-138">)</span><span class="sxs-lookup"><span data-stu-id="9e70c-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e70c-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9e70c-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-140">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-142">A short description of the object.</span></span> <span data-ttu-id="9e70c-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "VLAN endpoint".</span><span class="sxs-lookup"><span data-stu-id="9e70c-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-147">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="9e70c-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="9e70c-148">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9e70c-149">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-150">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e70c-150">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-151">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-153">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="9e70c-153">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="9e70c-154">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)ed è sempre impostata su "MSVM \_ VLANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="9e70c-154">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VLANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-155">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9e70c-155">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-158">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="9e70c-158">A description of the object.</span></span> <span data-ttu-id="9e70c-159">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft VLAN endpoint".</span><span class="sxs-lookup"><span data-stu-id="9e70c-159">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft VLAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-160">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="9e70c-160">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-161">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-162">Tipo di accesso: sola scrittura</span><span class="sxs-lookup"><span data-stu-id="9e70c-162">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-163">La modalità VLAN desiderata richiesta per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9e70c-163">The desired VLAN mode that is requested for use.</span></span> <span data-ttu-id="9e70c-164">La modalità corrente viene fornita dalla proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-164">The current mode is given by the **OperationalEndpointMode** property.</span></span> <span data-ttu-id="9e70c-165">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-165">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="9e70c-166">Valore</span><span class="sxs-lookup"><span data-stu-id="9e70c-166">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="9e70c-167">Significato</span><span class="sxs-lookup"><span data-stu-id="9e70c-167">Meaning</span></span>                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9e70c-168"><dt>**DMTF riservato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-168"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9e70c-169"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-169"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="9e70c-170"><dt>**Accesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-170"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="9e70c-171">Inserisce la porta di commutazione/endpoint in modalità non di trunking permanente e negozia per convertire il collegamento in un collegamento non trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-171">Puts the endpoint/switch port into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="9e70c-172">L'endpoint diventa un'interfaccia non trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-172">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="9e70c-173"><dt>**Auto dinamica**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-173"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="9e70c-174">Rende l'endpoint in grado di convertire il collegamento in un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-174">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="9e70c-175">L'endpoint diventa un'interfaccia trunk se l'interfaccia adiacente è impostata su trunk o sulla modalità desiderata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-175">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="9e70c-176"><dt>**Auspicabile dinamico**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-176"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="9e70c-177">Fa in modo che l'endpoint tenti attivamente di convertire il collegamento a un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-177">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="9e70c-178">L'endpoint diventa un'interfaccia trunk se l'interfaccia vicina è impostata su trunk, auspicabile o modalità auto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-178">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="9e70c-179">La modalità switch-Port predefinita per tutte le interfacce Ethernet è auspicabile dinamica.</span><span class="sxs-lookup"><span data-stu-id="9e70c-179">The default switch-port mode for all Ethernet interfaces is dynamic desirable.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="9e70c-180"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-180"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="9e70c-181">Inserisce l'endpoint in modalità di trunking permanente e negozia per convertire il collegamento in un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-181">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="9e70c-182">L'endpoint diventa un'interfaccia trunk anche se l'interfaccia adiacente non è un'interfaccia trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-182">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="9e70c-183"><dt>**Dot1Q tunnel**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-183"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="9e70c-184">Configura l'interfaccia come endpoint/porta del tunnel (non di trunking) per essere connessa in un collegamento asimmetrico con una porta trunk 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="9e70c-184">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="9e70c-185">il tunneling 802.1 q viene usato per mantenere l'integrità VLAN del cliente attraverso una rete del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="9e70c-185">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9e70c-186"><dt>**DMTF riservato**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-186"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9e70c-187"><dt> **Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-187"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="9e70c-188">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="9e70c-188">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-189">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-191">Tipo di incapsulamento VLAN richiesto per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="9e70c-191">The type of VLAN encapsulation that is requested for use.</span></span> <span data-ttu-id="9e70c-192">L'incapsulamento attualmente in uso viene fornito dalla proprietà **OperationalVLANTrunkEncapsulation** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-192">The encapsulation currently in use is given by the **OperationalVLANTrunkEncapsulation** property.</span></span> <span data-ttu-id="9e70c-193">Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-193">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="9e70c-194">Questa proprietà è 2 (non applicabile) (ovvero, l'endpoint non verrà mai inserito in modalità trunk), un tipo particolare (802.1 Q o Cisco ISL) o 5 (Negotiate) (ovvero il risultato della negoziazione tra questa interfaccia e il relativo adiacente).</span><span class="sxs-lookup"><span data-stu-id="9e70c-194">This property is either 2 (Not Applicable) (that is, the endpoint will never be placed in a trunking mode), a particular type (802.1Q or Cisco ISL), or 5 (Negotiate) (that is, the result of the negotiation between this interface and its neighbor).</span></span> <span data-ttu-id="9e70c-195">Il valore 5 (Negotiate) non è consentito se l'endpoint non supporta la negoziazione.</span><span class="sxs-lookup"><span data-stu-id="9e70c-195">The value, 5 (Negotiate) is not allowed if the endpoint does not support negotiation.</span></span> <span data-ttu-id="9e70c-196">Questa funzionalità è dipendente dall'hardware e dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="9e70c-196">This capability is hardware and vendor dependent.</span></span> <span data-ttu-id="9e70c-197">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-197">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="9e70c-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (0)</span><span class="sxs-lookup"><span data-stu-id="9e70c-198"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e70c-199"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="9e70c-200"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="9e70c-201"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="9e70c-202"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negoziazione** (5)</span><span class="sxs-lookup"><span data-stu-id="9e70c-203"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="9e70c-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="9e70c-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e70c-206">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-206">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-207">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-207">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-208">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-209">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="9e70c-209">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="9e70c-210">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-210">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9e70c-211">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-211">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-212">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9e70c-212">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-213">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-213">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-215">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-215">A display name for the object.</span></span> <span data-ttu-id="9e70c-216">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-216">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-217">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="9e70c-217">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-218">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-220">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="9e70c-220">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="9e70c-221">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="9e70c-221">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-222">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="9e70c-222">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-223">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-225">Stati abilitati e disabilitati di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="9e70c-225">The enabled and disabled states of this element.</span></span> <span data-ttu-id="9e70c-226">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9e70c-226">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-227">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-227">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-228">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-230">Indica se il protocollo di registrazione VLAN GARP (GVRP) è abilitato o disabilitato nell'endpoint/porta del trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-230">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint/port.</span></span> <span data-ttu-id="9e70c-231">Questa proprietà è 2 (non applicabile), a meno che GVRP non sia supportato dall'endpoint.</span><span class="sxs-lookup"><span data-stu-id="9e70c-231">This property is 2 (Not Applicable) unless GVRP is supported by the endpoint.</span></span> <span data-ttu-id="9e70c-232">Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-232">This property is applicable only when the endpoint is operating in trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="9e70c-233">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-233">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="9e70c-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9e70c-234"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="9e70c-235"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="9e70c-236"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabilitato** (4)</span><span class="sxs-lookup"><span data-stu-id="9e70c-237"><span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabled** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e70c-238">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="9e70c-238">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-239">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-241">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9e70c-241">The current health of the element.</span></span> <span data-ttu-id="9e70c-242">Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="9e70c-242">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="9e70c-243">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="9e70c-243">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="9e70c-244">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="9e70c-244">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-245">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9e70c-245">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-246">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e70c-246">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-247">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-248">Data e ora di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-248">The date and time when the object was installed.</span></span> <span data-ttu-id="9e70c-249">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-249">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-250">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9e70c-250">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-251">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-252">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-253">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9e70c-253">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-254">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="9e70c-254">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9e70c-255">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-255">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-256">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9e70c-256">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-257">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-259">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-259">The label by which the object is known.</span></span> <span data-ttu-id="9e70c-260">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-260">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-261">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="9e70c-261">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-262">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-262">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-263">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-264">Euristica di denominazione selezionata per garantire che il valore della proprietà **Name** sia univoco.</span><span class="sxs-lookup"><span data-stu-id="9e70c-264">The naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="9e70c-265">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-269">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="9e70c-270">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9e70c-271">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-272">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="9e70c-272">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-273">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-273">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-275">Modalità di configurazione per l'endpoint VLAN.</span><span class="sxs-lookup"><span data-stu-id="9e70c-275">The configuration mode for the VLAN endpoint.</span></span> <span data-ttu-id="9e70c-276">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-276">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>



| <span data-ttu-id="9e70c-277">Valore</span><span class="sxs-lookup"><span data-stu-id="9e70c-277">Value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="9e70c-278">Significato</span><span class="sxs-lookup"><span data-stu-id="9e70c-278">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9e70c-279"><dt>**DMTF riservato**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-279"><dt>**DMTF Reserved**</dt> <dt>0</dt></span></span> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="9e70c-280"><dt>**Altro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-280"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                       | <span data-ttu-id="9e70c-281">L'endpoint non è compatibile con le VLAN.</span><span class="sxs-lookup"><span data-stu-id="9e70c-281">The endpoint is not VLAN aware.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <span data-ttu-id="9e70c-282"><dt>**Accesso**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-282"><dt>**Access**</dt> <dt>2</dt></span></span> </dl>                                                   | <span data-ttu-id="9e70c-283">Inserisce l'endpoint in modalità non di trunking permanente e negozia per convertire il collegamento in un collegamento non trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-283">Puts the endpoint into permanent nontrunking mode and negotiates to convert the link into a nontrunk link.</span></span> <span data-ttu-id="9e70c-284">L'endpoint diventa un'interfaccia non trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-284">The endpoint becomes a nontrunk interface.</span></span><br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <span data-ttu-id="9e70c-285"><dt>**Auto dinamica**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-285"><dt>**Dynamic Auto**</dt> <dt>3</dt></span></span> </dl>                           | <span data-ttu-id="9e70c-286">Rende l'endpoint in grado di convertire il collegamento in un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-286">Makes the endpoint able to convert the link to a trunk link.</span></span> <span data-ttu-id="9e70c-287">L'endpoint diventa un'interfaccia trunk se l'interfaccia adiacente è impostata su trunk o sulla modalità desiderata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-287">The endpoint becomes a trunk interface if the neighboring interface is set to trunk or desirable mode.</span></span><br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <span data-ttu-id="9e70c-288"><dt>**Auspicabile dinamico**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-288"><dt>**Dynamic Desirable**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="9e70c-289">Fa in modo che l'endpoint tenti attivamente di convertire il collegamento a un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-289">Makes the endpoint actively attempt to convert the link to a trunk link.</span></span> <span data-ttu-id="9e70c-290">L'endpoint diventa un'interfaccia trunk se l'interfaccia vicina è impostata su trunk, auspicabile o modalità auto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-290">The endpoint becomes a trunk interface if the neighboring interface is set to trunk, desirable, or auto mode.</span></span> <span data-ttu-id="9e70c-291">Questa è la modalità predefinita per le porte switch per tutte le interfacce Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9e70c-291">This is the default switch-port mode for all Ethernet interfaces.</span></span><br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <span data-ttu-id="9e70c-292"><dt>**Trunk**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-292"><dt>**Trunk**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="9e70c-293">Inserisce l'endpoint in modalità di trunking permanente e negozia per convertire il collegamento in un collegamento di trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-293">Puts the endpoint into permanent trunking mode and negotiates to convert the link into a trunk link.</span></span> <span data-ttu-id="9e70c-294">L'endpoint diventa un'interfaccia trunk anche se l'interfaccia adiacente non è un'interfaccia trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-294">The endpoint becomes a trunk interface even if the neighboring interface is not a trunk interface.</span></span><br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <span data-ttu-id="9e70c-295"><dt>**Dot1Q tunnel**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-295"><dt>**Dot1Q Tunnel**</dt> <dt>6</dt></span></span> </dl>                           | <span data-ttu-id="9e70c-296">Configura l'interfaccia come endpoint/porta del tunnel (non di trunking) per essere connessa in un collegamento asimmetrico con una porta trunk 802.1 Q.</span><span class="sxs-lookup"><span data-stu-id="9e70c-296">Configures the interface as a tunnel (nontrunking) endpoint/port to be connected in an asymmetric link with an 802.1Q trunk port.</span></span> <span data-ttu-id="9e70c-297">il tunneling 802.1 q viene usato per mantenere l'integrità VLAN del cliente attraverso una rete del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="9e70c-297">802.1Q tunneling is used to maintain customer VLAN integrity across a service provider network.</span></span><br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9e70c-298"><dt>**DMTF riservato**</dt> <dt>7 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-298"><dt>**DMTF Reserved**</dt> <dt>7 32767</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9e70c-299"><dt> **Fornitore riservato**</dt> <dt>32768 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-299"><dt>**Vendor Reserved** </dt> <dt>32768 65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="9e70c-300">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-300">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-301">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-301">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-302">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-303">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9e70c-303">The current statuses of the object.</span></span> <span data-ttu-id="9e70c-304">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="9e70c-304">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-305">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="9e70c-305">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-306">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-306">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-307">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-308">Tipo di incapsulamento VLAN in uso su un endpoint/porta trunk.</span><span class="sxs-lookup"><span data-stu-id="9e70c-308">The type of VLAN encapsulation in use on a trunk endpoint/port.</span></span> <span data-ttu-id="9e70c-309">Questa proprietà è 2 (non applicabile) (ovvero l'endpoint non funziona in modalità di trunk), un tipo particolare (3-802.1 Q o 4-Cisco ISL), 5 (Negotiate) (ovvero gli endpoint stanno negoziando il tipo di incapsulamento).</span><span class="sxs-lookup"><span data-stu-id="9e70c-309">This property is either 2 (Not Applicable) (that is, the endpoint is not operating in trunking mode), a particular type (3 - 802.1Q or 4 - Cisco ISL), 5 (Negotiate) (that is, the endpoints are negotiating the encapsulation type).</span></span> <span data-ttu-id="9e70c-310">Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-310">This property is only applicable when the endpoint is operating in a trunking mode (see the **OperationalEndpointMode** property for additional details).</span></span> <span data-ttu-id="9e70c-311">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-311">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

<dl> <dt>

<span data-ttu-id="9e70c-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="9e70c-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="9e70c-313"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)</span><span class="sxs-lookup"><span data-stu-id="9e70c-314"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="9e70c-315"><span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="9e70c-316"><span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negoziazione** (5)</span><span class="sxs-lookup"><span data-stu-id="9e70c-317"><span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negotiating** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (6 32767)</span><span class="sxs-lookup"><span data-stu-id="9e70c-318"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (6 32767)</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="9e70c-319"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9e70c-320">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="9e70c-320">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-321">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-321">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-322">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-323">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="9e70c-323">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="9e70c-324">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="9e70c-324">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="9e70c-325">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="9e70c-325">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-326">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="9e70c-326">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-327">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-328">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-329">Tipo di modello di endpoint VLAN supportato da questo endpoint VLAN, quando il valore della proprietà **OperationalEndpointMode** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="9e70c-329">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the **OperationalEndpointMode** property is set to 1 (Other).</span></span> <span data-ttu-id="9e70c-330">Questa proprietà deve essere impostata su **null** se la proprietà **OperationalEndpointMode** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="9e70c-330">This property should be set to **Null** when the **OperationalEndpointMode** property is any value other than 1.</span></span> <span data-ttu-id="9e70c-331">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-331">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-332">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="9e70c-332">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-333">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-334">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-335">Tipo di incapsulamento VLAN supportato da questo endpoint VLAN, quando il valore della proprietà **OperationalVLANTrunkEncapsulation** è impostato su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="9e70c-335">The type of VLAN encapsulation that is supported by this VLAN endpoint, when the value of the **OperationalVLANTrunkEncapsulation** property is set to 1 (Other).</span></span> <span data-ttu-id="9e70c-336">Questa proprietà deve essere impostata su **null** se la proprietà di incapsulamento desiderata è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="9e70c-336">This property should be set to **Null** when the desired encapsulation property is any value other than 1.</span></span> <span data-ttu-id="9e70c-337">Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-337">This property is inherited from [**CIM\_VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-338">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="9e70c-338">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-339">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-339">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-340">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-341">Tipo di endpoint del protocollo quando la proprietà **Type** di questa classe (o una delle relative sottoclassi) è impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="9e70c-341">The type of protocol endpoint when the **Type** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="9e70c-342">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)ed è sempre impostata su "Virtual Ethernet".</span><span class="sxs-lookup"><span data-stu-id="9e70c-342">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to "Virtual Ethernet".</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="9e70c-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-344">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-345">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-346">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="9e70c-346">Provides high level status information.</span></span> <span data-ttu-id="9e70c-347">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="9e70c-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="9e70c-348">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="9e70c-349">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-350">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="9e70c-350">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-351">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-351">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-353">[IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="9e70c-353">The [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="9e70c-354">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)ed è sempre impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="9e70c-354">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is always set to 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-355">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="9e70c-355">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-356">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-356">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-358">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-358">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-359">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="9e70c-359">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-360">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-362">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="9e70c-362">The last requested or desired state for the management service.</span></span> <span data-ttu-id="9e70c-363">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="9e70c-363">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="9e70c-364">Valore</span><span class="sxs-lookup"><span data-stu-id="9e70c-364">Value</span></span>                                                                         | <span data-ttu-id="9e70c-365">Significato</span><span class="sxs-lookup"><span data-stu-id="9e70c-365">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="9e70c-366"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-366"><dt>12</dt></span></span> </dl> | <span data-ttu-id="9e70c-367">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="9e70c-367">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9e70c-368">**Status**</span><span class="sxs-lookup"><span data-stu-id="9e70c-368">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-369">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-371">Descrive lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9e70c-371">Describes the status of the element.</span></span> <span data-ttu-id="9e70c-372">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="9e70c-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="9e70c-373">OK</span><span class="sxs-lookup"><span data-stu-id="9e70c-373">"OK"</span></span>

<span data-ttu-id="9e70c-374">Errore</span><span class="sxs-lookup"><span data-stu-id="9e70c-374">"Error"</span></span>

<span data-ttu-id="9e70c-375">Degradato</span><span class="sxs-lookup"><span data-stu-id="9e70c-375">"Degraded"</span></span>

<span data-ttu-id="9e70c-376">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="9e70c-376">"Unknown"</span></span>

<span data-ttu-id="9e70c-377">"Errore di predazione"</span><span class="sxs-lookup"><span data-stu-id="9e70c-377">"Pred Fail"</span></span>

<span data-ttu-id="9e70c-378">Avvio</span><span class="sxs-lookup"><span data-stu-id="9e70c-378">"Starting"</span></span>

<span data-ttu-id="9e70c-379">Arresto</span><span class="sxs-lookup"><span data-stu-id="9e70c-379">"Stopping"</span></span>

<span data-ttu-id="9e70c-380">Servizio</span><span class="sxs-lookup"><span data-stu-id="9e70c-380">"Service"</span></span>

<span data-ttu-id="9e70c-381">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="9e70c-381">"Stressed"</span></span>

<span data-ttu-id="9e70c-382">"Non ripristino"</span><span class="sxs-lookup"><span data-stu-id="9e70c-382">"NonRecover"</span></span>

<span data-ttu-id="9e70c-383">"Nessun contatto"</span><span class="sxs-lookup"><span data-stu-id="9e70c-383">"No Contact"</span></span>

<span data-ttu-id="9e70c-384">"Lost comm"</span><span class="sxs-lookup"><span data-stu-id="9e70c-384">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-385">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="9e70c-385">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-386">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9e70c-386">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-387">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-388">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="9e70c-388">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="9e70c-389">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="9e70c-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-390">**SupportedEndpointModes**</span><span class="sxs-lookup"><span data-stu-id="9e70c-390">**SupportedEndpointModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-391">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-391">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-392">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-393">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="9e70c-393">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-394">Modalità dell'endpoint supportate da questa porta.</span><span class="sxs-lookup"><span data-stu-id="9e70c-394">The endpoint modes supported by this port.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-395">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9e70c-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-396">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-398">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9e70c-398">The creation class name of the scoping system.</span></span> <span data-ttu-id="9e70c-399">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)ed è sempre impostata su "MSVM \_ VirtualSwitch"</span><span class="sxs-lookup"><span data-stu-id="9e70c-399">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_VirtualSwitch"</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-400">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9e70c-400">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9e70c-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-403">Nome di sistema del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="9e70c-403">The system name of the scoping system.</span></span> <span data-ttu-id="9e70c-404">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="9e70c-404">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-405">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="9e70c-405">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-406">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9e70c-406">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-407">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-408">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="9e70c-408">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="9e70c-409">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-409">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9e70c-410">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="9e70c-410">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9e70c-411">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9e70c-411">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9e70c-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9e70c-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9e70c-413">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9e70c-413">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="9e70c-414">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="9e70c-414">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e70c-415">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e70c-415">Remarks</span></span>

<span data-ttu-id="9e70c-416">L'accesso alla **classe \_ VLANEndpoint di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="9e70c-416">Access to the **Msvm\_VLANEndpoint** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9e70c-417">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9e70c-417">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9e70c-418">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e70c-418">Examples</span></span>

<span data-ttu-id="9e70c-419">Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9e70c-419">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9e70c-420">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e70c-420">Requirements</span></span>



| <span data-ttu-id="9e70c-421">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e70c-421">Requirement</span></span> | <span data-ttu-id="9e70c-422">Valore</span><span class="sxs-lookup"><span data-stu-id="9e70c-422">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e70c-423">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e70c-423">Minimum supported client</span></span><br/> | <span data-ttu-id="9e70c-424">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9e70c-424">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9e70c-425">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e70c-425">Minimum supported server</span></span><br/> | <span data-ttu-id="9e70c-426">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9e70c-426">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9e70c-427">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9e70c-427">Namespace</span></span><br/>                | <span data-ttu-id="9e70c-428">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9e70c-428">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9e70c-429">MOF</span><span class="sxs-lookup"><span data-stu-id="9e70c-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e70c-430"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-430"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e70c-431">DLL</span><span class="sxs-lookup"><span data-stu-id="9e70c-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e70c-432"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9e70c-432"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9e70c-433">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e70c-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e70c-434">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="9e70c-434">**CIM\_VLANEndpoint**</span></span>](cim-vlanendpoint.md)
</dt> <dt>

[<span data-ttu-id="9e70c-435">**\_VLANENDPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="9e70c-435">**CIM\_VLANEndpoint**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

