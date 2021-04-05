---
description: Rappresenta le impostazioni per l'allocazione di spazio di archiviazione virtuale.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Classe CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756620"
---
# <a name="cim_storageallocationsettingdata-class"></a>CIM \_ StorageAllocationSettingData (classe)

Rappresenta le impostazioni per l'allocazione di spazio di archiviazione virtuale.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a>Members

La classe **CIM \_ StorageAllocationSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ StorageAllocationSettingData** dispone di queste proprietà.

<dl> <dt>

**Accesso**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Accesso**")
</dt> </dl>

Supporto di lettura/scrittura dell'allocazione di archiviazione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Leggibile** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Scrivibile** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lettura/scrittura supportata** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Nome**")
</dt> </dl>

Identificatore univoco dell'extent di archiviazione dell'host.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")
</dt> </dl>

Formato del valore della proprietà **HostExtentName** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)


</dt> <dd>

Il numero di serie/fornitore/modello (SNVM) SNVM è 3 stringhe che rappresentano il nome del fornitore, il nome del prodotto nello spazio dei nomi del fornitore e il numero di serie nello spazio dei nomi del modello. Le stringhe sono delimitate da' +'. Gli spazi possono essere inclusi e sono significativi. Il numero di serie è la rappresentazione testuale del numero di serie in lettere maiuscole esadecimali. Rappresenta il fornitore e l'ID modello dai dati di richiesta SCSI; il campo fornitore deve avere una larghezza di 8 caratteri e il campo prodotto deve avere una larghezza di 16 caratteri. Ad esempio,

' Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458' ( \_ è un carattere spazio)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)


</dt> <dd>

9 = NAA come formato generico. Vedere

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Formattato come 16 o 32 caratteri esadecimali maiuscoli non separati (2 per byte binario).

Ad esempio ' 21000020372D3C73'

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI come formato generico (EUI64) vedere

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

Formato dell'identificatore del fornitore T10 come restituito dalla richiesta SCSI Vital pagina 83, identificatore tipo 1. Vedere la specifica di T10 SPC-3. ID del fornitore ASCII a 8 byte dal registro di sistema T10 seguito da un identificatore ASCII specifico del fornitore. gli spazi sono consentiti. Per i volumi non SCSI,' SNVM ' può essere la scelta più appropriata.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome dispositivo del sistema operativo** (12)


</dt> <dd>

Nome del dispositivo del sistema operativo (per LogicalDisks). Per informazioni dettagliate, vedere la descrizione del nome disco logico.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Spazio dei nomi**")
</dt> </dl>

Formato di denominazione per la proprietà **Name** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Spazio dei nomi del dispositivo del sistema operativo** (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**CIM \_ BasedOn**](cim-basedon.md).**IndirizzoIniziale**")
</dt> </dl>

Indirizzo iniziale nell'extent di archiviazione dell'host. Un valore NULL Val; UE indica che non esiste alcun mapping diretto tra l'extent di archiviazione virtuale e l'extent di archiviazione dell'host.

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punito** (" byte ")
</dt> </dl>

Dimensione, in byte, dei blocchi allocati nell'host per l'allocazione dell'archiviazione. Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco in byte. Se le dimensioni del blocco sono sconosciute o se non si applica un concetto di blocco, è necessario usare il valore "1" (sconosciuto).

</dd> <dt>

**Limite**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Quantità massima di blocchi che verranno concessi per l'allocazione delle risorse di archiviazione nell'host. La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")
</dt> </dl>

Formato della proprietà **HostExtentName** se la proprietà è impostata su "1" (other).

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")
</dt> </dl>

Stringa che descrive lo spazio dei nomi della proprietà **HostExtentName** se il valore della proprietà **HostExtentNameNamespace** è "1" (other).

</dd> <dt>

**Prenotazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Quantità di blocchi di cui è garantita la disponibilità per l'allocazione delle risorse di archiviazione nell'host. La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Proprietà NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Il numero di blocchi che l'allocazione di archiviazione presenta al consumer.

> [!Note]  
> La proprietà **VirtualQuantity** può specificare una dimensione di blocco pari a "1", anche se **VirtualResourceBlockSize** è sconosciuta.

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Unità utilizzate dalla proprietà **VirtualQuantity** . Questo valore deve essere impostato su "Count (blocco a dimensione fissa)" o "byte". Il valore predefinito "Count (blocco a dimensione fissa)" deve essere utilizzato per una dimensione fissa del blocco e deve essere utilizzato "byte" per una dimensione del blocco sconosciuta o variabile.

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punito** (" byte ")
</dt> </dl>

Dimensione, in byte, dei blocchi che formano la richiesta di allocazione dell'archiviazione. Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco. Se la dimensione del blocco è sconosciuta o se non si applica un concetto di blocco, la dimensione del blocco deve essere "1" (sconosciuta).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

