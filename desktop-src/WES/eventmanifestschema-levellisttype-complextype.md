---
title: Tipo complesso LevelListType
description: Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- EventLog di tipo complesso LevelListType
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8087913cacac67f0c7487b5eb41f404ebdc205765c693bdfda9f86995a809493
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124301"
---
# <a name="levellisttype-complex-type"></a>Tipo complesso LevelListType

Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                          | Tipo                                                           | Descrizione                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**Livello**](eventmanifestschema-level-levellisttype-element.md) | [**LevelType**](eventmanifestschema-leveltype-complextype.md) | Definisce un valore di gravità che determina il livello di dettaglio degli eventi durante la registrazione.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





