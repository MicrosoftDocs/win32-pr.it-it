---
title: Tipo complesso EventType
description: Definisce il nodo radice dello schema Event.
ms.assetid: 1ff9299b-71ee-4bb3-8a9a-fb9880dbf577
keywords:
- EventType di tipo complesso EventLog
topic_type:
- apiref
api_name:
- EventType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da5948021c4a2db50776544c38adfa4ddc6e8ce5bcc1285c879ef528dec759e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957901"
---
# <a name="eventtype-complex-type"></a>Tipo complesso EventType

Definisce il nodo radice dello schema Event.

``` syntax
<xs:complexType name="EventType">
    <xs:sequence>
        <xs:element name="System"
            type="SystemPropertiesType"
         />
        <xs:choice>
            <xs:element name="EventData"
                type="EventDataType"
                minOccurs="0"
             />
            <xs:element name="UserData"
                type="UserDataType"
                minOccurs="0"
             />
            <xs:element name="DebugData"
                type="DebugDataType"
                minOccurs="0"
             />
            <xs:element name="BinaryEventData"
                type="hexBinary"
                minOccurs="0"
             />
            <xs:element name="ProcessingErrorData"
                type="ProcessingErrorDataType"
                minOccurs="0"
             />
        </xs:choice>
        <xs:element name="RenderingInfo"
            type="RenderingInfoType"
            minOccurs="0"
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



| Elemento                                                                          | Tipo                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData**](eventschema-binaryeventdata-eventtype-element.md)         | Hexbinary                                                                          | Contiene i dati dell'evento come BLOB binario. Il rendering dei dati dell'evento viene eseguito come BLOB binario se la funzione di rendering non riesce a trovare i metadati usati per decodificare l'evento.<br/>                                                                                                                                                            |
| [**DebugData**](eventschema-debugdata-eventtype-element.md)                     | [**DebugDataType**](eventschema-debugdatatype-complextype.md)                     | Contiene i dati che possono essere registrati per Windows eventi WPP (Software Trace Preprocessor).<br/>                                                                                                                                                                                                                                    |
| [**EventData**](eventschema-eventdata-eventtype-element.md)                     | [**EventDataType**](eventschema-eventdatatype-complextype.md)                     | Contiene i dati dell'evento. L'ordine degli elementi di dati nel modello determina il layout dei dati dell'evento.<br/>                                                                                                                                                                                                                 |
| [**ProcessingErrorData**](eventschema-processingerrordata-eventtype-element.md) | [**ProcessingErrorDataType**](eventschema-processingerrordatatype-complextype.md) | Contiene i dettagli dell'errore che si è verificato durante il tentativo di eseguire il rendering dell'evento. Ciò può verificarsi se i dati dell'evento non corrispondono alla definizione dei dati dell'evento nel manifesto. I dati dell'evento vengono inclusi come BLOB binario.<br/>                                                                                                         |
| [**RenderingInfo**](eventschema-renderinginfo-eventtype-element.md)             | [**RenderingInfoType**](eventschema-renderingtype-complextype.md)                 | Contiene le stringhe di messaggio di cui è stato eseguito il rendering per l'evento (include la stringa di messaggio dell'evento e le stringhe di messaggio per qualsiasi proprietà dell'evento, ad esempio livello, attività e codice operativo). Questa sezione sarà contenuta solo [Windows eventi](/windows/desktop/WEC/windows-event-collector) raccolti tramite il servizio Agente di raccolta eventi.<br/> |
| [**Sistema**](eventschema-system-eventtype-element.md)                           | [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md)       | Contiene informazioni che identificano il provider e come è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e informazioni di sistema, ad esempio gli ID di processo e thread.<br/>                                                                                                                                   |
| [**UserData**](eventschema-userdata-eventtype-element.md)                       | [**UserDataType**](eventschema-userdatatype-complextype.md)                       | Contiene i dati dell'evento. La sezione dei dati utente del modello determina il layout dei dati dell'evento.<br/>                                                                                                                                                                                                                       |



## <a name="remarks"></a>Commenti

In genere, questa sezione conterrà con la **sezione EventData** **o UserData.** La **sezione EventData** viene usata se il modello non contiene una **sezione UserData.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

