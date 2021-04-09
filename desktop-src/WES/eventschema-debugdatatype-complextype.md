---
title: Tipo complesso DebugDataType
description: Definisce i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Log eventi di tipo complesso DebugDataType
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047789"
---
# <a name="debugdatatype-complex-type"></a>Tipo complesso DebugDataType

Definisce i dati che possono essere registrati per gli eventi del preprocessore di traccia software Windows (WPP).

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
| [**FileLine**](eventschema-fileline-debugdatatype-element.md)             | string      | Il nome del file di origine e la riga all'interno del file di origine che ha registrato il messaggio di traccia.<br/>          |
| [**FlagName**](eventschema-flagname-debugdatatype-element.md)            | string      | Valore del flag passato al provider quando è stato abilitato.<br/>                                              |
| [**Funzione**](eventschema-function-debugdatatype-element.md)             | unsignedInt | Nome della funzione che ha registrato il messaggio di traccia.<br/>                                                 |
| [**LevelName**](eventschema-levelname-debugdatatype-element.md)           | string      | Valore del livello passato al provider quando è stato abilitato.<br/>                                             |
| [**Messaggio**](eventschema-message-debugdatatype-element.md)               | string      | La stringa di messaggio. Il codice XML contiene questo elemento se l'evento WPP ha specificato il campo FormattedString.<br/> |
| [**SequenceNumber**](eventschema-sequencenumber-debugdatatype-element.md) | unsignedInt | Numero di sequenza locale o globale del messaggio di traccia.<br/>                                               |
| [**Sottocomponente**](eventschema-subcomponent-debugdatatype-element.md)     | string      | Nome del sottocomponente che ha registrato il messaggio di traccia.<br/>                                             |



## <a name="remarks"></a>Commenti

Gli elementi sono inclusi solo se il provider imposta la \_ \_ variabile di ambiente% Trace Format Prefix% per includerli. Per informazioni dettagliate su questi elementi, vedere prefisso del messaggio di traccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





