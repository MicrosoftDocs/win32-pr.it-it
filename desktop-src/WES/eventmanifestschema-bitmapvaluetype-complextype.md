---
title: Tipo complesso BitMapValueType
description: Definisce il mapping tra un valore di bit e un valore stringa. | Tipo complesso BitMapValueType
ms.assetid: 2ef9ed89-83cf-4c47-9c6c-64459b6d7198
keywords:
- EventLog di tipo complesso BitMapValueType
topic_type:
- apiref
api_name:
- BitMapValueType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6d5f1b254ad4a833c1523f5a139224fc1fed508d4530a056ffdb0f111db5769e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032351"
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
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Valore stringa localizzato a cui viene eseguito il mapping del valore di bit. La stringa del messaggio fa riferimento a una stringa localizzata nella [**sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                  |
| simbolo  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento alla mappa nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore   | [**HexInt32Type**](eventmanifestschema-hex32type-simpletype.md)  | Valore di bit di cui eseguire il mapping al valore stringa. È necessario specificare un numero esadecimale con un singolo bit impostato.<br/>                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

Mappe un valore esadecimale (il numero deve essere preceduto da 0x) con un bit singolo impostato su un nome.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





