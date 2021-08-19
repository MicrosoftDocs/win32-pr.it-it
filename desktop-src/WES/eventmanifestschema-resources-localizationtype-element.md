---
title: Elemento resources (LocalizationType)
description: Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- Elemento resources EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3075b2b1741079f80c34e5acf9783b13b74b6973c1d16f2cd323890bcea5d0d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120578"
---
# <a name="resources-localizationtype-element"></a>Elemento resources (LocalizationType)

Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.

``` syntax
<xs:element name="resources">
    <xs:complexType>
        <xs:choice
            minOccurs="0"
            maxOccurs="unbounded"
        >
            <xs:element name="stringTable"
                type="StringTableType"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                namespace="##other"
             />
        </xs:choice>
        <xs:attribute name="culture"
            type="string"
            default="##fallback"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

**L'elemento** resources è definito dal [**tipo complesso LocalizationType.**](eventmanifestschema-localizationtype-complextype.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                  | Tipo                                                                       | Descrizione                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Stringtable**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.<br/> |



## <a name="attributes"></a>Attributi



| Nome    | Tipo   | Descrizione                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | string | Nome della lingua che identifica le impostazioni cultura delle stringhe localizzate nella tabella delle stringhe. Ad esempio, "en-US" per l'inglese (Stati Uniti).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**localizzazione (strumentazioneManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





