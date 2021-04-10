---
title: Elemento di eliminazione (QueryType)
description: Query XPath che identifica gli eventi da escludere dal set di risultati della query.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Non visualizzare l'elemento EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121538"
---
# <a name="suppress-querytype-element"></a>Elemento di eliminazione (QueryType)

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

L'elemento di **eliminazione** viene definito dal tipo complesso [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





