---
description: Rappresenta il punto di connessione logico per una porta Fibre Channel.
ms.assetid: 54e9cb76-04f2-417b-b250-1b3156772694
title: Classe Msvm_FcEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcEndpoint
- Msvm_FcEndpoint.InstanceID
- Msvm_FcEndpoint.Caption
- Msvm_FcEndpoint.Description
- Msvm_FcEndpoint.ElementName
- Msvm_FcEndpoint.InstallDate
- Msvm_FcEndpoint.Name
- Msvm_FcEndpoint.OperationalStatus
- Msvm_FcEndpoint.StatusDescriptions
- Msvm_FcEndpoint.Status
- Msvm_FcEndpoint.HealthState
- Msvm_FcEndpoint.CommunicationStatus
- Msvm_FcEndpoint.DetailedStatus
- Msvm_FcEndpoint.OperatingStatus
- Msvm_FcEndpoint.PrimaryStatus
- Msvm_FcEndpoint.EnabledState
- Msvm_FcEndpoint.OtherEnabledState
- Msvm_FcEndpoint.RequestedState
- Msvm_FcEndpoint.EnabledDefault
- Msvm_FcEndpoint.TimeOfLastStateChange
- Msvm_FcEndpoint.AvailableRequestedStates
- Msvm_FcEndpoint.TransitioningToState
- Msvm_FcEndpoint.SystemCreationClassName
- Msvm_FcEndpoint.SystemName
- Msvm_FcEndpoint.CreationClassName
- Msvm_FcEndpoint.NameFormat
- Msvm_FcEndpoint.ProtocolType
- Msvm_FcEndpoint.ProtocolIFType
- Msvm_FcEndpoint.OtherTypeDescription
- Msvm_FcEndpoint.Connected
- Msvm_FcEndpoint.WWPN
- Msvm_FcEndpoint.WWNN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b28136cfc4f0afcf84b5f53ade4976760c997e36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526844"
---
# <a name="msvm_fcendpoint-class"></a><span data-ttu-id="e0ef1-103">\_Classe MSVM FcEndpoint</span><span class="sxs-lookup"><span data-stu-id="e0ef1-103">Msvm\_FcEndpoint class</span></span>

<span data-ttu-id="e0ef1-104">Rappresenta il punto di connessione logico per una porta Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-104">Represents the logical connection point for a Fibre Channel port.</span></span> <span data-ttu-id="e0ef1-105">Quando l'endpoint del Fibre Channel è connesso a una porta di commutazione, la porta Fibre Channel connessa all'endpoint di Fibre Channel ha Fibre Channel connettività.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-105">When the Fibre Channel endpoint is connected to a switch port, the Fibre Channel port connected to the Fibre Channel endpoint has Fibre Channel connectivity.</span></span>

