---
title: Tipo complesso EventDefinitionType
description: Definisce un evento che il provider è in grado di scrivere.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- Log eventi di tipo complesso EventDefinitionType
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302664"
---
# <a name="eventdefinitiontype-complex-type"></a>Tipo complesso EventDefinitionType

Definisce un evento che il provider è in grado di scrivere.

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



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>channel</td>
<td>token</td>
<td>Identificatore che identifica il canale in cui viene scritto l'evento. Specificare un identificatore di canale di uno dei canali definiti o importati. Se il canale non specifica un identificatore del canale, utilizzare il nome del canale. Per informazioni dettagliate sulla definizione o sull'importazione di un canale, vedere il tipo complesso <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .<br/> Se non si specifica un canale, l'evento non viene scritto in un canale. In genere, l'unico motivo per non specificare un canale è se si scrivono eventi solo in una sessione ETW. Per informazioni dettagliate, vedere Creazione di una sessione ETW, vedere <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">controllo delle sessioni di traccia eventi</a>.<br/></td>
</tr>
<tr class="even">
<td>keywords</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></td>
<td>Elenco separato da spazi di nomi di parole chiave che identificano la categoria di eventi a cui appartiene l'evento. Specificare il nome di una parola chiave nell'elenco di parole chiave definite. Per informazioni dettagliate sulla definizione di parole chiave, vedere il tipo complesso <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .<br/> Se non si specificano le parole chiave, il descrittore dell'evento conterrà zero per le parole chiave.<br/></td>
</tr>
<tr class="odd">
<td>livello</td>
<td><strong>QName</strong></td>
<td>Livello di dettaglio da utilizzare durante la scrittura dell'evento. Specificare il nome di un livello definito nel manifesto o uno dei livelli definiti nel file \Include\Winmeta.xml incluso nel Windows SDK. Per informazioni dettagliate sulla definizione di un livello, vedere il tipo complesso <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .<br/> Se non si specifica un livello, il descrittore dell'evento conterrà uno zero per il livello.<br/> È necessario specificare un livello se il tipo di canale in cui viene scritto l'evento è admin; il livello deve essere uno dei livelli seguenti definiti in Winmeata.xml:
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></td>
<td>Messaggio localizzato per l'evento. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione <a href="eventmanifestschema-stringtable-resources-element.md"><strong>un'STRINGTABLE</strong></a> del manifesto.<br/> È necessario specificare un messaggio se il tipo di canale in cui viene scritto l'evento è admin.<br/></td>
</tr>
<tr class="odd">
<td>notLogged</td>
<td>boolean</td>
<td>Determina se il provider registra questo evento. Specificare true se il provider registra questo evento. in caso contrario, false. Utilizzare questo attributo per indicare che il provider non registra più questo evento anziché rimuovere l'evento dal manifesto. Mantenendo l'evento nel manifesto si consente ai consumer di decodificare i file ETL precedenti che includono l'evento.<br/> <strong>Windows Server 2008 e Windows Vista:</strong> Questo attributo non è supportato nelle versioni del compilatore di messaggi fornite prima della versione di Windows 7 del Windows SDK.<br/></td>
</tr>
<tr class="even">
<td>codice operativo</td>
<td><strong>QName</strong></td>
<td>Nome di un codice operativo che identifica un'operazione all'interno dell'attività. Specificare il nome di un codice operativo definito nel manifesto o uno dei codici operativi definiti in Winmeta.xml. Per informazioni dettagliate sulla definizione di un codice operativo, vedere il tipo complesso <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .<br/> Se l'attività a cui si fa riferimento contiene opcode specifici dell'attività (locale), è possibile specificare uno dei codici operativi specifici delle attività o un codice operativo definito a livello del provider (codice operativo globale). Se si specifica un codice operativo globale, il valore del codice operativo globale non può corrispondere a uno dei codici operativi locali per l'attività.<br/> Se si fa riferimento a un opcode locale, l'attributo dell'attività deve fare riferimento all'attività a cui appartiene il codice operativo locale.<br/> Se non si specifica un codice operativo, il descrittore dell'evento conterrà un valore zero per OpCode.<br/></td>
</tr>
<tr class="odd">
<td>simbolo</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td>Simbolo da utilizzare per fare riferimento al descrittore dell'evento per questo evento nell'applicazione. Il <a href="message-compiler--mc-exe-.md"><strong>compilatore di messaggi (MC.exe)</strong></a> usa il simbolo per creare una costante per il descrittore dell'evento nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente. Usare il descrittore quando si chiama la funzione <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> per scrivere l'evento.<br/></td>
</tr>
<tr class="even">
<td>attività</td>
<td><strong>QName</strong></td>
<td>Nome di un'attività che identifica il componente o il sottocomponente che genera l'evento. Consente di specificare il nome di un'attività definita nel manifesto. Per informazioni dettagliate sulla definizione di un'attività, vedere il tipo complesso <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .<br/> Se non si specifica un'attività, il descrittore dell'evento conterrà uno zero per l'attività.<br/></td>
</tr>
<tr class="odd">
<td>template</td>
<td>token</td>
<td>Identificatore del modello che definisce gli elementi di dati inclusi in questo evento. Specificare l'identificatore di un modello definito nel manifesto. Per informazioni dettagliate sulla definizione di un modello, vedere il tipo complesso <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>Valore</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>Identificatore dell'evento. L'identificatore deve essere univoco all'interno dell'elenco di eventi definito dall'utente.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Numero di versione a un byte della definizione dell'evento.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Se si utilizza [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) per formattare la stringa di messaggio per l'evento (oppure utilizzare il Visualizzatore eventi per visualizzare la stringa di messaggio), la stringa di messaggio può contenere stringhe di inserimento e una qualsiasi delle stringhe di formato supportate dalla funzione **FormatMessage** Win32. Le stringhe di inserimento sono limitate a%*n* o%*n*! s! (ad esempio, %1), dove *n* è il riferimento basato su uno degli elementi di dati definiti nel modello dell'evento. La stringa di messaggio può inoltre contenere stringhe di inserimento di parametri nel formato%%*n* , ad esempio% %4. Il numero massimo di stringhe di inserimento che il messaggio può contenere è 100.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

