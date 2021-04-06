---
description: Rappresenta le impostazioni per il servizio di replica in un host di ripristino. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il \_ Metodo MSVM ReplicationService. ModifyServiceSettings per modificare una di queste proprietà.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Classe Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882765"
---
# <a name="msvm_replicationservicesettingdata-class"></a>\_Classe MSVM ReplicationServiceSettingData

Rappresenta le impostazioni per il servizio di replica in un host di ripristino. Non è possibile modificare direttamente le proprietà di questa classe. Il client deve chiamare il metodo [**MSVM \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) per modificare una di queste proprietà.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a>Members

La **classe \_ ReplicationServiceSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ReplicationServiceSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**AllowedAuthenticationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definire le modalità di autenticazione consentite per la connessione al server host di ripristino.

<dt>

0
</dt> <dd>

Non definito.

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticazione Kerberos** (1)


</dt> <dd>

Autenticazione Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)


</dt> <dd>

Autenticazione basata su certificati.

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Autenticazione basata su certificati e autenticazione Kerberos** (3)


</dt> <dd>

Autenticazione basata su certificati e autenticazione integrata.

</dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Service Settings".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Identificazione personale del certificato da usare quando **AuthenticationType** è l'autenticazione basata su certificati.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "dati delle impostazioni di replica della macchina virtuale".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Service Settings".

</dd> <dt>

**HttpPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porta del server di ripristino da utilizzare quando si accetta una connessione non protetta per la replica. Il valore predefinito è 80.

</dd> <dt>

**HttpsPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porta del server di ripristino da utilizzare quando si accetta una connessione protetta per la replica. Il valore predefinito è 443.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**MonitoringInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo, in secondi, in cui devono essere reimpostate le statistiche di replica. L'intervallo predefinito è 12 ore (43200 secondi). Il valore minimo valido è 60 minuti (3600 secondi) e il valore massimo valido è 7 giorni (604800 secondi).

</dd> <dt>

**MonitoringStartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio per il monitoraggio della replica, in formato UTC. Il valore predefinito è 9:00 A.M., ora locale, rappresentato in formato UTC. Gli elementi date dell'oggetto **DateTime** devono essere pari a zero.

</dd> <dt>

**RecoveryServerEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se l'host Hyper-V è abilitato come server di ripristino.

</dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> <dt>

[**ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

