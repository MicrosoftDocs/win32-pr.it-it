---
title: Tipo complesso DebugDataType
description: Definisce i dati che possono essere registrati per gli Windows del preprocessore di traccia software (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- EventLog di tipo complesso DebugDataType
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38d5ec0297fce91b28592dfb9a894a62d3558f516a01ff18c942d37cc9c93f2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124231"
---
# <a name="debugdatatype-complex-type"></a>Tipo complesso DebugDataType

Definisce i dati che possono essere registrati per gli Windows del preprocessore di traccia software (WPP).

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                    | Tipo        | Descrizione                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [**Componente**](eventschema-component-debugdatatype-element.md)           | string      | Nome del componente che ha registrato il messaggio di traccia.<br/>                                                |
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | string      | Nome del file di origine e riga all'interno del file di origine che ha registrato il messaggio di traccia.<br/>          |
| [**FlagsName**](eventschema-flagname-debugdatatype-element.md)            | string      | Valore del flag passato al provider quando è stato abilitato.<br/>                                              |
| [**Funzione**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Nome della funzione che ha registrato il messaggio di traccia.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | Valore del livello passato al provider quando è stato abilitato.<br/>                                             |
| [**Messaggio**](eventschema-message-debugdatatype-element.md)               | string      | La stringa di messaggio. Il codice XML contiene questo elemento se l'evento WPP ha specificato il campo FormattedString.<br/> |
| [**Sequencenumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Numero di sequenza locale o globale del messaggio di traccia.<br/>                                               |
| [**Sottocomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | Nome del sottocomponente che ha registrato il messaggio di traccia.<br/>                                             |



## <a name="remarks"></a>Commenti

Gli elementi vengono inclusi solo se il provider imposta la variabile di ambiente %TRACE \_ FORMAT \_ PREFIX% per includerli. Per informazioni dettagliate su questi elementi, vedere Prefisso del messaggio di traccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





