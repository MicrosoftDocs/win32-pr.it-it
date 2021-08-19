---
description: Usato nei metodi GetSummaryInformation e GetDefinitionFileSummaryInformation nella classe Msvm VirtualSystemManagementService per recuperare rapidamente le informazioni comuni correlate a una macchina virtuale o \_ a uno snapshot.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4af759cf621f5afbaef90924351ad24a232889b1d81048f0e1372630c74f98f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950090"
---
# <a name="msvm_summaryinformation-class"></a>Classe Msvm \_ SummaryInformation

Usato nei [**metodi GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) e [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) nella classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per recuperare rapidamente le informazioni comuni correlate a una macchina virtuale o a uno snapshot.

La sintassi seguente è Managed Object Format (MOF).

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SummaryInformation** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SummaryInformation** ha queste proprietà.

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore dell'unità di elaborazione grafica fisica (GPU) allocata a questa macchina virtuale. Questa proprietà si applica solo alle macchine virtuali che usano RemoteFX.

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di integrità dell'applicazione corrente per la macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Application Critical** (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice \_ CiM ConcreteJob**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice di [**istanze di Msvm \_ ConcreteJob**](msvm-concretejob.md) che rappresentano le operazioni asincrone correlate alla macchina virtuale attualmente in esecuzione. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percentuale del buffer di memoria disponibile per la macchina virtuale. Quando la memoria dinamica è abilitata per una macchina virtuale, questa proprietà rappresenta il rapporto tra il buffer di memoria disponibile e il buffer di memoria ideale per la macchina virtuale. La dimensione ideale del buffer di memoria viene configurata usando la **proprietà TargetMemoryBuffer** della [**classe Msvm \_ MemorySettingData.**](msvm-memorysettingdata.md)

Questa proprietà non è valida per le istanze della **classe Msvm \_ SummaryInformation** che rappresentano le macchine virtuali per cui non è abilitata la memoria dinamica.

Questa proprietà non è valida per le istanze della **classe Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di creazione della macchina virtuale o dello snapshot.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per la macchina virtuale o lo snapshot.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente della macchina virtuale o dello snapshot. Per i **valori possibili,** vedere la proprietà EnabledState [**della classe \_ Msvm ComputerSystem.**](msvm-computersystem.md)

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le connessioni in modalità avanzata sono consentite dall'host e, se consentite, se sono disponibili per la macchina virtuale.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Consentito e disponibile** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Non consentito** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Consentito ma non disponibile** (6 )


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema operativo guest, se disponibile. Se queste informazioni non sono disponibili, il valore di questa proprietà è **Null.** Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Stato di integrità**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di integrità corrente per la macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Heartbeat**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato heartbeat corrente per la macchina virtuale. Per altre informazioni, vedere la documentazione relativa [**alla proprietà StatusDescriptions**](msvm-heartbeatcomponent.md) della **classe Msvm \_ HeartbeatComponent.** Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer che ospita la macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID è una proprietà facoltativa che può essere usata per identificare in modo opaco e univoco un'istanza di questa classe nell'ambito dello spazio dei nomi di creazione dell'istanza. Diverse sottoclassi di questa classe possono eseguire l'override di questa proprietà per renderla obbligatoria o una chiave. Tali sottoclassi possono anche modificare gli algoritmi preferiti per garantire l'univocità definita di seguito.

Per garantire l'univocità all'interno di NameSpace, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente:

<OrgID>:<LocalID>

Dove e sono separati da due punti (:) e dove devono includere un nome protetto da copyright, marchio o altrimenti univoco di proprietà dell'entità aziendale che crea o definisce InstanceID o che è un ID registrato assegnato all'entità aziendale da un'autorità globale <OrgID> <LocalID> <OrgID> riconosciuta. Questo requisito è simile al seguente: <Schema Name> \_ <Class Name> struttura dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, <OrgID> non deve contenere i due punti (:). Quando si usa questo algoritmo, i primi due punti da visualizzare in InstanceID devono essere compresi tra <OrgID> e <LocalID> .

<LocalID> viene scelto dall'entità business e non deve essere riutilizzato per identificare diversi elementi sottostanti (reali). Se non è Null e l'algoritmo "preferito" precedente non viene usato, l'entità di definizione deve garantire che l'InstanceID risultante non viene riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza.

Se non è impostato su Null per le istanze definite da DMTF, l'algoritmo "preferito" deve essere usato con <OrgID> impostato su CIM.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se i servizi di integrazione installati nella macchina virtuale sono aggiornati.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**UpToDate** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Mancata corrispondenza** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percentuale della memoria corrente disponibile per la macchina virtuale. Quando la memoria dinamica è abilitata per una macchina virtuale, questa proprietà rappresenta il rapporto tra la memoria disponibile della macchina virtuale e la memoria fisica totale assegnata alla macchina virtuale. Quando una macchina virtuale non ha memoria disponibile, questa proprietà sarà negativa e conterrà il rapporto tra la memoria necessaria per la macchina virtuale e la memoria fisica totale assegnata alla macchina virtuale.

Questa proprietà non è valida per le istanze della **classe Msvm \_ SummaryInformation** che rappresentano macchine virtuali per cui non è abilitata la memoria dinamica.

