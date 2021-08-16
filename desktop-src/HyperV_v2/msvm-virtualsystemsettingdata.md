---
description: Rappresenta le impostazioni specifiche della virtualizzazione per una macchina virtuale.
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fb57c7b96a6e2cd1839f4d830074bb69d742aef688325a37d61b67589d026436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147894"
---
# <a name="msvm_virtualsystemsettingdata-class"></a>Classe Msvm \_ VirtualSystemSettingData

Rappresenta le impostazioni specifiche della virtualizzazione per una macchina virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
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
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualSystemSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemSettingData** ha queste proprietà.

<dl> <dt>

**AdditionalRecoveryInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Eventuali informazioni aggiuntive fornite all'azione di ripristino. Il significato di questa proprietà è definito dall'azione in **AutomaticRecoveryAction**. Se **AutomaticRecoveryAction** è 0 ("None") o 1 ("Restart"), questo valore è **Null.** Se **AutomaticRecoveryAction** è 2 ("Ripristina snapshot"), si tratta del percorso dell'oggetto di uno snapshot che deve essere applicato in caso di errore del processo di lavoro della macchina virtuale.

</dd> <dt>

**AllowFullSCSICommandSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

**True** se i comandi SCSI del sistema operativo guest vengono passati ai dischi pass-through. in caso contrario, **False**. Se **True,** i comandi SCSI generati dal sistema operativo guest per i dischi pass-through non vengono filtrati. È consigliabile che i filtri SCSI rimangano abilitati per le distribuzioni di produzione.

</dd> <dt>

**AllowReducedFcRedundancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se la migrazione in tempo reale di una macchina virtuale configurata con una scheda Fibre Channel virtuale è consentita a un computer di destinazione che potrebbe non avere percorsi o percorsi ridotti per i dispositivi Fibre Channel destinazione. Questa proprietà deve essere cancellata dopo una migrazione in tempo reale.



| Valore                                                                            | Significato                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>False</dt> </dl> | Non è possibile eseguire la migrazione in tempo reale della macchina virtuale a un computer di destinazione che potrebbe non avere percorsi o percorsi ridotti per i dispositivi Fibre Channel destinazione.<br/>                                                                                                     |
| <dl> <dt>True</dt> </dl>  | È possibile eseguire la migrazione in tempo reale della macchina virtuale a un computer di destinazione che potrebbe non avere percorsi o percorsi ridotti per i dispositivi Fibre Channel destinazione. Il sistema operativo guest potrebbe perdere la connettività all'archiviazione e comportarsi in modo imprevedibile.<br/> |



 

</dd> <dt>

**Architettura**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Architettura di questo sistema.

> [!Note]  
> Aggiunta in Windows 10 versione 1709.

 

<dt>

<span id="x64"></span><span id="X64"></span>

**x64** ()


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

**arm64** ()


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Identifica l'azione da eseguire nella macchina virtuale, quando si verifica un errore critico, ad esempio la disconnessione dell'archiviazione.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** (0)


</dt> <dd>

Non verrà eseguita alcuna azione specifica per le condizioni di errore critiche.

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Sospendi ripresa** (1)


</dt> <dd>

Fa sì che la macchina virtuale sia sospesa e ripresa automaticamente quando viene risolta la condizione di errore critico.

</dd> </dl>

</dd> <dt>

**AutomaticCriticalErrorActionTimeout**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")
</dt> </dl>

Identifica la durata massima per la quale **verrà eseguito AutomaticCriticalErrorAction** per risolvere l'errore critico. Questa opzione è applicabile solo quando il valore **della proprietà AutomaticCriticalErrorAction** è diverso da 0 (Nessuno). Alla scadenza del timeout, la macchina virtuale verrà spenta. Il valore verrà arrotondato per es. Il valore 0 implica che la macchina virtuale deve essere spenta immediatamente quando si verifica una condizione di errore critico.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale in caso di errore del software eseguito dalla macchina virtuale. Gli errori in questo caso implicano un errore rilevabile dalla piattaforma host, ad esempio una condizione di stato di attesa non ininterrotta. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Può essere uno dei valori seguenti.



