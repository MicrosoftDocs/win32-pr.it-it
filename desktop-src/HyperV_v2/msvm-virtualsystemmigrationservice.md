---
description: Rappresenta il servizio di migrazione del sistema virtuale. Viene utilizzato per la migrazione di un sistema virtuale o per la migrazione dell'archiviazione di un sistema virtuale da una piattaforma di virtualizzazione a un'altra.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750154"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a>\_Classe MSVM VirtualSystemMigrationService

Rappresenta il servizio di migrazione del sistema virtuale. Viene utilizzato per la migrazione di un sistema virtuale o per la migrazione dell'archiviazione di un sistema virtuale da una piattaforma di virtualizzazione a un'altra.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemMigrationService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ VirtualSystemMigrationService di MSVM** dispone di questi metodi.



| Metodo                                                                                                                  | Descrizione                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddNetworkSettings**](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | Aggiunge le subnet della rete di migrazione per il servizio migrazione del sistema virtuale.<br/>                                                                                          |
| [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | Verifica le informazioni di compatibilità per la compatibilità con il sistema di hosting del computer.<br/>                                                                          |
| [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | Metodo per eseguire la migrazione di un sistema virtuale o l'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.<br/>                                              |
| [**CheckVirtualSystemIsMigratableToHost**](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un host di destinazione specificato da un nome di rete o un indirizzo IP.<br/>                                       |
| [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | Genera un BLOB opaco di dati che contiene informazioni sulla compatibilità per il sistema specificato.<br/>                                                                |
| [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | Ottiene i vettori di compatibilità per una macchina virtuale o un host.<br/> **Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.<br/> |
| [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.<br/>                                                       |
| [**MigrateVirtualSystemToSystem**](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | Consente di spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.<br/>                                                                                                |
| [**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | Modifica le subnet della rete di migrazione del servizio di migrazione del sistema virtuale.<br/>                                                                                       |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | Modifica i dati dell'impostazione per il servizio di migrazione.<br/>                                                                                                              |
| [**RemoveNetworkSettings**](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | Rimuove le subnet della rete di migrazione dal servizio di migrazione del sistema virtuale.<br/>                                                                                      |
| [**RequestStateChange**](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | Richiede una modifica dello stato<br/>                                                                                                                                           |
| [**StartService**](msvm-virtualsystemmigrationservice-startservice.md)                                                 | avvia il servizio.<br/>                                                                                                                                               |
| [**StopService**](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | arresta il servizio.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemMigrationService di MSVM** dispone di queste proprietà.

<dl> <dt>

**ActiveStorageMigrationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di migrazioni di archiviazione correnti in corso.

</dd> <dt>

**ActiveVirtualSystemMigrationCount**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di migrazioni correnti del sistema virtuale in corso.

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** . Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ VirtualSystemMigrationService".

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "servizio migrazione Hyper-V".

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento. Questa proprietà può anche indicare le transizioni tra questi stati richiesti. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato corrente dell'elemento. Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti. I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).

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

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su **null**.

</dd> <dt>

**MigrationServiceListenerIPAddressList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di indirizzi IP host che possono essere utilizzati per la migrazione del sistema virtuale.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Etichetta con cui l'oggetto è noto. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "migrationwmi".

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

Stati correnti dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 (other). Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore che fornisce informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via). Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del proprietario primario per il servizio, se ne è stato definito uno. Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni sullo stato di alto livello. Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti. Un valore **null** indica che questa proprietà non è implementata. Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ultimo stato richiesto o desiderato per l'elemento. Lo stato effettivo dell'elemento è rappresentato da **EnabledState**. Questa proprietà viene fornita per confrontare l'ultimo stato richiesto e corrente abilitato o disabilitato. Una particolare istanza di [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare il metodo **RequestStateChange** . In tal caso, viene utilizzato il valore 12 (non applicabile). Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il servizio è attualmente in esecuzione. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringhe che descrivono i vari valori della matrice **OperationalStatus** . Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e le stringhe sono sempre impostate su "OK".

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe di creazione del sistema di ambito. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del sistema di hosting del computer. Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data o ora dell'Ultima modifica dello stato abilitato dell'elemento. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica lo stato di destinazione a cui è in corso la transizione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

