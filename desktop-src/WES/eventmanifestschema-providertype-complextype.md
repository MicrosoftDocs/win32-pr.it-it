---
title: Tipo complesso ProviderType
description: Definisce un provider e i metadati utilizzati per definire i relativi eventi. | Tipo complesso ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- EventLog di tipo complesso ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e48edd19d6ff9a547ce1698f81c89f780ffaa48f6312a656ef18664b39e78410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511271"
---
# <a name="providertype-complex-type"></a>Tipo complesso ProviderType

Definisce un provider e i metadati utilizzati per definire i relativi eventi.

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
| [**Canali**](eventmanifestschema-channels-providertype-element.md)         | [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)   | Definisce un elenco di canali ai quali i provider possono registrare eventi.<br/>                                                                                                                                                                                      |
| [**Eventi**](eventmanifestschema-events-providertype-element.md)             | [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)     | Definisce un elenco di definizioni di eventi degli eventi che il provider può registrare.<br/>                                                                                                                                                                       |
| **Filtri**                                                                   | [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)     | Definisce un elenco di filtri supportati dal provider. È possibile usare i filtri, come si farebbe con le parole chiave level e , per determinare se si vuole scrivere un evento. <br/> **Windows Server 2008 e Windows Vista:** Non supportato fino Windows 7.<br/> |
| [**keywords**](eventmanifestschema-keywords-providertype-element.md)         | [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)   | Definisce un elenco di parole chiave che categorizzano gli eventi.<br/>                                                                                                                                                                                                 |
| [**Livelli**](eventmanifestschema-levels-providertype-element.md)             | [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)       | Definisce un elenco di livelli che specificano la gravità di un evento.<br/>                                                                                                                                                                                    |
| [**Mappe**](eventmanifestschema-maps-providertype-element.md)                 | [**MapType**](eventmanifestschema-maptype-complextype.md)                   | Definisce un elenco di coppie nome/valore a cui è possibile fare riferimento nella sezione del modello del manifesto.<br/>                                                                                                                                                 |
| [**namedQueries**](eventmanifestschema-namedqueries-providertype-element.md) | [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)     | Non usato. Definisce un elenco di query denominate che eseguono query sulla stringa del messaggio dell'evento per un valore ed eseguono un'azione specificata, se presente.<br/>                                                                                                                 |
| [**Opcodes**](eventmanifestschema-opcodes-providertype-element.md)           | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)     | Definisce un elenco di codici operativo che è possibile usare per raggruppare gli eventi all'interno di un'attività.<br/>                                                                                                                                                                          |
| [**Attività**](eventmanifestschema-tasks-providertype-element.md)               | [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)         | Definisce un elenco di attività che un provider può usare per raggruppare gli eventi. In genere, le attività vengono usate per raggruppare gli eventi per una funzionalità o un componente del provider.<br/>                                                                                              |
| [**Modelli**](eventmanifestschema-templates-providertype-element.md)       | [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md) | Definisce un elenco di modelli che specificano i dati da includere con gli eventi.<br/>                                                                                                                                                                      |



## <a name="attributes"></a>Attributi



| Nome                                | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| guid                                | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | GUID che identifica in modo univoco il provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Helplink                            | anyURI                                                            | L'URL o la Guida di Microsoft si collega al contenuto che fornisce informazioni sugli eventi generati dal provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| message                             | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nome visualizzato localizzato per il provider. La stringa del messaggio fa riferimento a una stringa localizzata [**nella sezione stringTable**](eventmanifestschema-stringtable-resources-element.md) del manifesto. <br/>                                                                                                                                                                                                                                                                                                                           |
| messageFileName                     | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse del messaggio localizzate del provider. Il file può essere un file eseguibile o un file DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| name                                | anyURI                                                            | Nome del provider. Il nome deve essere nel formato *Componente* - *prodotto* - *società*.<br/> Il nome non può essere più lungo di 255 caratteri e non può contenere i caratteri '>', '<', '&', '"', ' \| ', \\ ', ':', '', '?', ' ' o caratteri con codici minori di \* 31. Inoltre, il nome deve seguire i vincoli generali sui nomi di file e chiavi del Registro di sistema. Questi vincoli sono disponibili in Naming a File (Denominazione [di un file)](/windows/desktop/FileIO/naming-a-file)e [Registry Element Size Limits (Limiti delle dimensioni degli elementi del Registro di sistema).](/windows/desktop/SysInfo/registry-element-size-limits)<br/> |
| parameterFileName                   | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse della stringa del parametro del provider. Il file può essere un file eseguibile o un file DLL. È possibile specificare più file di parametri separati da un punto e virgola. La ricerca nel file viene verificata quando la stringa di messaggio di un evento contiene una stringa di parametro. I parametri consentono di specificare stringhe di inserimento localizzabili. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/>                                                                                                                                                |
| resourceFileName                    | [**Filepath**](eventmanifestschema-filepath-simpletype.md)       | Percorso completo del file che contiene le risorse di metadati del provider. Il file può essere un file eseguibile o un file DLL.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| source                              |                                                                   | Solo per uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| simbolo                              | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da usare per fare riferimento al GUID del provider nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il GUID del provider nel file di intestazione generato dal compilatore.<br/>                                                                                                                                                                                                                                                                           |
| warnOnApplicationCompatibilityError | **xs:boolean**                                                    | Solo per uso interno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a>Commenti

Il Windows Visualizzatore eventi (Eventvwr.exe) userà la stringa di messaggio localizzata, se disponibile; In caso contrario, usa la stringa dell'attributo name.

I percorsi per resourceFileName, messageFileName e parameterFileName possono contenere variabili di ambiente. Se si definisce una nuova variabile di ambiente da usare nel percorso, è necessario riavviare il computer in modo che il servizio registro eventi possa prelevare la nuova variabile. In caso contrario, il servizio non sarà in grado di trovare le risorse del provider.

La stringa di messaggio di un evento può contenere stringhe di inserimento e stringhe di parametri. Una stringa di inserimento è nel formato %*n*, dove *n* è un indice in base uno che identifica un elemento di dati dal modello di dati dell'evento che si vuole inserire nel messaggio. Una stringa di parametro (vedere **l'attributo parameterFileName)** è nel formato %%*n*, dove n è l'identificatore di un messaggio nella tabella dei messaggi. Se la stringa di messaggio dell'evento contiene "%1 %%11 = %2 %%12" e i valori dell'elemento dati per %1 e %2 sono rispettivamente 8 e 2 e le stringhe di parametro per %%11 e %%12 sono rispettivamente "quarts" e "ons", la stringa formattata sarà "8 quarts = 2 dons".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

