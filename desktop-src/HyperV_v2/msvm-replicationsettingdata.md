---
description: Rappresenta le impostazioni specifiche della replica per una macchina virtuale.
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 90e16e70f7b5bd0a075ffdef54cf0c591719d4993031f3abee19dd8186ec5996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148254"
---
# <a name="msvm_replicationsettingdata-class"></a>Classe Msvm \_ ReplicationSettingData

Rappresenta le impostazioni specifiche della replica per una macchina virtuale. Il client passa un'istanza di questa classe [**a Msvm \_ ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) per creare una relazione di replica. Il client non può modificare direttamente i valori di nessuna delle proprietà per questa classe. deve chiamare il [**metodo Msvm \_ ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) per modificare i valori. Ogni relazione di replica ha una singola istanza di impostazioni.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ReplicationSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ReplicationSettingData** ha queste proprietà.

<dl> <dt>

**AdditionalSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazioni di replica aggiuntive che il provider di endpoint può usare.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**ApplicationConsistentSnapshotInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di tempo tra snapshot coerenti con l'applicazione, specificato in ore. I valori validi sono da 1 ora a 12 ore.

</dd> <dt>

**Authenticationtype**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definire la modalità di autenticazione usata per connettersi al server di ripristino.

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Autenticazione Kerberos** (1)


</dt> <dd>

Autenticazione Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Autenticazione basata su certificati** (2)


</dt> <dd>

Autenticazione basata su certificato.

</dd> </dl>

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo di ritardo prima dell'avvio automatico della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))ma non viene usata.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData,**](/previous-versions//cc136954(v=vs.85))ma non viene usata.

</dd> <dt>

**AutoResynchronizeEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le operazioni di risincronizzazione vengono attivate automaticamente quando si verifica un errore di replica a causa di errori di alimentazione e hardware. Le operazioni di risincronizzazione vengono attivate solo quando l'errore si verifica tra gli orari specificati dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd.**

Il valore predefinito è **False**.

</dd> <dt>

**AutoResynchronizeIntervalEnd**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora di fine per l'attivazione delle operazioni di risincronizzazione automatica. Questo valore è nell'ora locale. Il valore predefinito è 06:00 (6:00).

Le operazioni di risincronizzazione vengono attivate solo quando l'errore si verifica tra gli orari specificati dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd.**

Le operazioni di risincronizzazione possono anche essere pianificate in modo che siano attivate durante l'intervallo successivo.

</dd> <dt>

**AutoResynchronizeIntervalStart**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora di inizio per l'attivazione delle operazioni di risincronizzazione automatica. Questo valore è nell'ora locale. Il valore predefinito è 18:30 (18:30).

Le operazioni di risincronizzazione vengono attivate solo quando l'errore si verifica tra gli orari specificati dalle proprietà **AutoResynchronizeIntervalStart** e **AutoResynchronizeIntervalEnd.**

Le operazioni di risincronizzazione possono anche essere pianificate in modo che siano attivate durante l'intervallo successivo.

</dd> <dt>

**BypassProxyServer**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se il server proxy deve essere ignorato durante la connessione a un server di ripristino.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Replication Impostazioni".

</dd> <dt>

**CertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Identificazione personale del certificato da usare quando la **proprietà AuthenticationType** è basata su certificato.

</dd> <dt>

**CompressionEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se i dati di replica verranno compressi durante l'invio al server di ripristino.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato.

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**File di configurazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo e nome file di un file in cui sono archiviate le informazioni sulla configurazione della macchina virtuale. Questo percorso è relativo alla **proprietà ConfigurationDataRoot.** Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione delle impostazioni per la macchina virtuale. Se questo oggetto rappresenta le impostazioni correnti per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato il sistema. Se questo oggetto rappresenta le impostazioni dello snapshot per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato lo snapshot. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il metodo [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Machine Replication Impostazioni Data".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è impostata sul nome visualizzato per la macchina virtuale.

</dd> <dt>

**EnableWriteOrderPreservationAcrossDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore")
</dt> </dl>

Specifica se tutti i dischi rigidi virtuali di replica per la macchina virtuale vengono replicati nello stesso momento. In questo modo la replica rispetta l'ordine di scrittura delle applicazioni nella macchina virtuale.

**Windows 8.1:** A partire Windows 8.1 e Windows Server 2012 R2, questa proprietà è deprecata e sempre impostata su **TRUE.**

</dd> <dt>

**IncludedDisks**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **HyperVEmbeddedInstance** ("CIM \_ StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Elenco dei dischi rigidi virtuali (VHD) collegati al sistema che verranno replicati dal motore di replica. Si tratta di una matrice di stringhe, ognuna delle quali contiene il **valore InstanceID** di [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) che rappresenta il disco rigido virtuale.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85)) Ad Windows 8, è sempre impostato su "Microsoft:*Virtual Machine GUID* \\ HVR". Ad Windows 8.1, è impostato su "Microsoft:*Virtual Machine GUID* \\ HVR<\\ 0/1>". Nel valore Windows 8.1 0 indica la replica primaria e 1 indica la replica estesa. Per altre informazioni sulla replica estesa, vedere [**Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni di log per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non usato e non può essere impostato.

Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**PrimaryConnectionPoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome del punto di connessione primario. Nel caso di un cluster primario, si tratta del nome CAP del broker. Nel caso di un server primario autonomo, si tratta del nome del sistema host.

</dd> <dt>

**PrimaryHostSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome di dominio completo del sistema host primario che ospita la macchina virtuale.

</dd> <dt>

**RecoveryConnectionPoint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome del punto di connessione di ripristino. Nel caso di un cluster di ripristino, si tratta del nome CAP del broker. Nel caso di un server di ripristino autonomo, si tratta del nome del sistema host.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo di un file in cui sono archiviate le informazioni correlate al ripristino per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**RecoveryHistory**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di snapshot di ripristino che verranno archiviati nel server di ripristino. I valori validi sono da 0 a 24.

</dd> <dt>

**RecoveryHostSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome di dominio completo del sistema host di ripristino che ospita la macchina virtuale.

</dd> <dt>

**RecoveryServerPortNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di porta del server di ripristino da utilizzare quando si effettua una connessione protetta per la replica.

</dd> <dt>

**ReplicateHostKvpItems**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se gli oggetti [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)solo host devono essere replicati dalla macchina virtuale primaria alla macchina virtuale di ripristino.

</dd> <dt>

**ReplicationInterval**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Intervallo di replica di una relazione di replica in secondi. I valori validi sono:

30

300

900

Il valore predefinito è 300 secondi.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Provider di replica**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso dell'istanza della classe [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md) che identifica l'endpoint del provider di replica.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**RootCertificateThumbPrint**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)
</dt> </dl>

Identificazione personale del certificato radice del certificato in uso quando **AuthenticationType** è 2 (autorizzazione basata su certificato).

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni sugli snapshot della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni relative alla sospensione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviati i file di scambio per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), ma non viene usata.

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome [**dell'oggetto \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione. Questa proprietà è un override di [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di macchina virtuale rappresentato dall'impostazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è sempre impostata su "Microsoft:Hyper-V:Replica".

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

