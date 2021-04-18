---
description: Rappresenta una porta di Fibre Channel esterna.
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Classe Msvm_ExternalFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307925"
---
# <a name="msvm_externalfcport-class"></a>\_Classe MSVM ExternalFcPort

> [!NOTE]
> Questo articolo contiene riferimenti al termine slave, che Microsoft non usa più. Quando il termine verrà rimosso dal software, verrà rimosso anche dall'articolo.

Rappresenta una porta di Fibre Channel esterna.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a>Members

La **classe \_ ExternalFcPort di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ ExternalFcPort di MSVM** dispone di questi metodi.



| Metodo                                                               | Descrizione                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                     | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                     | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                    | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-externalfcport-requeststatechange.md) | Richiede una modifica dello stato<br/>       |
| [**Reset**](msvm-externalfcport-reset.md)                           | Reimposta il dispositivo virtuale.<br/>    |
| **RestoreProperties**                                                | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                   | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                    | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ ExternalFcPort di MSVM** dispone di queste proprietà.

<dl> <dt>

**ActiveCOS**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di Integer che indica le classi del servizio attive. I COS supportati sono specificati dalla proprietà **SupportedCOS** . Questa proprietà viene ereditata da **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="1"></span>**1** (1)
</dt> <dt>

<span id="2"></span>**2** (2)
</dt> <dt>

<span id="3"></span>**3** (3)
</dt> <dt>

<span id="4"></span>**4** (4)
</dt> <dt>

<span id="5"></span>**5** (5)
</dt> <dt>

<span id="6"></span>**6** (6)
</dt> <dt>

<span id="F"></span><span id="f"></span>**F** (7)
</dt> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di numeri interi che indica il Fibre Channel i protocolli FC-4 attualmente in esecuzione. Un elenco di tutti i protocolli supportati viene specificato dalla proprietà **SupportedFC4Types** . Questa proprietà viene ereditata da **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)
</dt> </dl>

</dd> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("byte")
</dt> </dl>

Unità di trasmissione massima (MTU) attiva o negoziata che può essere supportata, in byte. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali disponibilità e stato aggiuntive del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**Rilevamento automatico**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta è in grado di determinare automaticamente la velocità o altre caratteristiche di comunicazione del supporto di rete collegato. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** . Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Un indirizzo o altre informazioni di identificazione per assegnare un nome univoco al dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

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

Configurazione predefinita o di avvio di un amministratore per la proprietà **EnabledState** di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e sarà uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                       | Significato                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                                 | Non è stato possibile determinare lo stato dell'elemento.<br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Altro**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Abilitato**</dt> <dt>2</dt> </dl>                                                 | L'elemento è in esecuzione.<br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Disabilitato**</dt> <dt>3</dt> </dl>                                             | L'elemento è disattivato.<br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Chiusura**</dt> di <dt>4</dt> </dl>                         | L'elemento è in corso di passaggio a uno stato disabilitato.<br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Non applicabile**</dt> <dt>5</dt> </dl>                     | L'elemento non supporta l'abilitazione o la disabilitazione.<br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Abilitato ma offline**</dt> <dt>6</dt> </dl> | L'elemento potrebbe essere il completamento dei comandi e verranno eliminate tutte le nuove richieste.<br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**Nel test**</dt> <dt>7</dt> </dl>                                                 | L'elemento si trova in uno stato di test.<br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Posticipato**</dt> <dt>8</dt> </dl>                                             | È possibile che l'elemento stia completando i comandi, ma verrà accodato qualsiasi nuova richiesta.<br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Mettere in stato**</dt> <dt>9</dt> </dl>                                                 | L'elemento è abilitato, ma è in modalità con restrizioni. Il comportamento dell'elemento è simile allo stato abilitato (2), ma elabora solo un set di comandi limitato. Tutte le altre richieste vengono accodate.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**A partire**</dt> da <dt>10</dt> </dl>                                            | L'elemento è in corso di attivazione dello stato abilitato (2). Le nuove richieste vengono accodate.<br/>                                                                                                                    |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'errore segnalato in **LastErrorCode** è ora cancellato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce ulteriori informazioni sull'errore registrato in **LastErrorCode** e informazioni sulle azioni correttive che possono essere eseguite. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la porta funziona in modalità full duplex. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** . Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di installazione dell'oggetto. Questa proprietà non richiede un valore per indicare che l'oggetto è installato. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**IsHyperVCapable**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se questa proprietà è impostata su **true**, la porta Fibre Channel può essere connessa alle opzioni e pertanto può fornire connettività a una macchina virtuale. Se questa proprietà è **false**, questa porta non può essere utilizzata dall'architettura Fibre Channel della macchina virtuale.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di tecnologia di collegamento per la porta. Quando è impostata su 1 (other), la proprietà **OtherLinkTechnology** contiene una descrizione di stringa del tipo di collegamento. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)
</dt> <dt>

<span id="IB"></span><span id="ib"></span>**IB** (3)
</dt> <dt>

<span id="FC"></span><span id="fc"></span>**FC** (4)
</dt> <dt>

<span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)
</dt> <dt>

