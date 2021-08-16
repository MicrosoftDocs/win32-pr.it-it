---
title: Tipo complesso PatternMapType
description: Non usato. Definisce un mapping tra due espressioni regolari. Un'espressione viene usata per trovare una stringa corrispondente nella stringa del messaggio e l'altra viene usata per modificare la stringa prima che il servizio la inserisca nuovamente nella stringa del messaggio.
ms.assetid: 184b6aeb-a554-4a92-b19e-1849c711d33b
keywords:
- EventLog di tipo complesso PatternMapType
topic_type:
- apiref
api_name:
- PatternMapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d4ba0c404220023a124c082ea448cbb7bdcab192b611bf35a2afc90df82e9e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136193"
---
# <a name="patternmaptype-complex-type"></a>Tipo complesso PatternMapType

Non usato. Definisce un mapping tra due espressioni regolari. Un'espressione viene usata per trovare una stringa corrispondente nella stringa del messaggio e l'altra viene usata per modificare la stringa prima che il servizio la inserisca nuovamente nella stringa del messaggio.

``` syntax
<xs:complexType name="PatternMapType">
    <xs:sequence>
        <xs:element name="map"
            type="PatternMapValueType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="format"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                       | Tipo                                                                               | Descrizione                                                                                                   |
|---------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Mappa**](eventmanifestschema-map-patternmaptype-element.md) | [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md) | Definisce le espressioni regolari usate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.<br/> |



## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| format | anyURI                                                            | Motore delle espressioni regolari da usare.<br/>                                                                                                                                                                                                                                                                    |
| name   | **QName**                                                         | Nome della mappa dei criteri. Usare il nome in un elemento dati per fare riferimento ai mapping.<br/>                                                                                                                                                                                                                   |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da usare per fare riferimento ai mapping nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per la mappa nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





