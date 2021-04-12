---
description: Rappresenta il punto di connessione logico per una scheda di rete. Quando l'endpoint LAN è connesso a una porta di commutazione, la scheda di rete connessa all'endpoint LAN dispone di connettività di rete.
ms.assetid: 68aad05e-64b5-44dc-ab5b-8f3051fa77ca
title: Classe Msvm_LANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LANEndpoint
- Msvm_LANEndpoint.InstanceID
- Msvm_LANEndpoint.Caption
- Msvm_LANEndpoint.Description
- Msvm_LANEndpoint.ElementName
- Msvm_LANEndpoint.InstallDate
- Msvm_LANEndpoint.Name
- Msvm_LANEndpoint.OperationalStatus
- Msvm_LANEndpoint.StatusDescriptions
- Msvm_LANEndpoint.Status
- Msvm_LANEndpoint.HealthState
- Msvm_LANEndpoint.CommunicationStatus
- Msvm_LANEndpoint.DetailedStatus
- Msvm_LANEndpoint.OperatingStatus
- Msvm_LANEndpoint.PrimaryStatus
- Msvm_LANEndpoint.EnabledState
- Msvm_LANEndpoint.OtherEnabledState
- Msvm_LANEndpoint.RequestedState
- Msvm_LANEndpoint.EnabledDefault
- Msvm_LANEndpoint.TimeOfLastStateChange
- Msvm_LANEndpoint.AvailableRequestedStates
- Msvm_LANEndpoint.TransitioningToState
- Msvm_LANEndpoint.SystemCreationClassName
- Msvm_LANEndpoint.SystemName
- Msvm_LANEndpoint.CreationClassName
- Msvm_LANEndpoint.NameFormat
- Msvm_LANEndpoint.ProtocolType
- Msvm_LANEndpoint.ProtocolIFType
- Msvm_LANEndpoint.OtherTypeDescription
- Msvm_LANEndpoint.LANID
- Msvm_LANEndpoint.LANType
- Msvm_LANEndpoint.OtherLANType
- Msvm_LANEndpoint.MACAddress
- Msvm_LANEndpoint.AliasAddresses
- Msvm_LANEndpoint.GroupAddresses
- Msvm_LANEndpoint.MaxDataSize
- Msvm_LANEndpoint.Connected
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7585b92461b435b99a05ed198c4c501e10703439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231751"
---
# <a name="msvm_lanendpoint-class"></a><span data-ttu-id="7f9e0-104">\_Classe MSVM LANEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f9e0-104">Msvm\_LANEndpoint class</span></span>

<span data-ttu-id="7f9e0-105">Rappresenta il punto di connessione logico per una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-105">Represents the logical connection point for a network adapter.</span></span> <span data-ttu-id="7f9e0-106">Quando l'endpoint LAN è connesso a una porta di commutazione, la scheda di rete connessa all'endpoint LAN dispone di connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-106">When the LAN endpoint is connected to a switch port, the network adapter connected to the LAN endpoint has network connectivity.</span></span>

