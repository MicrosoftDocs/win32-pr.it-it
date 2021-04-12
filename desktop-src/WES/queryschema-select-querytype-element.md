---
title: Select (QueryType)-elemento
description: Query XPath che identifica gli eventi da includere nel set di risultati della query.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Seleziona EventLog elemento
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1735f5de49853357eed1ce00b8d181edf2279ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400868"
---
# <a name="select-querytype-element"></a>Select (QueryType)-elemento

Query XPath che identifica gli eventi da includere nel set di risultati della query.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

L'elemento **Select** è definito dal tipo complesso [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>       |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





