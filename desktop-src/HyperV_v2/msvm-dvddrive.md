---
description: Rappresenta un'unità DVD all'interno di una macchina virtuale.
ms.assetid: BA813950-436F-46F1-8C1F-79C5AB1A459B
title: Classe Msvm_DVDDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive
- Msvm_DVDDrive.SetPowerState
- Msvm_DVDDrive.EnableDevice
- Msvm_DVDDrive.OnlineDevice
- Msvm_DVDDrive.QuiesceDevice
- Msvm_DVDDrive.SaveProperties
- Msvm_DVDDrive.RestoreProperties
- Msvm_DVDDrive.InstanceID
- Msvm_DVDDrive.Caption
- Msvm_DVDDrive.Description
- Msvm_DVDDrive.ElementName
- Msvm_DVDDrive.InstallDate
- Msvm_DVDDrive.Name
- Msvm_DVDDrive.OperationalStatus
- Msvm_DVDDrive.StatusDescriptions
- Msvm_DVDDrive.Status
- Msvm_DVDDrive.HealthState
- Msvm_DVDDrive.CommunicationStatus
- Msvm_DVDDrive.DetailedStatus
- Msvm_DVDDrive.OperatingStatus
- Msvm_DVDDrive.PrimaryStatus
- Msvm_DVDDrive.EnabledState
- Msvm_DVDDrive.OtherEnabledState
- Msvm_DVDDrive.RequestedState
- Msvm_DVDDrive.EnabledDefault
- Msvm_DVDDrive.TimeOfLastStateChange
- Msvm_DVDDrive.AvailableRequestedStates
- Msvm_DVDDrive.TransitioningToState
- Msvm_DVDDrive.SystemCreationClassName
- Msvm_DVDDrive.SystemName
- Msvm_DVDDrive.CreationClassName
- Msvm_DVDDrive.DeviceID
- Msvm_DVDDrive.PowerManagementSupported
- Msvm_DVDDrive.PowerManagementCapabilities
- Msvm_DVDDrive.Availability
- Msvm_DVDDrive.StatusInfo
- Msvm_DVDDrive.LastErrorCode
- Msvm_DVDDrive.ErrorDescription
- Msvm_DVDDrive.ErrorCleared
- Msvm_DVDDrive.OtherIdentifyingInfo
- Msvm_DVDDrive.PowerOnHours
- Msvm_DVDDrive.TotalPowerOnHours
- Msvm_DVDDrive.IdentifyingDescriptions
- Msvm_DVDDrive.AdditionalAvailability
- Msvm_DVDDrive.MaxQuiesceTime
- Msvm_DVDDrive.Capabilities
- Msvm_DVDDrive.CapabilityDescriptions
- Msvm_DVDDrive.ErrorMethodology
- Msvm_DVDDrive.CompressionMethod
- Msvm_DVDDrive.NumberOfMediaSupported
- Msvm_DVDDrive.MaxMediaSize
- Msvm_DVDDrive.DefaultBlockSize
- Msvm_DVDDrive.MaxBlockSize
- Msvm_DVDDrive.MinBlockSize
- Msvm_DVDDrive.NeedsCleaning
- Msvm_DVDDrive.MediaIsLocked
- Msvm_DVDDrive.Security
- Msvm_DVDDrive.LastCleaned
- Msvm_DVDDrive.MaxAccessTime
- Msvm_DVDDrive.UncompressedDataRate
- Msvm_DVDDrive.LoadTime
- Msvm_DVDDrive.UnloadTime
- Msvm_DVDDrive.MountCount
- Msvm_DVDDrive.TimeOfLastMount
- Msvm_DVDDrive.TotalMountTime
- Msvm_DVDDrive.UnitsDescription
- Msvm_DVDDrive.MaxUnitsBeforeCleaning
- Msvm_DVDDrive.UnitsUsed
- Msvm_DVDDrive.FormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e4b3c9006babb2c7e18b6aed6e85cbee47299429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884598"
---
# <a name="msvm_dvddrive-class"></a>\_Classe MSVM DVDDrive