<span data-ttu-id="7f9e0-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9e0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f9e0-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LANEndpoint : CIM_LANEndpoint
{
  string   InstanceID;
  string   Caption = "LAN Endpoint";
  string   Description = "Microsoft Virtual LAN Endpoint";
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
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_LANEndpoint";
  string   NameFormat = "Microsoft Virtual Device ID";
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
};
```

## <a name="members"></a><span data-ttu-id="7f9e0-109">Members</span><span class="sxs-lookup"><span data-stu-id="7f9e0-109">Members</span></span>

<span data-ttu-id="7f9e0-110">La **classe \_ LANEndpoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7f9e0-110">The **Msvm\_LANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="7f9e0-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="7f9e0-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7f9e0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f9e0-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7f9e0-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="7f9e0-113">Methods</span></span>

<span data-ttu-id="7f9e0-114">La **classe \_ LANEndpoint di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-114">The **Msvm\_LANEndpoint** class has these methods.</span></span>



| <span data-ttu-id="7f9e0-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="7f9e0-115">Method</span></span>                                                            | <span data-ttu-id="7f9e0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f9e0-116">Description</span></span>                         |
|:------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="7f9e0-117">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-117">**RequestStateChange**</span></span>](msvm-lanendpoint-requeststatechange.md) | <span data-ttu-id="7f9e0-118">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-118">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7f9e0-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f9e0-119">Properties</span></span>

<span data-ttu-id="7f9e0-120">La **classe \_ LANEndpoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-120">The **Msvm\_LANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f9e0-121">**AliasAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-121">**AliasAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-122">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-122">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-124">Altri indirizzi unicast che possono essere utilizzati per comunicare con l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-124">Other unicast addresses that may be used to communicate with the LAN endpoint.</span></span> <span data-ttu-id="7f9e0-125">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-125">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-126">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-129">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="7f9e0-130">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span> <span data-ttu-id="7f9e0-131">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="7f9e0-132">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="7f9e0-133">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="7f9e0-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="7f9e0-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="7f9e0-144">)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9e0-145">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-148">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-148">A short description of the object.</span></span> <span data-ttu-id="7f9e0-149">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "LAN endpoint".</span><span class="sxs-lookup"><span data-stu-id="7f9e0-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-150">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-153">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="7f9e0-154">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9e0-155">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-156">**Connessione effettuata**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-156">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-157">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-159">Questa proprietà è impostata su **true** se l'endpoint LAN è connesso a una porta di commutazione.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-159">This property is set to **True** if the LAN endpoint is connected to a switch port.</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-160">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-160">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-163">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-163">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-164">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-164">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7f9e0-165">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)ed è sempre impostata su "MSVM \_ LANEndpoint".</span><span class="sxs-lookup"><span data-stu-id="7f9e0-165">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint), and it is always set to "Msvm\_LANEndpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-166">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-166">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-169">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-169">A description of the object.</span></span> <span data-ttu-id="7f9e0-170">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft Virtual LAN endpoint".</span><span class="sxs-lookup"><span data-stu-id="7f9e0-170">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual LAN Endpoint".</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-171">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-171">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-172">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-172">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-174">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-174">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="7f9e0-175">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-175">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9e0-176">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-176">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-180">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-180">A display name for the object.</span></span> <span data-ttu-id="7f9e0-181">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-181">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-182">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-182">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-183">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-185">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-185">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="7f9e0-186">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-186">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7f9e0-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-187"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-188"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-189"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9e0-190">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-190">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-191">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-193">Specifica lo stato abilitato del sistema pianificato.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-193">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="7f9e0-194">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-194">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="7f9e0-195">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9e0-195">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="7f9e0-196">Significato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-196">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="7f9e0-197"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-197"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="7f9e0-198">Il sistema è disattivato.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-198">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="7f9e0-199"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-199"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="7f9e0-200">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-200">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="7f9e0-201"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-201"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="7f9e0-202">Il sistema è abilitato, ma non è in linea.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-202">The system is enabled, but offline.</span></span> <span data-ttu-id="7f9e0-203">Tutte le nuove richieste verranno eliminate.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-203">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f9e0-204">**GroupAddresses**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-204">**GroupAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-205">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-205">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-206">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-207">Indirizzi multicast su cui è in ascolto l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-207">Multicast addresses to which the LAN endpoint listens.</span></span> <span data-ttu-id="7f9e0-208">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-208">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-209">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-209">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-210">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-212">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-212">The current health of the element.</span></span> <span data-ttu-id="7f9e0-213">Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-213">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="7f9e0-214">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-214">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="7f9e0-215">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="7f9e0-216">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9e0-216">Value</span></span>                                                                        | <span data-ttu-id="7f9e0-217">Significato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-217">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7f9e0-218"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-218"><dt>5</dt></span></span> </dl> | <span data-ttu-id="7f9e0-219">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-219">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f9e0-220">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-220">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-221">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-221">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-223">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-223">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="7f9e0-224">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-224">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-225">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-225">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-226">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-227">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-228">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-228">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-229">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-229">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7f9e0-230">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-230">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-231">**LANId**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-231">**LANID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-232">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-233">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-234">Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-234">A label or identifier for the LAN segment to which the endpoint is connected.</span></span> <span data-ttu-id="7f9e0-235">Se l'endpoint non è attualmente attivo/connesso o queste informazioni non sono note, questa proprietà sarà **null**.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-235">If the endpoint is not currently active/connected, or this information is not known, then this property will be **Null**.</span></span> <span data-ttu-id="7f9e0-236">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-236">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-237">**LANType**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-237">**LANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-238">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-238">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-240">Questa proprietà è deprecata al posto della proprietà **ProtocolType** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-240">This property is deprecated in lieu of the **ProtocolType** property.</span></span> <span data-ttu-id="7f9e0-241">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-241">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-242">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-242">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-243">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-245">Qualificatori: **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-245">Qualifiers: **MaxLen** ( 12 )</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-246">Indirizzo MAC utilizzato per la comunicazione con l'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-246">The MAC address used in communication with the LAN endpoint.</span></span> <span data-ttu-id="7f9e0-247">L'indirizzo MAC è formattato come dodici cifre esadecimali (ad esempio, "010203040506"), ciascuna delle quali rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico in base a RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-247">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span> <span data-ttu-id="7f9e0-248">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-248">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-249">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-249">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-250">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-250">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-251">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-252">Qualificatori: **unità** ("bits")</span><span class="sxs-lookup"><span data-stu-id="7f9e0-252">Qualifiers: **Units** ("Bits")</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-253">Dimensione massima, in numero di bit, del campo informazioni che può essere inviato o ricevuto dall'endpoint LAN.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-253">The largest size, in number of bits, of the information field that may be sent or received by the LAN endpoint.</span></span> <span data-ttu-id="7f9e0-254">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-254">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-255">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-255">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-256">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-257">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-258">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-258">The label by which the object is known.</span></span> <span data-ttu-id="7f9e0-259">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-260">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-260">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-261">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-262">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-263">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-263">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-264">Contiene l'euristica di denominazione selezionata per garantire che il valore della proprietà **Name** sia univoco.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-264">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="7f9e0-265">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)ed è impostata su "Microsoft Virtual Device ID".</span><span class="sxs-lookup"><span data-stu-id="7f9e0-265">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint), and it is set to "Microsoft Virtual Device ID".</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-269">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="7f9e0-270">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9e0-271">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-273">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-275">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-275">The current statuses of the object.</span></span> <span data-ttu-id="7f9e0-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-277">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-277">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-278">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-279">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-280">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="7f9e0-280">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="7f9e0-281">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-281">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="7f9e0-282">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-282">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-283">**OtherLANType**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-283">**OtherLANType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-284">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-286">Questa proprietà è deprecata al posto della proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-286">This property is deprecated in lieu of the **OtherTypeDescription** property.</span></span> <span data-ttu-id="7f9e0-287">Questa proprietà viene ereditata da [**CIM \_ LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-287">This property is inherited from [**CIM\_LANEndpoint**](/previous-versions//cc136865(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-288">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-288">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-289">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-290">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-291">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-291">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-292">Stringa che descrive il tipo di endpoint del protocollo quando la proprietà **ProtocolIFType** di questa classe (o una delle relative sottoclassi) viene impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-292">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="7f9e0-293">Questa proprietà deve essere impostata su **null** se la proprietà **ProtocolIFType** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-293">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="7f9e0-294">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-294">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-295">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-295">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-296">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-297">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-298">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-298">Provides high level status information.</span></span> <span data-ttu-id="7f9e0-299">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-299">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="7f9e0-300">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-300">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="7f9e0-301">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-301">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-302">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-302">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-303">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-303">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-304">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-305">La proprietà viene utilizzata per suddividere in categorie e classificare le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-305">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="7f9e0-306">Se **ProtocolIFType** è impostato su 1 (other), le informazioni sul tipo devono essere fornite nella proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-306">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="7f9e0-307">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-307">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="7f9e0-308">**ProtocolIFType** è un'enumerazione sincronizzata con [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-308">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="7f9e0-309">Sono inclusi anche valori aggiuntivi definiti da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-309">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="7f9e0-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-310"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-311"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Normale 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-312"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-313"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-314"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-315"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**CSMA Ethernet/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-316"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-317"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Bus token ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-318"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Anello token ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-319"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 uomo** (10)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-320"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-321"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-322"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-323"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Ipercanale** (14)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-324"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-325"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-326"><span id="LAP-B"></span><span id="lap-b"></span>**Lap-B** (16)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-326"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-327"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-328"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-329"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**ISDN Basic** (20)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-330"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**ISDN primario** (21)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-331"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Seriale point-to-Point proprietario** (22)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-332"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-333"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Loopback software** (24)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-334"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-335"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-336"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-337"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-338"><span id="SLIP"></span><span id="slip"></span>**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-338"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-339"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-340"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-341"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Inoltro frame** (32)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-342"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-343"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallelo** (34)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-344"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-345"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-346"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-347"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-348"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-349"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 PLE** (40)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-350"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**802.211 ISO c** (41)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-351"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-352"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-353"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Servizio frame relay** (44)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-354"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-355"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-355"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-356"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-357"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-358"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-359"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Percorso SONET** (50)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-360"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**VT SONET** (51)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-361"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-362"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietario virtuale/interno** (53)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-363"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexer proprietario** (54)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-364"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-365"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-366"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interfaccia HIPPI** (57)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-367"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconnessione frame relay** (58)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-368"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**LAN emulata ATM per 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-369"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**LAN emulata ATM per 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-370"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuito emulato ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-371"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Ethernet veloce (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-372"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-373"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-374"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-374"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-375"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-375"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 a 64K** (66)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-376"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 a 2MB** (67)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-377"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-378"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-379"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canale** (70)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-380"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-381"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canale OEMI IBM 260/370** (72)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-382"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-383"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Cambio collegamento dati** (74)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-384"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interfaccia S/T ISDN** (75)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-385"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interfaccia ISDN U** (76)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-386"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-387"><span id="LAP-D"></span><span id="lap-d"></span>**Lap-D** (77)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-387"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Opzione IP** (78)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-388"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Bridging Route origine remota** (79)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-389"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**Logica ATM** (80)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-390"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-391"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Bundle DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-392"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-393"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-394"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat net radio** (85)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-395"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**802.5 ISO r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-396"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Sistema di segnalazione EXT POS loc** (87)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-397"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocollo di accesso remoto AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-398"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>Senza **connessione proprietaria** (89)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-399"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Pad host ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-400"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Pad terminale ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-401"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI frame relay** (92)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-402"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-403"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-404"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-405"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-406"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-407"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-408"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-409"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Ricezione e trasmissione vocale** (100)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-410"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>Segreteria esterna per la **voce di Exchange** (101)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-411"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Servizio scambio vocale** (102)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-412"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Incapsulamento vocale** (103)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-413"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-414"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**DXi ATM** (105)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-415"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**Funi ATM** (106)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-416"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-417"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Bundle Multilink PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-418"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP su CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-419"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over Claw** (110)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-420"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack da** stack (111)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-421"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Indirizzo IP virtuale** (112)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-422"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-423"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP su ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-424"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**Anello di token fibre ISO 802.5 j** (115)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-425"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-426"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Ethernet Gigabit** (117)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-427"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-428"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-429"><span id="LAP-F"></span><span id="lap-f"></span>**Lap-F** (119)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-429"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-430"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-430"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-431"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Gruppo di caccia X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-432"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-433"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Canale interleave** (124)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-434"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Canale rapido** (125)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-435"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (per APPN HPR in reti IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-436"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Livello Mac CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-437"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV downstream** (128)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-438"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV upstream** (129)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-439"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Switch Avalon 12MPP** (130)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-440"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-441"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Caffè** (132)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-442"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Servizio di emulazione del circuito** (133)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-443"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Sottointerfaccia ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-444"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN di livello 2 con 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-445"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**VLAN di livello 3 con IP** (136)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-446"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**VLAN di livello 3 con IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-447"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Linea di alimentazione digitale** (138)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-448"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Posta elettronica multimediale su IP** (139)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-449"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-450"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-451"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Inoltri IP** (142)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-452"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-453"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-454"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/HIPPI-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-455"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Livello Mac DVB-RCC** (146)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-456"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC downstream** (147)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-457"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC upstream** (148)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-458"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM virtuale** (149)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-459"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Tunnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-460"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-461"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-462"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Inoltro del frame Voice over** (153)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-463"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-464"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Collegamento composito** (155)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-465"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Collegamento di segnalazione SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-466"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Wireless P2P proprietario** (157)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-467"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame in** poi (158)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-468"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol su ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-469"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-470"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Aggregazione collegamento ad IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-471"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Contabilità dei criteri BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-472"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-473"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Gatekeeper H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-474"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**Proxy H. 323** (165)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-475"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-476"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Collegamento** per la segnalazione a più frequenze (167)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-477"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-478"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-479"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Collegamento dati della struttura DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-480"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-481"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Input DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-482"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Output DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-483"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Linea di alimentazione** (174)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-484"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Segnalazione non associata alla struttura** (175)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-485"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-486"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-487"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-488"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-489"><span id="ISUP"></span><span id="isup"></span>**IsUp** (179)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-489"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Livello MAC wireless proprietario** (180)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-490"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Wireless proprietario a valle** (181)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-491"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Upstream senza fili proprietario** (182)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-492"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**Hiperlan tipo 2** (183)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-493"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Punto di accesso wireless a banda larga proprietario per MultiPoint** (184)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-494"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canale overhead SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-495"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canale overhead del wrapper digitale** (186)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-496"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Livello 2 di adattamento ATM** (187)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-497"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac Radio** (188)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-498"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Radio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-499"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Trunk tra computer** (190)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-500"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**DSL MVL** (191)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-501"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**DSL lungo lettura** (192)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-502"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Endpoint DLCI frame relay** (193)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-503"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Endpoint VCI ATM** (194)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-504"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canale ottico** (195)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-505"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Trasporto ottico** (196)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-506"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM proprietario** (197)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-507"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Cavo Voice over** (198)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-508"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-509"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Collegamento te** (200)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-510"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-511"><span id="Q.2931"></span><span id="q.2931"></span>**D. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-511"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Gruppo Trunk virtuale** (202)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-512"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Gruppo Trunk SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-513"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Segnalazione SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-514"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canale upstream CATV** (205)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-515"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**ECONT** (206)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-516"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB pon** (207)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-517"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB pon** (208)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-518"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Bridge trasparente** (209)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-519"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Gruppo di righe** (210)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-520"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Gruppo di funzionalità Voice &** (211)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-521"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-522"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voce did** (213)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-523"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Trasporto MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-524"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-525"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-526"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-527"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-528"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Gruppo canale ottico** (219)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-529"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-530"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-531"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-532"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-533"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-534"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA riservato** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-535"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-536"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-537"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-538"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-539"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-540"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-541"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-542"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-543"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-544"><span id="VINES"></span><span id="vines"></span>**Viti** (4104)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-544"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-545"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Endpoint del canale ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-546"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Endpoint canale ISDN D** (4107)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-547"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-548"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-549"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-550"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-551"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-552"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-553"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-554"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-555"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-556"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-557"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-558"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-559"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-560"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-560"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-561"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-562"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-563"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-564"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**CLP SM** (4402)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-565"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-566"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-567"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-568"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-569"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-569"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-570"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768..</span><span class="sxs-lookup"><span data-stu-id="7f9e0-571"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="7f9e0-572">)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-572">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7f9e0-573">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-573">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-574">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-574">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-575">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-575">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-576">Questa proprietà è deprecata al posto della proprietà **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-576">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="7f9e0-577">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-577">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-578">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-578">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-579">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-579">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-580">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-580">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-581">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-581">The last requested or desired state for the management service.</span></span> <span data-ttu-id="7f9e0-582">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-582">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="7f9e0-583">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9e0-583">Value</span></span>                                                                         | <span data-ttu-id="7f9e0-584">Significato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-584">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7f9e0-585"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-585"><dt>12</dt></span></span> </dl> | <span data-ttu-id="7f9e0-586">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-586">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f9e0-587">**Status**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-587">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-588">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-589">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-589">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-590">Descrive lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-590">Describes the status of the element.</span></span> <span data-ttu-id="7f9e0-591">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-591">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="7f9e0-592">OK</span><span class="sxs-lookup"><span data-stu-id="7f9e0-592">"OK"</span></span>

<span data-ttu-id="7f9e0-593">Errore</span><span class="sxs-lookup"><span data-stu-id="7f9e0-593">"Error"</span></span>

<span data-ttu-id="7f9e0-594">Degradato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-594">"Degraded"</span></span>

<span data-ttu-id="7f9e0-595">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="7f9e0-595">"Unknown"</span></span>

<span data-ttu-id="7f9e0-596">"Errore di predazione"</span><span class="sxs-lookup"><span data-stu-id="7f9e0-596">"Pred Fail"</span></span>

<span data-ttu-id="7f9e0-597">Avvio</span><span class="sxs-lookup"><span data-stu-id="7f9e0-597">"Starting"</span></span>

<span data-ttu-id="7f9e0-598">Arresto</span><span class="sxs-lookup"><span data-stu-id="7f9e0-598">"Stopping"</span></span>

<span data-ttu-id="7f9e0-599">Servizio</span><span class="sxs-lookup"><span data-stu-id="7f9e0-599">"Service"</span></span>

<span data-ttu-id="7f9e0-600">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-600">"Stressed"</span></span>

<span data-ttu-id="7f9e0-601">"Non ripristino"</span><span class="sxs-lookup"><span data-stu-id="7f9e0-601">"NonRecover"</span></span>

<span data-ttu-id="7f9e0-602">"Nessun contatto"</span><span class="sxs-lookup"><span data-stu-id="7f9e0-602">"No Contact"</span></span>

<span data-ttu-id="7f9e0-603">"Lost comm"</span><span class="sxs-lookup"><span data-stu-id="7f9e0-603">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-604">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-604">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-605">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-605">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-606">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-607">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="7f9e0-607">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="7f9e0-608">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="7f9e0-608">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-609">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-609">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-610">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-611">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-612">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-612">The hosting system's creation class name.</span></span> <span data-ttu-id="7f9e0-613">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-613">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-614">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-614">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-615">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-615">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-616">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-616">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-617">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="7f9e0-617">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-618">Nome del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-618">The name of the hosting system.</span></span> <span data-ttu-id="7f9e0-619">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="7f9e0-619">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-620">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-620">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-621">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-621">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-622">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-623">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-623">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="7f9e0-624">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-624">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7f9e0-625">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-625">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f9e0-626">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7f9e0-626">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7f9e0-627">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f9e0-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f9e0-628">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-628">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="7f9e0-629">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="7f9e0-629">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f9e0-630">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f9e0-630">Requirements</span></span>



| <span data-ttu-id="7f9e0-631">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9e0-631">Requirement</span></span> | <span data-ttu-id="7f9e0-632">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9e0-632">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9e0-633">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-633">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9e0-634">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7f9e0-634">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7f9e0-635">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f9e0-635">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9e0-636">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7f9e0-636">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f9e0-637">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f9e0-637">Namespace</span></span><br/>                | <span data-ttu-id="7f9e0-638">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7f9e0-638">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7f9e0-639">MOF</span><span class="sxs-lookup"><span data-stu-id="7f9e0-639">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f9e0-640"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-640"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f9e0-641">DLL</span><span class="sxs-lookup"><span data-stu-id="7f9e0-641">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f9e0-642"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7f9e0-642"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

