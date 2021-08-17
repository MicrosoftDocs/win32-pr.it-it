---
title: Tipo semplice strTableRef
description: Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (con estensione mc).
ms.assetid: ecbcefcb-3265-4508-be7d-17a0fe3fe911
keywords:
- EventLog di tipo semplice strTableRef
topic_type:
- apiref
api_name:
- strTableRef
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97280b342015338be1cea089f8cb14121e2e51466506e89818501302c3fa891a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750917"
---
# <a name="strtableref-simple-type"></a>Tipo semplice strTableRef

Definisce una stringa che fa riferimento a una stringa di messaggio definita in una tabella di stringhe nel manifesto o in un file di messaggio (con estensione mc).

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

Il **tipo semplice strTableRef** è **un tipo xs:string** limitato dal modello seguente:

-   `(\$([Ss]tring\..*))|(\$([Mm][Cc]\..*))`

    La stringa deve essere nel formato $string. *stringid* o $mc.*symbolid*. Se la stringa ha il formato , $string. *stringid*, deve fare riferimento a una stringa nella [**sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto. Se la stringa ha il formato $mc.*symbolid*, deve fare riferimento a un simbolo definito nel file di messaggio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





