---
description: Rappresenta il punto di connessione logico per una scheda di rete. Quando l'endpoint Wi-Fi è connesso a una porta del commutatore, la scheda di rete connessa all'endpoint Wi-Fi ha connettività di rete.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c87667a8a16ff6b8e038c84d51b7229ce53c3397dca8ef8bb4708275512593ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146170"
---
# <a name="msvm_wifiendpoint-class"></a>Classe \_ Msvm WiFiEndpoint

Rappresenta il punto di connessione logico per una scheda di rete. Quando l'endpoint Wi-Fi è connesso a una porta del commutatore, la scheda di rete connessa all'endpoint Wi-Fi ha connettività di rete.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
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
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ WiFiEndpoint** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ WiFiEndpoint** dispone di questi metodi.



| Metodo                 | Descrizione                              |
|:-----------------------|:-----------------------------------------|
| **RequestStateChange** | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ WiFiEndpoint** ha queste proprietà.

<dl> <dt>

**AccessPointAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene l'indirizzo MAC del punto di accesso a cui l'endpoint Wi-Fi è attualmente associato. Se lWi-Fi endpoint non è attualmente associato, **AccessPointAddress** deve essere **Null.** L'indirizzo MAC deve essere formattato come dodici cifre esadecimali (ad esempio, "010203040506"), con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico (ad esempio, il bit dell'indirizzo del gruppo si trova nel bit di ordine basso del primo carattere della stringa).

</dd> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Altri indirizzi unicast che possono essere usati per comunicare con l'endpoint LAN. Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**Associazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'endpoint Wi-Fi è attualmente associato a un punto di accesso o a una stazione client.

Contiene **True se** l'endpoint Wi-Fi è associato a un punto di accesso o a una stazione client; in caso contrario, **False**.

</dd> <dt>

**AuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il metodo usato per autenticare l'endpoint Wi-Fi e la rete tra loro.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Open System** (2)
</dt> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Chiave condivisa** (3)
</dt> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)
</dt> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1x** (5)
</dt> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**WPA2 PSK** (6)
</dt> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**WPA2 IEEE 802.1x** (7)
</dt> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1x** (8)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (9.. )
</dt> </dl>

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il *parametro RequestedState* del [**metodo RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica dello stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente di [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85)) Questa proprietà può essere non **Null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **Null se** un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

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

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvio** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Inattiva** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DmTF riservato** (.. )
</dt> </dl>

</dd> <dt>

**BSSType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il tipo di set di servizi di base (BSS) della rete che corrisponde all'istanza di . Un set di servizi di base è un set di stazioni controllate da una singola funzione di coordinamento.



| Valore                                                                                                                                                                                                                                                      | Significato                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <dt>**Indipendente**</dt> <dt>2</dt> </dl>                | LWi-Fi endpoint è associato direttamente a un'altra stazione client.<br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <dt>**Infrastruttura**</dt> <dt>3</dt> </dl>    | LWi-Fi endpoint è associato a una rete usando un punto di accesso.<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **DMTF riservato**</dt> <dt>4..</dt> </dl> |                                                                                    |



 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la possibilità della strumentazione di comunicare con l'elemento gestito sottostante. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Connessione effettuata**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà è impostata su **True** se l'endpoint Wi-Fi è connesso a una porta del commutatore.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza. Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integra la **proprietà PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) e sarà uno dei valori seguenti.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Abilitato ma offline** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica lo stato abilitato del sistema pianificato. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e può essere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | Il sistema è spento.<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>5</dt> </dl>                     | L'elemento non supporta l'a abilitato o disabilitato.<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | Il sistema è abilitato, ma offline. Tutte le nuove richieste verranno eliminate.<br/> |



 

</dd> <dt>

**Encryptionmethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il metodo di crittografia in uso per proteggere la riservatezza dei dati inviati e ricevuti dal Wi-Fi endpoint.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="WEP"></span><span id="wep"></span>**WEP** (2)
</dt> <dt>

<span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)
</dt> <dt>

