---
description: Rappresenta la configurazione corrente di un commutatore Ethernet virtuale.
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbd8cd77a96301187e9b5c9f8544a23b616bf9db78af6560296660b0a3995bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681241"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a>Classe Msvm \_ VirtualEthernetSwitchSettingData

Rappresenta la configurazione corrente di un commutatore Ethernet virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
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
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualEthernetSwitchSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualEthernetSwitchSettingData** ha queste proprietà.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di pool di risorse host da associare o attualmente associati al commutatore Ethernet allo scopo di allocazioni di connessioni Ethernet tra una macchina virtuale e un commutatore Ethernet. Ogni valore deve essere conforme all'URI WBEM di produzione \_ \_ UntypedInstancePath, come definito in DSP0207. Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData.**

</dd> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale in caso di errore del software eseguito dalla macchina virtuale. Errori in questo caso indica un errore rilevabile dalla piattaforma host, ad esempio una condizione di stato di attesa non interrompibile. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale quando l'host viene arrestato. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Azione da eseguire per la macchina virtuale all'avvio dell'host. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tempo di ritardo prima dell'avvio automatico della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero che indica la sequenza relativa di attivazione della macchina virtuale all'avvio del sistema host. Un numero inferiore indica un'attivazione precedente. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**BandwidthReservationMode**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Modalità di prenotazione della larghezza di banda.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (0)


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

**Peso** (1)


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

**Assoluto** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Ethernet Switch Impostazioni".

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni sulla configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**File di configurazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso relativo e nome file di un file in cui sono archiviate le informazioni sulla configurazione della macchina virtuale. Questo percorso è relativo alla **proprietà ConfigurationDataRoot.** Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco della configurazione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione delle impostazioni. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Impostazioni attive per il commutatore Ethernet virtuale".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**ExtensionOrder**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Matrice di istanze incorporate della classe [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) che rappresentano le estensioni del commutatore associate a questa opzione, nell'ordine in cui vengono applicate.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ed è sempre impostata su "Microsoft:*GUID* \\ *DeviceSpecificData".*

</dd> <dt>

**IOVPreferred**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se la virtualizzazione I/O radice singola (SR-IOV) è preferibile o meno, se disponibile, sulla scheda sottostante.

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni di log per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il numero massimo di indirizzi MAC univoci che possono essere appresi dall'opzione per supportare l'Learning di indirizzi MAC, come definito nello standard IEEE 802.1. Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData.**

</dd> <dt>

**Note**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Note fornite dall'utente correlate alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**PacketDirectEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se usare PacketDirect, se disponibile. Il valore predefinito è **false**.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso completo di un file in cui sono archiviate le informazioni correlate al ripristino per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviate le informazioni sugli snapshot della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui vengono archiviate le informazioni relative alla sospensione della macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Percorso di una directory in cui sono archiviati i file di scambio per la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))e non viene usata.

</dd> <dt>

**TeamingEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se è necessario usare gruppo NIC. Il valore predefinito è **false**.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 e Windows Server 2016.

 

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

Specifica il tipo di macchina virtuale rappresentato dall'impostazione. Questa proprietà viene ereditata da [**CIM \_ VirtualSystemSettingData.**](/previous-versions//cc136954(v=vs.85))

</dd> <dt>

**Connessione VLAN**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elenco di identificatori VLAN a cui questa opzione può accedere. Questa proprietà viene ereditata da **CIM \_ VirtualEthernetSwitchSettingData.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

