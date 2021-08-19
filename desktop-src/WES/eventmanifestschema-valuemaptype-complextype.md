---
title: Tipo complesso ValueMapType
description: Definisce un elenco di mapping nome/valore tra valori interi e valori stringa.
ms.assetid: 754578bf-d3c6-4467-af39-af56d5a11dce
keywords:
- EventLog di tipo complesso ValueMapType
topic_type:
- apiref
api_name:
- ValueMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c05452197fb71ca436fea4854346efa90f53ce6b3396e66af7e9b7ccb6615200
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120389"
---
# <a name="valuemaptype-complex-type"></a>Tipo complesso ValueMapType

Definisce un elenco di mapping nome/valore tra valori interi e valori stringa.

``` syntax
<xs:complexType name="ValueMapType">
    <xs:sequence>
        <xs:element name="map"
            type="ValueMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                     | Tipo                                                                           | Descrizione                                                                 |
|-------------------------------------------------------------|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Mappa**](eventmanifestschema-map-valuemaptype-element.md) | [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md) | Definisce il mapping tra un valore integer e un valore stringa.<br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name   | string                                                            | Nome della mappa valori. Usare il nome in un elemento dati per fare riferimento ai mapping.<br/>                                                                                                                                                                                                                     |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento ai mapping nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





