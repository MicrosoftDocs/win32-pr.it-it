---
title: Tipo complesso FilterType
description: Definisce un filtro dati utilizzato da una sessione per filtrare gli eventi in base ai dati degli eventi.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- EventLog di tipo complesso FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 079f31376967e2fcb719731a8d7f70065bd5210313c02b9ecaa0ee5fe8164ad0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117936906"
---
# <a name="filtertype-complex-type"></a>Tipo complesso FilterType

Definisce un filtro dati utilizzato da una sessione per filtrare gli eventi in base ai dati degli eventi.

``` syntax
<xs:complexType name="FilterType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="version"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="tid"
                type="token"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                                                                                                                                                                                                                      |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Descrizione localizzata per il filtro. La stringa del messaggio fa riferimento a una stringa localizzata nella [**sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto.<br/>                                   |
| name    | **QName**                                                         | Nome che identifica il filtro.<br/>                                                                                                                                                                                                    |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al filtro nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il filtro nel file di intestazione generato dal compilatore.<br/> |
| tid     | token                                                             | Identificatore di modello che descrive i dati di filtro che la sessione passa al provider quando abilita il provider.<br/>                                                                                                            |
| Valore   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore intero che identifica in modo univoco il filtro all'interno dell'elenco di filtri definiti.<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore intero che identifica questa versione del filtro. Se non viene specificato, il valore è zero.<br/>                                                                                                                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





