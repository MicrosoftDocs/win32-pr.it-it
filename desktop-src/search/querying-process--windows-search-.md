---
description: .
ms.assetid: 0e5a633e-1703-4b72-8a04-6da71aec0ae2
title: Esecuzione di query sul processo in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92d868cb843e96b04d6b4bd575284638b6652ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750346"
---
# <a name="querying-process-in-windows-search"></a>Esecuzione di query sul processo in Windows Search

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulle query in Windows Search](#about-querying-in-windows-search)
    -   [Query locali e remote](#local-and-remote-queries)
    -   [Panoramica dell'API di query strutturata](#structured-query-api-overview)
-   [Esecuzione di query sugli scenari](#querying-scenarios)
    -   [Estrazione della condizione e analisi delle query](#condition-extraction-and-query-parsing)
    -   [Esecuzione di query sull'indice](#querying-the-index)
-   [Argomenti correlati](#related-topics)

## <a name="about-querying-in-windows-search"></a>Informazioni sulle query in Windows Search

L'esecuzione di query in Windows Search si basa sui quattro approcci seguenti:

-   [Sintassi di query avanzate](-search-3x-advancedquerysyntax.md) (AQS)
-   Sintassi di query naturali (NQS)
-   Structured Query Language (SQL)
-   Interfacce di query strutturate

AQS è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca. AQS è destinato principalmente all'utente e può essere usato dagli utenti per compilare query AQS, ma può anche essere usato dagli sviluppatori per compilare query a livello di codice. In Windows 7 è stato introdotto il AQS canonico e deve essere usato per generare query AQS a livello di codice. In Windows 7 e versioni successive, può essere disponibile un'opzione di menu di scelta rapida a seconda che venga soddisfatta una condizione AQS. Per ulteriori informazioni, vedere "recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata" nella sezione [creazione di gestori di menu di scelta rapida](../shell/context-menu-handlers.md). Le query AQS possono essere limitate a specifici tipi di file, noti come tipi di file. Per altre informazioni, vedere [tipi di file e associazioni](../shell/fa-intro.md). Per la documentazione di riferimento sulle proprietà pertinenti, vedere [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).

NQS è una sintassi di query più rilassata rispetto a AQS ed è simile al linguaggio umano. NQS può essere usato da Windows Search per eseguire una query sull'indice se è selezionato NQS anziché il valore predefinito AQS.

SQL è un linguaggio testuale che definisce le query. SQL è comune in molte tecnologie di database diverse. Windows Search USA SQL, ne implementa un subset e lo estende aggiungendo elementi al linguaggio. Windows Search SQL estende la sintassi di query di database standard SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo. Tutte le funzionalità di Windows Search SQL sono compatibili con Windows Search in Windows XP e Windows Server 2003 e versioni successive. Per ulteriori informazioni su Windows Search SQL, vedere [esecuzione di query sull'indice con la sintassi SQL di ricerca](-search-sql-windowssearch-entry.md)di Windows e [Panoramica della sintassi SQL di Windows Search](-search-sql-ovwofsearchquery.md).

Le API di query strutturate sono descritte più avanti in questo argomento. Per la documentazione di riferimento sulle API di query strutturate, vedere [query sulle interfacce](-search-querying-interfaces-entry-page.md). Le interfacce come [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) consentono di costruire stringhe SQL da un set di valori di input. Questa interfaccia converte le query utente AQS in Windows Search SQL e specifica le restrizioni di query che possono essere espresse in SQL ma non in AQS. [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) ottiene anche una stringa di connessione OLE DB per la connessione al database di Windows Search.

### <a name="local-and-remote-queries"></a>Query locali e remote

È possibile eseguire le query in locale o in remoto. Nell'esempio seguente viene illustrata una query locale che usa la [clausola from](-search-sql-from.md) . Una query locale esegue una query solo nel catalogo SystemIndex locale.


```
FROM SystemIndex
```



Nell'esempio seguente viene illustrata una query remota che usa la [clausola from](-search-sql-from.md) . L'aggiunta di ComputerName trasforma l'esempio precedente in una query remota.


```
FROM [<ComputerName>.]SystemIndex
```



Per impostazione predefinita, Windows XP e Windows Server 2003 non hanno installato Windows Search. Solo Windows Search 4 (WS4) fornisce il supporto per le query remote. Le versioni precedenti di Windows Desktop Search (WDS), ad esempio 3,01 e versioni precedenti, non supportano l'esecuzione di query remote. Con Esplora risorse è possibile eseguire una query sull'indice locale di un computer remoto per file system elementi (elementi gestiti dal protocollo "file:").

Per recuperare un elemento in base a una query remota, è necessario che l'elemento soddisfi i requisiti seguenti:

-   Essere accessibile tramite il percorso Universal Naming Convention (UNC).
-   Esistere nel computer remoto a cui il client ha accesso.
-   Impostare la sicurezza per consentire al client di disporre dell'accesso in lettura.

Esplora risorse include funzionalità per la condivisione di elementi, tra cui una condivisione "pubblica" ( \\ \\ computer \\ pubblico \\ ...) nel **centro di rete e condivisione** e una condivisione "Users" ( \\ \\ \\ utenti computer \\ ...) per gli elementi condivisi tramite la procedura guidata di condivisione. Una volta condivise le cartelle, è possibile eseguire una query sull'indice locale specificando il nome computer del computer remoto nella clausola FROM e un percorso UNC nel computer remoto nella clausola SCOPE. Nell'esempio seguente viene illustrata una query remota che usa le clausole FROM e SCOPE.


```
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>' 
```



Gli esempi forniti qui usano SQL.

### <a name="structured-query-api-overview"></a>Panoramica dell'API di query strutturata

Una query strutturata consente di cercare le informazioni in base a combinazioni booleane di query su singole proprietà. In questo argomento viene illustrata la funzionalità delle API e dei metodi di query strutturati più importanti. Per la documentazione di riferimento sulle API di query strutturate, vedere [query sulle interfacce](-search-querying-interfaces-entry-page.md).

### <a name="iqueryparser"></a>IQueryParser

Il metodo [**IQueryParser::P ass**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) analizza una stringa di input dell'utente e produce un'interpretazione sotto forma di [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution). Se il parametro *pCustomProperties* di tale metodo non è null, è un'enumerazione di oggetti [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) (uno per ogni proprietà personalizzata riconosciuta). Gli altri metodi [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) consentono all'applicazione di impostare diverse opzioni, ad esempio impostazioni locali, uno schema, un Word breaker e gestori per vari tipi di entità denominate. [**IQueryParser:: GetSchemaProvider**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-getschemaprovider) restituisce un'interfaccia [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) per l'esplorazione dello schema caricato.

### <a name="iquerysolution--iconditionfactory"></a>IQuerySolution : IConditionFactory

L'interfaccia [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) fornisce tutte le informazioni sul risultato dell'analisi di una stringa di input. Poiché **IQuerySolution** è anche un'interfaccia [**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) , è possibile creare ulteriori nodi dell'albero delle condizioni. Il metodo [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) produce un albero delle condizioni per l'interpretazione. **IQuerySolution:: GetQuery** restituisce anche il tipo semantico.

### <a name="iconditionfactory"></a>IConditionFactory

[**IConditionFactory**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory) crea nodi dell'albero delle condizioni. Se il parametro *semplificato* di [**IConditionFactory:: MakeNot**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makenot) è **Variant \_ true**, il [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) risultante è semplificato e non deve essere un nodo di negazione. Se il parametro *pSubConditions* di [**IConditionFactory:: MakeAndOr**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeandor) non è null, tale parametro deve essere un'enumerazione di oggetti [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) e diventare sottoalberi. [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf) costruisce un nodo foglia con un nome, un'operazione e un valore di proprietà specificati. La stringa nel parametro *pValueType* deve corrispondere al nome di un tipo semantico dello schema. Se il parametro *expand* è **Variant \_ true** e la proprietà è virtuale, l'albero delle condizioni risultante è in genere una disgiunzione risultante dall'espansione della proprietà nei relativi componenti definiti. Se non è null, i parametri *pPropertyNameTerm*, *pOperatorTerm* e *pValueTerm* devono identificare i termini che indicano la proprietà, l'operazione e il valore.

### <a name="icondition--ipersiststream"></a>ICondition: IPersistStream

L'interfaccia [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) è un singolo nodo in un albero delle condizioni. Il nodo può essere un nodo di negazione, un nodo, un nodo o un nodo foglia. Per un nodo non foglia [**ICondition:: GetSubConditions**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getsubconditions) restituisce un'enumerazione dei sottoalberi. Per un nodo foglia i seguenti metodi di [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) restituiscono i valori seguenti:

-   [**GetComparisonInfo**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getcomparisoninfo) restituisce il nome della proprietà, l'operazione e il valore.
-   [**Getvaluetype**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluetype) restituisce il tipo semantico del valore, che è stato specificied nel parametro *pszValueType* di [**IConditionFactory:: MakeLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-makeleaf).
-   [**GetValueNormalization**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getvaluenormalization) restituisce un formato stringa del valore. Se il valore è già una stringa, il form verrà normalizzato in relazione a maiuscole e minuscole, accenti e così via.
-   [**GetInputTerms**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-getinputterms) restituisce informazioni sulle parti della frase di input che hanno generato il nome della proprietà, l'operazione e il valore.
-   [**Clone**](/windows/desktop/api/structuredquerycondition/nf-structuredquerycondition-icondition-clone) restituisce una copia completa di un albero delle condizioni.

### <a name="irichchunk"></a>IRichChunk

Ogni oggetto [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) identifica un intervallo di token e una stringa. **IRichChunk** è un'interfaccia di utilità che rappresenta le informazioni su un intervallo (in genere un intervallo di token) identificato da una posizione e una lunghezza iniziali. Queste informazioni sull'intervallo includono una stringa e/o una **variante**.

### <a name="iconditiongenerator"></a>IConditionGenerator

L'interfaccia [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) viene fornita dall'applicazione per gestire la generazione dell'albero delle condizioni e del riconoscimento per un tipo di entità denominato. Un generatore di condizione viene assegnato a un [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) tramite [**IQueryParser:: SetMultiOption**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-setmultioption). [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) chiama [**IConditionGenerator:: Initialize**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-initialize) con un [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) per lo schema attualmente caricato. Questa operazione consente a [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) di ottenere le informazioni sullo schema necessarie. Quando si analizza una stringa di input, **IQueryParser** chiama il metodo [**IConditionGenerator:: RecognizeNamedEntities**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-recognizenamedentities) di ogni [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), in modo che sia possibile segnalare l'occorrenza delle entità denominate riconosciute nella stringa di input. **IQueryParser** è in grado di utilizzare le impostazioni locali correnti e di utilizzare la suddivisione in token dell'input perché deve segnalare gli intervalli di token di qualsiasi entità denominata.

Quando [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) sta per emettere un nodo foglia e il tipo semantico del valore corrisponde al tipo di entità denominato per un [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator), **IQueryParser** chiama [**IConditionGenerator:: GenerateforLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf) con le informazioni relative al nodo da generare. Se il [**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) restituisce S \_ OK, deve restituire un albero delle condizioni (che non deve essere un nodo foglia) e informare **IQueryParser** se annullare l'interpretazione della stringa alternativa che verrebbe normalmente generata come precauzione.

### <a name="itokencollection"></a>ITokenCollection

Il metodo [**ITokenCollection:: NumberOfTokens**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-numberoftokens) restituisce il numero di token. [**ITokenCollection:: GetToken**](/windows/desktop/api/Structuredquery/nf-structuredquery-itokencollection-gettoken) restituisce informazioni sul token *i* th. L'inizio e la lunghezza sono posizioni dei caratteri nella stringa di input. Il testo restituito sarà non null solo se è presente un testo che esegue l'override dei caratteri dalla stringa di input. Viene usato, ad esempio, per eseguire l'override di un trattino nella stringa di input senza quando tale trattino si trova in un contesto in cui deve essere interpretato come una negazione.

### <a name="inamedentitycollector"></a>INamedEntityCollector

[**IConditionGenerator**](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator) chiama [**INamedEntityCollector:: Add**](/windows/desktop/api/Structuredquery/nf-structuredquery-inamedentitycollector-add) per ogni entità denominata riconosciuta. Gli intervalli sono intervalli di token. Deve sempre essere il caso *beginSpan* ? *beginActual*  <  *endActual* ? *endSpan*. *beginSpan* e *endSpan* possono differire da *beginActual* e *endActual* se l'entità denominata inizia e/o termina con token semanticamente non significativi, ad esempio virgolette (che sono comunque coperte dall'entità denominata). Il valore deve essere espresso come stringa e successivamente verrà visualizzato in una chiamata a [**IConditionGenerator:: GenerateForLeaf**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditiongenerator-generateforleaf).

### <a name="ischemaprovider"></a>ISchemaProvider

L'interfaccia [**ISchemaProvider**](/windows/desktop/api/Structuredquery/nn-structuredquery-ischemaprovider) può essere utilizzata per esplorare uno schema caricato per le entità (tipi) e le relazioni (proprietà). Ecco quali sono i singoli metodi:

-   [**Entità**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-entities) restituisce un'enumerazione di ogni entità ([**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity)) nello schema.
-   [**RootEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-rootentity) restituisce l'entità radice dello schema. Per uno schema flat, viene restituito il tipo principale di ogni [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) .
-   [**GetEntity**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-getentity) trova un'entità in base al nome e restituisce \_ false se tale entità non è presente nello schema.
-   I [**metadati**](/windows/desktop/api/Structuredquery/nf-structuredquery-ischemaprovider-metadata) restituiscono un'enumerazione delle interfacce [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) .

### <a name="ientity"></a>IEntity

L'interfaccia [**IEntity**](/windows/desktop/api/Structuredquery/nn-structuredquery-ientity) è un'entità dello schema che rappresenta un tipo con un nome, ha una serie di relazioni denominate con altri tipi (proprietà) e deriva da un'entità di base. Ecco quali sono i singoli metodi:

-   [**IEntity:: relationships**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-relationships) restituisce un'enumerazione di oggetti [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) , uno per ogni relazione in uscita di questo tipo. Ogni relazione in uscita di un'entità ha un nome.
-   [**IEntity:: GetRelationship**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-getrelationship) trova una relazione in base al nome e restituisce \_ false se non esiste una relazione di questo tipo per questa entità.
-   [**IEntity:: Metadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-metadata) restituisce un'enumerazione di interfacce [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , una per ogni coppia di metadati di questa entità.
-   [**IEntity::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-ientity-defaultphrase) restituisce una frase predefinita per facilitare la generazione di una riformulazione AQS o NQS di un albero delle condizioni.

### <a name="irelationship"></a>IRelationship

L'interfaccia [**IRelationship**](/windows/desktop/api/Structuredquery/nn-structuredquery-irelationship) rappresenta una relazione tra due entità, ovvero un'origine e una destinazione. Ecco quali sono i singoli metodi:

-   [**IRelationship:: Unreal**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-isreal) indica se una relazione è reale. Se, ad esempio, l'entità A deriva dall'entità B e eredita una relazione denominata R da essa, è possibile che una relazione denominata R sia ancora presente. Tuttavia, la relazione beween A e R deve avere lo stesso tipo di destinazione di B e l'unico motivo per esistere è archiviare i metadati specifici di B. Una relazione di questo tipo è detta non reale.
-   [**IRelationship:: medadata**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-metadata) restituisce un'enumerazione di interfacce [**IMetadata**](/windows/desktop/api/Structuredquery/nn-structuredquery-imetadata) , una per ogni coppia di metadati di questa entità.
-   [**IRelationship::D efaultphrase**](/windows/desktop/api/Structuredquery/nf-structuredquery-irelationship-defaultphrase) restituisce la frase predefinita da utilizzare per la relazione in riformulazioni. Ogni relazione ha una frase predefinita che la denota per facilitare la generazione di una riformulazione AQS o NQS di un albero delle condizioni.

### <a name="imetadata"></a>IMetaData

I metadati sono coppie chiave-valore associate a un'entità, a una relazione o a un intero schema. Poiché le chiavi non sono necessariamente univoche, una raccolta di metadati può essere considerata come una mappa a più livelli. [**IMetadata:: GetData**](/windows/desktop/api/Structuredquery/nf-structuredquery-imetadata-getdata) viene chiamato per recuperare la chiave e il valore per una coppia di metatdata.

## <a name="querying-scenarios"></a>Esecuzione di query sugli scenari

Negli scenari seguenti viene descritto l'utilizzo di API di query strutturate in Windows Search in scenari comuni di query, ad esempio la creazione di un albero delle condizioni e l'esecuzione di query sull'indice.

### <a name="condition-extraction-and-query-parsing"></a>Estrazione della condizione e analisi delle query

Quando viene creata una query, l'ambito viene definito indicando al sistema dove eseguire la ricerca. In questo modo i risultati della ricerca vengono limitati. Dopo aver definito l'ambito, viene applicato un filtro e viene restituito un set di filtri. I risultati della ricerca sono limitati mediante la compilazione di un albero delle condizioni con nodi foglia, simile a un grafico. Tali condizioni vengono quindi estratte. Un albero delle condizioni è una combinazione booleana (AND, OR, NOT) delle condizioni foglia, ognuna delle quali correla una proprietà, tramite un'operazione, a un valore. Un nodo foglia rappresenta una restrizione su una singola proprietà a un valore tramite alcune operazioni.

Una restrizione di filtro richiede un'espressione logica che descriva la restrizione. La definizione di questa espressione inizia con l'interfaccia [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) , che viene usata per creare un singolo nodo in un albero delle condizioni. Poiché nell'esempio seguente è presente una sola condizione, l'albero non cambia.


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



Se è presente più di una condizione di filtro, vengono usati e e altri operatori booleani per ottenere un singolo albero. AND-Trees e OR-Trees rappresentano le congiunzioni e le disgiunzioni dei rispettivi sottoalberi. Un NOT-Tree rappresenta la negazione del singolo sottoalbero. AQS fornisce un approccio testuale per ottenere espressioni logiche con operatori booleani ed è spesso più semplice.

Nell'esempio seguente viene convertito l'albero delle condizioni ([**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)) in formato visivo. Il parser di query, usando l'interfaccia [**IQueryParser**](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser) , converte [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition) in una stringa di query RTF (Rich text formatted). Il metodo [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) restituisce il testo della query, mentre il metodo [**IQueryParser::P ass**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) produce un'interfaccia [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution) . Nell'esempio seguente viene illustrato come eseguire questa operazione.


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



L'input principale di [**IQueryParser::P ass**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-parse) è una stringa di input dell'utente da analizzare, ma l'applicazione può anche informare il parser di query delle proprietà riconosciute nell'input (dalla sintassi specifica dell'applicazione). L'output di **IQueryParser::P ass** è un [**IQuerySolution**](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution), che fornisce tutte le informazioni relative alla chiamata di analisi. Sono disponibili metodi per ottenere la stringa di input, il modo in cui la stringa di input è stata suddivisa in token, eventuali errori di analisi e la query analizzata come albero delle condizioni, rappresentata da un [**ICondition**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition). Nell'esempio seguente viene illustrato...


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



Nell'esempio precedente, [**IQuerySolution:: GetQuery**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getquery) può ottenere tutte le informazioni sulla query, inclusi il testo originale, i token che comprendono il testo o l'albero delle condizioni. Nella tabella seguente sono elencati alcuni esempi di possibili valori di query restituiti.



| Esempi di valori di query restituiti                        | Descrizione                                                                                               |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| `  author:relja OR author:tyler`                         | Il testo della query restituito da [**IQueryParser:: RestateToString**](/windows/desktop/api/Structuredquery/nf-structuredquery-iqueryparser-restatetostring) |
| `?author?, ?:?, ?relja?, ?OR?, ?author?, ?:?, ?tyler?`   | Suddivisione dei token                                                                                  |
| ![albero delle condizioni non risolte](images/queryvalues1.png) | Albero delle condizioni non risolte                                                                              |



 

L'albero della condizione iniziale restituito non è risolto. In un albero delle condizioni non risolto, i riferimenti di data e ora, ad esempio `date:yesterday` , non vengono convertiti in tempo assoluto. Inoltre, le proprietà virtuali non vengono espanse. Le proprietà virtuali sono proprietà che fungono da aggregazioni di più proprietà.

La query produce ad esempio `kind:email from:reljai` gli alberi delle condizioni non risolte e risolte seguenti. L'albero delle condizioni non risolte è a sinistra e l'albero delle condizioni risolto è a destra.

![strutture ad albero delle condizioni non risolte e risolte](images/conditiontree.png)

È possibile ottenere l'albero risolto chiamando [**IConditionFactory:: Resolve**](/windows/desktop/api/Structuredquery/nf-structuredquery-iconditionfactory-resolve). Tuttavia, il passaggio di [**SQRO \_ dont \_ Resolve \_ DateTime**](/windows/desktop/api/Structuredquery/ne-structuredquery-structured_query_resolve_option) lascia la data e l'ora non risolte. L'albero di una condizione non risolta presenta vantaggi, perché un albero delle condizioni non risolto contiene informazioni sulla query. Ogni nodo foglia punta ai token restituiti da [**IQuerySolution:: GetLexicalData**](/windows/desktop/api/Structuredquery/nf-structuredquery-iquerysolution-getlexicaldata), che corrispondono alla proprietà, all'operatore e al valore quando si usa l'interfaccia [**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk) . Nell'esempio seguente viene illustrato...


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

Esistono diversi approcci per eseguire query sull'indice. Alcuni sono basati su SQL e altri sono basati su AQS. È anche possibile eseguire una query sull'indice di ricerca di Windows a livello di codice usando le [interfacce di query](./-search-querying-interfaces-entry-page.md). Sono disponibili tre interfacce specifiche per l'esecuzione di query sull'indice: [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper), [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)e [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents). Per informazioni concettuali, vedere [esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md).

È possibile sviluppare una classe componente o helper per eseguire una query sull'indice usando l'interfaccia [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) . Questa interfaccia viene implementata come classe helper per [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (e [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) ed è ottenuta chiamando [**ISearchCatalogManager:: GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper). Per informazioni concettuali, vedere [esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md).

[**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) consente di:

-   Ottenere una stringa di connessione OLE DB per connettersi al database di Windows Search.
-   Converte le query utente AQS in SQL Search di Windows.
-   Specificare le restrizioni per le query che possono essere espresse in SQL ma non in AQS.

Le priorità di indicizzazione e gli eventi del set di righe sono supportati in Windows 7 e versioni successive. Con [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) è presente uno stack di priorità che consente al client di richiedere che agli ambiti utilizzati in una determinata query venga assegnata una priorità più alta rispetto alla priorità normale. [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents) fornisce la notifica delle modifiche apportate agli elementi nei set di righe, tra cui l'aggiunta di nuovi elementi, l'eliminazione di elementi e la modifica dei dati dell'elemento. L'utilizzo delle notifiche degli eventi del set di righe garantisce che i risultati delle query esistenti siano i più aggiornati possibili. Per informazioni concettuali, vedere [indicizzazione di priorità e eventi del set di righe in Windows 7](indexing-prioritization-and-rowset-events.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione, query e notifiche in Windows Search](-search-3x-wds-included-in-index.md)
</dt> <dt>

[Contenuto dell'indice](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di indicizzazione in Windows Search](-search-indexing-process-overview.md)
</dt> <dt>

[Processo di notifica in Windows Search](-search-3x-wds-support.md)
</dt> <dt>

[Requisiti per la formattazione degli URL](url-formatting-requirements.md)
</dt> </dl>

 

 
