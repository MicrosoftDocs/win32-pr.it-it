---
title: Tipo complesso FilterType
description: Definisce un filtro di dati utilizzato da una sessione per filtrare gli eventi in base ai dati dell'evento.
ms.assetid: f2874b3f-cf3a-4dd9-b914-6adaac33cf7b
keywords:
- Log eventi di tipo complesso FilterType
topic_type:
- apiref
api_name:
- FilterType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ef3d80b8cb5347c1adf0e2b21a745e4d4f5fae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479276"
---
# <a name="filtertype-complex-type"></a>Tipo complesso FilterType

Definisce un filtro di dati utilizzato da una sessione per filtrare gli eventi in base ai dati dell'evento.

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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Descrizione localizzata per il filtro. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.<br/>                                   |
| name    | **QName**                                                         | Nome che identifica il filtro.<br/>                                                                                                                                                                                                    |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al filtro nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il filtro nel file di intestazione generato dal compilatore.<br/> |
| tid     | token                                                             | Identificatore di modello che descrive i dati del filtro che la sessione passa al provider quando Abilita il provider.<br/>                                                                                                            |
| Valore   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore intero che identifica in modo univoco il filtro all'interno dell'elenco di filtri definiti.<br/>                                                                                                                                      |
| version | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore intero che identifica la versione del filtro. Se non è specificato, il valore è zero.<br/>                                                                                                                                     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





