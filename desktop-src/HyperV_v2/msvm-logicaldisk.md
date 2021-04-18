---
description: Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione.
ms.assetid: 06955C09-CA56-4B4C-997B-9B65AF125375
title: Classe Msvm_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalDisk
- Msvm_LogicalDisk.SetPowerState
- Msvm_LogicalDisk.EnableDevice
- Msvm_LogicalDisk.OnlineDevice
- Msvm_LogicalDisk.QuiesceDevice
- Msvm_LogicalDisk.SaveProperties
- Msvm_LogicalDisk.RestoreProperties
- Msvm_LogicalDisk.InstanceID
- Msvm_LogicalDisk.Caption
- Msvm_LogicalDisk.Description
- Msvm_LogicalDisk.ElementName
- Msvm_LogicalDisk.InstallDate
- Msvm_LogicalDisk.Name
- Msvm_LogicalDisk.OperationalStatus
- Msvm_LogicalDisk.StatusDescriptions
- Msvm_LogicalDisk.Status
- Msvm_LogicalDisk.HealthState
- Msvm_LogicalDisk.CommunicationStatus
- Msvm_LogicalDisk.DetailedStatus
- Msvm_LogicalDisk.OperatingStatus
- Msvm_LogicalDisk.PrimaryStatus
- Msvm_LogicalDisk.EnabledState
- Msvm_LogicalDisk.OtherEnabledState
- Msvm_LogicalDisk.RequestedState
- Msvm_LogicalDisk.EnabledDefault
- Msvm_LogicalDisk.TimeOfLastStateChange
- Msvm_LogicalDisk.AvailableRequestedStates
- Msvm_LogicalDisk.TransitioningToState
- Msvm_LogicalDisk.SystemCreationClassName
- Msvm_LogicalDisk.SystemName
- Msvm_LogicalDisk.CreationClassName
- Msvm_LogicalDisk.DeviceID
- Msvm_LogicalDisk.PowerManagementSupported
- Msvm_LogicalDisk.PowerManagementCapabilities
- Msvm_LogicalDisk.Availability
- Msvm_LogicalDisk.StatusInfo
- Msvm_LogicalDisk.LastErrorCode
- Msvm_LogicalDisk.ErrorDescription
- Msvm_LogicalDisk.ErrorCleared
- Msvm_LogicalDisk.OtherIdentifyingInfo
- Msvm_LogicalDisk.PowerOnHours
- Msvm_LogicalDisk.TotalPowerOnHours
- Msvm_LogicalDisk.IdentifyingDescriptions
- Msvm_LogicalDisk.AdditionalAvailability
- Msvm_LogicalDisk.MaxQuiesceTime
- Msvm_LogicalDisk.DataOrganization
- Msvm_LogicalDisk.Purpose
- Msvm_LogicalDisk.Access
- Msvm_LogicalDisk.ErrorMethodology
- Msvm_LogicalDisk.BlockSize
- Msvm_LogicalDisk.NumberOfBlocks
- Msvm_LogicalDisk.ConsumableBlocks
- Msvm_LogicalDisk.IsBasedOnUnderlyingRedundancy
- Msvm_LogicalDisk.SequentialAccess
- Msvm_LogicalDisk.ExtentStatus
- Msvm_LogicalDisk.NoSinglePointOfFailure
- Msvm_LogicalDisk.DataRedundancy
- Msvm_LogicalDisk.PackageRedundancy
- Msvm_LogicalDisk.DeltaReservation
- Msvm_LogicalDisk.Primordial
- Msvm_LogicalDisk.NameFormat
- Msvm_LogicalDisk.NameNamespace
- Msvm_LogicalDisk.OtherNameNamespace
- Msvm_LogicalDisk.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5071f2a102a32364888c9c7de5121ede5249f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312909"
---
# <a name="msvm_logicaldisk-class"></a>\_Classe MSVM disco logico

