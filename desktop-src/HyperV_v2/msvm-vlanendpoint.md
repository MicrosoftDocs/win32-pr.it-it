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
# <a name="msvm_vlanendpoint-class"></a>\_Classe MSVM VLANEndpoint

Rappresenta l'endpoint VLAN di una porta di commutazione. La configurazione di questo endpoint cambierà il modo in cui la porta del commutatore invia i pacchetti VLAN tramite il commutatore.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

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

## <a name="members"></a>Members

La **classe \_ VLANEndpoint di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ VLANEndpoint di MSVM** dispone di questi metodi.



| Metodo                                                             | Descrizione                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-vlanendpoint-requeststatechange.md) | Richiede una modifica dello stato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ VLANEndpoint di MSVM** dispone di queste proprietà.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente del [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)). Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (.. )
</dt> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "VLAN endpoint".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)ed è sempre impostata su "MSVM \_ VLANEndpoint".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Microsoft VLAN endpoint".

</dd> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola scrittura
</dt> </dl>

La modalità VLAN desiderata richiesta per l'utilizzo. La modalità corrente viene fornita dalla proprietà **OperationalEndpointMode** . Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).



| Valore                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Accesso**</dt> <dt>2</dt> </dl>                                                   | Inserisce la porta di commutazione/endpoint in modalità non di trunking permanente e negozia per convertire il collegamento in un collegamento non trunk. L'endpoint diventa un'interfaccia non trunk.<br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Auto dinamica**</dt> <dt>3</dt> </dl>                           | Rende l'endpoint in grado di convertire il collegamento in un collegamento di trunk. L'endpoint diventa un'interfaccia trunk se l'interfaccia adiacente è impostata su trunk o sulla modalità desiderata.<br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Auspicabile dinamico**</dt> <dt>4</dt> </dl>       | Fa in modo che l'endpoint tenti attivamente di convertire il collegamento a un collegamento di trunk. L'endpoint diventa un'interfaccia trunk se l'interfaccia vicina è impostata su trunk, auspicabile o modalità auto. La modalità switch-Port predefinita per tutte le interfacce Ethernet è auspicabile dinamica.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Trunk**</dt> <dt>5</dt> </dl>                                                       | Inserisce l'endpoint in modalità di trunking permanente e negozia per convertire il collegamento in un collegamento di trunk. L'endpoint diventa un'interfaccia trunk anche se l'interfaccia adiacente non è un'interfaccia trunk.<br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q tunnel**</dt> <dt>6</dt> </dl>                           | Configura l'interfaccia come endpoint/porta del tunnel (non di trunking) per essere connessa in un collegamento asimmetrico con una porta trunk 802.1 Q. il tunneling 802.1 q viene usato per mantenere l'integrità VLAN del cliente attraverso una rete del provider di servizi.<br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornitore riservato**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di incapsulamento VLAN richiesto per l'utilizzo. L'incapsulamento attualmente in uso viene fornito dalla proprietà **OperationalVLANTrunkEncapsulation** . Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** . Questa proprietà è 2 (non applicabile) (ovvero, l'endpoint non verrà mai inserito in modalità trunk), un tipo particolare (802.1 Q o Cisco ISL) o 5 (Negotiate) (ovvero il risultato della negoziazione tra questa interfaccia e il relativo adiacente). Il valore 5 (Negotiate) non è consentito se l'endpoint non supporta la negoziazione. Questa funzionalità è dipendente dall'hardware e dal fornitore. Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negoziazione** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768 65535)
</dt> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) ed è sempre impostata su 2 (Enabled).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di questo elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (non applicabile).

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il protocollo di registrazione VLAN GARP (GVRP) è abilitato o disabilitato nell'endpoint/porta del trunk. Questa proprietà è 2 (non applicabile), a meno che GVRP non sia supportato dall'endpoint. Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** . Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (3)
</dt> <dt>

