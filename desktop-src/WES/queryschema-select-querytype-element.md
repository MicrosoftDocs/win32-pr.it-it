---
title: Elemento Select (QueryType)
description: Query XPath che identifica gli eventi da includere nel set di risultati della query.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Selezionare l'elemento EventLog
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587404"
---
# <a name="select-querytype-element"></a>Elemento Select (QueryType)

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

**L'elemento** Select è definito dal [**tipo complesso QueryType.**](queryschema-querytype-complextype.md)

## <a name="attributes"></a>Attributi



| Nome | Tipo   | Descrizione                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Percorso | anyURI | Nome del canale o percorso del file di log che contiene gli eventi.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>       |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**Query (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





