---
description: Rappresenta le impostazioni di migrazione per la migrazione di un sistema virtuale e dello spazio di archiviazione collegato a un sistema virtuale.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878698"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>\_Classe MSVM VirtualSystemMigrationSettingData

Rappresenta le impostazioni di migrazione per la migrazione di un sistema virtuale e dello spazio di archiviazione collegato a un sistema virtuale.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemMigrationSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemMigrationSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**AllowOverwriteExistingFile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Consente all'operazione di migrazione dell'archiviazione di sovrascrivere i file. vhdx esistenti.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703.

 

</dd> <dt>

**AvoidRemovingVHDs**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Non rimuovere i VHD durante la migrazione, ad esempio i dischi rigidi virtuali nell'origine nei dischi rigidi virtuali far nella destinazione in caso di errore.

> [!Note]  
> Aggiunta in Windows 10, versione 1703 e Windows Server 2016.

 

</dd> <dt>

**Larghezza di banda**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la larghezza di banda assegnata o richiesta per un'operazione di migrazione del sistema virtuale. Le unità di larghezza di banda sono specificate dalla proprietà **BandwidthUnit** . All'interno di una migrazione, un valore pari a 0 indica la larghezza di banda predefinita. In caso contrario, un valore pari a 0 indica che non sono supportate le larghezze di banda.

La **larghezza di banda** e la **priorità** possono essere utilizzate insieme. I processi di migrazione con il valore di uguale priorità più alto condividono la larghezza di banda disponibile in base alla larghezza di banda richiesta. Se non viene utilizzata tutta la larghezza di banda da questo set di processi, i processi di migrazione con la stessa priorità inferiore successiva condividono la larghezza di banda rimanente. Se la larghezza di banda rimane ancora maggiore, vengono considerati i processi di migrazione con la priorità più bassa uguale e così via.

Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le unità utilizzate dalla proprietà della **larghezza di banda** . Il valore di questa proprietà deve essere un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.

Se il valore di questa proprietà è "percent", il valore della proprietà della **larghezza di banda** deve essere compreso tra 0 e 100, con valori più elevati che indicano una larghezza di banda maggiore. Il valore 100 indica la larghezza di banda totale disponibile per l'esecuzione delle operazioni di migrazione del sistema virtuale. I valori compresi tra 1 e 100 devono essere correlati in modo lineare con l'intervallo della larghezza di banda disponibile. Ad esempio, il valore 50 deve richiedere metà della larghezza di banda disponibile.

Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**CancelIfBlackoutThresholdExceeded**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Annulla la migrazione se viene superato il tempo di soglia di blackout.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CPUCappingMagnitude**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")
</dt> </dl>

Grado di limitazione della CPU durante la migrazione.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Normale** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Bassa** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Alta** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationIPAddressList**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Questa operazione sarà **null** per la migrazione dell'archiviazione. Per la migrazione del sistema virtuale, può contenere un elenco di indirizzi IP dell'host di destinazione.

</dd> <dt>

**DestinationPlannedVirtualSystemId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Se nella destinazione della migrazione esiste una macchina virtuale pianificata, questa proprietà verrà impostata sul GUID della macchina virtuale di destinazione pianificata in cui deve essere eseguita la migrazione della macchina virtuale. Questa operazione è utile nei casi in cui un utente ha creato una macchina virtuale pianificata nella destinazione, insieme alla configurazione delle risorse e desidera che una macchina virtuale dall'origine venga migrata in questa macchina virtuale pianificata.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se comprimere il traffico di migrazione in tempo reale. **True** indica di comprimere. in caso contrario, **false**.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

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

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")
</dt> </dl>

Specifica il tipo di operazione di migrazione da eseguire. Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)


</dt> <dd>

Esegue la migrazione del sistema virtuale all'host di destinazione.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Archiviazione** (32769)


</dt> <dd>

Esegue la migrazione solo delle risorse di archiviazione del sistema virtuale.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>Gestione **temporanea** (32770)


</dt> <dd>

Utilizzando la configurazione del sistema virtuale, in viene creato un sistema virtuale pianificato nell'host di destinazione.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)


</dt> <dd>

Esegue la migrazione del sistema virtuale e della relativa archiviazione nell'host di destinazione.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)


</dt> <dd>

Esegue una verifica della capacità di migrazione delle risorse di archiviazione del sistema virtuale nell'host di destinazione.

</dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di trasporto da applicare se il valore di **TransportType** è 1 (other). Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica un'importanza della migrazione relativa, che può essere usata dal sistema di migrazione per ordinare o altrimenti assegnare la preferenza tra più richieste di migrazione in sospeso. Più basso è il valore, maggiore è la priorità. All'interno di una migrazione, un valore pari a 0 indica la priorità predefinita. In caso contrario, il valore 0 indica che le priorità non sono supportate.

Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**RemoveSourceUnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Rimuovere i dischi rigidi virtuali non gestiti di origine.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**RetainVhdCopiesOnSource**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Per una migrazione dell'archiviazione, specifica se i VHD di sola lettura nell'host di origine devono essere rimossi al termine della migrazione.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")
</dt> </dl>

Specifica il tipo di trasporto da applicare per un'operazione di migrazione del sistema virtuale. Questa proprietà viene ereditata da **CIM \_ VirtualSystemMigrationSettingData**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (32768...)


</dt> <dd></dd> </dl>

Per la migrazione in tempo reale, questa proprietà specifica il tipo di trasporto da utilizzare per il trasferimento dello stato del sistema virtuale all'host di destinazione. I valori supportati sono:

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Indica il tipo di trasporto TCP.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Indica che il tipo di trasporto per il trasferimento dello stato della macchina virtuale è SMB.

</dd> </dl>

</dd> <dt>

**UnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), **HyperVEmbeddedInstance** ("MSVM \_ MoveUnmanagedVhd")
</dt> </dl>

Matrice di istanze di [**\_ MoveUnmanagedVhd MSVM**](msvm-moveunmanagedvhd.md) incorporate contenenti informazioni sui dischi rigidi virtuali non gestiti.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

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

[**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

