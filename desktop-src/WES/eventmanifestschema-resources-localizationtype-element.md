---
title: Elemento resources (LocalizationType)
description: Definisce un gruppo di tabelle di stringhe che contengono le stringhe localizzate a cui si fa riferimento nel manifesto.
ms.assetid: b984894a-0ae8-49be-af93-3acdcce53ee9
keywords:
- elemento resources-EventLog
topic_type:
- apiref
api_name:
- resources
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55bdfe504da08c754c18b790e282eba6787c3ee3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300917"
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

L'elemento **Resources** viene definito dal tipo complesso [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                  | Tipo                                                                       | Descrizione                                                                             |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) | [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md) | Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.<br/> |



## <a name="attributes"></a>Attributi



| Nome    | Tipo   | Descrizione                                                                                                                                            |
|---------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| culture | string | Nome di linguaggio che identifica le impostazioni cultura delle stringhe localizzate nella tabella di stringhe. Ad esempio, "en-US" per l'inglese (Stati Uniti).<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Elemento padre**
</dt> <dt>

[**localizzazione (instrumentationManifest)**](eventmanifestschema-localization-instrumentationmanifest-element.md)
</dt> </dl>

 

 