<span id="ATM"></span><span id="atm"></span>**ATM** (6)
</dt> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)
</dt> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)
</dt> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarossi** (9)
</dt> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)
</dt> <dt>

<span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN wireless** (11)
</dt> </dl>

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà è stata deprecata. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**MaxSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("bit al secondo")
</dt> </dl>

Larghezza di banda massima della porta, in bit al secondo. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Matrice di stringhe che contengono gli indirizzi MAC per la porta. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** . Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa che descrive **LinkTechnology** quando è impostato su 1, (other). Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'utilizzo di questa proprietà è deprecato al posto della proprietà **portType** . Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**OtherPortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive il tipo di modulo, quando **portType** è impostato su 1 (other). Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **maxlen** (64)
</dt> </dl>

Indirizzo di rete hardcoded in una porta. Questo indirizzo hardcoded può essere modificato usando un aggiornamento del firmware o una configurazione software. Quando questa modifica viene apportata, il campo deve essere aggiornato nello stesso momento. Questa proprietà deve essere **null** se non esiste alcun indirizzo hardcoded per la scheda di rete. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**NumeroPorta**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero della porta. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità specifica attualmente abilitata per la porta. Quando è impostata su 1 (other), la proprietà **OtherPortType** correlata contiene una descrizione di stringa del tipo di porta. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 rame 10BaseT** (50)
</dt> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)
</dt> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)
</dt> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)
</dt> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)
</dt> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)
</dt> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)
</dt> <dt>

<span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 fibre 100BASE-FX** (100)
</dt> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100BASE-SX** (101)
</dt> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)
</dt> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)
</dt> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000BASE-CX** (104)
</dt> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)
</dt> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)
</dt> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)
</dt> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)
</dt> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)
</dt> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)
</dt> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-EW** (111)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (16000.65535)
</dt> </dl>

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità di risparmio energia del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il dispositivo può essere gestito da energia elettrica. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di ore consecutive in cui il dispositivo è stato alimentato dall'ultimo ciclo di alimentazione. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedSpeed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola scrittura
</dt> <dt>

Qualificatori: **unità** ("bit al secondo")
</dt> </dl>

Larghezza di banda richiesta della porta, in bit al secondo. La larghezza di banda effettiva viene segnalata nella proprietà **velocità** . Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 12 (non applicabile).

</dd> <dt>

**Velocità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("bit al secondo")
</dt> </dl>

Larghezza di banda della porta, in bit al secondo. Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente del dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**SupportedCOS**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di Integer che indica le classi di Fibre Channel di servizio (COS) supportate. Il COS attivo viene specificato dalla proprietà **ActiveCOS** . Questa proprietà viene ereditata da **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="1"></span>**1** (1)
</dt> <dt>

<span id="2"></span>**2** (2)
</dt> <dt>

<span id="3"></span>**3** (3)
</dt> <dt>

<span id="4"></span>**4** (4)
</dt> <dt>

<span id="5"></span>**5** (5)
</dt> <dt>

<span id="6"></span>**6** (6)
</dt> <dt>

<span id="F_"></span><span id="f_"></span>**F** (7)
</dt> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di Integer che indica i protocolli Fibre Channel FC-4 supportati. I protocolli attivi e in esecuzione sono specificati dalla proprietà **ActiveFC4Types** . Questa proprietà viene ereditata da **CIM \_ FCPort**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)
</dt> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP su FC** (5)
</dt> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)
</dt> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)
</dt> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 Master** (17)
</dt> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 slave** (18)
</dt> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 peer** (19)
</dt> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 Master** (21)
</dt> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 slave** (22)
</dt> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 peer** (23)
</dt> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canale SBCCS** (25)
</dt> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unità di controllo SBCCS** (26)
</dt> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canale FC-SB-2** (27)
</dt> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unità di controllo FC-SB-2** (28)
</dt> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Servizi di Fibre Channel (FC-GS, FC-GS-2, FC-GS-3)** (32)
</dt> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)
</dt> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)
</dt> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)
</dt> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Controllo BBL** (80)
</dt> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI incapsulato LAN PDU** (81)
</dt> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**Rete LAN incapsulata BBL 802,3** (82)
</dt> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-vi** (88)
</dt> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)
</dt> <dt>

<span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Fornitore univoco** (255)
</dt> </dl>

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **unità** ("byte")
</dt> </dl>

Unità di trasmissione massima (MTU) che può essere supportata, in byte. Questa proprietà viene ereditata da [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero totale di ore in cui il dispositivo è stato alimentato. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**UsageRestriction**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

In alcuni casi, una porta logica potrebbe essere identificabile come porta front-end o back-end. Un esempio di questa situazione è costituito da un array di archiviazione che può avere porte back-end per comunicare con le unità disco e le porte front-end per comunicare con gli host. Se non esiste alcuna restrizione sull'uso della porta, il valore deve essere impostato su 4 (senza restrizioni). Questa proprietà viene ereditata da [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)
</dt> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)
</dt> <dt>

<span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Senza restrizioni** (4)
</dt> </dl>

</dd> <dt>

**WWNN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del nodo universale per la porta Fibre Channel.

</dd> <dt>

**WWPN**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della porta universale per la porta Fibre Channel.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

