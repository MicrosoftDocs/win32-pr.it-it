---
title: Tipi complessi dello schema EventManifest
description: Di seguito sono riportati i tipi complessi definiti nello schema EventManifest.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69200d90253b27f9e73035a14ba5817917b24e1367d3bc4a54fff37e15d112ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590060"
---
# <a name="eventmanifest-schema-complex-types"></a>Tipi complessi dello schema EventManifest

Di seguito sono riportati i tipi complessi definiti nello schema EventManifest.



| Tipo complesso                                                                                       | Descrizione                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)                                   | Definisce un elenco di mapping nome/valore tra valori di bit e valori stringa.<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Definisce il mapping tra un valore di bit e un valore stringa.<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | Definisce un elenco di canali in cui i provider possono registrare gli eventi.<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | Definisce le proprietà del file di log che contiene il canale, ad esempio la capacità e se è sequenziale o circolare.<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | Definisce le proprietà di registrazione per la sessione utilizzata dal canale.<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | Definisce un canale in cui i provider possono registrare gli eventi.<br/>                                                                                                                                                                         |
| [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Definisce un elemento di dati da includere con l'evento .<br/>                                                                                                                                                                 |
| [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)                           | Definisce un elenco di eventi che il provider può registrare.<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Definisce un evento che il provider può scrivere.<br/>                                                                                                                                                                               |
| [**EventsType**](eventmanifestschema-eventstype-complextype.md)                                   | Contiene un elenco di provider definiti nel manifesto.<br/>                                                                                                                                                               |
| [**Filtertype**](eventmanifestschema-filtertype-complextype.md)                                   | Definisce un filtro dati utilizzato da una sessione per filtrare gli eventi in base ai dati degli eventi.<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Definisce un tipo di dati di input.<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Definisce un elenco di tipi di input.<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Definisce il tipo di base per [**l'elemento instrumentationManifest.**](eventmanifestschema-instrumentationmanifest-element.md)<br/>                                                                                                |
| [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md)                 | Definisce il contenuto della sezione di strumentazione del manifesto.<br/>                                                                                                                                                         |
| [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)                         | Definisce un elenco di parole chiave che categorizzano gli eventi.<br/>                                                                                                                                                                           |
| [**KeywordType**](eventmanifestschema-keywordtype-complextype.md)                                 | Definisce una parola chiave che identifica una categoria di eventi.<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.<br/>                                                                                                                                           |
| [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)                       | Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Definisce un elenco di coppie nome/valore.<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | Definisce un elenco di query denominate che eseguono query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se presente.<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | Definisce un elenco di opcode usati per identificare le operazioni di un componente dell'applicazione.<br/>                                                                                                                        |
| [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | Definisce un'operazione all'interno di un componente dell'applicazione.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Definisce un tipo di dati di output che determina la modalità di rendering dei dati.<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Definisce un elenco di coppie di espressioni regolari usate per modificare la stringa del messaggio.<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | Definisce un mapping tra due espressioni regolari. Un'espressione viene usata per trovare una stringa corrispondente nella stringa di messaggio e l'altra viene usata per modificare la stringa prima che il servizio la inserisca nuovamente nella stringa del messaggio.<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Definisce le espressioni regolari usate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Definisce un provider e i metadati utilizzati per definire gli eventi.<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | Definisce una struttura che include uno o più elementi di dati da includere con l'evento .<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Definisce un evento specifico dell'attività che il provider può registrare.<br/>                                                                                                                                                                    |
| [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)                               | Definisce un elenco di attività usate per identificare i componenti di un'applicazione.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Definisce un componente o un sottocomponente di un'applicazione.<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | Modello che definisce i dati da includere con un evento.<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | Definisce un elenco di modelli che specificano i dati da includere con gli eventi.<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | Definisce i tipi usati nel manifesto.<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | Definisce un elenco di mapping nome/valore tra valori interi e valori stringa.<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Definisce il mapping tra un valore integer e un valore stringa.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Definisce un frammento XML.<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.<br/>                                                                                                                             |



 

 

 





