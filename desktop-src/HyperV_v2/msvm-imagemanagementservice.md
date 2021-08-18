---
description: Gestisce il supporto virtuale (file VHD, VHDX, ISO o VFD) per una macchina virtuale.
ms.assetid: 7caa720e-37cf-454e-8634-f2bd82bcf83d
title: Msvm_ImageManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService
- Msvm_ImageManagementService.InstanceID
- Msvm_ImageManagementService.Caption
- Msvm_ImageManagementService.Description
- Msvm_ImageManagementService.ElementName
- Msvm_ImageManagementService.InstallDate
- Msvm_ImageManagementService.OperationalStatus
- Msvm_ImageManagementService.StatusDescriptions
- Msvm_ImageManagementService.Status
- Msvm_ImageManagementService.HealthState
- Msvm_ImageManagementService.CommunicationStatus
- Msvm_ImageManagementService.DetailedStatus
- Msvm_ImageManagementService.OperatingStatus
- Msvm_ImageManagementService.PrimaryStatus
- Msvm_ImageManagementService.EnabledState
- Msvm_ImageManagementService.OtherEnabledState
- Msvm_ImageManagementService.RequestedState
- Msvm_ImageManagementService.EnabledDefault
- Msvm_ImageManagementService.TimeOfLastStateChange
- Msvm_ImageManagementService.AvailableRequestedStates
- Msvm_ImageManagementService.TransitioningToState
- Msvm_ImageManagementService.SystemCreationClassName
- Msvm_ImageManagementService.SystemName
- Msvm_ImageManagementService.CreationClassName
- Msvm_ImageManagementService.Name
- Msvm_ImageManagementService.PrimaryOwnerName
- Msvm_ImageManagementService.PrimaryOwnerContact
- Msvm_ImageManagementService.StartMode
- Msvm_ImageManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6836477bbeadac015c2759758b81d0f93ce938ea9ac730d5d610a2ddc819759a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148404"
---
# <a name="msvm_imagemanagementservice-class"></a>Classe Msvm \_ ImageManagementService

Gestisce il supporto virtuale (file VHD, VHDX, ISO o VFD) per una macchina virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ImageManagementService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Image Management Service";
  string   Description = "Provides Image Management servicing for Hyper-V";
  string   ElementName = "Hyper-V Image Management Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
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
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ImageManagementService";
  string   Name = "vhdsvc";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ImageManagementService** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Msvm \_ ImageManagementService** include questi metodi.



