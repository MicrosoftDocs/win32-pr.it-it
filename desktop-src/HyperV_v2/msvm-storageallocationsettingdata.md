---
description: Rappresenta le impostazioni correlate in modo specifico all'allocazione dell'archiviazione virtuale.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Msvm_StorageAllocationSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9ba95ef5f4eb0afd20b80ab97db1ab7fc9a37b11e45638188c31459f8003cbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950220"
---
# <a name="msvm_storageallocationsettingdata-class"></a>Classe Msvm \_ StorageAllocationSettingData

Rappresenta le impostazioni correlate in modo specifico all'allocazione dell'archiviazione virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ StorageAllocationSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ StorageAllocationSettingData** ha queste proprietà.

<dl> <dt>

**Accesso**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'accesso all'archiviazione. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Leggibile** (1)
</dt> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Scrivibile** (2)
</dt> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Lettura/scrittura supportata** (3)
</dt> </dl>

</dd> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive l'indirizzo di questa risorsa nel contesto dell'elemento padre. Le **proprietà Parent** **e AddressOnParent** vengono usate per descrivere la relazione tra controller e l'ordinamento dei dispositivi in un controller. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità di allocazione usate dalle **proprietà Reservation** **e Limit.** Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà allocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la risorsa verrà deallocata automaticamente. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Modalità di memorizzazione nella cache**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se e come usare la memorizzazione nella cache dei file in memoria per questo disco rigido virtuale. I criteri predefiniti vengono impostati nel **campo DefaultVirtualHardDiskCachingMode** della [**classe Msvm \_ VirtualSystemManagementServiceSettingData.**](msvm-virtualsystemmanagementservicesettingdata.md)

> [!Note]  
> Aggiunta in Windows 10.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (2)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Nessuna Caching** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Cache Sharable Parents** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** (64)
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hard Disk Image Default Impostazioni".

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dispositivo a cui è connessa la risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Visibilità del consumer sulla risorsa allocata. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Pass-through** (2)
</dt> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualizzato** (3)
</dt> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**Non rappresentato** (4)
</dt> </dl>

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Descrive le impostazioni predefinite per le risorse dell'immagine del disco rigido".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco per l'extent host. L'extent host identificato viene usato per l'allocazione delle risorse di archiviazione. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il formato usato per la **proprietà HostExtentName.** Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)
</dt> <dt>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)
</dt> <dt>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)
</dt> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome del dispositivo del sistema operativo** (12)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DmTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se l'extent host è un volume SCSI, l'origine preferita per i nomi di volume SCSI è scsi VPD pagina 83 risposte. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)
</dt> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)
</dt> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)
</dt> <dt>

<span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)
</dt> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Spazio dei nomi del dispositivo del sistema** operativo (8)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DmTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica l'indirizzo iniziale nell'extent di archiviazione host, identificato dalla proprietà **HostExtentName,** usato per l'allocazione dell'extent di archiviazione virtuale. Un **valore Null** indica che non esiste alcun mapping diretto dell'extent di archiviazione virtuale all'extent di archiviazione host a cui si fa riferimento. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**Risorsa host**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

