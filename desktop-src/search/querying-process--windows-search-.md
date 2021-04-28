---
description: Processo di query in Windows Search
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Processo di query in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3585f2cca2a6d5d8548a85ae8fac759ec94b4fa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117329"
---
# <a name="querying-process-in-windows-search"></a>Processo di query in Windows Search

Questo argomento è organizzato come segue:

-   [Informazioni sull'esecuzione di query in Windows Search](#about-querying-in-windows-search)
    -   [Query locali e remote](#local-and-remote-queries)
    -   [Panoramica dell'API Query strutturata](#structured-query-api-overview)
-   [Scenari di query](#querying-scenarios)
    -   [Estrazione di condizioni e analisi delle query](#condition-extraction-and-query-parsing)
    -   [Esecuzione di query sull'indice](#querying-the-index)
-   [Argomenti correlati](#related-topics)

## <a name="about-querying-in-windows-search"></a>Informazioni sull'esecuzione di query in Windows Search

L'esecuzione di query Windows Search si basa sui quattro approcci seguenti:

-   [Sintassi di query](-search-3x-advancedquerysyntax.md) avanzata (AQS)
-   Sintassi di query naturali (NQS)
-   Structured Query Language (SQL)
-   Interfacce di query strutturate

AQS è la sintassi di query predefinita usata Windows Search query sull'indice e per perfezionare e limitare i parametri di ricerca. AQS è principalmente rivolto agli utenti e può essere usato dagli utenti per compilare query AQS, ma può anche essere usato dagli sviluppatori per compilare query a livello di codice. In Windows 7 è stato introdotto AQS canonico e deve essere usato per generare query AQS a livello di codice. In Windows 7 e versioni successive può essere disponibile un'opzione di menu di scelta rapida a seconda che sia soddisfatta una condizione AQS. Per altre informazioni, vedere "Recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata" in Creazione di gestori [del menu di scelta rapida.](../shell/context-menu-handlers.md) Le query AQS possono essere limitate a tipi specifici di file, noti come tipi di file. Per altre informazioni, vedere [Tipi di file e associazioni.](../shell/fa-intro.md) Per la documentazione di riferimento sulle proprietà pertinenti, vedere [System.Kind](../properties/props-system-kind.md)e [System.KindText.](../properties/props-system-kindtext.md)

NQS è una sintassi di query più disincisa rispetto ad AQS ed è simile al linguaggio umano. NQS può essere usato Windows Search eseguire query sull'indice se È selezionato NQS anziché il valore predefinito, AQS.

SQL è un linguaggio di testo che definisce le query. SQL è comune in molte tecnologie di database diverse. Windows Search usa SQL, implementa un subset di esso e lo estende aggiungendo elementi al linguaggio. Windows Search SQL estende la sintassi di query standard di database SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo. Tutte le funzionalità Windows Search SQL sono compatibili con Windows Search in Windows XP e Windows Server 2003 e versioni successive. Per altre informazioni su Windows Search SQL, vedere [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md)e Overview of Windows Search SQL [Syntax](-search-sql-ovwofsearchquery.md).

Le API di query strutturate sono descritte più avanti in questo argomento. Per la documentazione di riferimento sulle API di query strutturate, vedere [Querying Interfaces](-search-querying-interfaces-entry-page.md). Interfacce come [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) consentono di costruire stringhe SQL da un set di valori di input. Questa interfaccia converte le query utente AQS in Windows Search SQL e specifica le restrizioni di query che possono essere espresse in SQL ma non in AQS. [**ISearchQueryHelper ottiene**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) anche una OLE DB stringa di connessione per connettersi al database Windows Search.

### <a name="local-and-remote-queries"></a>Query locali e remote

È possibile eseguire le query in locale o in remoto. Nell'esempio seguente viene [illustrata una](-search-sql-from.md) query locale che usa la clausola FROM. Una query locale esegue una query solo sul catalogo SystemIndex locale.


```
FROM SystemIndex
```



Nell'esempio seguente viene illustrata una query remota che usa la clausola [FROM.](-search-sql-from.md) L'aggiunta di ComputerName trasforma l'esempio precedente in una query remota.


```
FROM [<ComputerName>.]SystemIndex
```



Per impostazione predefinita, Windows XP e Windows Server 2003 non Windows Search installati. Solo Windows Search 4 (WS4) fornisce il supporto delle query remote. Le versioni precedenti di Windows Desktop Search (WDS), ad esempio 3.01 e versioni precedenti, non supportano l'esecuzione di query remote. Con Esplora risorse è possibile eseguire una query sull'indice locale di un computer remoto per file system elementi (elementi gestiti dal protocollo "file:").

Per recuperare un elemento tramite query remota, l'elemento deve soddisfare i requisiti seguenti:

-   Essere accessibile tramite Universal Naming Convention (UNC).
-   Esiste nel computer remoto a cui il client ha accesso.
-   Impostare la sicurezza per consentire al client di avere accesso in lettura.

Esplora risorse include funzionalità per la condivisione di elementi, tra cui una condivisione "Pubblica" ( Computer pubblico ...) nel Centro connessioni di rete e condivisione e una condivisione \\ \\ \\ \\ "Utenti" ( Utenti computer \\ \\ \\ \\ ...) per gli elementi condivisi tramite la Condivisione guidata. Dopo aver condiviso le cartelle, è possibile eseguire una query sull'indice locale specificando il nome del computer remoto nella clausola FROM e un percorso UNC nel computer remoto nella clausola SCOPE. Nell'esempio seguente viene illustrata una query remota che usa le clausole FROM e SCOPE.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Gli esempi forniti qui usano SQL.

### <a name="structured-query-api-overview"></a>Panoramica dell'API Query strutturata

Una query strutturata consente di cercare informazioni in base a combinazioni booleane di query su singole proprietà. In questo argomento vengono descritte le funzionalità delle API e dei metodi di query strutturate più importanti. Per la documentazione di riferimento sulle API di query strutturate, vedere [Querying Interfaces](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

Il [**metodo IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analizza una stringa di input utente e produce un'interpretazione sotto forma [**di IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Se il *parametro pCustomProperties* di tale metodo non è Null, si tratta di un'enumerazione di oggetti [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (uno per ogni proprietà personalizzata riconosciuta). Gli altri [**metodi IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) consentono all'applicazione di impostare diverse opzioni, ad esempio impostazioni locali, uno schema, un word breaker e gestori per vari tipi di entità denominate. [**IQueryParser::GetSchemaProvider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) restituisce [**un'interfaccia ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) per l'esplorazione dello schema caricato.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution: IConditionFactory

[**L'interfaccia IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) fornisce tutte le informazioni sul risultato dell'analisi di una stringa di input. Poiché **IQuerySolution è** anche [**un'interfaccia IConditionFactory,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) è possibile creare altri nodi dell'albero delle condizioni. Il [**metodo IQuerySolution::GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) produce un albero delle condizioni per l'interpretazione. **Anche IQuerySolution::GetQuery** restituisce il tipo semantico.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory crea**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) nodi dell'albero delle condizioni. Se il *parametro simplify* di [**IConditionFactory::MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) è **VARIANT \_ TRUE,** l'oggetto [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) risultante viene semplificato e non deve essere un nodo di negazione. Se il *parametro pSubConditions* di [**IConditionFactory::MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) non è Null, tale parametro deve essere un'enumerazione di [**oggetti ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) e diventare sottoalberi. [**IConditionFactory::MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) costruisce un nodo foglia con un nome di proprietà, un'operazione e un valore specificati. La stringa nel *parametro pValueType* deve essere il nome di un tipo semantico dello schema. Se il *parametro expand* è **VARIANT \_ TRUE** e la proprietà è virtuale, l'albero delle condizioni risultante è in genere una disgiunzione risultante dall'espansione della proprietà ai costituenti definiti. Se non è Null, i parametri *pPropertyNameTerm*, *pOperatorTerm* e *pValueTerm* devono identificare i termini che indicano la proprietà, l'operazione e il valore.

### <a name="icondition--ipersiststream"></a>ICondition: IPersistStream

[**L'interfaccia ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) è un singolo nodo in un albero delle condizioni. Il nodo può essere un nodo di negazione, un nodo AND, un nodo OR o un nodo foglia. Per un nodo non foglia [**ICondition::GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) restituisce un'enumerazione dei sottoalberi. Per un nodo foglia, i metodi seguenti di [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) restituiscono i valori seguenti:

-   [**GetComparisonInfo restituisce**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) il nome, l'operazione e il valore della proprietà.
-   [**GetValueType**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) restituisce il tipo semantico del valore, specificato nel parametro *pszValueType* di [**IConditionFactory::MakeLeaf.**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf)
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) restituisce una forma stringa del valore. Se il valore era già una stringa, questo formato verrà normalizzato per quanto riguarda la distinzione tra maiuscole e minuscole, gli accenti e così via.
-   [**GetInputTerms restituisce**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) informazioni sulle parti della frase di input che hanno generato il nome della proprietà, l'operazione e il valore.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) restituisce una copia completa di un albero delle condizioni.

### <a name="irichchunk"></a>IRichChunk

Ogni [**oggetto IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifica un intervallo di token e una stringa. **IRichChunk è** un'interfaccia di utilità che rappresenta informazioni su un intervallo (in genere un intervallo di token) identificato da una posizione iniziale e da una lunghezza. Queste informazioni sull'intervallo includono una stringa e/o **una VARIANT.**

### <a name="iconditiongenerator"></a>IConditionGenerator

[**L'interfaccia IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) viene fornita dall'applicazione per gestire il riconoscimento e la generazione dell'albero delle condizioni per un tipo di entità denominato. Un generatore di condizioni viene assegnato a [**un IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) [**tramite IQueryParser::SetMultiOption.**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption) [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) chiama [**IConditionGenerator::Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) con [**un oggetto ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) per lo schema attualmente caricato. Questa operazione consente [**a IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) di ottenere le informazioni sullo schema necessarie. Quando si analizza una stringa di input, **IQueryParser** chiama il metodo [**IConditionGenerator::RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) di ogni [**IConditionGenerator,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)in modo che l'occorrenza di entità denominate riconosciute nella stringa di input possa essere segnalata. **IQueryParser** può usare le impostazioni locali correnti e deve usare la tokenizzazione dell'input perché deve segnalare gli intervalli di token di qualsiasi entità denominata.

Quando [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) sta per generare un nodo foglia e il tipo semantico del valore corrisponde al tipo di entità denominato per [**IConditionGenerator,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) **IQueryParser** chiama [**IConditionGenerator::GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) con le informazioni per il nodo da generare. Se [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) restituisce S OK, deve restituire un albero delle condizioni (che non deve essere un nodo foglia) e indicare \_ a **IQueryParser** se eliminare l'interpretazione di stringa alternativa che normalmente genererebbe come precauzione.

### <a name="itokencollection"></a>ITokenCollection

Il [**metodo ITokenCollection::NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) restituisce il numero di token. [**ITokenCollection::GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) restituisce informazioni sul token *i* th. L'inizio e la lunghezza sono posizioni di caratteri nella stringa di input. Il testo restituito sarà diverso da Null solo se è presente un testo che esegue l'override dei caratteri della stringa di input. Viene usato, ad esempio, per eseguire l'override di un trattino nella stringa di input con NOT quando tale trattino si trova in un contesto in cui deve essere interpretato come negazione.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) chiama [**INamedEntityCollector::Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) per ogni entità denominata riconosciuta. Gli intervalli sono intervalli di token. Deve sempre essere il caso in cui *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* ed *endSpan* possono differire da *beginActual* ed *endActual* se l'entità denominata inizia e/o termina con token semanticamente non significativi, ad esempio le virgolette (che sono comunque coperte dall'entità denominata). Il valore deve essere espresso come stringa e verrà successivamente visualizzato in una chiamata a [**IConditionGenerator::GenerateForLeaf.**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf)

### <a name="ischemaprovider"></a>ISchemaProvider

[**L'interfaccia ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) può essere usata per cercare entità (tipi) e relazioni (proprietà) in uno schema caricato. Ecco cosa fanno i singoli metodi:

-   [**Entities**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) restituisce un'enumerazione di ogni entità ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) nello schema.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) restituisce l'entità radice dello schema. Per uno schema flat, viene restituito il tipo principale di [**ogni oggetto IQuerySolution.**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)
-   [**GetEntity trova**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) un'entità in base al nome e restituisce S FALSE se tale \_ entità non è presente nello schema.
-   [**MetaData**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) restituisce un'enumerazione [**di interfacce IMetaData.**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata)

### <a name="ientity"></a>IEntity

[**L'interfaccia IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) è un'entità dello schema che rappresenta un tipo con un nome, ha una serie di relazioni denominate con altri tipi (proprietà) e deriva da un'entità di base. Ecco cosa fanno i singoli metodi:

-   [**IEntity::Relationships restituisce**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) un'enumerazione di [**oggetti IRelationship,**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) uno per ogni relazione in uscita di questo tipo. Ogni relazione in uscita di un'entità ha un nome.
-   [**IEntity::GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) trova una relazione in base al nome e restituisce S FALSE se tale relazione non esiste \_ per questa entità.
-   [**IEntity::MetaData**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) restituisce un'enumerazione [**di interfacce IMetaData,**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) una per ogni coppia di metadati di questa entità.
-   [**IEntity::D efaultPhrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) restituisce una frase predefinita per facilitare la generazione di una riformazione AQS o NQS di un albero delle condizioni.

### <a name="irelationship"></a>IRelationship

[**L'interfaccia IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) rappresenta una relazione tra due entità: un'origine e una destinazione. Ecco cosa fanno i singoli metodi:

-   [**IRelationship::IsReal indica**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) se una relazione è reale. Ad esempio, se l'entità A deriva dall'entità B ed eredita una relazione denominata R da essa, A può comunque avere una propria relazione denominata R. Tuttavia, le relazioni A e R devono avere lo stesso tipo di destinazione di B e l'unico motivo per cui esiste è archiviare i metadati specifici di B. Si dice che una relazione di questo tipo di B non sia reale.
-   [**IRelationship::Medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) restituisce un'enumerazione di [**interfacce IMetaData,**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) una per ogni coppia di metadati di questa entità.
-   [**IRelationship::D efaultPhrase restituisce**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) la frase predefinita da usare per questa relazione nelle restatements. Ogni relazione ha una frase predefinita che la denota per facilitare la generazione di un'istanza AQS o NQS di un albero delle condizioni.

### <a name="imetadata"></a>IMetaData

I metadati sono coppie chiave-valore associate a un'entità, a una relazione o all'intero schema. Poiché le chiavi non sono necessariamente univoche, una raccolta di metadati può essere pensata come una mappa multipla. [**IMetaData::GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) viene chiamato per recuperare la chiave e il valore per una coppia di metatdata.

## <a name="querying-scenarios"></a>Scenari di query

Gli scenari seguenti descrivono l'uso delle API di query strutturate in Windows Search in scenari di query comuni, ad esempio la creazione di un albero delle condizioni e l'esecuzione di query sull'indice.

### <a name="condition-extraction-and-query-parsing"></a>Estrazione di condizioni e analisi delle query

Quando viene creata una query, il relativo ambito viene definito indicando al sistema dove eseguire la ricerca. In questo modo si limitano i risultati della ricerca. Dopo aver definito l'ambito, viene applicato un filtro e viene restituito un set di filtri. I risultati della ricerca sono limitati creando un albero delle condizioni con nodi foglia, in modo simile a un grafo. Tali condizioni vengono quindi estratte. Un albero delle condizioni è una combinazione booleana (AND, OR, NOT) di condizioni foglia, ognuna delle quali mette in relazione una proprietà, tramite un'operazione, a un valore. Un nodo foglia rappresenta una restrizione su una singola proprietà a un valore tramite alcune operazioni.

Una restrizione di filtro richiede un'espressione logica che descrive la restrizione. La definizione di questa espressione inizia con [**l'interfaccia ICondition,**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) usata per creare un singolo nodo in un albero delle condizioni. Poiché nell'esempio seguente è presente una sola condizione, l'albero non cambia.


```C++
    
    [
        object,
        uuid(0FC988D4-C935-4b97-A973-46282EA175C8),
        pointer_default(unique)
    ]
    interface ICondition : IPersistStream
    {
        HRESULT GetConditionType([out, retval] CONDITION_TYPE* pNodeType);
        HRESULT GetSubConditions([in] REFIID riid, [out, retval, iid_is(riid)] void** ppv);
        [local] HRESULT GetComparisonInfo([out, annotation("__deref_opt_out")] LPWSTR *ppszPropertyName, [out, annotation("__out_opt")] CONDITION_OPERATION *pOperation, [out, annotation("__out_opt")] PROPVARIANT *pValue);
        HRESULT GetValueType([out, retval] LPWSTR* ppszValueTypeName);
        HRESULT GetValueNormalization([out, retval] LPWSTR* ppszNormalization);
        [local] HRESULT GetInputTerms([out, annotation("__out_opt")] IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] IRichChunk** ppValueTerm);
        HRESULT Clone([out, retval] ICondition** ppc);
    };


```



Se è presente più di una condizione di filtro, and e altri operatori booleani vengono usati per ottenere un singolo albero. Gli alberi AND e OR rappresentano congiunzioni e disgiunzioni dei relativi sottoalberi. Un albero NOT rappresenta la negazione del relativo singolo sottoalbero. AQS offre un approccio di testo per ottenere espressioni logiche con operatori booleani ed è spesso più semplice.

Nell'esempio successivo l'albero delle condizioni ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) viene convertito in formato visivo. Il parser di query, che usa [**l'interfaccia IQueryParser,**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) converte [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) in una stringa di query RTF (Rich Text Formatted). Il [**metodo IQueryParser::RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) restituisce il testo della query, mentre il metodo [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) produce [**un'interfaccia IQuerySolution.**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) Nell'esempio seguente viene illustrato come eseguire tutte queste operazioni.


```C++
    [
        object,
        uuid(2EBDEE67-3505-43f8-9946-EA44ABC8E5B0),
        pointer_default(unique)
    ]
    interface IQueryParser : IUnknown
    {
        HRESULT Parse([in] LPCWSTR pszInputString, [in] IEnumUnknown* pCustomProperties, [out, retval] IQuerySolution** ppSolution);
        HRESULT SetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetOption([in] STRUCTURED_QUERY_SINGLE_OPTION option, [out, retval] PROPVARIANT* pOptionValue);
        HRESULT SetMultiOption([in] STRUCTURED_QUERY_MULTIOPTION option, [in] LPCWSTR pszOptionKey, [in] PROPVARIANT const* pOptionValue);
        HRESULT GetSchemaProvider([out, retval] ISchemaProvider** ppSchemaProvider);
        HRESULT RestateToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszQueryString);
        HRESULT ParsePropertyValue([in] LPCWSTR pszPropertyName, [in] LPCWSTR pszInputString, [out, retval] IQuerySolution** ppSolution);
        HRESULT RestatePropertyValueToString([in] ICondition* pCondition, [in] BOOL fUseEnglish, [out] LPWSTR* ppszPropertyName, [out] LPWSTR* ppszQueryString);
    };

```



L'input principale di [**IQueryParser::P arse**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) è una stringa di input utente da analizzare, ma l'applicazione può anche informare il parser di query di tutte le proprietà riconosciute nell'input (dalla sintassi specifica dell'applicazione). L'output **di IQueryParser::P arse** è un [**oggetto IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)che fornisce tutte le informazioni relative a tale chiamata di analisi. Sono disponibili metodi per ottenere la stringa di input, il modo in cui la stringa di input è stata tokenizzata, eventuali errori di analisi e la query analizzata come albero delle condizioni, rappresentato da [**un ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). L'esempio seguente mostra ...


```C++
    [
        object,
        uuid(D6EBC66B-8921-4193-AFDD-A1789FB7FF57),
        pointer_default(unique)
    ]
    interface IQuerySolution : IConditionFactory
    {
        [local] HRESULT GetQuery([out, annotation("__out_opt")] ICondition** ppQueryNode, [out, annotation("__out_opt")] IEntity** ppMainType);
        HRESULT GetErrors([in] REFIID riid, [out, retval, iid_is(riid)] void** ppParseErrors);
        [local] HRESULT GetLexicalData([out, annotation("__deref_opt_out")] LPWSTR* ppszInputString, [out, annotation("__out_opt")] ITokenCollection** ppTokens, [out, annotation("__out_opt")] LCID* pLocale, [out, annotation("__out_opt")] IUnknown** ppWordBreaker);
    }    

    

```



Nell'esempio [**precedente, IQuerySolution::GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) può ottenere informazioni sulla query, inclusi il testo originale, i token che costituiscono il testo o l'albero delle condizioni. Nella tabella seguente sono elencati esempi di possibili valori di query restituiti.



| Esempi di valori di query restituiti                        | Descrizione                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Testo della query [**restituito da IQueryParser::RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | L'interruzione dei token                                                                                  |
| ![un albero delle condizioni non risolto](images/queryvalues1.png) | Albero delle condizioni non risolto                                                                              |



 

L'albero delle condizioni iniziale restituito non è stato risolto. In un albero delle condizioni non risolto, i riferimenti a data e ora, ad esempio , non `date:yesterday` vengono convertiti in ora assoluta. Inoltre, le proprietà virtuali non vengono espanse. Le proprietà virtuali sono proprietà che fungono da aggregazioni di più proprietà.

Ad esempio, la query `kind:email from:reljai` produce gli alberi delle condizioni non risolti e risolti seguenti. L'albero delle condizioni non risolto si trova a sinistra e l'albero delle condizioni risolto si trova a destra.

![alberi delle condizioni non risolti e risolti](images/conditiontree.png)

L'albero risolto può essere ottenuto chiamando [**IConditionFactory::Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Tuttavia, il passaggio [**di SQRO \_ DONT \_ RESOLVE \_ DATETIME**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) lascia la data e l'ora non risolte. Esistono vantaggi per un albero delle condizioni non risolto, perché un albero delle condizioni non risolto contiene informazioni sulla query. Ogni nodo foglia punta ai token restituiti da [**IQuerySolution::GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), che corrispondono alla proprietà, all'operatore e al valore quando si usa [**l'interfaccia IRichChunk.**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) L'esempio seguente mostra ...


```C++
    interface ITokenCollection : IUnknown
    {
        HRESULT NumberOfTokens(ULONG* pCount);
        HRESULT GetToken([in] ULONG i, [out, annotation("__out_opt")] ULONG* pBegin, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz);
    };

ICondition:: GetInputTerms([out, annotation("__out_opt")] 
IRichChunk** ppPropertyTerm, [out, annotation("__out_opt")] 
IRichChunk** ppOperationTerm, [out, annotation("__out_opt")] 
IRichChunk** ppValueTerm);

    interface IRichChunk : IUnknown
    {
        HRESULT GetData([out, annotation("__out_opt")] ULONG* pFirstPos, [out, annotation("__out_opt")] ULONG* pLength, [out, annotation("__deref_opt_out")] LPWSTR* ppsz, [out, annotation("__out_opt")] PROPVARIANT* pValue);
    }
```



### <a name="querying-the-index"></a>Esecuzione di query sull'indice

Esistono diversi approcci all'esecuzione di query sull'indice. Alcuni sono basati su SQL e altri si basano su AQS. È anche possibile eseguire query sull'indice Windows Search a livello di codice usando [le interfacce di query](./-search-querying-interfaces-entry-page.md). Esistono tre interfacce specifiche per l'esecuzione di query sull'indice: [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)e [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Per informazioni concettuali, vedere [Esecuzione di query sull'indice a livello di codice.](-search-3x-wds-qryidx-overview.md)

È possibile sviluppare un componente o una classe helper per eseguire query sull'indice usando [**l'interfaccia ISearchQueryHelper.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2)**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)e viene ottenuta chiamando [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Per informazioni concettuali, vedere [Esecuzione di query sull'indice con ISearchQueryHelper.](-search-3x-wds-qryidx-searchqueryhelper.md)

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) consente di:

-   Ottenere una OLE DB di connessione per connettersi al database Windows Search dati.
-   Convertire query utente AQS in Windows Search SQL.
-   Specificare restrizioni di query che possono essere espresse in SQL ma non in AQS.

Gli eventi di priorità e set di righe di indicizzazione sono supportati in Windows 7 e versioni successive. Con [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) esiste uno stack di priorità che consente al client di richiedere che agli ambiti usati in una determinata query sia assegnato un livello superiore alla priorità normale. [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) fornisce la notifica delle modifiche agli elementi nei set di righe, tra cui l'aggiunta di nuovi elementi, l'eliminazione di elementi e la modifica dei dati degli elementi. L'uso delle notifiche degli eventi del set di righe garantisce che i risultati per le query esistenti siano il più aggiornati possibile. Per informazioni concettuali, vedere Indicizzazione di priorità ed eventi di set di [righe in Windows 7.](indexing-prioritization-and-rowset-events.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Elementi inclusi nell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di notifica in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisiti di formattazione url](url-formatting-requirements.md)
</dt> </dl>

 

 