| Valore                                                                               | Significato                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>2</dt> </dl>        | Nessuno.<br/>               |
| <dl> <dt>3</dt> </dl>        | Riavvia.<br/>            |
| <dl> <dt>4</dt> </dl>        | Ripristinare lo snapshot.<br/> |
| <dl> <dt>5..32768</dt> </dl> | Riservato.<br/>           |



 

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale quando l'host viene arrestato. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Può essere uno dei valori seguenti.



| Valore                                                                               | Significato                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <dt>2</dt> </dl>        | Spegni.<br/>   |
| <dl> <dt>3</dt> </dl>        | Salvare lo stato.<br/> |
| <dl> <dt>4</dt> </dl>        | Arresto.<br/>   |
| <dl> <dt>5..32768</dt> </dl> | Riservato.<br/>   |



 

</dd> <dt>

**AutomaticSnapshotsEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se in questa macchina virtuale devono essere abilitati gli snapshot automatici.

> [!Note]  
> Aggiunta in Windows 10 versione 1709.

 

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale all'avvio dell'host. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

Può essere uno dei valori seguenti.



| Valore                                                                               | Significato                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>2</dt> </dl>        | Nessuno.<br/>                         |
| <dl> <dt>3</dt> </dl>        | Riavviare se precedentemente attivo.<br/> |
| <dl> <dt>4</dt> </dl>        | Iniziare sempre.<br/>                 |
| <dl> <dt>5..32768</dt> </dl> | Riservato.<br/>                     |



 

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo di ritardo prima dell'avvio automatico della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host. Un numero inferiore indica l'attivazione precedente. Se una o più configurazioni mostrano lo stesso valore, la sequenza dipende dall'implementazione. Il valore 0 indica che la sequenza dipende dall'implementazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero di serie della scheda di base per la macchina virtuale.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Identificatore univoco globale per il BIOS della macchina virtuale.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

**True** se il tasto BLOC NUM è impostato su on dal BIOS; **False** se il tasto BLOC NUM è impostato su off dal BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero di serie del BIOS per la macchina virtuale.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Ordine di avvio impostato nel BIOS della macchina virtuale. Questa proprietà è una matrice di valori, **da BootOrder** \[ 0 a \] **BootOrder** 3, inclusi, in cui ogni valore indica un dispositivo da cui \[ eseguire \] l'avvio. Ognuno dei 4 valori nella matrice deve essere impostato e non deve corrispondere a un altro valore nella matrice. La macchina virtuale tenterà prima di tutto di eseguire l'avvio dal dispositivo indicato dal primo valore all'interno della matrice. Se il dispositivo non contiene un settore di avvio, la macchina virtuale tenterà di eseguire l'avvio dal dispositivo successivo specificato dalla **proprietà BootOrder** e così via. Se nessun dispositivo specificato all'interno **di BootOrder** contiene un settore di avvio, l'avvio della macchina virtuale non riuscirà. Il valore predefinito per una macchina virtuale è \[ 0, 1, 2, \] 3.

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)


</dt> <dd>

La macchina virtuale tenterà di avviare dal disco floppy all'interno dell'unità floppy.

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)


</dt> <dd>

La macchina virtuale tenterà di eseguire l'avvio dal primo disco CD o DVD trovato con un settore di avvio.

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**Disco rigido IDE** (2)


</dt> <dd>

La macchina virtuale tenterà di eseguire l'avvio dalla prima unità disco rigido trovata con un settore di avvio.

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**Avvio PXE** (3)


</dt> <dd>

