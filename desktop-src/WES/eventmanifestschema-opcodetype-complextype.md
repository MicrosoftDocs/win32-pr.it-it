---
title: Tipo complesso OpcodeType
description: Definisce un'operazione all'interno di un componente dell'applicazione.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- EventLog di tipo complesso OpcodeType
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b18fa8a7591a54877251e10448842c3cd9d2394099028bf3a2cb680aee979bbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136214"
---
# <a name="opcodetype-complex-type"></a>Tipo complesso OpcodeType

Definisce un'operazione all'interno di un componente dell'applicazione. Utilizzato insieme a un'attività per identificare la sezione dell'applicazione che sta registrare l'evento.

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome     | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il codice operativo. La stringa del messaggio fa riferimento a una stringa localizzata nella [**sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Riservato esclusivamente per uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Nome del codice operativo. Questo nome deve essere univoco nell'ambito di questo provider. <br/>                                                                                                                                                                                                                      |
| simbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al codice operativo nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il codice operativo nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore del codice operativo. È possibile specificare valori nell'intervallo 10 e 239. Per un elenco dei valori predefiniti del codice operativo, vedere Osservazioni.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori predefiniti del codice operativo che è possibile usare. Questi valori sono definiti nel file Winmeta.xml incluso nell'SDK Windows.



| Nome          | Valore | Simbolo                      | Descrizione                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| win:Info      | 0     | INFORMAZIONI SUL \_ CODICE OPERATIVO \_ WINEVENT      | Evento informativo.                                                                                |
| win:Start     | 1     | AVVIO \_ DEL CODICE OPERATIVO WINEVENT \_     | Evento che rappresenta l'avvio di un'attività.                                                         |
| win:Stop      | 2     | ARRESTO \_ DEL CODICE OPERATIVO WINEVENT \_      | Evento che rappresenta l'arresto di un'attività. L'evento corrisponde all'ultimo evento di avvio non associato. |
| win:DC \_ Start | 3     | AVVIO DEL CONTROLLER \_ DI DOMINIO WINEVENT OPCODE \_ \_ | Evento che rappresenta l'avvio della raccolta dati. Si tratta di tipi di evento rundown.                      |
| win:DC \_ Stop  | 4     | ARRESTO DEL \_ CONTROLLER DI DOMINIO OPCODE \_ WINEVENT \_  | Evento che rappresenta l'arresto della raccolta dati. Si tratta di tipi di evento rundown.                      |
| win:Extension | 5     | ESTENSIONE \_ WINEVENT \_ OPCODE | Evento di estensione.                                                                                    |
| win:Reply     | 6     | RISPOSTA \_ AL CODICE OPERATIVO WINEVENT \_     | Evento di risposta.                                                                                         |
| win:Resume    | 7     | RIPRESA \_ DEL CODICE OPERATIVO WINEVENT \_    | Evento che rappresenta un'attività ripresa dopo la sospensione.                                   |
| win:Suspend   | 8     | WINEVENT \_ OPCODE \_ SUSPEND   | Evento che rappresenta l'attività sospesa in attesa del completamento di un'altra attività.           |
| win:Send      | 9     | WINEVENT \_ OPCODE \_ SEND      | Evento che rappresenta il trasferimento dell'attività a un altro componente.                                   |
| win:Receive   | 240   | RICEZIONE \_ DEL CODICE OPERATIVO WINEVENT \_   | Evento che rappresenta la ricezione di un trasferimento di attività da un altro componente.                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





