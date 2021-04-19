---
description: Indica al generatore di codice di generare un file e di specificare il nome del file di output.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: file (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc20f7d6853ccd52b231e19c99d60fe4b71d15b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310308"
---
# <a name="file-element"></a>file (elemento)

Indica al generatore di codice di generare un file e di specificare il nome del file di output.

## <a name="usage"></a>Utilizzo

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Attributi



| Attributo           | Type                       | Obbligatoria       | Descrizione                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **nome**<br/> | stringa PathName<br/> | Sì<br/> | Nome del file di output per il contenuto generato. La stringa del nome file deve includere informazioni complete sul percorso.<br/> <br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                 | Descrizione                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CDATA**<br/>                                                                                    | Le sezioni text e CDATA vengono copiate nel file senza modifiche. Il codice sorgente che non è una funzione dei dati di input del contratto può essere aggiunto ai file di output usando le sezioni text e CDATA.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Genera dichiarazioni C per i valori di tutti i tipi enumerati.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Genera dichiarazioni per le funzioni che creano classi di origine eventi.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Genera funzioni che creano classi di origine eventi.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera dichiarazioni di implementazione per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Genera una dichiarazione per una funzione che crea un host tipizzato.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Genera una funzione che crea un host tipizzato.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera dichiarazioni IDL per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                                                                                                       |
| [**includere**](include.md)<br/>                                                                   | Include il contenuto di una macro o di un file nell'output generato.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Genera dichiarazioni per QueryInterface, AddRef e release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Genera implementazioni per QueryInterface, AddRef e release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Inserisce un'istruzione di inclusione C o IDL nel codice generato. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definizioni della struttura C per i tipi di messaggio.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi di messaggio.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera costanti C per XML Schema tabelle per i tipi di messaggio.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Genera dichiarazioni C per le tabelle dello spazio dei nomi.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Genera definizioni C per le tabelle dello spazio dei nomi.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera dichiarazioni di costanti C per i tipi di porta.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera costanti C per i tipi di porta.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Genera dichiarazioni per le funzioni per la creazione di proxy tipizzati.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Genera funzioni per la creazione di proxy tipizzati.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementazioni per le funzioni proxy per le operazioni del tipo di porta.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Genera una dichiarazione in diretta per i metadati di hosting specificati nell'elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Genera una definizione di costante C per i metadati host specificati nell'elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Genera dichiarazioni di struttura C per i tipi noti.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Genera definizioni della struttura C per i tipi noti.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera dichiarazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementazioni per le funzioni stub per le operazioni del tipo di porta.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera dichiarazioni di implementazione per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera dichiarazioni IDL per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementazioni per le funzioni proxy di sottoscrizione e annullamento della sottoscrizione per le operazioni di notifica del tipo di porta.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Le sezioni text e CDATA vengono copiate nel file senza modifiche. Il codice sorgente che non è una funzione dei dati di input del contratto può essere aggiunto ai file di output usando le sezioni text e CDATA.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Genera una dichiarazione in diretta per la costante C per i metadati del produttore specificati nell'elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Genera una costante C per i metadati del produttore specificati nell'elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Genera dichiarazioni di costanti C per XML Schema tabelle per i tipi noti.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Genera costanti C per XML Schema tabelle per i tipi noti.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Sequenza di elementi figlio

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Elementi padre



| Elemento                                     | Descrizione                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento radice di un file di script XML del generatore di codice WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Commenti

Il nome del file è determinato dal valore dell'attributo del nome o dell'elemento figlio. Il contenuto del file è determinato dagli altri elementi figlio, text e CDATA nell'elemento **file** . Il testo e il CDATA vengono copiati nel file senza modifiche. Gli elementi figlio vengono sostituiti con il codice generato. Gli elementi text, CDATA e figlio possono verificarsi in qualsiasi ordine e possono essere ripetuti a tempo indefinito.

## <a name="element-information"></a>Informazioni sull'elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema minimo supportato<br/> | Windows Vista |
| Può essere vuoto                        | No            |



 

 




