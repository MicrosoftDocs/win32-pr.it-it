---
title: Tipo complesso OpcodeType
description: Definisce un'operazione all'interno di un componente dell'applicazione.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Log eventi di tipo complesso OpcodeType
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121334"
---
# <a name="opcodetype-complex-type"></a>Tipo complesso OpcodeType

Definisce un'operazione all'interno di un componente dell'applicazione. Utilizzato insieme a un'attività per identificare la sezione dell'applicazione che registra l'evento.

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
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il codice operativo. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Riservato esclusivamente per uso interno.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Nome del codice operativo. Questo nome deve essere univoco all'interno dell'ambito di questo provider. <br/>                                                                                                                                                                                                                      |
| simbolo   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al codice operativo nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il codice operativo nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |
| Valore    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valore OpCode. È possibile specificare valori compresi tra 10 e 239. Per un elenco di valori opcode predefiniti, vedere la sezione Osservazioni.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Commenti

Di seguito sono riportati i valori opcode predefiniti che è possibile utilizzare. Questi valori vengono definiti nel file di Winmeta.xml incluso nel Windows SDK.



| Nome          | Valore | Simbolo                      | Descrizione                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| Win: info      | 0     | \_informazioni OPCODE \_ WINEVENT      | Evento informativo.                                                                                |
| Win: avvio     | 1     | \_avvio OPCODE \_ WINEVENT     | Evento che rappresenta l'avvio di un'attività.                                                         |
| Win: arresta      | 2     | WINEVENT \_ OPCODE \_ Stop      | Evento che rappresenta l'arresto di un'attività. L'evento corrisponde all'ultimo evento di inizio non associato. |
| Win: avvio del controller di dominio \_ | 3     | avvio del controller di dominio \_ OPCODE WINEVENT \_ \_ | Evento che rappresenta l'avvio della raccolta dati. Si tratta di tipi di evento rundown.                      |
| Win: arresto del controller di dominio \_  | 4     | WINEVENT \_ OPCODE \_ DC \_ Stop  | Evento che rappresenta l'arresto della raccolta dati. Si tratta di tipi di evento rundown.                      |
| Win: estensione | 5     | \_estensione OPCODE \_ WINEVENT | Evento di estensione.                                                                                    |
| Win: risposta     | 6     | \_risposta OPCODE \_ WINEVENT     | Un evento di risposta.                                                                                         |
| Win: Resume    | 7     | \_riavvio del codice operativo WINEVENT \_    | Evento che rappresenta una ripresa dell'attività dopo la sospensione.                                   |
| Win: sospensione   | 8     | \_sospensione OPCODE \_ WINEVENT   | Evento che rappresenta l'attività sospesa in attesa del completamento di un'altra attività.           |
| Win: invio      | 9     | \_invio OPCODE \_ WINEVENT      | Evento che rappresenta il trasferimento dell'attività a un altro componente.                                   |
| Win: ricezione   | 240   | \_ricezione OPCODE \_ WINEVENT   | Evento che rappresenta la ricezione di un trasferimento di attività da un altro componente.                        |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