Questa proprietà non è valida per le istanze della **classe Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la memoria di uno o più nodi NUMA (Virtual NonUniform Memory Access) della macchina virtuale si estende su più nodi NUMA fisici del computer host. Contiene **True se** la memoria si estende su più nodi NUMA fisici oppure False in caso **contrario.**

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utilizzo corrente della memoria, in megabyte, della macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome univoco per la macchina virtuale o lo snapshot.

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note associate alla macchina virtuale o allo snapshot.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di processori virtuali allocati alla macchina virtuale o allo snapshot.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stati operativi correnti della macchina virtuale. Per i **valori possibili,** vedere la proprietà OperationalStatus [**della classe \_ Msvm ComputerSystem.**](msvm-computersystem.md)

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1. Questa proprietà verrà impostata su **Null** quando **EnabledState** è un valore diverso da 1.

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utilizzo corrente del processore della macchina virtuale, in percentuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**ProcessoreLoadHistory**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice dei 100 campioni precedenti dell'utilizzo del processore, in percentuale, per la macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Replicationhealth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationHealthEx**")
</dt> </dl>

Integrità della replica per la macchina virtuale. Per i **valori possibili,** vedere la proprietà ReplicationHealth [**della classe Msvm \_ ComputerSystem.**](msvm-computersystem.md)

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece **ReplicationHealthEx**.

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice di valori di integrità della replica per le varie relazioni di replica della macchina virtuale. Per i **valori possibili,** vedere la proprietà ReplicationHealth [**della classe Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Non applicabile** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Avviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di replica per la macchina virtuale. Per i **valori possibili,** vedere la proprietà ReplicationMode [**della classe Msvm \_ ComputerSystem.**](msvm-computersystem.md)

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Primario** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Replica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Replica di test** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Replica estesa** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Per la macchina virtuale di replica primaria o estesa, si tratta dell'ID del provider di replica primaria. Per una macchina virtuale di replica e se la replica estesa è abilitata, si tratta dell'ID provider per la relazione estesa.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Stato replica**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecati**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationStateEx**")
</dt> </dl>

Stato di replica per la macchina virtuale. Per i **valori possibili,** vedere la proprietà ReplicationState [**della classe Msvm \_ ComputerSystem.**](msvm-computersystem.md)

> [!Note]  
> Questa proprietà è deprecata a partire da Windows 8.1; usare invece **ReplicationStateEx.**

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Pronto per la replica** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**In attesa del completamento della replica iniziale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replica** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replica sincronizzata completata** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Ripristinato** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Commit** eseguito (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Sospeso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Critico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**In attesa di avviare la risincronizzazione** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Risincronizzazione** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Risincronizzazione sospesa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover in corso** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice di valori dello stato di replica per le varie relazioni di replica della macchina virtuale. Per i **valori possibili,** vedere la proprietà ReplicationState [**della classe Msvm \_ ReplicationRelationship.**](msvm-replicationrelationship.md)

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto per la replica** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**In attesa del completamento della replica iniziale** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replica** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replica sincronizzata completata** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Ripristinato** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Commit** eseguito (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Sospeso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**In attesa di avviare la risincronizzazione** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Risincronizzazione** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Risincronizzazione sospesa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover in corso** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback in corso** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback completato** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Aggiornamento del disco in corso** (15)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Aggiornamento del disco critico** (16)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (17)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Ridefinire la replica in corso** (18)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparata per la replica di** sincronizzazione (19)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparata per la replica inversa di** gruppo (20)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill in corso** (21)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Schermato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la schermatura è configurata o meno per la macchina virtuale.

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**Snapshot**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matrice di istanze [**di Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresentano gli snapshot per la macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Stringhe che descrivono i valori **della matrice OperationalStatus** corrispondenti. Corrisponde alla proprietà **StatusDescriptions** della [**classe Msvm \_ ComputerSystem.**](msvm-computersystem.md)

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il paging di secondo livello è attivo. Contiene **True se** il paging di secondo livello è attivo o False in caso **contrario.**

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a [**un'istanza \_ ComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) che rappresenta la macchina virtuale di replica di test per la macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Immagine di anteprima**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **OctetString,** [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImageWidth**", "**Msvm \_ SummaryInformation**.**ThumbnailImageHeight**")
</dt> </dl>

Matrice che contiene una piccola immagine in formato anteprima del desktop per la macchina virtuale o uno snapshot in formato RGB565.

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Altezza in pixel dell'immagine nella proprietà ThumbnailImage.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Larghezza in pixel dell'immagine nella proprietà ThumbnailImage.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**Uptime**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Periodo di tempo dall'ultimo avvio della macchina virtuale. Questa proprietà non è valida per le istanze di **Msvm \_ SummaryInformation** che rappresentano uno snapshot di macchina virtuale.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del sistema virtuale nel formato "major.minor", ad esempio "2.0".

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato")
</dt> </dl>

Stringhe che specificano i nomi descrittivi dei commutatori virtuali a cui è connessa la macchina virtuale.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sottotipo del sistema virtuale.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SummaryInformation** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Classi di sistema virtuale](virtual-system-classes.md)
</dt> </dl>

 

