---
description: Introduce lo schema di descrizione del connettore di ricerca utilizzato dalle librerie di Esplora risorse e dai provider di ricerca federati.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Cerca nello schema di descrizione del connettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f502f67cdc933bf4d27a3475cd6adef70c00fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306068"
---
# <a name="search-connector-description-schema"></a>Cerca nello schema di descrizione del connettore

Introduce lo schema di descrizione del connettore di ricerca utilizzato dalle librerie di Esplora risorse e dai provider di ricerca federati. Lo schema specifica la struttura e i requisiti per i file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS) e per gli elementi **searchConnectorDescriptionType** dei file di descrizione della libreria della shell ( \* libreria-MS).

In questo argomento viene descritto lo schema correlato ai connettori di ricerca federati. Per ulteriori informazioni sulle librerie e sullo schema di descrizione della libreria, vedere [Library Description schema](../shell/library-schema-entry.md).

Questo argomento include le sezioni seguenti:

-   [Che cosa sono i connettori di ricerca?](#what-are-search-connectors)
-   [Come funzionano i file di descrizione del connettore di ricerca?](#search-connector-description-schema)
-   [Che cos'è lo schema di descrizione del connettore di ricerca?](#what-is-the-search-connector-description-schema)
-   [Quali sono le parti principali dello schema?](#what-are-the-major-parts-of-the-schema)
-   [Esempi di file di descrizione del connettore di ricerca](#examples-of-search-connector-description-files)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-search-connectors"></a>Che cosa sono i connettori di ricerca?

I connettori di ricerca connettono gli utenti con i dati archiviati in servizi Web o posizioni di archiviazione remota. Con Windows 7, gli utenti possono installare i connettori di ricerca per le posizioni, ad esempio i servizi Web, in modo da cercare tali percorsi direttamente da Esplora risorse. I connettori di ricerca sono file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS) che specificano come connettersi, inviare query a e ricevere i risultati dal percorso.

Oltre ai servizi Web, è possibile usare i connettori di ricerca per eseguire ricerche negli ambiti degli indici locali creati dai gestori del protocollo. Ad esempio, gli utenti possono eseguire ricerche nella posta elettronica indicizzata localmente con il gestore del protocollo MAPI usando un connettore di ricerca per l'archivio di posta elettronica.

## <a name="how-do-search-connector-description-files-work"></a>Come funzionano i file di descrizione del connettore di ricerca?

Quando i file di descrizione del connettore di ricerca sono installati nei sistemi degli utenti, gli utenti possono aprire Esplora risorse, fare clic sul connettore Cerca nel riquadro di spostamento e immettere una query di ricerca. Esplora risorse Invia la query usando le informazioni del file di descrizione del connettore di ricerca, ad esempio il provider da usare e l'ambito della ricerca. I risultati vengono restituiti come elementi feed RSS o Atom e visualizzati agli utenti come se fossero elementi normali della shell.

La modalità di distribuzione del file di descrizione del connettore di ricerca dipende dal tipo di posizione supportata dal connettore di ricerca:

-   In un file di configurazione di OpenSearch (con \* estensione osdx) per il servizio Web
-   Come parte dell'installazione del gestore di protocollo

È necessario assicurarsi che si verifichi quanto segue quando un utente apre il file con estensione osdx o installa il gestore di protocollo:

-   Il file con estensione searchconnector-ms viene creato nella cartella **ricerche di Windows** degli utenti (% USERPROFILE%/Searches).
-   Viene creato un collegamento al file. searchconnector-ms nella cartella **collegamenti** degli utenti (% USERPROFILE%/Links).

## <a name="what-is-the-search-connector-description-schema"></a>Che cos'è lo schema di descrizione del connettore di ricerca?

Lo schema di descrizione del connettore di ricerca è un XML Schema che definisce la struttura dei file di descrizione del connettore di ricerca (con \* estensione searchConnector-MS). Ogni connettore di ricerca deve avere un file di descrizione del connettore di ricerca che specifichi come connettersi, inviare query a e ricevere i risultati dal percorso.

## <a name="what-are-the-major-parts-of-the-schema"></a>Quali sono le parti principali dello schema?

Nella tabella seguente sono elencate le parti principali dello schema.



| Elementi figlio                                                                         | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Indica se i percorsi supportati dal connettore di ricerca sono di sola ricerca o di ricerca ed esplorazione.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Solo per l'uso della libreria.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Solo per l'uso della libreria.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Descrive il connettore di ricerca.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifica la posizione di un'icona personalizzata per il connettore di ricerca.                                                                                                                      |
| [Collegamentoimmagine](search-schema-sconn-imagelink.md)                                         | Identifica la posizione di un'anteprima personalizzata per il connettore di ricerca.                                                                                                                 |
| [autore](search-schema-sconn-author.md)                                               | Identifica l'autore del connettore di ricerca.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Identifica la data di creazione del connettore di ricerca.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Specifica un tipo di cartella per il connettore di ricerca.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Specifica il provider di ricerca che deve essere usato da questo connettore di ricerca.                                                                                                                      |
| [ambito](search-schema-sconn-scope.md)                                                 | Specifica i percorsi da includere ed escludere dall'ambito di ricerca.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Specifica il percorso di un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basato su XML per questo connettore di ricerca. Il **IPropertyStore** supporta i metadati aperti del connettore di ricerca. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Specifica se la posizione rappresentata dal connettore di ricerca deve essere inclusa nell'ambito di ricerca del menu Start.                                                                 |
| [dominio](search-schema-sconn-domain.md)                                               | Identifica il dominio di primo livello del connettore di ricerca.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Specifica se il connettore di ricerca supporta la sintassi di query avanzata (AQS).                                                                                                            |
| [isIndexed](search-schema-sconn-isindexed.md)                                         | Specifica se la posizione rappresentata dal connettore di ricerca è indicizzata.                                                                                                          |



 

## <a name="examples-of-search-connector-description-files"></a>Esempi di file di descrizione del connettore di ricerca

Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un servizio Web di ricerca federata.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Di seguito è riportato un esempio di un file di descrizione del connettore di ricerca per un gestore di protocollo MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="additional-resources"></a>Risorse aggiuntive

-   Per ulteriori informazioni sullo schema di descrizione della libreria, vedere [Library Description schema](../shell/library-schema-entry.md).
-   Per altre informazioni sull'installazione di un connettore di ricerca, vedere [ricerca federata in Windows](-search-federated-search-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[OpenSearch](http://www.opensearch.org/Home)
</dt> <dt>

[Area download Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx)
</dt> </dl>

 

 