<span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Disabilitato** (4)
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questa proprietà esprime l'integrità di questo elemento ma non necessariamente dei relativi sottocomponenti. I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e non viene utilizzata.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Euristica di denominazione selezionata per garantire che il valore della proprietà **Name** sia univoco. Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e non viene utilizzata.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** . Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità di configurazione per l'endpoint VLAN. Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).



| Valore                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                                       | L'endpoint non è compatibile con le VLAN.<br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Accesso**</dt> <dt>2</dt> </dl>                                                   | Inserisce l'endpoint in modalità non di trunking permanente e negozia per convertire il collegamento in un collegamento non trunk. L'endpoint diventa un'interfaccia non trunk.<br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Auto dinamica**</dt> <dt>3</dt> </dl>                           | Rende l'endpoint in grado di convertire il collegamento in un collegamento di trunk. L'endpoint diventa un'interfaccia trunk se l'interfaccia adiacente è impostata su trunk o sulla modalità desiderata.<br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Auspicabile dinamico**</dt> <dt>4</dt> </dl>       | Fa in modo che l'endpoint tenti attivamente di convertire il collegamento a un collegamento di trunk. L'endpoint diventa un'interfaccia trunk se l'interfaccia vicina è impostata su trunk, auspicabile o modalità auto. Questa è la modalità predefinita per le porte switch per tutte le interfacce Ethernet.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Trunk**</dt> <dt>5</dt> </dl>                                                       | Inserisce l'endpoint in modalità di trunking permanente e negozia per convertire il collegamento in un collegamento di trunk. L'endpoint diventa un'interfaccia trunk anche se l'interfaccia adiacente non è un'interfaccia trunk.<br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q tunnel**</dt> <dt>6</dt> </dl>                           | Configura l'interfaccia come endpoint/porta del tunnel (non di trunking) per essere connessa in un collegamento asimmetrico con una porta trunk 802.1 Q. il tunneling 802.1 q viene usato per mantenere l'integrità VLAN del cliente attraverso una rete del provider di servizi.<br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Fornitore riservato**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di incapsulamento VLAN in uso su un endpoint/porta trunk. Questa proprietà è 2 (non applicabile) (ovvero l'endpoint non funziona in modalità di trunk), un tipo particolare (3-802.1 Q o 4-Cisco ISL), 5 (Negotiate) (ovvero gli endpoint stanno negoziando il tipo di incapsulamento). Questa proprietà è applicabile solo quando l'endpoint opera in modalità di trunking. per ulteriori informazioni, vedere la proprietà **OperationalEndpointMode** . Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1 q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negoziazione** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (32768 65535)
</dt> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro"). Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di modello di endpoint VLAN supportato da questo endpoint VLAN, quando il valore della proprietà **OperationalEndpointMode** è impostato su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà **OperationalEndpointMode** è un valore qualsiasi diverso da 1. Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di incapsulamento VLAN supportato da questo endpoint VLAN, quando il valore della proprietà **OperationalVLANTrunkEncapsulation** è impostato su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà di incapsulamento desiderata è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint).

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di endpoint del protocollo quando la proprietà **Type** di questa classe (o una delle relative sottoclassi) è impostata su 1 (other). Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)ed è sempre impostata su "Virtual Ethernet".

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

[IANA IFTYPE MIB](https://www.iana.org/assignments/ianaiftype-mib). Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)ed è sempre impostata su 1 (other).

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) e non viene utilizzata.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per il servizio di gestione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).



| Valore                                                                         | Significato                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Non applicabile.<br/> |



 

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive lo stato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

OK

Errore

Degradato

Sconosciuto

"Errore di predazione"

Avvio

Arresto

Servizio

Sottolineato

"Non ripristino"

"Nessun contatto"

"Lost comm"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".

</dd> <dt>

**SupportedEndpointModes**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Modalità dell'endpoint supportate da questa porta.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)ed è sempre impostata su "MSVM \_ VirtualSwitch"

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome di sistema del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non è supportata.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ VLANEndpoint di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VLANENDPOINT CIM**](cim-vlanendpoint.md)
</dt> <dt>

[**\_VLANENDPOINT CIM**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

