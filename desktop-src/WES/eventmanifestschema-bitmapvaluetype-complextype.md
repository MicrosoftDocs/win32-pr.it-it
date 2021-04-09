---
title: Tipo complesso BitMapValueType
description: Definisce il mapping tra un valore di bit e un valore stringa. | Tipo complesso BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- Log eventi di tipo complesso BitMapValueType
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f2da7e0576579b0f0c509de7a8318e46e5dd955d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969150"
---
# <a name="bitmapvaluetype-complex-type"></a>Tipo complesso BitMapValueType

Definisce il mapping tra un valore di bit e un valore stringa.

``` syntax
<xs:complexType name="BitMapValueType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="HexInt32Type"
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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valore stringa localizzato a cui viene eseguito il mapping del valore di bit. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                  |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento alla mappa nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Valore di bit di cui eseguire il mapping al valore stringa. È necessario specificare un numero esadecimale con un singolo set di bit.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Esegue il mapping di un valore esadecimale (il numero deve essere preceduto da 0x) con un solo bit impostato su un nome.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