La macchina virtuale tenterà di avviare PXE dalla rete.

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**Disco rigido SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (5..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**BootSourceOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Ordine di origine di avvio per la macchina virtuale.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Tag di asset dello chassis per la macchina virtuale.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero di serie dello chassis per la macchina virtuale.

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni sulla configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo e nome file di un file in cui sono archiviate le informazioni sulla configurazione della macchina virtuale. Questo percorso è relativo alla **proprietà ConfigurationDataRoot.** Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ConsoleMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Identifica la modalità console per la macchina virtuale.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (0)


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

**COM1** (1)


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

**COM2** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione delle impostazioni per la macchina virtuale. Se questo oggetto rappresenta le impostazioni correnti per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato il sistema. Se questo oggetto rappresenta le impostazioni dello snapshot per la macchina virtuale, questo valore corrisponde all'ora in cui è stato creato lo snapshot. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**DebugChannelId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Identificatore di canale usato per eseguire il debug della macchina virtuale usando il debugger unificato.

</dd> <dt>

**DebugPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Porta TCP/IP usata per eseguire il debug della macchina virtuale usando il debug sintetico.

</dd> <dt>

**DebugPortEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Specifica se la macchina virtuale usa il debug sintetico. Può essere uno dei valori seguenti.

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>**Disattivato** (0)


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)


</dt> <dd>

Assegnato automaticamente

</dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e viene sempre impostata su uno dei valori seguenti.



| Valore                                                                                                                  | Significato                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>"Impostazioni attive per la macchina virtuale"</dt> </dl>   | Questa istanza fa riferimento a una macchina virtuale.<br/> |
| <dl> <dt>"Impostazioni snapshot per la macchina virtuale"</dt> </dl> | Questa istanza fa riferimento a uno snapshot.<br/>        |



 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))ed è sempre impostata sul nome visualizzato per il computer. Questo nome non può superare i 100 caratteri.

</dd> <dt>

**EnhancedSessionTransportType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica il tipo di trasporto da utilizzare per la connessione a una sessione avanzata.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1803.

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

**Pipe VMBus** (0)


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

**Socket Hyper-V** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestControlledCacheTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se il guest può controllare i tipi di cache.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**GuestStateDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso file di una directory in cui sono archiviate le informazioni sullo stato del runtime guest.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**GuestStateFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso file di un file in cui vengono archiviate le informazioni sullo stato del runtime guest. Un percorso relativo viene aggiunto al valore della **proprietà GuestStateDataRoot.**

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**HighMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Le dimensioni del valore High (superiore a 4 GB) Memory-Mapped I/O in MB

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

</dd> <dt>

**IncrementalBackupEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se la macchina virtuale Hyper-V VSS writer l'esecuzione di backup incrementali di questa macchina virtuale.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IsAutomaticSnapshot**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se si tratta di uno snapshot creato automaticamente per l'utente.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**IsSaved**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se la configurazione ha un riferimento a un file di stato salvato. in caso contrario, **False**. Questo non indica la presenza di un file di questo tipo, ma solo che la configurazione ne specifica uno.

</dd> <dt>

**LockOnDisconnect**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Bloccare la console quando ci si disconnette da vmconnect.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni di log per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**LowMmioGapSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Configura le dimensioni, in megabyte, del primo gap MMIO per una macchina virtuale (VM).

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

Intervallo: 128 3584

</dd> <dt>

**NetworkBootPreferredProtocol**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Determina se il protocollo preferito per l'avvio PXE è IPv4 o IPv6.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> </dl>

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note fornite dall'utente correlate alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se questa istanza non rappresenta un sistema basato su uno snapshot di una macchina virtuale, questa proprietà è **Null.** In caso contrario, la proprietà contiene il percorso dell'oggetto **Msvm \_ VirtualSystemSettingData** su cui si basa questa istanza. Quando si compila una gerarchia dell'albero degli snapshot per la macchina virtuale, questa proprietà fa riferimento all'oggetto da cui deriva l'istanza corrente (l'istanza corrente è il nodo figlio e l'oggetto a cui si fa riferimento in questa proprietà è il nodo padre).

</dd> <dt>

