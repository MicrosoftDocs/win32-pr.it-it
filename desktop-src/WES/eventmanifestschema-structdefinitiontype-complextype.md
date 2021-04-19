---
title: Tipo complesso StructDefinitionType
description: Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento. | Tipo complesso StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Log eventi di tipo complesso StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321470"
---
# <a name="structdefinitiontype-complex-type"></a>Tipo complesso StructDefinitionType

Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento.

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
| [**dati**](eventmanifestschema-data-structdefinitiontype-element.md) | [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md) | Definisce un elemento di dati che si desidera includere nella struttura.<br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                            | Descrizione                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**CountType**](eventmanifestschema-counttype-simpletype.md)   | Numero di elementi in una matrice di strutture. Questo attributo indica che la struttura definisce una matrice di strutture. È possibile specificare il conteggio effettivo o il nome di un elemento di dati all'esterno della struttura che contiene il conteggio. <br/>                               |
| length | [**LengthType**](eventmanifestschema-lengthtype-simpletype.md) | Non disponibile.<br/> **Windows Server 2008 e Windows Vista:** Lunghezza, in byte, della struttura. Non disponibile a partire da Windows 7.<br/>                                                                                                                            |
| name   | string                                                          | Nome della struttura. È possibile usare il nome per fare riferimento all'elemento dati nel frammento XML se si specifica una sezione [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) nel modello.<br/> **Windows Vista:** Questo attributo è facoltativo.<br/> |



## <a name="remarks"></a>Commenti

I provider scrivono la struttura come un BLOB e non come singoli membri della struttura. Se la struttura C che si sta scrivendo contiene puntatori, ad esempio un puntatore di tipo LPWSTR, i dati dell'evento conterranno il valore del puntatore, non i dati dereferenziati.

È consigliabile non utilizzare le strutture ma definire gli elementi di dati per ogni membro e scriverli separatamente. Se si decide di utilizzare la struttura, la struttura deve contenere solo tipi integrali ed è necessario assicurarsi che i membri della struttura siano allineati a un limite di 8 byte. In caso contrario, è probabile che vengano restituiti errori di allineamento quando si tenta di accedere ai dati. Si consiglia di utilizzare la \# direttiva pragma pack () per forzare l'allineamento su un limite di 8 byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





