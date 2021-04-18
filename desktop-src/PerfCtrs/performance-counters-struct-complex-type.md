---
description: Definisce una struttura che contiene uno o più valori dei contatori.
ms.assetid: 3085d490-4ac1-491c-bce0-8af46b16fab9
title: Tipo complesso struct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc59103a1a98b0baf1559ead159221ea42288936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312111"
---
# <a name="struct-complex-type"></a>Tipo complesso struct

Definisce una struttura che contiene uno o più valori dei contatori.

``` syntax
<xs:complexType name="struct">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="man:CSymbolType"
                use="required"
             />
            <xs:attribute name="type"
                type="man:CSymbolType"
                use="required"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome | Tipo                                                                    | Descrizione                                                                                                                                      |
|------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| name | [**uomo: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nome della struttura.<br/>                                                                                                            |
| tipo | [**uomo: CSymbolType**](performance-counters-csymboltype-simple-type.md) | Nome simbolico che identifica la struttura. Lo strumento [CTRPP](ctrpp.md) crea una variabile struct con questo nome che è possibile usare.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 




