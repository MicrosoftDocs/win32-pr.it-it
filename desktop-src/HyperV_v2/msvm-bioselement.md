---
description: Rappresenta il software di basso livello caricato nella RAM per configurare e avviare il sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Msvm_BIOSElement classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8433c8fda6d438e4f77fb763be42467aab05ab976927f018e895a30d5f9c6226
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149301"
---
# <a name="msvm_bioselement-class"></a>Classe \_ MSvm BIOSElement

Rappresenta il software di basso livello caricato nella RAM per configurare e avviare il sistema. Il BIOS non è un dispositivo logico, quindi il BIOS virtuale non deve essere pensato come un dispositivo macchina virtuale. Poiché non è un dispositivo, non dispone di un pool di risorse corrispondente. L'oggetto BIOS è associato alla macchina virtuale tramite [**l'associazione \_ SystemBIOS msvm.**](msvm-systembios.md)

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a>Members

La **classe \_ MSvm BIOSElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSvm \_ BIOSElement** ha queste proprietà.

<dl> <dt>

**BaseBoardSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di serie per la scheda di base nella macchina virtuale.

</dd> <dt>

**BIOSGUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco per il BIOS.

</dd> <dt>

**BIOSNumLock**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato del blocco num nel BIOS.

</dd> <dt>

**BIOSSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di serie per il BIOS.

</dd> <dt>

**BootOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)
</dt> </dl>

Ordine in cui i dispositivi verranno cercati per un settore di avvio all'avvio.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Identificatore interno per questa compilazione dell'elemento software. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e viene sempre impostata su 14.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ChassisAssetTag**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Popolato automaticamente dal BIOS quando viene creata la macchina virtuale.

</dd> <dt>

**ChassisSerialNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Popolato automaticamente dal BIOS quando viene creata la macchina virtuale.

</dd> <dt>

**CodeSet**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Set di codice utilizzato dall'elemento software. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **Null.**

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la possibilità della strumentazione di comunicare con l'elemento gestito sottostante. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lingua attualmente selezionata per il BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "en \| US \| iso8859-1".

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

Nome visualizzato per l'elemento. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente quella dei relativi sottocomponenti.

Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate. Anche **la proprietà EnabledState** può contenere altre informazioni. Ad esempio, quando lo spazio su disco è criticamente basso, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (In pausa).

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)



| Valore                                                                                                                                                                                                                                                            | Significato                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>5</dt> </dl>                                                                               | La macchina virtuale è completamente funzionante e funziona entro i normali parametri operativi e senza errori.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Errore principale**</dt> <dt>20</dt> </dl>             | La macchina virtuale ha subito un errore grave. Questo valore viene usato quando uno o più dischi contenenti i dischi rigidi virtuali della macchina virtuale hanno spazio su disco insufficiente e la macchina virtuale è stata sospesa.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Errore critico**</dt> <dt>25</dt> </dl> | L'elemento non è funzionante e il ripristino potrebbe non essere possibile. Ciò può indicare che il processo di lavoro per la macchina virtuale (Vmwp.exe) non risponde alle richieste di controllo o informazioni o che uno o più dischi che contengono i dischi rigidi virtuali per la macchina virtuale hanno spazio su disco insufficiente.<br/> |



 

</dd> <dt>

**Codice di identificazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Identificatore del produttore per questo elemento software. Spesso si tratta di un'unità di mantenimento delle scorte (SKU) o di un numero di parte. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **Null.**

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Popolato automaticamente dal BIOS quando viene creata la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (32)
</dt> </dl>

Edizione del linguaggio di questo elemento software. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **Null.**

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di lingue installabili per il BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "en \| US \| iso8859-1".

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **unit64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo finale della memoria occupata da questo BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su 0xFFFFF.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **unit64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo iniziale della memoria occupata da questo BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su 0xE0000.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive l'utilità flash/caricamento BIOS necessaria per aggiornare l'elemento BIOS. La versione e altre informazioni possono essere indicate in questa proprietà. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su **Null.**

</dd> <dt>

**Produttore**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (256)
</dt> </dl>

Produttore del BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "Microsoft Corporation".

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (1024)
</dt> </dl>

Nome utilizzato per identificare questo elemento software. Quando è sottoclassata, questa proprietà può essere sottoposta a override come proprietà chiave. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su "BIOS".

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