**ParentPackage**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Se questo sistema è un contenitore, il percorso di Msvm \_ ContainerPackage da cui si basa questo sistema.

> [!Note]  
> Aggiunta in Windows 10; rimosso in Windows 10 versione 1703.

 

</dd> <dt>

**PauseAfterBootFailure**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se il BIOS viene sospeso dopo ogni errore di immissione di avvio in attesa che l'utente premo un tasto. **True** se il BIOS viene sospeso. in caso contrario, **False**.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo di un file in cui sono archiviate le informazioni correlate al ripristino per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SecureBootEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica se l'avvio protetto è abilitato per la macchina virtuale. **True se** abilitata; in caso contrario, **False**.

> [!Note]  
> L'avvio sicuro può essere abilitato solo per le macchine virtuali di seconda generazione.

 

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**SecureBootTemplateId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Identificatore univoco globale del modello di valori iniziali delle variabili correlate all'avvio sicuro UEFI.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il [**metodo ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) della [**classe Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni sugli snapshot della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni relative alla sospensione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviati i file di scambio per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**UserSnapshotType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Indica il tipo di snapshot definito dall'utente.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (2)


</dt> <dd>

Disabilitare la creazione di qualsiasi snapshot.

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)


</dt> <dd>

Snapshot coerente con i dati da usare nell'ambiente di produzione. Esegue uno snapshot con lo stato dell'applicazione quando non è disponibile la possibilità di creare snapshot coerenti con i dati.

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)


</dt> <dd>

Snapshot coerente con i dati da usare nell'ambiente di produzione. Non crea uno snapshot con lo stato dell'applicazione se non è possibile creare uno snapshot coerente con i dati.

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)


</dt> <dd>

Snapshot che contiene informazioni sulla memoria e sul dispositivo a scopo di test e sviluppo.

</dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione della macchina virtuale nel formato "major.minor", ad esempio "2.0".

</dd> <dt>

**VirtualNumaEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")
</dt> </dl>

**True** se i nodi NUMA (Virtual Non-Uniform Memory Access) vengono proiettati nella macchina virtuale; **False** se la macchina virtuale avrà un singolo nodo. Se **True,** il numero di nodi NUMA virtuali proiettati nella macchina virtuale è determinato dai valori delle proprietà [**Msvm \_ ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) e [**Msvm \_ MemorySettingData.MaxMemoryBlocksPerNumaNode.**](msvm-memorysettingdata.md)

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome ")**
</dt> </dl>

Nome [**dell'oggetto CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) a cui appartengono i dati dell'impostazione. Questa proprietà è un override di [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

I valori validi per questa proprietà sono Microsoft:Hyper-V:SubType:1 e Microsoft:Hyper-V:SubType:2. Una macchina virtuale di prima generazione è il sottotipo 1. Una macchina virtuale di seconda generazione è il sottotipo 2.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di macchina virtuale rappresentato da dati di impostazione. Questa proprietà viene ereditata dalla [**classe CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85)) Questo sarà uno dei valori seguenti.



| Valore                                                                                                                                 | Significato                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>"Microsoft:Hyper-V:System:Realized"</dt> </dl>                        | Una macchina virtuale realizzata.<br/>               |
| <dl> <dt>"Microsoft:Hyper-V:System:Planned"</dt> </dl>                         | Una macchina virtuale pianificata.<br/>                |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt> </dl>                      | Snapshot di una macchina virtuale realizzata.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt> </dl>                      | Snapshot di una macchina virtuale di ripristino.<br/> |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt> </dl>                       | Snapshot di una macchina virtuale pianificata.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt> </dl>                       | Snapshot mancante.<br/>                       |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt> </dl>              | Snapshot del punto di replica basato sul tempo.<br/>  |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt> </dl> | Snapshot del punto di replica vss.<br/>         |
| <dl> <dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt> </dl>       | Snapshot di replica pianificato.<br/>           |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualSystemSettingData** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[Classi di sistema virtuale](virtual-system-classes.md)
</dt> </dl>

 