<span data-ttu-id="e0ef1-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ef1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0ef1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcEndpoint : CIM_ProtocolEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
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
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
  boolean  Connected;
  string   WWPN;
  string   WWNN;
};
```

## <a name="members"></a><span data-ttu-id="e0ef1-108">Members</span><span class="sxs-lookup"><span data-stu-id="e0ef1-108">Members</span></span>

<span data-ttu-id="e0ef1-109">La **classe \_ FcEndpoint di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e0ef1-109">The **Msvm\_FcEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e0ef1-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="e0ef1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="e0ef1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0ef1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e0ef1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e0ef1-112">Methods</span></span>

<span data-ttu-id="e0ef1-113">La **classe \_ FcEndpoint di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-113">The **Msvm\_FcEndpoint** class has these methods.</span></span>



| <span data-ttu-id="e0ef1-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="e0ef1-114">Method</span></span>                                                           | <span data-ttu-id="e0ef1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0ef1-115">Description</span></span>                         |
|:-----------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="e0ef1-116">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-116">**RequestStateChange**</span></span>](msvm-fcendpoint-requeststatechange.md) | <span data-ttu-id="e0ef1-117">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e0ef1-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e0ef1-118">Properties</span></span>

<span data-ttu-id="e0ef1-119">La **classe \_ FcEndpoint di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-119">The **Msvm\_FcEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-120">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-121">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-123">Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-123">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="e0ef1-124">I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-124">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class.</span></span> <span data-ttu-id="e0ef1-125">Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-125">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="e0ef1-126">Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-126">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="e0ef1-127">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-127">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-128"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-129"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-130"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-131"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-132"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-133"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-134"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-135"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-136"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (..</span><span class="sxs-lookup"><span data-stu-id="e0ef1-137"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="e0ef1-138">)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-138">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0ef1-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-142">A short description of the object.</span></span> <span data-ttu-id="e0ef1-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-144">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-144">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-145">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-147">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-147">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="e0ef1-148">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-148">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e0ef1-149">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-149">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-150">**Connessione effettuata**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-150">**Connected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-151">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-151">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-153">Questa proprietà è impostata su **true** se l'endpoint Fibre Channel è attivamente connesso a un altro endpoint Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-153">This property is set to **True** if this Fibre Channel endpoint is actively connected to another Fibre Channel endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-154">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-154">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-157">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-157">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-158">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-158">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="e0ef1-159">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-159">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-160">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-163">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-163">A description of the object.</span></span> <span data-ttu-id="e0ef1-164">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-164">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-165">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-165">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-166">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-167">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-168">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-168">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="e0ef1-169">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-169">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e0ef1-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-170">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-172">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-174">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-174">A display name for the object.</span></span> <span data-ttu-id="e0ef1-175">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-176">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-177">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-179">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="e0ef1-180">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e0ef1-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-181"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-182"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-183"><span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Enabled but Offline** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0ef1-184">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-184">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-185">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-185">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-187">Specifica lo stato abilitato del sistema pianificato.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-187">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="e0ef1-188">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-188">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="e0ef1-189">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ef1-189">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="e0ef1-190">Significato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-190">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="e0ef1-191"><dt>**Disabilitato**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-191"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="e0ef1-192">Il sistema è disattivato.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-192">The system is turned off.</span></span><br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="e0ef1-193"><dt>**Non applicabile**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-193"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="e0ef1-194">L'elemento non supporta l'abilitazione o la disabilitazione.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-194">The element does not support being enabled or disabled.</span></span><br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="e0ef1-195"><dt>**Abilitato ma offline**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-195"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="e0ef1-196">Il sistema è abilitato, ma non è in linea.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-196">The system is enabled, but offline.</span></span> <span data-ttu-id="e0ef1-197">Tutte le nuove richieste verranno eliminate.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-197">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0ef1-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-199">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-201">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-201">The current health of the element.</span></span> <span data-ttu-id="e0ef1-202">Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-202">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="e0ef1-203">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-203">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="e0ef1-204">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-204">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-205">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-205">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-206">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-206">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-208">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-208">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="e0ef1-209">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-212">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-213">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-214">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e0ef1-215">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-216">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-216">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-217">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-219">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-219">The label by which the object is known.</span></span> <span data-ttu-id="e0ef1-220">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-220">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-221">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-221">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-224">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-224">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-225">Contiene l'euristica di denominazione selezionata per garantire che il valore della proprietà **Name** sia univoco.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-225">Contains the naming heuristic that is selected to ensure that the value of the **Name** property is unique.</span></span> <span data-ttu-id="e0ef1-226">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-226">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-227">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-227">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-228">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-228">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-230">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-230">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="e0ef1-231">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-231">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e0ef1-232">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-232">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-233">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-233">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-234">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-234">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-235">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-236">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-236">The current statuses of the object.</span></span> <span data-ttu-id="e0ef1-237">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-237">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-238">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-238">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-240">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-241">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="e0ef1-241">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="e0ef1-242">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-242">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="e0ef1-243">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-243">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-244">**OtherTypeDescription**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-244">**OtherTypeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-245">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-246">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-247">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-247">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-248">Stringa che descrive il tipo di endpoint del protocollo quando la proprietà **ProtocolIFType** di questa classe (o una delle relative sottoclassi) viene impostata su 1 (other).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-248">A string that describes the type of protocol endpoint when the **ProtocolIFType** property of this class (or any of its subclasses) is set to 1 (Other).</span></span> <span data-ttu-id="e0ef1-249">Questa proprietà deve essere impostata su **null** se la proprietà **ProtocolIFType** è un valore qualsiasi diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-249">This property should be set to **Null** when the **ProtocolIFType** property is any value other than 1.</span></span> <span data-ttu-id="e0ef1-250">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-250">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-251">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-251">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-252">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-254">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-254">Provides high level status information.</span></span> <span data-ttu-id="e0ef1-255">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-255">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="e0ef1-256">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-256">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="e0ef1-257">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-257">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-258">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-258">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-259">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-260">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-261">La proprietà viene utilizzata per suddividere in categorie e classificare le istanze di questa classe.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-261">The property is used to categorize and classify instances of this class.</span></span> <span data-ttu-id="e0ef1-262">Se **ProtocolIFType** è impostato su 1 (other), le informazioni sul tipo devono essere fornite nella proprietà **OtherTypeDescription** .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-262">If the **ProtocolIFType** is set to 1 (Other), then the type information should be provided in the **OtherTypeDescription** property.</span></span> <span data-ttu-id="e0ef1-263">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-263">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

> [!Note]  
> <span data-ttu-id="e0ef1-264">**ProtocolIFType** è un'enumerazione sincronizzata con [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-264">**ProtocolIFType** is an enumeration that is synchronized with the [IANA ifType MIB](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <span data-ttu-id="e0ef1-265">Sono inclusi anche valori aggiuntivi definiti da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-265">Additional values defined by the DMTF are also included.</span></span>

 

<dl> <dt>

<span data-ttu-id="e0ef1-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-266"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-267"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Normale 1822** (2)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-268"><span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>**Regular 1822** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-269"><span id="HDH_1822"></span><span id="hdh_1822"></span>**HDH 1822** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X. 25** (4)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-270"><span id="DDN_X.25"></span><span id="ddn_x.25"></span>**DDN X.25** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X. 25** (5)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-271"><span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>**RFC877 X.25** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**CSMA Ethernet/CD** (6)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-272"><span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>**Ethernet CSMA/CD** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802,3 CSMA/CD** (7)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-273"><span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>**ISO 802.3 CSMA/CD** (7)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**Bus token ISO 802,4** (8)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-274"><span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>**ISO 802.4 Token Bus** (8)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**Anello token ISO 802,5** (9)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-275"><span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>**ISO 802.5 Token Ring** (9)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802,6 uomo** (10)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-276"><span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>**ISO 802.6 MAN** (10)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-277"><span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>**StarLAN** (11)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-278"><span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>**Proteon 10Mbit** (12)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-279"><span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>**Proteon 80Mbit** (13)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**Ipercanale** (14)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-280"><span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>**HyperChannel** (14)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-281"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (15)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-282"><span id="LAP-B"></span><span id="lap-b"></span>**Lap-B** (16)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-282"><span id="LAP-B"></span><span id="lap-b"></span>**LAP-B** (16)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-283"><span id="SDLC"></span><span id="sdlc"></span>**SDLC** (17)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-284"><span id="DS1"></span><span id="ds1"></span>**DS1** (18)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-285"><span id="E1"></span><span id="e1"></span>**E1** (19)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**ISDN Basic** (20)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-286"><span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>**Basic ISDN** (20)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**ISDN primario** (21)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-287"><span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>**Primary ISDN** (21)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Seriale point-to-Point proprietario** (22)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-288"><span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>**Proprietary Point-to-Point Serial** (22)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-289"><span id="PPP"></span><span id="ppp"></span>**PPP** (23)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Loopback software** (24)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-290"><span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>**Software Loopback** (24)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-291"><span id="EON"></span><span id="eon"></span>**EON** (25)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-292"><span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>**Ethernet 3Mbit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-293"><span id="NSIP"></span><span id="nsip"></span>**NSIP** (27)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-294"><span id="SLIP"></span><span id="slip"></span>**Slip** (28)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-294"><span id="SLIP"></span><span id="slip"></span>**SLIP** (28)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-295"><span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>**Ultra** (29)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-296"><span id="DS3"></span><span id="ds3"></span>**DS3** (30)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-297"><span id="SIP"></span><span id="sip"></span>**SIP** (31)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Inoltro frame** (32)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-298"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (32)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-299"><span id="RS-232"></span><span id="rs-232"></span>**RS-232** (33)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallelo** (34)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-300"><span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>**Parallel** (34)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-301"><span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>**ARCNet** (35)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-302"><span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>**ARCNet Plus** (36)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-303"><span id="ATM"></span><span id="atm"></span>**ATM** (37)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**Mio X. 25** (38)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-304"><span id="MIO_X.25"></span><span id="mio_x.25"></span>**MIO X.25** (38)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-305"><span id="SONET"></span><span id="sonet"></span>**SONET** (39)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X. 25 PLE** (40)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-306"><span id="X.25_PLE"></span><span id="x.25_ple"></span>**X.25 PLE** (40)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**802.211 ISO c** (41)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-307"><span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>**ISO 802.211c** (41)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-308"><span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>**LocalTalk** (42)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-309"><span id="SMDS_DXI"></span><span id="smds_dxi"></span>**SMDS DXI** (43)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Servizio frame relay** (44)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-310"><span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>**Frame Relay Service** (44)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-311"><span id="V.35"></span><span id="v.35"></span>**V. 35** (45)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-311"><span id="V.35"></span><span id="v.35"></span>**V.35** (45)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-312"><span id="HSSI"></span><span id="hssi"></span>**HSSI** (46)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-313"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (47)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-314"><span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>**Modem** (48)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-315"><span id="AAL5"></span><span id="aal5"></span>**AAL5** (49)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**Percorso SONET** (50)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-316"><span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>**SONET Path** (50)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**VT SONET** (51)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-317"><span id="SONET_VT"></span><span id="sonet_vt"></span>**SONET VT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-318"><span id="SMDS_ICIP"></span><span id="smds_icip"></span>**SMDS ICIP** (52)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietario virtuale/interno** (53)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-319"><span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>**Proprietary Virtual/Internal** (53)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Multiplexer proprietario** (54)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-320"><span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>**Proprietary Multiplexor** (54)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802,12** (55)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-321"><span id="IEEE_802.12"></span><span id="ieee_802.12"></span>**IEEE 802.12** (55)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-322"><span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>**Fibre Channel** (56)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**Interfaccia HIPPI** (57)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-323"><span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>**HIPPI Interface** (57)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Interconnessione frame relay** (58)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-324"><span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>**Frame Relay Interconnect** (58)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**LAN emulata ATM per 802,3** (59)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-325"><span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>**ATM Emulated LAN for 802.3** (59)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**LAN emulata ATM per 802,5** (60)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-326"><span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>**ATM Emulated LAN for 802.5** (60)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**Circuito emulato ATM** (61)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-327"><span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>**ATM Emulated Circuit** (61)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Ethernet veloce (100BaseT)** (62)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-328"><span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>**Fast Ethernet (100BaseT)** (62)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-329"><span id="ISDN"></span><span id="isdn"></span>**ISDN** (63)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-330"><span id="V.11"></span><span id="v.11"></span>**V. 11** (64)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-330"><span id="V.11"></span><span id="v.11"></span>**V.11** (64)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-331"><span id="V.36"></span><span id="v.36"></span>**V. 36** (65)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-331"><span id="V.36"></span><span id="v.36"></span>**V.36** (65)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 a 64K** (66)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-332"><span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>**G703 at 64K** (66)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 a 2MB** (67)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-333"><span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>**G703 at 2Mb** (67)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-334"><span id="QLLC"></span><span id="qllc"></span>**QLLC** (68)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-335"><span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>**Fast Ethernet 100BaseFX** (69)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Canale** (70)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-336"><span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>**Channel** (70)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-337"><span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**Canale OEMI IBM 260/370** (72)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-338"><span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>**IBM 260/370 OEMI Channel** (72)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-339"><span id="ESCON"></span><span id="escon"></span>**ESCON** (73)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Cambio collegamento dati** (74)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-340"><span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>**Data Link Switching** (74)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**Interfaccia S/T ISDN** (75)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-341"><span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>**ISDN S/T Interface** (75)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**Interfaccia ISDN U** (76)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-342"><span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>**ISDN U Interface** (76)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-343"><span id="LAP-D"></span><span id="lap-d"></span>**Lap-D** (77)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-343"><span id="LAP-D"></span><span id="lap-d"></span>**LAP-D** (77)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**Opzione IP** (78)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-344"><span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>**IP Switch** (78)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Bridging Route origine remota** (79)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-345"><span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>**Remote Source Route Bridging** (79)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**Logica ATM** (80)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-346"><span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>**ATM Logical** (80)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-347"><span id="DS0"></span><span id="ds0"></span>**DS0** (81)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**Bundle DS0** (82)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-348"><span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>**DS0 Bundle** (82)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-349"><span id="BSC"></span><span id="bsc"></span>**BSC** (83)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-350"><span id="Async"></span><span id="async"></span><span id="ASYNC"></span>**Async** (84)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat net radio** (85)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-351"><span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>**Combat Net Radio** (85)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**802.5 ISO r DTR** (86)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-352"><span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>**ISO 802.5r DTR** (86)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Sistema di segnalazione EXT POS loc** (87)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-353"><span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>**Ext Pos Loc Report System** (87)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**Protocollo di accesso remoto AppleTalk** (88)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-354"><span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>**AppleTalk Remote Access Protocol** (88)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>Senza **connessione proprietaria** (89)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-355"><span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>**Proprietary Connectionless** (89)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**Pad host ITU X. 29** (90)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-356"><span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>**ITU X.29 Host PAD** (90)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**Pad terminale ITU X. 3** (91)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-357"><span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>**ITU X.3 Terminal PAD** (91)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**MPI frame relay** (92)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-358"><span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>**Frame Relay MPI** (92)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X. 213** (93)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-359"><span id="ITU_X.213"></span><span id="itu_x.213"></span>**ITU X.213** (93)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-360"><span id="ADSL"></span><span id="adsl"></span>**ADSL** (94)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-361"><span id="RADSL"></span><span id="radsl"></span>**RADSL** (95)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-362"><span id="SDSL"></span><span id="sdsl"></span>**SDSL** (96)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-363"><span id="VDSL"></span><span id="vdsl"></span>**VDSL** (97)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802,5 CRFP** (98)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-364"><span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>**ISO 802.5 CRFP** (98)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-365"><span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>**Myrinet** (99)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Ricezione e trasmissione vocale** (100)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-366"><span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>**Voice Receive and Transmit** (100)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>Segreteria esterna per la **voce di Exchange** (101)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-367"><span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>**Voice Foreign Exchange Office** (101)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Servizio scambio vocale** (102)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-368"><span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>**Voice Foreign Exchange Service** (102)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Incapsulamento vocale** (103)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-369"><span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>**Voice Encapsulation** (103)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-370"><span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>**Voice over IP** (104)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**DXi ATM** (105)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-371"><span id="ATM_DXI"></span><span id="atm_dxi"></span>**ATM DXI** (105)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**Funi ATM** (106)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-372"><span id="ATM_FUNI"></span><span id="atm_funi"></span>**ATM FUNI** (106)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-373"><span id="ATM_IMA"></span><span id="atm_ima"></span>**ATM IMA** (107)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**Bundle Multilink PPP** (108)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-374"><span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>**PPP Multilink Bundle** (108)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP su CDLC** (109)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-375"><span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>**IP over CDLC** (109)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over Claw** (110)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-376"><span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>**IP over CLAW** (110)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack da** stack (111)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-377"><span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>**Stack to Stack** (111)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Indirizzo IP virtuale** (112)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-378"><span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>**Virtual IP Address** (112)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-379"><span id="MPC"></span><span id="mpc"></span>**MPC** (113)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP su ATM** (114)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-380"><span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>**IP over ATM** (114)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**Anello di token fibre ISO 802.5 j** (115)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-381"><span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>**ISO 802.5j Fibre Token Ring** (115)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-382"><span id="TDLC"></span><span id="tdlc"></span>**TDLC** (116)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Ethernet Gigabit** (117)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-383"><span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>**Gigabit Ethernet** (117)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-384"><span id="HDLC"></span><span id="hdlc"></span>**HDLC** (118)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-385"><span id="LAP-F"></span><span id="lap-f"></span>**Lap-F** (119)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-385"><span id="LAP-F"></span><span id="lap-f"></span>**LAP-F** (119)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-386"><span id="V.37"></span><span id="v.37"></span>**V. 37** (120)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-386"><span id="V.37"></span><span id="v.37"></span>**V.37** (120)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X. 25 MLP** (121)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-387"><span id="X.25_MLP"></span><span id="x.25_mlp"></span>**X.25 MLP** (121)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**Gruppo di caccia X. 25** (122)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-388"><span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>**X.25 Hunt Group** (122)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-389"><span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>**Transp HDLC** (123)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Canale interleave** (124)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-390"><span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>**Interleave Channel** (124)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**Canale rapido** (125)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-391"><span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>**FAST Channel** (125)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (per APPN HPR in reti IP)** (126)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-392"><span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>**IP (for APPN HPR in IP Networks)** (126)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**Livello Mac CATV** (127)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-393"><span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>**CATV MAC Layer** (127)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV downstream** (128)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-394"><span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>**CATV Downstream** (128)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV upstream** (129)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-395"><span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>**CATV Upstream** (129)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Switch Avalon 12MPP** (130)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-396"><span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>**Avalon 12MPP Switch** (130)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-397"><span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>**Tunnel** (131)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Caffè** (132)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-398"><span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>**Coffee** (132)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Servizio di emulazione del circuito** (133)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-399"><span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>**Circuit Emulation Service** (133)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**Sottointerfaccia ATM** (134)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-400"><span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>**ATM SubInterface** (134)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**VLAN di livello 2 con 802.1 q** (135)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-401"><span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>**Layer 2 VLAN using 802.1Q** (135)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**VLAN di livello 3 con IP** (136)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-402"><span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>**Layer 3 VLAN using IP** (136)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**VLAN di livello 3 con IPX** (137)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-403"><span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>**Layer 3 VLAN using IPX** (137)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Linea di alimentazione digitale** (138)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-404"><span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>**Digital Power Line** (138)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Posta elettronica multimediale su IP** (139)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-405"><span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>**Multimedia Mail over IP** (139)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-406"><span id="DTM"></span><span id="dtm"></span>**DTM** (140)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-407"><span id="DCN"></span><span id="dcn"></span>**DCN** (141)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**Inoltri IP** (142)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-408"><span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>**IP Forwarding** (142)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-409"><span id="MSDSL"></span><span id="msdsl"></span>**MSDSL** (143)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-410"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (144)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**If-GSN/HIPPI-6400** (145)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-411"><span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>**IF-GSN/HIPPI-6400** (145)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**Livello Mac DVB-RCC** (146)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-412"><span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>**DVB-RCC MAC Layer** (146)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC downstream** (147)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-413"><span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>**DVB-RCC Downstream** (147)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC upstream** (148)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-414"><span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>**DVB-RCC Upstream** (148)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM virtuale** (149)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-415"><span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>**ATM Virtual** (149)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**Tunnel MPLS** (150)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-416"><span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>**MPLS Tunnel** (150)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-417"><span id="SRP"></span><span id="srp"></span>**SRP** (151)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-418"><span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>**Voice over ATM** (152)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Inoltro del frame Voice over** (153)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-419"><span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>**Voice over Frame Relay** (153)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-420"><span id="ISDL"></span><span id="isdl"></span>**ISDL** (154)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Collegamento composito** (155)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-421"><span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>**Composite Link** (155)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**Collegamento di segnalazione SS7** (156)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-422"><span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>**SS7 Signaling Link** (156)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Wireless P2P proprietario** (157)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-423"><span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>**Proprietary P2P Wireless** (157)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame in** poi (158)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-424"><span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>**Frame Forward** (158)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol su ATM** (159)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-425"><span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>**RFC1483 Multiprotocol over ATM** (159)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-426"><span id="USB"></span><span id="usb"></span>**USB** (160)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**Aggregazione collegamento ad IEEE 802.3** (161)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-427"><span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>**IEEE 802.3ad Link Aggregate** (161)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**Contabilità dei criteri BGP** (162)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-428"><span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>**BGP Policy Accounting** (162)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink fr** (163)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-429"><span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>**FRF .16 Multilink FR** (163)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**Gatekeeper H. 323** (164)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-430"><span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>**H.323 Gatekeeper** (164)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**Proxy H. 323** (165)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-431"><span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>**H.323 Proxy** (165)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-432"><span id="MPLS"></span><span id="mpls"></span>**MPLS** (166)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Collegamento** per la segnalazione a più frequenze (167)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-433"><span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>**Multi-Frequency Signaling Link** (167)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-434"><span id="HDSL-2"></span><span id="hdsl-2"></span>**HDSL-2** (168)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-435"><span id="S-HDSL"></span><span id="s-hdsl"></span>**S-HDSL** (169)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**Collegamento dati della struttura DS1** (170)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-436"><span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>**DS1 Facility Data Link** (170)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-437"><span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>**Packet over SONET/SDH** (171)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**Input DVB-ASI** (172)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-438"><span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>**DVB-ASI Input** (172)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**Output DVB-ASI** (173)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-439"><span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>**DVB-ASI Output** (173)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Linea di alimentazione** (174)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-440"><span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>**Power Line** (174)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Segnalazione non associata alla struttura** (175)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-441"><span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>**Non Facility Associated Signaling** (175)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-442"><span id="TR008"></span><span id="tr008"></span>**TR008** (176)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-443"><span id="GR303_RDT"></span><span id="gr303_rdt"></span>**GR303 RDT** (177)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-444"><span id="GR303_IDT"></span><span id="gr303_idt"></span>**GR303 IDT** (178)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-445"><span id="ISUP"></span><span id="isup"></span>**IsUp** (179)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-445"><span id="ISUP"></span><span id="isup"></span>**ISUP** (179)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Livello MAC wireless proprietario** (180)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-446"><span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>**Proprietary Wireless MAC Layer** (180)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Wireless proprietario a valle** (181)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-447"><span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>**Proprietary Wireless Downstream** (181)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Upstream senza fili proprietario** (182)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-448"><span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>**Proprietary Wireless Upstream** (182)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**Hiperlan tipo 2** (183)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-449"><span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>**HIPERLAN Type 2** (183)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Punto di accesso wireless a banda larga proprietario per MultiPoint** (184)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-450"><span id="Proprietary_Broadband_Wireless_Access_Point_to_Multipoint"></span><span id="proprietary_broadband_wireless_access_point_to_multipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULTIPOINT"></span>**Proprietary Broadband Wireless Access Point to Multipoint** (184)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**Canale overhead SONET** (185)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-451"><span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>**SONET Overhead Channel** (185)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Canale overhead del wrapper digitale** (186)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-452"><span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>**Digital Wrapper Overhead Channel** (186)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**Livello 2 di adattamento ATM** (187)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-453"><span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>**ATM Adaptation Layer 2** (187)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Mac Radio** (188)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-454"><span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>**Radio MAC** (188)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**Radio ATM** (189)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-455"><span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>**ATM Radio** (189)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Trunk tra computer** (190)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-456"><span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>**Inter Machine Trunk** (190)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**DSL MVL** (191)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-457"><span id="MVL_DSL"></span><span id="mvl_dsl"></span>**MVL DSL** (191)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**DSL lungo lettura** (192)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-458"><span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>**Long Read DSL** (192)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Endpoint DLCI frame relay** (193)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-459"><span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>**Frame Relay DLCI Endpoint** (193)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**Endpoint VCI ATM** (194)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-460"><span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>**ATM VCI Endpoint** (194)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Canale ottico** (195)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-461"><span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>**Optical Channel** (195)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Trasporto ottico** (196)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-462"><span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>**Optical Transport** (196)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**ATM proprietario** (197)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-463"><span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>**Proprietary ATM** (197)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Cavo Voice over** (198)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-464"><span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>**Voice over Cable** (198)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**InfiniBand** (199)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-465"><span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>**Infiniband** (199)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**Collegamento te** (200)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-466"><span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>**TE Link** (200)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-467"><span id="Q.2931"></span><span id="q.2931"></span>**D. 2931** (201)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-467"><span id="Q.2931"></span><span id="q.2931"></span>**Q.2931** (201)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Gruppo Trunk virtuale** (202)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-468"><span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>**Virtual Trunk Group** (202)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**Gruppo Trunk SIP** (203)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-469"><span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>**SIP Trunk Group** (203)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**Segnalazione SIP** (204)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-470"><span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>**SIP Signaling** (204)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**Canale upstream CATV** (205)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-471"><span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>**CATV Upstream Channel** (205)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**ECONT** (206)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-472"><span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>**Econet** (206)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155MB pon** (207)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-473"><span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>**FSAN 155Mb PON** (207)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622MB pon** (208)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-474"><span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>**FSAN 622Mb PON** (208)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Bridge trasparente** (209)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-475"><span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>**Transparent Bridge** (209)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Gruppo di righe** (210)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-476"><span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>**Line Group** (210)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Gruppo di funzionalità Voice &** (211)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-477"><span id="Voice___Feature_Group"></span><span id="voice___feature_group"></span><span id="VOICE___FEATURE_GROUP"></span>**Voice & Feature Group** (211)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-478"><span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>**Voice FGD EANA** (212)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voce did** (213)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-479"><span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>**Voice DID** (213)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**Trasporto MPEG** (214)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-480"><span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>**MPEG Transport** (214)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6to4** (215)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-481"><span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>**6To4** (215)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-482"><span id="GTP"></span><span id="gtp"></span>**GTP** (216)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-483"><span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>**Paradyne EtherLoop 1** (217)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-484"><span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>**Paradyne EtherLoop 2** (218)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Gruppo canale ottico** (219)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-485"><span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>**Optical Channel Group** (219)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-486"><span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>**HomePNA** (220)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-487"><span id="GFP"></span><span id="gfp"></span>**GFP** (221)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-488"><span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>**ciscoISLvlan** (222)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-489"><span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>**actelisMetaLOOP** (223)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**FCIP** (224)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-490"><span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>**Fcip** (224)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA riservato** (225.. 4095)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-491"><span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA Reserved** (225..4095)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-492"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-493"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-494"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-495"><span id="IPX"></span><span id="ipx"></span>**IPX** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-496"><span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>**DECnet** (4100)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-497"><span id="SNA"></span><span id="sna"></span>**SNA** (4101)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-498"><span id="CONP"></span><span id="conp"></span>**CONP** (4102)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-499"><span id="CLNP"></span><span id="clnp"></span>**CLNP** (4103)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-500"><span id="VINES"></span><span id="vines"></span>**Viti** (4104)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-500"><span id="VINES"></span><span id="vines"></span>**VINES** (4104)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-501"><span id="XNS"></span><span id="xns"></span>**XNS** (4105)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**Endpoint del canale ISDN B** (4106)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-502"><span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>**ISDN B Channel Endpoint** (4106)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**Endpoint canale ISDN D** (4107)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-503"><span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>**ISDN D Channel Endpoint** (4107)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-504"><span id="BGP"></span><span id="bgp"></span>**BGP** (4108)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-505"><span id="OSPF"></span><span id="ospf"></span>**OSPF** (4109)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-506"><span id="UDP"></span><span id="udp"></span>**UDP** (4110)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-507"><span id="TCP"></span><span id="tcp"></span>**TCP** (4111)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11 a** (4112)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-508"><span id="802.11a"></span><span id="802.11A"></span>**802.11a** (4112)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11 b** (4113)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-509"><span id="802.11b"></span><span id="802.11B"></span>**802.11b** (4113)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11 g** (4114)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-510"><span id="802.11g"></span><span id="802.11G"></span>**802.11g** (4114)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11 h** (4115)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-511"><span id="802.11h"></span><span id="802.11H"></span>**802.11h** (4115)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-512"><span id="NFS"></span><span id="nfs"></span>**NFS** (4200)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-513"><span id="CIFS"></span><span id="cifs"></span>**CIFS** (4201)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-514"><span id="DAFS"></span><span id="dafs"></span>**DAFS** (4202)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-515"><span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>**WebDAV** (4203)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-516"><span id="HTTP"></span><span id="http"></span>**Http** (4204)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-516"><span id="HTTP"></span><span id="http"></span>**HTTP** (4204)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-517"><span id="FTP"></span><span id="ftp"></span>**FTP** (4205)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-518"><span id="NDMP"></span><span id="ndmp"></span>**NDMP** (4300)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-519"><span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>**Telnet** (4400)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-520"><span id="SSH"></span><span id="ssh"></span>**SSH** (4401)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**CLP SM** (4402)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-521"><span id="SM_CLP"></span><span id="sm_clp"></span>**SM CLP** (4402)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-522"><span id="SMTP"></span><span id="smtp"></span>**SMTP** (4403)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-523"><span id="LDAP"></span><span id="ldap"></span>**LDAP** (4404)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-524"><span id="RDP"></span><span id="rdp"></span>**RDP** (4405)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-525"><span id="HTTPS"></span><span id="https"></span>**Https** (4406)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-525"><span id="HTTPS"></span><span id="https"></span>**HTTPS** (4406)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-526"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768..</span><span class="sxs-lookup"><span data-stu-id="e0ef1-527"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768..</span></span> <span data-ttu-id="e0ef1-528">)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-528">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e0ef1-529">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-529">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-530">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-530">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-531">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-531">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-532">Questa proprietà è deprecata al posto della proprietà **ProtocolIFType** .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-532">This property is deprecated in lieu of the **ProtocolIFType** property.</span></span> <span data-ttu-id="e0ef1-533">Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-533">This property is inherited from [**CIM\_ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-534">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-534">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-535">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-535">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-536">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-537">Ultimo stato richiesto o desiderato per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-537">The last requested or desired state for the management service.</span></span> <span data-ttu-id="e0ef1-538">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-538">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="e0ef1-539">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ef1-539">Value</span></span>                                                                         | <span data-ttu-id="e0ef1-540">Significato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-540">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="e0ef1-541"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-541"><dt>12</dt></span></span> </dl> | <span data-ttu-id="e0ef1-542">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-542">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0ef1-543">**Status**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-543">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-544">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-545">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-545">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-546">Descrive lo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-546">Describes the status of the element.</span></span> <span data-ttu-id="e0ef1-547">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-547">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="e0ef1-548">OK</span><span class="sxs-lookup"><span data-stu-id="e0ef1-548">"OK"</span></span>

<span data-ttu-id="e0ef1-549">Errore</span><span class="sxs-lookup"><span data-stu-id="e0ef1-549">"Error"</span></span>

<span data-ttu-id="e0ef1-550">Degradato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-550">"Degraded"</span></span>

<span data-ttu-id="e0ef1-551">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="e0ef1-551">"Unknown"</span></span>

<span data-ttu-id="e0ef1-552">"Errore di predazione"</span><span class="sxs-lookup"><span data-stu-id="e0ef1-552">"Pred Fail"</span></span>

<span data-ttu-id="e0ef1-553">Avvio</span><span class="sxs-lookup"><span data-stu-id="e0ef1-553">"Starting"</span></span>

<span data-ttu-id="e0ef1-554">Arresto</span><span class="sxs-lookup"><span data-stu-id="e0ef1-554">"Stopping"</span></span>

<span data-ttu-id="e0ef1-555">Servizio</span><span class="sxs-lookup"><span data-stu-id="e0ef1-555">"Service"</span></span>

<span data-ttu-id="e0ef1-556">Sottolineato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-556">"Stressed"</span></span>

<span data-ttu-id="e0ef1-557">"Non ripristino"</span><span class="sxs-lookup"><span data-stu-id="e0ef1-557">"NonRecover"</span></span>

<span data-ttu-id="e0ef1-558">"Nessun contatto"</span><span class="sxs-lookup"><span data-stu-id="e0ef1-558">"No Contact"</span></span>

<span data-ttu-id="e0ef1-559">"Lost comm"</span><span class="sxs-lookup"><span data-stu-id="e0ef1-559">"Lost Comm"</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-560">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-560">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-561">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-561">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-562">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-562">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-563">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="e0ef1-563">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="e0ef1-564">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-564">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-565">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-565">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-566">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-567">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-568">Nome della classe di creazione del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-568">The hosting system's creation class name.</span></span> <span data-ttu-id="e0ef1-569">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-569">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-570">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-570">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-571">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-572">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-573">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="e0ef1-573">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-574">Nome del sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-574">The name of the hosting system.</span></span> <span data-ttu-id="e0ef1-575">Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span><span class="sxs-lookup"><span data-stu-id="e0ef1-575">This property is inherited from [**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-576">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-576">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-577">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-577">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-578">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-578">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-579">Data e ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-579">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="e0ef1-580">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-580">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-581">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-581">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-582">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-582">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-583">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-583">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-584">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-584">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="e0ef1-585">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-585">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-586">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-586">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-587">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-588">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-588">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-589">Nome del nodo universale della porta Fibre Channel a cui è connesso questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-589">The world wide node name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> <dt>

<span data-ttu-id="e0ef1-590">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-590">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0ef1-591">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e0ef1-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0ef1-592">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e0ef1-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0ef1-593">Nome della porta universale della porta Fibre Channel a cui è connesso questo endpoint.</span><span class="sxs-lookup"><span data-stu-id="e0ef1-593">The world wide port name of the Fibre Channel port this endpoint is connected to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0ef1-594">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0ef1-594">Requirements</span></span>



| <span data-ttu-id="e0ef1-595">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0ef1-595">Requirement</span></span> | <span data-ttu-id="e0ef1-596">Valore</span><span class="sxs-lookup"><span data-stu-id="e0ef1-596">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ef1-597">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-597">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ef1-598">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e0ef1-598">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e0ef1-599">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0ef1-599">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ef1-600">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e0ef1-600">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0ef1-601">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0ef1-601">Namespace</span></span><br/>                | <span data-ttu-id="e0ef1-602">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0ef1-602">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e0ef1-603">MOF</span><span class="sxs-lookup"><span data-stu-id="e0ef1-603">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0ef1-604"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-604"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0ef1-605">DLL</span><span class="sxs-lookup"><span data-stu-id="e0ef1-605">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0ef1-606"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0ef1-606"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