Rappresenta un'unità DVD all'interno di una macchina virtuale. Questa unità DVD può essere un dispositivo pass-through (se un disco rigido fisico è stato collegato alla macchina virtuale) o sintetico e popolato con file multimediali ISO. Poiché le unità DVD virtuali e fisiche possono essere aggiunte e rimosse dalla macchina virtuale, sono presenti due pool di risorse associati a questa classe, uno per le unità DVD pass-through e l'altro per le unità DVD virtuali. Le unità DVD possono essere aggiunte o rimosse solo se la macchina virtuale è offline.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DVDDrive : CIM_DVDDrive
{
  string   InstanceID;
  string   Caption = "DVD Drive";
  string   Description = "Microsoft Virtual DVD Drive";
  string   ElementName = "DVD Drive";
  datetime InstallDate;
  string   Name = "DVD Drive";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_DVDDrive";
  string   DeviceID = "Microsoft:GUID\device-specific-data";
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
  uint16   AdditionalAvailability[] = 6;
  uint64   MaxQuiesceTime;
  uint32   Capabilities[] = {3, 7};
  string   CapabilityDescriptions[] = {"Random Access", "Supports Removable Media"};
  string   ErrorMethodology = "None";
  string   CompressionMethod = "Not Compressed";
  uint32   NumberOfMediaSupported = 1;
  uint64   MaxMediaSize = 9400000;
  uint64   DefaultBlockSize = 2048;
  uint64   MaxBlockSize = 2048;
  uint64   MinBlockSize = 2048;
  boolean  NeedsCleaning = False;
  boolean  MediaIsLocked = False;
  uint16   Security = 3;
  datetime LastCleaned;
  uint64   MaxAccessTime = 0;
  uint32   UncompressedDataRate;
  uint64   LoadTime = 0;
  uint64   UnloadTime = 0;
  uint64   MountCount = 0;
  datetime TimeOfLastMount;
  uint64   TotalMountTime = 0;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning = 0xffffffffffffffff;
  uint64   UnitsUsed = 0;
  uint16   FormatsSupported[] = {16, 22};
};
```

## <a name="members"></a>Members

La **classe \_ DVDDrive di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ DVDDrive di MSVM** dispone di questi metodi.



| Metodo                                                         | Descrizione                              |
|:---------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                               | Questo metodo non è supportato.<br/> |
| [**LockMedia**](msvm-dvddrive-lockmedia.md)                   | Blocca o rilascia i supporti.<br/>  |
| **OnlineDevice**                                               | Questo metodo non è supportato.<br/> |
| **QuiesceDevice**                                              | Questo metodo non è supportato.<br/> |
| [**RequestStateChange**](msvm-dvddrive-requeststatechange.md) | Richiede una modifica dello stato.<br/>      |
| [**Reset**](msvm-dvddrive-reset.md)                           | Reimposta il dispositivo virtuale.<br/>    |
| **RestoreProperties**                                          | Questo metodo non è supportato.<br/> |
| **SaveProperties**                                             | Questo metodo non è supportato.<br/> |
| **SetPowerState**                                              | Questo metodo non è supportato.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ DVDDrive di MSVM** dispone di queste proprietà.

<dl> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali disponibilità e stato aggiuntive del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).

</dd> <dt>

**Disponibilità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Disponibilità e stato primari del dispositivo. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su 6 (non applicabile).

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

**Capabilities**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Funzionalità del dispositivo di accesso multimediale. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice)ed è impostata sui valori seguenti.



| Valore                                                                             | Significato                                                                                         |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>{3, 7}</dt> </dl> |                                                                                                 |
| <dl> <dt>3</dt> </dl>      | La voce corrispondente in **CapabilityDescriptions** è "accesso casuale".<br/>            |
| <dl> <dt>7</dt> </dl>      | La voce corrispondente in **CapabilityDescriptions** è "supporta supporti rimovibili".<br/> |



 

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe in formato libero che fornisce spiegazioni dettagliate per le funzionalità di accesso ai dispositivi indicate nella matrice di proprietà delle **funzionalità** . Ogni voce di questa matrice è correlata alla voce nella matrice di proprietà **capabilities** , che si trova nello stesso indice. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

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

</dd> <dt>

**CompressionMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che indica l'algoritmo o lo strumento utilizzato per comprimere il file logico. Se lo schema di compressione è sconosciuto o non è descritto, utilizzare "Unknown". Se il file logico è compresso, ma lo schema di compressione è sconosciuto o non è descritto, utilizzare "compresso". Se il file logico non è compresso, utilizzare "non compresso". Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

"Non compresso"

Sconosciuto

Compressi

"Non compresso"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**DefaultBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del blocco predefinite, in byte, per il dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

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

Tipo di dati: **UInt16**
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

Stringa che descrive i tipi di rilevamento e correzione degli errori supportati da questo dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**FormatsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Formati CD e DVD supportati da questo dispositivo. Questa proprietà viene ereditata da [**CIM \_ DVDDrive**](/previous-versions//cc136812(v=vs.85)).

Questa matrice contiene i valori seguenti per ISO.

<dl> <dt>

{16, 22}
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD** (22)
</dt> </dl>

Questa matrice contiene i valori seguenti per il pass-through fisico.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (16)
</dt> <dt>

<span id="CD-ROM_XA"></span><span id="cd-rom_xa"></span>**CD-ROM/XA** (17)
</dt> <dt>

<span id="CD-I"></span><span id="cd-i"></span>**CD-I** (18)
</dt> <dt>

<span id="CD_Recordable"></span><span id="cd_recordable"></span><span id="CD_RECORDABLE"></span>**CD registrabile** (19)
</dt> <dt>

<span id="DVD"></span><span id="dvd"></span>**DVD** (22)
</dt> <dt>

<span id="DVD-RW_"></span><span id="dvd-rw_"></span>**DVD-RW +** (23)
</dt> <dt>

<span id="DVD-RAM"></span><span id="dvd-ram"></span>**DVD-RAM** (24)
</dt> <dt>

<span id="DVD-ROM"></span><span id="dvd-rom"></span>**DVD-ROM** (25)
</dt> <dt>

<span id="DVD-Video"></span><span id="dvd-video"></span><span id="DVD-VIDEO"></span>**DVD-video** (26)
</dt> <dt>

<span id="Divx"></span><span id="divx"></span><span id="DIVX"></span>**DivX** (27)
</dt> <dt>

<span id="CD-RW"></span><span id="cd-rw"></span>**CD-RW** (33)
</dt> <dt>

<span id="CD-DA"></span><span id="cd-da"></span>**CD-da** (34)
</dt> <dt>

<span id="CD_"></span><span id="cd_"></span>**CD +** (35)
</dt> <dt>

<span id="DVD_Recordable"></span><span id="dvd_recordable"></span><span id="DVD_RECORDABLE"></span>**DVD registrabile** (36)
</dt> <dt>

<span id="DVD-RW"></span><span id="dvd-rw"></span>**DVD-RW** (37)
</dt> <dt>

<span id="DVD-Audio"></span><span id="dvd-audio"></span><span id="DVD-AUDIO"></span>**DVD-audio** (38)
</dt> <dt>

<span id="DVD-5"></span><span id="dvd-5"></span>**DVD-5** (39)
</dt> <dt>

<span id="DVD-9"></span><span id="dvd-9"></span>**DVD-9** (40)
</dt> <dt>

<span id="DVD-10"></span><span id="dvd-10"></span>**DVD-10** (41)
</dt> <dt>

<span id="DVD-18"></span><span id="dvd-18"></span>**DVD-18** (42)
</dt> </dl>

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

**LastCleaned**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora dell'ultima pulizia del dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo codice di errore segnalato dal dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**LoadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in millisecondi, da "Load" per poter leggere o scrivere un supporto. Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per la lettura/scrittura (ovvero, il disco viene ruotato a velocità nominale). Per le unità nastro, questo è il tempo da inserire in un supporto per segnalare che è pronto per un'applicazione. Si tratta in genere dell'area BOT del nastro. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxAccessTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in millisecondi, per spostarsi dalla prima posizione sul supporto alla posizione più lontana rispetto al tempo. Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo. Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente. (La fine di un nastro può essere il punto più distante fisicamente, ma ciò non è necessariamente vero). Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxMediaSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo. I kilobyte vengono interpretati come il numero di byte moltiplicato per 1000 (non per il numero di byte moltiplicato per 1024). Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La proprietà è stata deprecata. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), ma non viene utilizzata.

</dd> <dt>

**MaxUnitsBeforeCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità massime che è possibile utilizzare prima di pulire il dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MediaIsLocked**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MinBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**MountCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Per un dispositivo che supporta supporti rimovibili, il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo. Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è uguale alla proprietà **ElementName** .

</dd> <dt>

**NeedsCleaning**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se il dispositivo di accesso multimediale deve essere pulito. in caso contrario, **false**. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**NumberOfMediaSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di supporti singoli che possono essere supportati o inseriti. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

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
</dt> </dl>

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** se la proprietà **EnabledState** è un valore qualsiasi diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Eventuali dati aggiuntivi, oltre alle informazioni sull'ID del dispositivo, che possono essere usati per identificare un dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)ed è impostata su **null**.

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

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato dalla proprietà **EnabledState** . Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato. Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** . In tal caso, viene utilizzato il valore 12 (non applicabile). Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement**.

</dd> <dt>

**Sicurezza**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Sicurezza operativa definita per il dispositivo. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

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

**TimeOfLastMount**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Per un dispositivo che supporta supporti rimovibili, la data e l'ora più recenti in cui il supporto è stato montato sul dispositivo. Per i dispositivi che accedono a supporti non rimovibili, ad esempio i dischi rigidi, questa proprietà non ha significato e non è applicabile. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**TotalMountTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Per un dispositivo che supporta supporti rimovibili, il tempo totale (in secondi) per cui sono stati montati i supporti per il trasferimento dei dati o per la pulizia del dispositivo. Per i dispositivi che accedono a supporti non rimovibili, ad esempio dischi rigidi, questa proprietà non è applicabile e deve essere impostata su 0. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

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

</dd> <dt>

**UncompressedDataRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Velocità di trasferimento dati prolungata, in KB al secondo, che il dispositivo può leggere e scrivere su un supporto. Si tratta di una velocità dati continua e non elaborata. Frequenze o tariffe massime che presuppongono che la compressione non venga segnalata in questa proprietà. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnitsDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità relative all'uso in **MaxUnitsBeforeCleaning**. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnitsUsed**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero corrente di unità utilizzate. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> <dt>

**UnloadTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo, in millisecondi, durante il quale è possibile leggere o scrivere un supporto nel relativo ' Unload '. Questa proprietà viene ereditata da [**CIM \_ MediaAccessDevice**](/windows/desktop/CIMWin32Prov/cim-mediaaccessdevice).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ DVDDrive di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_DVDDRIVE CIM**](cim-dvddrive.md)
</dt> <dt>

[**\_DVDDRIVE CIM**](/previous-versions//cc136812(v=vs.85))
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

