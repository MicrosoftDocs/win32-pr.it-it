---
title: Tipo complesso StructDefinitionType
description: Definisce una struttura che include uno o più elementi di dati da includere con l'evento . | Tipo complesso StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- EventLog di tipo complesso StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 035b8abe5440ffb80b902e1f4b1564b2fb80b77ee34b20f4f068d298b251478a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124251"
---
# <a name="structdefinitiontype-complex-type"></a>Tipo complesso StructDefinitionType

Definisce una struttura che include uno o più elementi di dati da includere con l'evento .

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                                             | Descrizione                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**Dati**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Definisce un elemento di dati da includere nella struttura .<br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | Numero di elementi in una matrice di strutture . Questo attributo indica che la struttura sta definendo una matrice di strutture. È possibile specificare il conteggio effettivo o il nome di un elemento dati all'esterno della struttura che contiene il conteggio. <br/>                               |
| length | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | Non disponibile.<br/> **Windows Server 2008 e Windows Vista:** Lunghezza, in byte, di questa struttura . Non disponibile a partire da Windows 7.<br/>                                                                                                                            |
| name   | string                                                          | Nome della struttura. È possibile usare il nome per fare riferimento all'elemento di dati nel frammento XML se si specifica una [**sezione UserData**](eventmanifestschema-userdata-templateitemtype-element.md) nel modello.<br/> **Windows Vista:** Questo attributo è facoltativo.<br/> |



## <a name="remarks"></a>Commenti

I provider scrivono la struttura come BLOB e non come singoli membri della struttura. Se la struttura C che si sta scrivendo contiene puntatori (ad esempio, un puntatore di tipo LPWSTR), i dati dell'evento conterranno il valore del puntatore, non i dati dereferenziati.

Non è consigliabile usare le strutture, ma definire gli elementi di dati per ogni membro e scriverli separatamente. Se si decide di usare la struttura , la struttura deve contenere solo tipi integrali ed è necessario assicurarsi che i membri della struttura siano allineati a un limite di 8 byte. In caso contrario, è probabile che si ricevano errori di allineamento quando si tenta di accedere ai dati. Prendere in considerazione \# l'uso della direttiva pragma pack() per forzare l'allineamento su un limite di 8 byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





