---
title: Tipi complessi dello schema EventManifest
description: Di seguito sono riportati i tipi complessi definiti dallo schema EventManifest.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d952a98bea78bab18f76da091a392e4b6247ca5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298372"
---
# <a name="eventmanifest-schema-complex-types"></a>Tipi complessi dello schema EventManifest

Di seguito sono riportati i tipi complessi definiti dallo schema EventManifest.



| Tipo complesso                                                                                       | Descrizione                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)                                   | Definisce un elenco di mapping nome/valore tra valori di bit e valori di stringa.<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Definisce il mapping tra un valore di bit e un valore stringa.<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | Definisce un elenco di canali a cui i provider possono registrare gli eventi.<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se è sequenziale o circolare.<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | Definisce le proprietà di registrazione per la sessione utilizzata dal canale.<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | Definisce un canale al quale i provider possono registrare gli eventi.<br/>                                                                                                                                                                         |
| [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Definisce un elemento di dati che si desidera includere nell'evento.<br/>                                                                                                                                                                 |
| [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)                           | Definisce un elenco di eventi che il provider può registrare.<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Definisce un evento che il provider è in grado di scrivere.<br/>                                                                                                                                                                               |
| [**EventsType**](eventmanifestschema-eventstype-complextype.md)                                   | Contiene un elenco di provider definiti nel manifesto.<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | Definisce un filtro di dati utilizzato da una sessione per filtrare gli eventi in base ai dati dell'evento.<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | Definisce un elenco di filtri che un controller ETW può passare al provider per limitare ulteriormente gli eventi scritti.<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Definisce un tipo di dati di input.<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Definisce un elenco di tipi di input.<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Definisce il tipo di base per l'elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .<br/>                                                                                                |
| [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md)                 | Definisce il contenuto della sezione di strumentazione del manifesto.<br/>                                                                                                                                                         |
| [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)                         | Definisce un elenco di parole chiave che categorizzano gli eventi.<br/>                                                                                                                                                                           |
| [**KeywordType**](eventmanifestschema-keywordtype-complextype.md)                                 | Definisce una parola chiave che identifica una categoria di eventi.<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | Definisce un elenco di livelli di gravità che specificano il livello di dettaglio di un evento.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.<br/>                                                                                                                                           |
| [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)                       | Definisce un gruppo di risorse localizzate a cui si fa riferimento nel manifesto.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Definisce un elenco di coppie nome/valore.<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | Definisce i tipi di metadati che è possibile definire nella sezione dei metadati del manifesto.<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | Definisce un elenco di query denominate che eseguono una query sulla stringa del messaggio di evento per un valore ed eseguono un'azione specificata, se trovata.<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | Definisce un elenco di codici operativi usati per identificare le operazioni di un componente dell'applicazione.<br/>                                                                                                                        |
| [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | Definisce un'operazione all'interno di un componente dell'applicazione.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Definisce un tipo di dati di output che determina la modalità di rendering dei dati.<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Definisce un elenco di coppie di espressioni regolari utilizzate per modificare la stringa del messaggio.<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | Definisce un mapping tra due espressioni regolari. Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Definisce le espressioni regolari utilizzate per trovare una stringa corrispondente nella stringa del messaggio e modificarla.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Definisce un provider e i metadati utilizzati per definire gli eventi.<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | Definisce un elenco di stringhe localizzate a cui è possibile fare riferimento nel manifesto.<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento.<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Definisce un evento specifico dell'attività che il provider è in grado di registrare.<br/>                                                                                                                                                                    |
| [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)                               | Definisce un elenco di attività utilizzate per identificare i componenti di un'applicazione.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Definisce un componente o un sottocomponente di un'applicazione.<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | Modello che definisce i dati da includere in un evento.<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | Definisce un elenco di modelli che specificano i dati da includere con gli eventi.<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | Definisce i tipi utilizzati nel manifesto.<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | Definisce un elenco di mapping nome/valore tra valori interi e valori di stringa.<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Definisce il mapping tra un valore integer e un valore stringa.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Definisce un frammento XML.<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Definisce un elenco di tipi di output utilizzati dal servizio per determinare come eseguire il rendering di un tipo di dati di input.<br/>                                                                                                                             |



 

 

 