<span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)
</dt> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (5)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (6.. )
</dt> </dl>

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzi multicast a cui l'endpoint LAN è in ascolto. Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Questa proprietà esprime l'integrità di questo elemento, ma non necessariamente quella dei relativi sottocomponenti. I valori possibili sono da 0 a 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionante. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**IEEE8021xAuthenticationProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene il tipo EAP (Extensible Authentication Protocol) se e solo se **AuthenticationMethod** contiene 5 (WPA IEEE 802.1x), 7 (WPA2 IEEE 802.1x) o 8 (CCKM IEEE 802.1x).

<dl> <dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)
</dt> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)
</dt> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)
</dt> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)
</dt> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)
</dt> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)
</dt> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)
</dt> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)
</dt> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)
</dt> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)
</dt> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF riservato** (11.. )
</dt> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta o identificatore per il segmento LAN a cui è connesso l'endpoint. Se l'endpoint non è attualmente attivo/connesso o queste informazioni non sono note, questa proprietà sarà **Null.** Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà è deprecata al posto della **proprietà ProtocolType.** Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**Macaddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 12 )
</dt> </dl>

Indirizzo MAC usato per la comunicazione con l'endpoint LAN. L'indirizzo MAC è formattato come dodici cifre esadecimali (ad esempio, "010203040506"), con ogni coppia che rappresenta uno dei sei ottetti dell'indirizzo MAC in ordine di bit canonico in base a RFC 2469. Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("bit")
</dt> </dl>

Dimensione massima, in numero di bit, del campo di informazioni che può essere inviato o ricevuto dall'endpoint LAN. Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 256 )
</dt> </dl>

Contiene l'euristica di denominazione selezionata per garantire che il valore della **proprietà Name** sia univoco. Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint.**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere usato per fornire maggiori dettagli rispetto al valore della **proprietà EnabledState.** Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OtherAuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il metodo di autenticazione 802.11 se e solo se **AuthenticationMethod** contiene 1 (Altro). Il formato di questa stringa è specifico del fornitore.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 ("Other"). Questa proprietà deve essere impostata **su Null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**OtherEncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il metodo di crittografia 802.11 se e solo se **EncryptionMethod** contiene 1 (Altro). Il formato di questa stringa è specifico del fornitore.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà è deprecata al posto della **proprietà OtherTypeDescription.** Questa proprietà viene ereditata da [**CIM \_ LANEndpoint.**](/previous-versions//cc136865(v=vs.85))

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 64 )
</dt> </dl>

Stringa che descrive il tipo di endpoint del protocollo quando la proprietà **ProtocolIFType** di questa classe (o di una delle relative sottoclassi) è impostata su 1 (Altro). Questa proprietà deve essere impostata **su Null** quando la **proprietà ProtocolIFType** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint.**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)

</dd> <dt>

**Stato primario**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni generali sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà viene utilizzata per classificare e classificare le istanze di questa classe. Se **ProtocolIFType è** impostato su 1 (Altro), le informazioni sul tipo devono essere fornite nella **proprietà OtherTypeDescription.** Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint.**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)

> [!Note]  
> **ProtocolIFType** è un'enumerazione sincronizzata con il [mib ifType IANA.](https://www.iana.org/assignments/ianaiftype-mib) Sono inclusi anche i valori aggiuntivi definiti da DMTF.

 

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802.11** (71)
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**Riservato IANA** (225..4095)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (4301..32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768. )
</dt> </dl>

</dd> <dt>

**Protocoltype**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà è deprecata al posto della **proprietà ProtocolIFType.** Questa proprietà viene ereditata da [**CIM \_ ProtocolEndpoint.**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per il servizio di gestione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive lo stato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

"OK"

"Error"

"Danneggiato"

"Sconosciuto"

"Pred Fail"

"Avvio in corso"

"Arresto in corso"

"Servizio"

"Stressed"

"NonRecover"

"No Contact"

"Lost Comm"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari **valori della matrice OperationalStatus.** Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema host. Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **MaxLen** ( 256 )
</dt> </dl>

Nome del sistema di hosting. Questa proprietà viene ereditata da [**CIM \_ ServiceAccessPoint.**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui l'istanza è in fase di transizione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