| Metodo                                                                                                           | Descrizione                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachVirtualHardDisk**](attachvirtualharddisk-msvm-imagemanagementservice.md)                               | Collega un file di immagine del disco virtuale in modalità loopback.<br/>                                                                                                                                                                             |
| [**CompactVirtualHardDisk**](compactvirtualharddisk-msvm-imagemanagementservice.md)                             | Compatta un file del disco rigido virtuale.<br/>                                                                                                                                                                                               |
| [**ConvertVirtualHardDisk**](convertvirtualharddisk-msvm-imagemanagementservice.md)                             | Converte un disco rigido virtuale esistente in un tipo o formato diverso.<br/>                                                                                                                                                            |
| [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md)             | Converte un file di disco rigido virtuale creando un nuovo file set di dischi rigidi virtuali insieme al disco rigido virtuale esistente.<br/>                                                                                                                       |
| [**CreateVirtualFloppyDisk**](createvirtualfloppydisk-msvm-imagemanagementservice.md)                           | Crea un file disco floppy virtuale.<br/>                                                                                                                                                                                              |
| [**CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md)                               | Crea un file del disco rigido virtuale.<br/>                                                                                                                                                                                                |
| [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md)                                       | Elimina una voce snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.<br/>                                                                                                                                                                              |
| [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md)           | Trova un oggetto Msvm \_ MountedStorageImage per un percorso di immagine disco specificato.<br/>                                                                                                                                                            |
| [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md)                                 | Recupera informazioni su un file set di dischi rigidi virtuali.<br/>                                                                                                                                                                                      |
| [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md)                       | Recupera informazioni su uno snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali.<br/>                                                                                                                                                                |
| [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md)                               | Recupera un elenco di modifiche nell'area specificata di un disco virtuale a partire dall'ID Rilevamento modifiche resiliente o dall'ID snapshot VHDSet specificato.<br/>                                                                                     |
| [**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | Recupera i dati delle impostazioni associati ai file del disco rigido virtuale.<br/>                                                                                                                                                                  |
| [**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)                           | Recupera lo stato dei file del disco rigido virtuale.<br/>                                                                                                                                                                                      |
| [**MergeVirtualHardDisk**](mergevirtualharddisk-msvm-imagemanagementservice.md)                                 | Unisce un disco rigido virtuale figlio in una catena differenze con uno o più dischi rigidi virtuali padre nella catena.<br/>                                                                                                                |
| [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)                                             | Ottimizza un file set di dischi rigidi virtuali in modo da usare meno spazio su disco.<br/>                                                                                                                                                                                 |
| [**RequestStateChange**](msvm-imagemanagementservice-requeststatechange.md)                                     | Richiede una modifica dello stato.<br/>                                                                                                                                                                                                         |
| [**ResizeVirtualHardDisk**](resizevirtualharddisk-msvm-imagemanagementservice.md)                               | Ridimensiona un disco rigido virtuale esistente.<br/>                                                                                                                                                                                           |
| [**SetParentVirtualHardDisk**](setparentvirtualharddisk-msvm-imagemanagementservice.md)                         | Aggiorna l'elemento padre per i file del disco rigido virtuale foglia e figlio specificati.<br/>                                                                                                                                                     |
| [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)                       | Modifica una voce snapshot del disco rigido virtuale all'interno di un file di set di dischi rigidi virtuali. Se l'ID snapshot in questione esiste già, la voce snapshot esistente verrà sovrascritta con la nuova voce. In caso contrario, la nuova voce verrà aggiunta al file del set di dischi rigidi virtuali.<br/> |
| [**SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md)               | Imposta un file del disco rigido virtuale.<br/>                                                                                                                                                                                                   |
| [**Startservice**](msvm-imagemanagementservice-startservice.md)                                                 | avvia il servizio.<br/>                                                                                                                                                                                                              |
| [**StopService**](msvm-imagemanagementservice-stopservice.md)                                                   | arresta il servizio.<br/>                                                                                                                                                                                                               |
| [**ValidatePersistentReservationSupport**](msvm-imagemanagementservice-validatepersistentreservationsupport.md) | Convalida se un file system può supportare un disco rigido virtuale con prenotazioni persistenti abilitate.<br/>                                                                                                                            |
| [**ValidateVirtualHardDisk**](validatevirtualharddisk-msvm-imagemanagementservice.md)                           | Convalida se un'immagine del disco virtuale può essere aperta in modalità di sola lettura.<br/>                                                                                                                                                          |



 

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ImageManagementService** ha queste proprietà.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il *parametro RequestedState* del **metodo RequestStateChange.** Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Servizio di gestione immagini Hyper-V".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione OK** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata nella creazione di un'istanza di . Questa proprietà viene ereditata [**dal servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "Msvm \_ ImageManagementService".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Provides Image Management servicing for Hyper-V".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Completa la **proprietà PrimaryStatus** con dettagli aggiuntivi sullo stato. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressato** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore non ripristinabile** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Servizio gestione immagini Hyper-V".

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (abilitato).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Può anche indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (abilitato).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Integrità corrente dell'elemento. Questo attributo esprime l'integrità di questo elemento, ma non necessariamente quella dei relativi sottocomponenti. I valori possibili sono da 0 a 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento non è completamente funzionante. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e viene sempre impostata su 5.

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

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Key,** **Override** ("Name"), **MaxLen** (256)
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "vhdsvc".

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere usato per fornire maggiori dettagli rispetto al valore della **proprietà EnabledState.** Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partire** da (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattiva** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Disasserazione** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Creazione di snapshot** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In servizio** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice viene sempre impostato su 2 (OK).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato dell'elemento quando la **proprietà EnabledState** è impostata su 1 (Altro). Questa proprietà deve essere impostata su **Null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che fornisce informazioni su come è possibile raggiungere il proprietario primario del servizio, ad esempio il numero di telefono, l'indirizzo di posta elettronica e così via. Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **Null.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario primario per il servizio, se definito. Il proprietario primario è il contatto di supporto iniziale per il servizio. Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **Null.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni di alto livello sullo stato. Questa proprietà deve essere usata insieme alla proprietà **DetailedStatus** per fornire lo stato di integrità generale e dettagliato dell'elemento e dei relativi sottocomponenti. Un **valore Null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato da **EnabledState.** Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e quello corrente abilitato o disabilitato. Una particolare istanza di **EnabledLogicalElement** potrebbe non supportare **RequestedStateChange.** In questo caso, viene usato il valore 12 (Non applicabile). Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))e viene sempre impostata su 12 (non applicabile).

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il servizio è stato avviato. Questa proprietà viene ereditata [**dal servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **True.**

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, da un sistema operativo o solo su richiesta. Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **Null.**

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
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus.** Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata dal [**servizio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "Msvm \_ ComputerSystem".

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema del computer di hosting. Questa proprietà viene ereditata dal [**servizio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**Transizione a Uno stato**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui l'istanza è in fase di transizione. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **Null.**

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ImageManagementService** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Servizio \_ CIM**](cim-service.md)
</dt> <dt>

[**Servizio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> <dt>

[Archiviazione Classi](storage-classes.md)
</dt> </dl>

 

