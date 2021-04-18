---
description: Definisce un elenco di strutture che contengono valori dei contatori.
ms.assetid: 6f6b33ed-6440-456c-8379-61a37798c95f
title: Tipo complesso struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c36de698d1e0eb136f17034e0740851fc751d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312108"
---
# <a name="structs-complex-type"></a>Tipo complesso struct

Definisce un elenco di strutture che contengono valori dei contatori.

``` syntax
<xs:complexType name="structs">
    <xs:choice
        minOccurs="1"
        maxOccurs="unbounded"
    >
        <xs:element name="struct"
            type="man:struct"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento    | Tipo                                                           | Descrizione                                                      |
|------------|----------------------------------------------------------------|------------------------------------------------------------------|
| **struct** | [**uomo: struct**](performance-counters-struct-complex-type.md) | Nome di una struttura che contiene i valori del contatore.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