Rappresenta il supporto dell'unità di archiviazione e viene utilizzato per popolare le unità di archiviazione. I tipi di supporto supportati includono i file rigidi virtuali, i file floppy virtuali, i file ISO e i supporti per i dispositivi fisici.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalDisk : CIM_LogicalDisk
{
  string   InstanceID;
  string   Caption;
  uint64   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_LogicalDisk";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = { 6 };
  uint64   MaxQuiesceTime;
  uint16   DataOrganization = 2;
  string   Purpose;
  uint16   Access;
  string   ErrorMethodology;
  uint64   BlockSize = 512;
  uint64   NumberOfBlocks = 266338304;
  uint64   ConsumableBlocks = 0;
  boolean  IsBasedOnUnderlyingRedundancy = False;
  boolean  SequentialAccess = False;
  uint16   ExtentStatus[] = { 2 };
  boolean  NoSinglePointOfFailure = False;
  uint16   DataRedundancy = 0;
  uint16   PackageRedundancy = 0;
  uint8    DeltaReservation = 0;
  boolean  Primordial = False;
  uint16   NameFormat = 12;
  uint16   NameNamespace = 8;
  string   OtherNameNamespace;
  string   OtherNameFormat;
};
```

## <a name="members"></a>Members

La **classe \_ disco logico di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ disco logico di MSVM** dispone di questi metodi.



| Metodo                                                            | Descrizione                              |
|:------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                  | Questo metodo non è supportato.<br/> |
| **OnlineDevice**                                                  | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                                 | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-logicaldisk-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-logicaldisk-reset.md)                           | Reimposta il servizio.<br/>           |
| **RestoreProperties**                                             | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                                | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                                 | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ disco logico di MSVM** dispone di queste proprietà.

<dl> <dt>

**Accesso**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il supporto è leggibile, scrivibile o entrambi. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).



| Valore                                                                        | Significato                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Sconosciuto<br/>     |
| <dl> <dt>1</dt> </dl> | Leggibile.<br/>   |
| <dl> <dt>2</dt> </dl> | Scrivibile.<br/>  |
| <dl> <dt>3</dt> </dl> | Proprietà di lettura/scrittura.<br/> |
| <dl> <dt>4</dt> </dl> | Scrivere una sola volta.<br/> |



 

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali disponibilità e stato aggiuntive del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).



| Valore                                                                            | Significato                    |
|----------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>6</dt> </dl> | Non applicabile.<br/> |



 

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).



| Valore                                                                        | Significato                    |
|------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>6</dt> </dl> | Non applicabile.<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usato per avviare una modifica di stato. I valori elencati saranno un subset dei valori contenuti nella proprietà **RequestedStatesSupported** dell'istanza associata di **CIM \_ EnabledLogicalElementCapabilities**, dove i valori selezionati sono una funzione dello stato corrente dell'oggetto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Questa proprietà può essere diversa da **null** se un'implementazione è in grado di annunciare il set di valori possibili come funzione dello stato corrente. Questa proprietà sarà **null** se un'implementazione non è in grado di determinare il set di valori possibili come funzione dello stato corrente.

Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione, in byte, dei blocchi che formano l'extent di archiviazione. Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco in byte. Se la dimensione del blocco è sconosciuta o se un concetto di blocco non è valido, ad esempio per extent di aggregazione, memoria o dischi logici, questo conterrà 1. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

"Immagine disco ISO"

"Immagine disco rigido"

"Immagine disco floppy"

"Disco CD/DVD"

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di blocchi, di dimensioni **blockSize**, che sono disponibili per l'utilizzo quando si esegue il layering degli extent di archiviazione utilizzando l'associazione [**MSVM \_ BasedOn**](msvm-basedon.md) . Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Dataorganization**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di organizzazione dati utilizzato. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).



| Valore                                                                        | Significato                 |
|------------------------------------------------------------------------------|-------------------------|
| <dl> <dt>2</dt> </dl> | Blocco fisso.<br/> |



 

</dd> <dt>

**Ridondanza dataridondanza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di copie complete dei dati attualmente mantenute. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percentuale che specifica la quantità di spazio che deve essere riservata in una replica per la memorizzazione nella cache delle modifiche. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
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

Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su "Microsoft:*GUID* \\ *Device-Specific-Data*".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

"Immagine disco ISO"

"Immagine disco rigido"

"Immagine disco floppy"

"Disco CD/DVD"

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Può inoltre indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

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

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali informazioni aggiuntive sullo stato oltre a quelle acquisite in **OperationalStatus** e altre proprietà ereditate.



| Valore                                                                            | Significato                         |
|----------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>2</dt> </dl> | Nessuno/non applicabile.<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti. I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni e dettagli dietro le voci nella matrice di proprietà **OtherIdentifyingInfo** . Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se gli extent di archiviazione sottostanti partecipano a un gruppo di ridondanza di archiviazione. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà è stata deprecata. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).



| Valore                                                                         | Significato                                 |
|-------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>1</dt> </dl>  | Altro<br/>                        |
| <dl> <dt>12</dt> </dl> | Nome dispositivo del sistema operativo<br/> |



 

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).



| Valore                                                                        | Significato                                      |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>1</dt> </dl> | Altro<br/>                             |
| <dl> <dt>8</dt> </dl> | Spazio dei nomi del dispositivo del sistema operativo<br/> |



 

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se non esiste alcun singolo punto di errore. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di blocchi consecutivi, ciascuno dei quali blocca la dimensione del valore contenuto nella proprietà **blockSize** , che costituisce l'extent di archiviazione. Le dimensioni totali dell'extent di archiviazione possono essere calcolate moltiplicando il valore della proprietà **blockSize** in base al valore di questa proprietà. Se il valore di **blockSize** è 1, questa proprietà corrisponde alla dimensione totale dell'extent di archiviazione. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** . Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")
</dt> </dl>

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Quando il livello di QoS richiesto per il disco virtuale non può essere soddisfatto, lo stato primario (OperationalStatus \[ 0 \] ) viene impostato su ridotto (3) e la matrice OperationalStatus contiene inoltre un valore di stato secondario che indica il motivo specifico della condizione QoS, in base a questa tabella.



| Valore                                                                                                                                                                                                    | Descrizione                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="_Insufficient_Throughput___32788_"></span><span id="_insufficient_throughput___32788_"></span><span id="_INSUFFICIENT_THROUGHPUT___32788_"></span> Velocità effettiva insufficiente (32788)<br/> | La velocità di IOPS minima richiesta non è attualmente disponibile per il dispositivo. <br/> |



 

> [!Note]  
> OperationalStatus viene utilizzato anche per segnalare altre condizioni di errore o avviso, ad esempio la mancata corrispondenza del protocollo tra VSP e VSC. Se esistono più condizioni, lo stato primario viene impostato come danneggiato e uno o più valori di stato secondari, in qualsiasi ordine a partire dall'indice 1, vengono inseriti nella matrice.

 

<dt>

<span id="OK"></span><span id="ok"></span>

<span id="OK"></span><span id="ok"></span>**OK** (2)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (3)


</dt> <dd></dd> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (7)


</dt> <dd></dd> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (11)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (12)


</dt> <dd></dd> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (13)


</dt> <dd></dd> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (16)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> <dt>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>

<span id="Protocol_Mismatch"></span><span id="protocol_mismatch"></span><span id="PROTOCOL_MISMATCH"></span>**Mancata corrispondenza del protocollo** (32775)


</dt> <dd></dd> <dt>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>

<span id="Communication_Timed_Out"></span><span id="communication_timed_out"></span><span id="COMMUNICATION_TIMED_OUT"></span>**Timeout della comunicazione** (32783)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> <dt>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>

<span id="Insufficient_Throughput"></span><span id="insufficient_throughput"></span><span id="INSUFFICIENT_THROUGHPUT"></span>**Velocità effettiva insufficiente** (32788)


</dt> <dd></dd> <dt>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>

<span id="Unknown_QoS_Policy_ID"></span><span id="unknown_qos_policy_id"></span><span id="UNKNOWN_QOS_POLICY_ID"></span>**ID criterio QoS sconosciuto** (32791)


</dt> <dd></dd> <dt>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>

<span id="QoS_Not_Supported"></span><span id="qos_not_supported"></span><span id="QOS_NOT_SUPPORTED"></span>**QoS non supportata** (32792)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> <dt>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>

<span id="QoS_Configuration_Mismatch"></span><span id="qos_configuration_mismatch"></span><span id="QOS_CONFIGURATION_MISMATCH"></span>**Configurazione QoS non corrispondente** (32793)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> <dt>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>

<span id="Disk_Full"></span><span id="disk_full"></span><span id="DISK_FULL"></span>**Disco pieno** (32794)


</dt> <dd>

> [!Note]  
> Aggiunto in Windows 10.

 

</dd> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il formato della proprietà **Name** quando **NameFormat** contiene il valore 1 (other). Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo spazio dei nomi della proprietà **Name** quando **NameNamespace** contiene il valore 1 (other). Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di pacchetti fisici che attualmente possono avere esito negativo senza perdita di dati. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

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

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Originale**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il sistema contenitore è in grado di creare o eliminare questo elemento operativo. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)ed è impostata su **false** per i supporti basati su file e **true** per i supporti pass-through.

</dd> <dt>

**Scopo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive i supporti e/o il relativo utilizzo. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato da **EnabledState**. Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato. Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** . In tal caso, viene utilizzato il valore 12 (non applicabile). Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se l'accesso alla risorsa di archiviazione viene eseguito in modo sequenziale da un dispositivo di accesso multimediale. Il supporto per nastri pass-through è un esempio di un extent di archiviazione a cui si accede in modo sequenziale. Questa proprietà viene ereditata da [**CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent).

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

Identificatore univoco per la macchina virtuale di ambito. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

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

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), ma non viene utilizzata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ disco logico di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Disco logico CIM**](cim-logicaldisk.md)
</dt> <dt>

[**\_Disco logico CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldisk)
</dt> <dt>

[**\_StorageAlert MSVM**](msvm-storagealert.md)
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

