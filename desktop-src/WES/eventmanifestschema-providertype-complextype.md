---
title: Tipo complesso ProviderType
description: Definisce un provider e i metadati utilizzati per definire gli eventi. | Tipo complesso ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Log eventi di tipo complesso ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353371"
---
# <a name="providertype-complex-type"></a>Tipo complesso ProviderType

Definisce un provider e i metadati utilizzati per definire gli eventi.

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                       | Tipo                                                                         | Descrizione                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**canali**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Definisce un elenco di canali a cui i provider possono registrare gli eventi.<br/>                                                                                                                                                                                      |
| [**eventi**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Definisce un elenco di definizioni di evento degli eventi che il provider è in grado di registrare.<br/>                                                                                                                                                                       |
| **filtri**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Definisce un elenco di filtri supportati dal provider. Per determinare se si vuole scrivere un evento, è possibile usare i filtri, come per le parole chiave e per il livello. <br/> **Windows Server 2008 e Windows Vista:** Non supportato fino a Windows 7.<br/> |
| [**Parole**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Definisce un elenco di parole chiave che categorizzano gli eventi.<br/>                                                                                                                                                                                                 |
| [**livelli**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Definisce un elenco di livelli che specificano la gravità di un evento.<br/>                                                                                                                                                                                    |
| [**Mappe**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Definisce un elenco di coppie nome/valore a cui è possibile fare riferimento nella sezione modello del manifesto.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | Non usato. Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata.<br/>                                                                                                                 |
| [**OpCodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Definisce un elenco di codici operativi che è possibile usare per raggruppare gli eventi all'interno di un'attività.<br/>                                                                                                                                                                          |
| [**attività**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Definisce un elenco di attività che possono essere utilizzate da un provider per raggruppare gli eventi. In genere, è possibile utilizzare le attività per raggruppare gli eventi per una funzionalità o un componente del provider.<br/>                                                                                              |
| [**modelli**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Definisce un elenco di modelli che specificano i dati da includere con gli eventi.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Attributi



| Nome                                | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | GUID che identifica in modo univoco il provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| helpLink                            | anyURI                                                            | Il collegamento all'URL o alla Guida MS al contenuto che fornisce informazioni sugli eventi generati dal provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il provider. La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse del messaggio localizzato del provider. Il file può essere un file eseguibile o un file DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Nome del provider. Il nome deve essere nel formato, componente del prodotto *aziendale* -  - .<br/> Il nome non può contenere più di 255 caratteri e non può contenere i caratteri seguenti:' >',' <',' &',' "',' \| ',' \\ ',':','','?',' \* ' o caratteri con codici minori di 31. Inoltre, il nome deve seguire i vincoli generali sui nomi di file e chiavi del registro di sistema. Questi vincoli sono disponibili nella pagina relativa alla [denominazione di un file](/windows/desktop/FileIO/naming-a-file)e ai [limiti delle dimensioni degli elementi del registro di sistema](/windows/desktop/SysInfo/registry-element-size-limits).<br/> |
| parameterFileName                   | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse di stringa del parametro del provider. Il file può essere un file eseguibile o un file DLL. È possibile specificare più di un file di parametri separati da un punto e virgola. Viene eseguita una ricerca nel file quando la stringa del messaggio di un evento contiene una stringa di parametro. I parametri consentono di fornire stringhe di inserimento localizzabili. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                |
| resourceFileName                    | [**filePath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse di metadati del provider. Il file può essere un file eseguibile o un file DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Solo per uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| simbolo                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al GUID del provider nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il GUID del provider nel file di intestazione generato dal compilatore.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | Solo per uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Commenti

Il Visualizzatore eventi di Windows (Eventvwr.exe) utilizzerà la stringa di messaggio localizzata, se disponibile. in caso contrario, usa la stringa dall'attributo Name.

I percorsi per resourceFileName, messageFileName e parameterFileName possono contenere variabili di ambiente. Se si definisce una nuova variabile di ambiente da usare nel percorso, è necessario riavviare il computer in modo che il servizio Registro eventi possa selezionare la nuova variabile. in caso contrario, il servizio non sarà in grado di trovare le risorse del provider.

Una stringa di messaggio di un evento può contenere stringhe di inserimento e stringhe di parametri. Una stringa di inserimento è nel formato%*n*, dove *n* è un indice in base uno che identifica un elemento dati dal modello di dati dell'evento che si desidera inserire nel messaggio. Una stringa di parametro (vedere l'attributo **parameterFileName** ) è nel formato%%*n*, dove n è l'identificatore di un messaggio nella tabella del messaggio. Se la stringa di messaggio dell'evento contiene "%1% %11 = %2% %12" e i valori degli elementi di dati per %1 e %2 sono rispettivamente 8 e 2 e le stringhe di parametri per% %11 e% %12 erano "quarte" e "Gallon", la stringa formattata sarebbe "8 litri = 2 litri".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

