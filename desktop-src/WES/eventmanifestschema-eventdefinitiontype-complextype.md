---
title: Tipo complesso EventDefinitionType
description: Definisce un evento che il provider può scrivere.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType di tipo complesso EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42959edd4c7f7f49c3ced305b5b9bd1072f721a4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482987"
---
# <a name="eventdefinitiontype-complex-type"></a>Tipo complesso EventDefinitionType

Definisce un evento che il provider può scrivere.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi




| Nome | Tipo | Descrizione | 
|------|------|-------------|
| channel | token | Identificatore che identifica il canale in cui viene scritto l'evento. Specificare un identificatore di canale di uno dei canali definiti o importati. Se il canale non specifica un identificatore di canale, usare il nome del canale. Per informazioni dettagliate sulla definizione o l'importazione di un canale, vedere il <a href="eventmanifestschema-channellisttype-complextype.md"><strong>tipo complesso ChannelListType.</strong></a><br /> Se non si specifica un canale, l'evento non viene scritto in un canale. In genere, l'unico motivo per non specificare un canale è la scrittura di eventi solo in una sessione ETW. Per informazioni dettagliate, vedere Creazione di una sessione ETW. Vedere <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controllo delle sessioni di traccia eventi.</a><br /> | 
| keywords | <a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a> | Elenco delimitato da spazi di nomi di parole chiave che identificano la categoria di eventi a cui appartiene questo evento. Specificare un nome di parola chiave dall'elenco di parole chiave definite. Per informazioni dettagliate sulla definizione di parole chiave, vedere il <a href="eventmanifestschema-keywordtype-complextype.md"><strong>tipo complesso KeywordType.</strong></a><br /> Se non si specificano parole chiave, il descrittore dell'evento conterrà uno zero per le parole chiave.<br /> | 
| livello | <strong>QName</strong> | Livello di dettaglio da utilizzare durante la scrittura dell'evento. Specificare il nome di un livello definito nel manifesto o uno dei livelli definiti nel file \Include\Winmeta.xml incluso in Windows SDK. Per informazioni dettagliate sulla definizione di un livello, vedere il <a href="eventmanifestschema-leveltype-complextype.md"><strong>tipo complesso LevelType.</strong></a><br /> Se non si specifica un livello, il descrittore dell'evento conterrà uno zero per level.<br /> È necessario specificare un livello se il tipo di canale in cui viene scritto l'evento è Admin; il livello deve essere uno dei livelli seguenti definiti in Winmeata.xml:<ul><li>win:Critical</li><li>win:Error</li><li>win:Warning</li><li>win:Informational</li></ul><br /> | 
| message | <a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a> | Messaggio localizzato per l'evento. La stringa del messaggio fa riferimento a una stringa localizzata <a href="eventmanifestschema-stringtable-resources-element.md"><strong>nella sezione stringTable</strong></a> del manifesto.<br /> È necessario specificare un messaggio se il tipo di canale in cui viene scritto l'evento è Admin.<br /> | 
| notLogged | boolean | Determina se il provider registra questo evento. Specificare true se il provider registra questo evento. in caso contrario, false. Usare questo attributo per indicare che il provider non sta più registrare questo evento anziché rimuoverlo dal manifesto. Mantenendo l'evento nel manifesto, i consumer potranno decodificare i file etl meno recenti che includono l'evento.<br /><strong>Windows Server 2008 e Windows Vista:</strong> Questo attributo non è supportato nelle versioni del compilatore di messaggi fornite prima della versione Windows 7 di Windows SDK.<br /> | 
| Opcode | <strong>QName</strong> | Nome di un codice operativo che identifica un'operazione all'interno dell'attività. Specificare il nome di un codice operativo definito nel manifesto o uno dei codici operativo definiti in Winmeta.xml. Per informazioni dettagliate sulla definizione di un codice operativo, vedere il <a href="eventmanifestschema-opcodetype-complextype.md"><strong>tipo complesso OpcodeType.</strong></a><br /> Se l'attività a cui si fa riferimento contiene opcode (locali) specifici dell'attività, è possibile specificare uno dei relativi opcode specifici dell'attività o un codice operativo definito a livello di provider (codice operativo globale). Se si specifica un codice operativo globale, il valore del codice operativo globale non può essere uguale a uno dei codici operativo locali per l'attività.<br /> Se si fa riferimento a un codice operativo locale, l'attributo task deve fare riferimento all'attività a cui appartiene il codice operativo locale.<br /> Se non si specifica un codice operativo, il descrittore dell'evento conterrà uno zero per il codice operativo.<br /> | 
| simbolo | <a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a> | Simbolo da usare per fare riferimento al descrittore di evento per questo evento nell'applicazione. Il <a href="message-compiler--mc-exe-.md"><strong>compilatore di messaggi (MC.exe)</strong></a> usa il simbolo per creare una costante per il descrittore di evento nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente. Il descrittore viene utilizzato quando si chiama la <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>funzione EventWrite</strong></a> per scrivere l'evento.<br /> | 
| attività | <strong>QName</strong> | Nome di un'attività che identifica il componente o il sottocomponente che genera questo evento. Specificare il nome di un'attività definita nel manifesto. Per informazioni dettagliate sulla definizione di un'attività, vedere il <a href="eventmanifestschema-tasktype-complextype.md"><strong>tipo complesso TaskType.</strong></a><br /> Se non si specifica un'attività, il descrittore dell'evento conterrà uno zero per l'attività.<br /> | 
| template | token | Identificatore del modello che definisce gli elementi di dati inclusi in questo evento. Specificare l'identificatore di un modello definito nel manifesto. Per informazioni dettagliate sulla definizione di un modello, vedere il <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>tipo complesso TemplateItemType.</strong></a><br /> | 
| Valore | <a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a> | Identificatore dell'evento. L'identificatore deve essere univoco all'interno dell'elenco di eventi definiti.<br /> | 
| version | unsignedByte | Numero di versione a un byte della definizione dell'evento.<br /> | 




## <a name="remarks"></a>Commenti

Se si usa [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) per formattare la stringa di messaggio per l'evento (o si usa il Visualizzatore eventi per visualizzare la stringa del messaggio), la stringa di messaggio può contenere stringhe di inserimento e qualsiasi stringa di formato supportate dalla funzione **FormatMessage** win32. Le stringhe di inserimento sono limitate a %*n* o %*n*!s! (ad esempio, %1) dove *n* è il riferimento in base uno agli elementi di dati definiti nel modello dell'evento. La stringa di messaggio può anche contenere stringhe di inserimento di parametri nel formato %%*n* (ad esempio% %%4). Il numero massimo di stringhe di inserimento che il messaggio può contenere è 100.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

