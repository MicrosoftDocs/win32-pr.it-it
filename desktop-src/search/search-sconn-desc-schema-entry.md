---
description: Introduce lo schema di descrizione del connettore di ricerca usato dalle librerie Windows Explorer e dai provider di ricerca federati.
ms.assetid: b85a04c6-9398-4cc7-a894-881216600203
title: Schema di descrizione del connettore di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8d8ab60ba472cca961a4208b1c551679ef93eacd46e07cf5e080a3e73f3d14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226382"
---
# <a name="search-connector-description-schema"></a>Schema di descrizione del connettore di ricerca

Introduce lo schema di descrizione del connettore di ricerca usato dalle librerie Windows Explorer e dai provider di ricerca federati. Lo schema specifica la struttura e i requisiti per i file di descrizione del connettore di ricerca (.searchConnector-ms) e per gli elementi searchConnectorDescriptionType dei file di descrizione della libreria shell \*  \* (.library-ms).

Questo argomento descrive lo schema correlato ai connettori di ricerca federati. Per altre informazioni sulle librerie e sullo schema di descrizione della libreria, vedere [Schema di descrizione della libreria.](../shell/library-schema-entry.md)

Questo argomento include le sezioni seguenti:

-   [Che cosa sono i connettori di ricerca?](#what-are-search-connectors)
-   [Come funzionano i file di descrizione del connettore di ricerca?](#search-connector-description-schema)
-   [Che cos'è lo schema di descrizione del connettore di ricerca?](#what-is-the-search-connector-description-schema)
-   [Quali sono le parti principali dello schema?](#what-are-the-major-parts-of-the-schema)
-   [Esempi di file di descrizione del connettore di ricerca](#examples-of-search-connector-description-files)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="what-are-search-connectors"></a>Che cosa sono i connettori di ricerca?

I connettori di ricerca connettono gli utenti ai dati archiviati in servizi Web o posizioni di archiviazione remota. Con Windows 7, gli utenti possono installare i connettori di ricerca per le posizioni, ad esempio i servizi Web, in modo da eseguire ricerche in tali percorsi direttamente da Windows Explorer. I connettori di ricerca sono file di descrizione del connettore di ricerca (.searchConnector-ms) che specificano come connettersi, inviare query a e ricevere \* risultati dalla posizione.

Oltre ai servizi Web, i connettori di ricerca possono essere usati per cercare gli ambiti dell'indice locale creati dai gestori di protocollo. Ad esempio, gli utenti possono cercare la posta elettronica indicizzata in locale con il gestore del protocollo MAPI usando un connettore di ricerca per tale archivio di posta elettronica.

## <a name="how-do-search-connector-description-files-work"></a>Come funzionano i file di descrizione del connettore di ricerca?

Quando i file di descrizione del connettore di ricerca sono installati nei sistemi degli utenti, gli utenti possono aprire Windows Explorer, fare clic sul connettore di ricerca nel riquadro di spostamento e immettere una query di ricerca. Windows Explorer invia la query usando le informazioni del file di descrizione del connettore di ricerca, ad esempio il provider da usare e l'ambito della ricerca. I risultati vengono restituiti come elementi feed RSS o Atom e visualizzati agli utenti come se fossero normali elementi della shell.

La modalità di distribuzione del file di descrizione del connettore di ricerca dipende dal tipo di posizione supportato dal connettore di ricerca:

-   In un OpenSearch file di configurazione (con estensione \* osdx) per il servizio Web
-   Come parte dell'installazione del gestore di protocollo

Quando un utente apre il file con estensione osdx o installa il gestore del protocollo, è necessario assicurarsi che si verifica quanto segue:

-   Il file con estensione searchconnector-ms viene creato nella cartella ricerche Windows **utenti** (%userprofile%/Searches).
-   Viene creato un collegamento al file .searchconnector-ms nella cartella **Collegamenti** degli utenti (%userprofile%/Links).

## <a name="what-is-the-search-connector-description-schema"></a>Che cos'è lo schema di descrizione del connettore di ricerca?

Lo schema di descrizione del connettore di ricerca è uno schema XML che definisce la struttura dei file di descrizione del connettore di ricerca \* (.searchConnector-ms). Ogni connettore di ricerca deve avere un file di descrizione del connettore di ricerca che specifica come connettersi, inviare query a e ricevere risultati dalla posizione.

## <a name="what-are-the-major-parts-of-the-schema"></a>Quali sono le parti principali dello schema?

Nella tabella seguente sono elencate le parti principali dello schema.



| Elementi figlio                                                                         | Descrizione                                                                                                                                                                             |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [isSearchOnlyItem](search-schema-sconn-issearchonlyitem.md)                           | Identifica se i percorsi supportati dal connettore di ricerca sono di sola ricerca o ricerca ed esplorazione.                                                                                |
| [isDefaultSaveLocation](search-schema-sconn-isdefaultsavelocation.md)                 | Solo per uso di librerie.                                                                                                                                                                   |
| [isDefaultNonOwnerSaveLocation](search-schema-sconn-isdefaultnonownersavelocation.md) | Solo per uso di librerie.                                                                                                                                                                   |
| [description](search-schema-sconn-description.md)                                     | Descrive il connettore di ricerca.                                                                                                                                                         |
| [iconReference](search-schema-sconn-iconreference.md)                                 | Identifica la posizione di un'icona personalizzata per il connettore di ricerca.                                                                                                                      |
| [imageLink](search-schema-sconn-imagelink.md)                                         | Identifica la posizione di un'anteprima personalizzata per il connettore di ricerca.                                                                                                                 |
| [Autore](search-schema-sconn-author.md)                                               | Identifica l'autore del connettore di ricerca.                                                                                                                                          |
| [dateCreated](search-schema-sconn-datecreated.md)                                     | Identifica la data di creazione del connettore di ricerca.                                                                                                                              |
| [templateInfo](search-schema-sconn-templateinfo.md)                                   | Specifica un tipo di cartella per il connettore di ricerca.                                                                                                                                       |
| [locationProvider](search-schema-sconn-locationprovider.md)                           | Specifica il provider di ricerca che deve essere usato da questo connettore di ricerca.                                                                                                                      |
| [ambito](search-schema-sconn-scope.md)                                                 | Specifica i percorsi da includere ed escludere dall'ambito di ricerca.                                                                                                                |
| [propertyStore](search-schema-sconn-propertystore.md)                                 | Specifica il percorso di un [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) basato su XML per questo connettore di ricerca. **IPropertyStore supporta** i metadati aperti del connettore di ricerca. |
| [includeInStartMenuScope](search-schema-sconn-includeinstartmenuscope.md)             | Specifica se la posizione rappresentata dal connettore di ricerca deve essere inclusa nell'menu Start di ricerca dell'applicazione.                                                                 |
| [Dominio](search-schema-sconn-domain.md)                                               | Identifica il dominio di primo livello del connettore di ricerca.                                                                                                                                     |
| [supportsAdvancedQuerySyntax](search-schema-sconn-supportsadvancedquerysyntax.md)     | Specifica se il connettore di ricerca supporta la sintassi AQS (Advanced Query Syntax).                                                                                                            |
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

-   Per altre informazioni sullo schema di descrizione della libreria, vedere [Schema di descrizione della libreria.](../shell/library-schema-entry.md)
-   Per altre informazioni sull'installazione di un connettore di ricerca, vedere [Ricerca federata in Windows](-search-federated-search-overview.md).

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

 

 