Matrice che contiene gli stati correnti dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) Il valore in corrispondenza dell'indice zero (0) è uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**OK**</dt> <dt>2</dt> </dl>                                                                                      | La macchina virtuale funziona e funziona normalmente.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Danneggiato**</dt> <dt>3</dt> </dl>                                         | La macchina virtuale è solo parzialmente funzionale. Ciò indica che l'archiviazione che contiene la configurazione non è accessibile. Una macchina virtuale in questo stato può essere solo spenta o eliminata. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Errore predittivo**</dt> <dt>5</dt> </dl> | La macchina virtuale è funzionante ma potrebbe avere esito negativo in futuro. Ciò indica che lo spazio di archiviazione che contiene il disco rigido virtuale della macchina virtuale è insufficiente. La macchina virtuale verrà sospesa se non è disponibile più spazio su disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Arrestato**</dt> <dt>10</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene arrestata, il valore della proprietà **EnabledState** sarà 3 (Disabled).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**Nel servizio**</dt> <dt>11</dt> </dl>                                | La macchina virtuale sta elaborando una richiesta.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inattivo**</dt> <dt>15</dt> </dl>                                            | Questo valore non è supportato. Se la macchina virtuale viene sospesa o sospesa, il valore della proprietà **EnabledState** sarà 32769 (Sospeso) o 32768 (Sospeso).<br/>                                                                                    |



 

Il valore in corrispondenza dell'indice 1 (1) è facoltativo e contiene informazioni sullo stato secondario. Un client deve usare lo stato primario dall'indice zero (0) per determinare se è possibile determinare se è possibile emissione di una nuova richiesta alla macchina virtuale. Se **OperationalStatus** \[ 0 è \] 2 (OK), l'operazione indicata da **OperationalStatus** \[ 1 può essere \] interrotta.

Il valore **in OperationalStatus** \[ 1 è uno dei valori \] seguenti.



| Valore                                                                                                                                                                                                                                                                                                   | Significato                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creazione dello snapshot**</dt> <dt>32768</dt> </dl>                                 | È in corso la creazione di uno snapshot per la macchina virtuale.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Applicazione dello snapshot**</dt> <dt>32769</dt> </dl>                                 | È in corso l'applicazione di uno snapshot alla macchina virtuale.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminazione dello snapshot**</dt> <dt>32770</dt> </dl>                                 | È in corso l'eliminazione di uno snapshot dalla macchina virtuale.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**In attesa dell'avvio**</dt> <dt>32771</dt> </dl>                                     | La macchina virtuale verrà avviata dopo che è trascorso il ritardo di avvio automatico.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Unione di dischi**</dt> <dt>32772</dt> </dl>                                                 | È in corso il merge dei dischi rigidi virtuali degli snapshot eliminati in precedenza.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Esportazione della macchina virtuale**</dt> <dt>32773</dt> </dl> | È in corso l'esportazione della macchina virtuale.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrazione della macchina virtuale**</dt> <dt>32774</dt> </dl> | La macchina virtuale viene migrata in tempo reale da un computer fisico a un altro.<br/>  |



 

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Produttore e sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha valore 1 (Other), che richiede che la proprietà **OtherTargetOS** abbia un valore diverso da **Null.** Per tutti gli altri valori **di TargetOperatingSystem,** la **proprietà OtherTargetOS** deve essere **Null.** Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **Null.**

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se True, si tratta del BIOS primario del sistema informatico. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su **True.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che rappresenta il percorso di pubblicazione del registro attributi BIOS o dei registri a cui è conforme l'implementazione. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di rilascio del BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Numero di serie assegnato del BIOS. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement.**](/windows/desktop/CIMWin32Prov/cim-softwareelement)

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (256)
</dt> </dl>

Identificatore per l'elemento software. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su "Microsoft:*GUID* \\ *device-specific data".*

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del ciclo di vita di un elemento software. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)e viene sempre impostata su 2 (eseguibile).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ma non viene usata.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **ArrayType** ("Indicizzato")
</dt> </dl>

Matrice contenente stringhe che descrivono i valori della matrice **OperationalStatus** corrispondenti. Ad esempio, se 11 (In Service) è il valore assegnato a **OperationalStatus** \[ \] 0, **StatusDescriptions** 0 può contenere una spiegazione del motivo per cui la macchina virtuale sta elaborando \[ una \] richiesta. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ambiente del sistema operativo dell'elemento. Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su 0 (Sconosciuto).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Versione del BIOS. Questa proprietà viene ereditata da [**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "8.02.00".

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe MSvm \_ BIOSElement** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[Classi BIOS](bios-classes.md)
</dt> <dt>

[**CIM \_ BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 

