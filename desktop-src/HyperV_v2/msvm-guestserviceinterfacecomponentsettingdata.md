---
description: Rappresenta lo stato configurato del componente dell'interfaccia del servizio Guest.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Classe Msvm_GuestServiceInterfaceComponentSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306042"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>\_Classe MSVM GuestServiceInterfaceComponentSettingData

Rappresenta lo stato configurato del componente dell'interfaccia del servizio Guest. Questa classe deriva dalla classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a>Members

La **classe \_ GuestServiceInterfaceComponentSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ GuestServiceInterfaceComponentSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo della risorsa. Ad esempio, l'indirizzo MAC di una porta Ethernet.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica le unità di allocazione utilizzate dalle proprietà di prenotazione e limite. Ad esempio, quando ResourceType = Processor, AllocationUnits può essere impostato su MHz. Quando ResourceType = Memory, AllocationUnits può essere impostato su MB

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica se la risorsa verrà allocata automaticamente. Se, ad esempio, è impostato su true, quando il computer virtuale che lo utilizza è acceso, questa risorsa verrebbe allocata. Il valore false indica che la risorsa deve essere allocata in modo esplicito. Ad esempio, l'impostazione può rappresentare supporti rimovibili (ovvero CDROM o floppy) in cui, in fase di accensione, il supporto non è presente. Per allocare la risorsa è necessaria un'operazione esplicita.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica se la risorsa verrà deallocata automaticamente. Se, ad esempio, si imposta su true, quando il computer virtuale che lo utilizza è spento, questa risorsa verrebbe deallocata. Se impostata su false, la risorsa rimane allocata e deve essere deallocata in modo esplicito.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento a cui è connessa questa risorsa. Ad esempio, una rete denominata o una porta di commutazione.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive la visibilità dei consumer per la risorsa allocata.



| Valore                                                                                                                                                                                                                                                                  | Significato                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Sconosciuto**</dt> <dt>0</dt> </dl>                                            | Sconosciuto.<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Passato-a**</dt> <dt>2</dt> </dl>                | La risorsa host o sottostante viene utilizzata e passata al consumer, possibilmente utilizzando il partizionamento. Nella proprietà DeviceID deve essere presente almeno un elemento.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Virtualizzato**</dt> <dt>3</dt> </dl>                            | La risorsa è virtualizzata e non può essere mappata direttamente a una risorsa host o sottostante. Alcune implementazioni possono supportare un'assegnazione specifica per le risorse virtualizzate, nel qual caso le risorse host vengono esposte tramite la proprietà DeviceID.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**Non rappresentato**</dt> <dt>4</dt> </dl>            | Una rappresentazione della risorsa non esiste nel contesto del consumer di risorse.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF riservato**</dt> <dt>..</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> 32767 <dt>**riservato al fornitore**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**DefaultEnabledStatePolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Per impostazione predefinita, gli stati abilitati e disabilitati dei servizi di comunicazione Guest.

Si tratta di una proprietà di sola lettura, ma è possibile modificarla utilizzando il metodo [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) della [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> Aggiunto in Windows 10.

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per questa istanza di SettingData. Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query. Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stati abilitati e disabilitati di un elemento.

Si tratta di una proprietà di sola lettura, ma può essere modificata usando il metodo [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (o [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 o versione successiva) della classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

I valori validi sono:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Abilitato** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Disabilitato** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà espone un'assegnazione specifica a un host o a risorse sottostanti. Le istanze incorporate devono contenere solo proprietà chiave e essere considerate come percorsi di oggetti. Se la risorsa virtuale può essere pianificata su una serie di risorse sottostanti, questa proprietà deve rimanere **null**. In tal caso, è possibile usare le associazioni DeviceAllocatedFromPool o ResourceAllocationFromPool per determinare il pool di risorse host in cui la risorsa virtuale può essere pianificata. Se viene utilizzata un'assegnazione specifica, tutte le risorse sottostanti utilizzate da questa risorsa virtuale verranno elencate in questa matrice. In genere, la matrice conterrà un elemento, tuttavia per le allocazioni di aggregazione, ad esempio più processori, è possibile specificare più risorse host.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

All'interno dell'ambito dello spazio dei nomi di creazione di istanze, InstanceID indica in modo opaco e univoco un'istanza di questa classe. Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID*:*localizzato* in cui *OrgID* e *LocalId* sono separati da due punti (:) e dove *OrgID* deve includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità di business da un'autorità globale riconosciuta. (Questo requisito è simile a *SchemaName* \_ Struttura *ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:). Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono comparire tra *OrgID* e *localizzato*. *Localizzato* viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti. Se non viene utilizzato l'algoritmo "preferito" precedente, l'entità di definizione deve garantire che l'ID istanza risultante non venga riutilizzato in tutte le InstanceID generate da questo o da altri provider per lo spazio dei nomi di questa istanza. Per le istanze definite da DMTF, è necessario usare l'algoritmo "preferenziale" con *OrgID* impostato su CIM.

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica il limite superiore o la quantità massima di risorse che verrà concessa per l'allocazione. Ad esempio, un sistema che supporta il paging della memoria può supportare l'impostazione del limite di un'allocazione di memoria inferiore a quella del VirtualQuantity, forzando così il paging per l'allocazione.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il modo in cui viene eseguito il mapping della risorsa alle risorse sottostanti. Se la matrice HostResource contiene voci, questa proprietà riflette il modo in cui viene eseguito il mapping della risorsa a tali risorse specifiche.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Non supportato** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicato** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Affinità Soft** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Affinità hardware** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive il tipo di risorsa quando non è disponibile un valore ben definito e ResourceType ha il valore "other".

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento padre della risorsa. Ad esempio, un controller per l'allocazione corrente.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica il ResourcePool da cui la risorsa è attualmente allocata o il ResourcePool da cui verrà allocata la risorsa quando si verifica l'allocazione.

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica la quantità di risorse garantita per l'allocazione. Nel sistema che supporta l'overcommit delle risorse, questo valore viene in genere usato per il controllo dell'ammissione per impedire che un'allocazione venga accettata, impedendo così l'esaurimento delle risorse.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che descrive un sottotipo specifico dell'implementazione per questa risorsa. Ad esempio, può essere usato per distinguere modelli diversi dello stesso tipo di risorsa.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di risorsa rappresentata da questa impostazione di allocazione.

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

<span id="FC_HBA"></span><span id="fc_hba"></span>**HBA FC** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Scheda Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Altra scheda di rete** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Slot I/O** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo I/O** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unità floppy** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unità CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unità DVD** (16)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Porta seriale** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Porta parallela** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controller USB** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controller grafica** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extent di archiviazione** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Nastro** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Altro dispositivo di archiviazione** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controller FireWire** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unità partizionabile** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unità partizionabile di base** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Alimentatore** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo di raffreddamento** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica la quantità di risorse presentate al consumer. Ad esempio, quando ResourceType = Processor, questa proprietà riflette il numero di processori discreti presentati al sistema del computer virtuale. Quando ResourceType = Memory, questa proprietà può riflettere il numero di MB restituiti al sistema del computer virtuale.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà specifica una priorità relativa per l'allocazione in relazione alle altre allocazioni dello stesso ResourcePool. Questa proprietà non dispone di unità di misura ed è pertinente solo se confrontata con altre allocazioni che competono per le stesse risorse host.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