È possibile assegnare una sola risorsa host a ogni dispositivo nella macchina virtuale, quindi è possibile impostare solo il primo elemento di questa matrice. Per i dispositivi che supportano questa funzionalità, impostare il primo elemento della matrice **HostResource** in modo che contenga un riferimento alla risorsa host sottostante da assegnare. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Questa proprietà è di sola lettura. Se tuttavia la proprietà **ResourceType** è 31 (disco logico) e la proprietà **ResourceSubType** è "Microsoft:Hyper-V:Disco rigido virtuale", "Microsoft:Hyper-V:Disco CD/DVD virtuale" o "Microsoft:Hyper-V:Disco floppy virtuale", la proprietà **HostResource** può essere modificata usando il metodo [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della classe [**\_ Msvm VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni, in byte, dei blocchi allocati nell'host come risultato di questa richiesta di allocazione delle risorse di archiviazione o di allocazione delle risorse di archiviazione. Se la dimensione del blocco è variabile, verranno specificate le dimensioni massime del blocco, in byte. Se la dimensione del blocco è sconosciuta o se non si applica un concetto di blocco, verrà usato il valore 1. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**IgnoreFlushes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se impostato su true, Hyper-V ignorerà lo scaricamento write-back per la macchina virtuale specifica. Se impostato su false, Hyper-V continuerà a eseguire il write back sul disco a ogni scaricamento. L'impostazione predefinita è false.

**Windows 10:** Questo valore non è supportato fino a Windows 10.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IOPSAllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le unità di allocazione usate dalle **proprietà IOPSLimit** **e IOPSReservation.** Questa proprietà ha sempre il valore :

"count(normalized I/O) /second"

La velocità effettiva viene misurata in operazioni di I/O normalizzate al secondo (IOPS) anziché in operazioni di I/O al secondo non elaborate. Quando si usano operazioni di I/O normalizzate, ogni richiesta di I/O viene valutata come 1 I/O normalizzato se le dimensioni della richiesta sono minori o uguali a una dimensione di base predefinita (8 KB). Le richieste con dimensioni maggiori delle dimensioni di base vengono rappresentate come N operazioni di I/O, dove N è il valore arrotondato per esere della dimensione della richiesta diviso per la dimensione di base. Ad esempio, se le dimensioni di base sono di 8 KB, una richiesta di 16 KB viene conteggiata come 2 operazioni di I/O normalizzate, una richiesta di 32 KB come 4 operazioni di I/O normalizzate e così via.

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**IOPSLimit**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)
</dt> </dl>

Numero massimo di operazioni di I/O al secondo (IOPS) che verranno eseguite per questo extent di archiviazione virtuale. Se il valore non è definito o è zero, non esiste alcun limite al numero di operazioni di I/O al secondo che il dispositivo può rilasciare.

> [!Note]  
> È possibile usare il [**metodo ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per modificare il valore di questa proprietà. Questa proprietà è significativa solo per le **istanze di Msvm \_ StorageAllocationSettingData** che richiedono allocazioni di risorse per le macchine virtuali. Viene ignorato quando si allocano risorse a un pool figlio.

 

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**IOPSReservation**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1000000000)
</dt> </dl>

Numero minimo di operazioni di I/O al secondo (IOPS) che verranno eseguite per questo extent di archiviazione virtuale.

Se sono **definiti sia IOPSLimit** che **IOPSReservation,** il valore di **IOPSLimit** deve essere maggiore o uguale al valore di **IOPSReservation**.

> [!Note]  
> È possibile usare il [**metodo ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) della [**classe Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) per modificare il valore di questa proprietà. Questa proprietà è significativa solo per le **istanze di Msvm \_ StorageAllocationSettingData** che richiedono allocazioni di risorse per le macchine virtuali. Viene ignorato quando si allocano risorse a un pool figlio.

 

**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di blocchi che verranno concessi per l'allocazione delle risorse di archiviazione nell'host. La dimensione del blocco viene specificata dalla **proprietà HostResourceBlockSize.** In genere il valore di questa proprietà riflette una dimensione massima per l'extent host allocato corrispondente alla dimensione dell'extent di archiviazione virtuale presentata al consumer. Un valore minore di indica una situazione in cui è previsto un extent di archiviazione virtuale popolato in modo sparse, in cui il fill rate è limitato dal valore della proprietà Limit. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il mapping di questa risorsa alle risorse sottostanti. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il formato della proprietà **HostExtentName** se la **proprietà HostExtentNameFormat** è 1 (Altro). Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive lo spazio dei nomi della **proprietà HostExtentName** se la **proprietà HostExtentNameNamespace** contiene 1 (Altro). Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e [**ResourceType**](msvm-processorsettingdata.md) ha il valore 1(Other). Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre della risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**PersistentReservationsSupported**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il disco rigido virtuale supporta le prenotazioni permanenti SCSI-3.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del pool di risorse da cui è stata allocata la risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Override** ("Reservation"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData.HostResourceBlockSize")
</dt> </dl>

Numero di blocchi che sono garantiti per l'allocazione delle risorse di archiviazione nell'host. Le dimensioni del blocco vengono specificate dalla **proprietà HostResourceBlockSize.** Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risorsa rappresentato da questa impostazione di allocazione. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processore** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controller IDE** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI parallelo** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di** rete (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot di I/O** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo di I/O** (13)
</dt> <dt>

<span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unità dischetto** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unità disco** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unità nastro** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Archiviazione extent** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro Archiviazione dispositivo** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (22)
</dt> <dt>

<span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafico** (24)
</dt> <dt>

<span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Porta commutatore Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco logico** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Archiviazione volume** (32)
</dt> <dt>

<span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Connessione Ethernet** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768 65535)
</dt> </dl>

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID che rappresenta lo snapshot all'interno del file del set di dischi rigidi virtuali da collegare.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**StorageQoSPolicyID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'identificatore univoco del Archiviazione criteri QoS da applicare a questo extent di archiviazione virtuale.

> [!Note]  
> Aggiunta in Windows 10.

 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di blocchi presentati al consumer. Le dimensioni del blocco vengono specificate dalla **proprietà VirtualResourceBlockSize.** Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica le unità usate dalla **proprietà VirtualQuantity.** Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**



| Valore                                                                                                | Significato                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>"count(fixed size block)"</dt> </dl> | La dimensione fissa del blocco è contenuta nella **proprietà VirtualResourceBlockSize.**<br/> |
| <dl> <dt>"byte"</dt> </dl>                    | La **proprietà VirtualQuantity** viene misurata in byte.<br/>                          |



 

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni, in byte, dei blocchi presentati al consumer come risultato di questa richiesta di allocazione delle risorse di archiviazione o di allocazione delle risorse di archiviazione. Se la dimensione del blocco è variabile, verrà specificata la dimensione massima in byte del blocco. Se la dimensione del blocco è sconosciuta o se non si applica un concetto di blocco, verrà usato il valore 1. Questa proprietà viene ereditata da **CIM \_ StorageAllocationSettingData.**

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Weight"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)
</dt> </dl>

Specifica una priorità relativa per questa allocazione in relazione ad altre allocazioni dallo stesso pool di risorse. Questa proprietà non ha unità di misura ed è rilevante solo se confrontata con altre allocazioni in vying per le stesse risorse host. Questa proprietà viene ereditata da [**CIM \_ ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Intervallo: 1 10000

</dd> <dt>

**WriteHardeningMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il metodo di protezione avanzata della scrittura supportato dal disco.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10 versione 1703.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (0)


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

**WriteCacheEnabled** (1)


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

**WriteCacheandFUAEnabled** (2)


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

**WriteCacheDisabled** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

