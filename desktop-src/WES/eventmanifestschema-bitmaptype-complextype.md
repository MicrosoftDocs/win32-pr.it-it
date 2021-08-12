---
title: Tipo complesso BitMapType
description: Definisce un elenco di mapping nome/valore tra valori di bit e valori stringa.
ms.assetid: 65dc6a48-878c-415c-872c-41dc27691b7f
keywords:
- EventLog di tipo complesso BitMapType
topic_type:
- apiref
api_name:
- BitMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c899718cd28e337bbc5d34301b7bb49446fde51f21db5b742e98dd95c5092c23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590411"
---
# <a name="bitmaptype-complex-type"></a>Tipo complesso BitMapType

Definisce un elenco di mapping nome/valore tra valori di bit e valori stringa.

``` syntax
<xs:complexType name="BitMapType">
    <xs:sequence>
        <xs:element name="map"
            type="BitMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Tipo                                                                       | Descrizione                                                            |
|-----------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Mappa**](eventmanifestschema-map-bitmaptype-element.md) | [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md) | Definisce il mapping tra un valore di bit e un valore stringa.<br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | Nome della bitmap.<br/>                                                                                                                                                                                                                                                                                  |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento ai mapping nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





