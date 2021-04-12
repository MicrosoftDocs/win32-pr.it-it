---
title: Tipo semplice strTableRef
description: Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (. MC).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- Log eventi di tipo semplice strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95b7db446af056987e2aa25cd1483e9e53c01d39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517998"
---
# <a name="strtableref-simple-type"></a>Tipo semplice strTableRef

Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (. MC).

``` syntax
<xs:simpleType name="strTableRef">
    <xs:restriction
        base="xs:string"
    >
        <xs:pattern
            value="(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a>Modelli

Il tipo semplice **strTableRef** è **xs: String** limitato dal modello seguente:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    Il formato della stringa deve essere $string. *stringid* o $MC.*SymbolId*. Se la stringa è nel formato $string. *stringid* deve fare riferimento a una stringa nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. Se la stringa è nel formato $mc.*SymbolId*, deve fare riferimento a un simbolo definito nel file di messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





