---
title: Elemento Suppress (QueryType)
description: Query XPath che identifica gli eventi da escludere dal set di risultati della query.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Eliminare l'elemento EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032011"
---
# <a name="suppress-querytype-element"></a>Elemento Suppress (QueryType)

Query XPath che identifica gli eventi da escludere dal set di risultati della query.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento Suppress** è definito dal [**tipo complesso QueryType.**](queryschema-querytype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





