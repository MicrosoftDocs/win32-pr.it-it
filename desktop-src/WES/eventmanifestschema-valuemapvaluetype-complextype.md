---
title: Tipo complesso ValueMapValueType
description: Definisce il mapping tra un valore integer e un valore stringa. | Tipo complesso ValueMapValueType
ms.assetid: 8fd3b3ed-5b62-4e2e-b6f9-8e1bf6d83a35
keywords:
- Log eventi di tipo complesso ValueMapValueType
topic_type:
- apiref
api_name:
- ValueMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 197eb7e402068f541dc5a385eca14a631de2488c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104401856"
---
# <a name="valuemapvaluetype-complex-type"></a>Tipo complesso ValueMapValueType

Definisce il mapping tra un valore integer e un valore stringa.

``` syntax
<xs:complexType name="ValueMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome    | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                    |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valore stringa localizzato a cui viene eseguito il mapping del valore intero. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                              |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento alla mappa nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Valore intero di cui eseguire il mapping al valore stringa.<br/>                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





