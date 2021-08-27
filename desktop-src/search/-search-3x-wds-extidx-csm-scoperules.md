---
description: Il Gestione ambito ricerca per indicizzazione (CSM) consente di definire regole di ambito che includono o escludono URL dall'Windows ricerca per indicizzazione.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Gestione delle regole di ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6374ff3f29bebfcaeeddd02a4ec1c1d7746a19ab48c4ad8d3669aeb0cfaebdb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058191"
---
# <a name="managing-scope-rules"></a>Gestione delle regole di ambito

Il Gestione ambito ricerca per indicizzazione (CSM) consente di definire regole di ambito che includono o escludono URL dall'Windows ricerca per indicizzazione.

Il CSM consente di eseguire le operazioni seguenti:

-   Aggiungere nuove regole di ambito al set di regole di lavoro
-   Rimuovere le regole di ambito esistenti
-   Enumerare le regole di ambito predefinite
-   Scoprire se un url specifico è incluso o escluso dall'ambito della ricerca per indicizzazione o ha una regola di ambito padre o figlio

 

Vengono inoltre presentati gli argomenti seguenti:

-   [Informazioni sulle regole di ambito](#about-scope-rules)
-   [Prima di iniziare](#before-you-begin)
-   [Aggiunta di regole di ambito](#adding-scope-rules)
    -   [Note sulle regole utente](#notes-on-user-rules)
-   [Rimozione di regole di ambito](#removing-scope-rules)
-   [Ripristino delle regole predefinite](#reverting-to-default-rules)
-   [Enumerazione delle regole di ambito](#enumerating-scope-rules)
-   [Regole di ambito di traccia](#tracing-scope-rules)
-   [Argomenti correlati](#related-topics)

## <a name="about-scope-rules"></a>Informazioni sulle regole di ambito

Una regola di ambito è una regola che include o esclude gli URL all'interno di una radice di ricerca dalla ricerca per indicizzazione e dall'indicizzazione. Le regole di inclusione determinano l'inclusione dell'URL nell'ambito scrawl e le regole di esclusione causano l'esclusione dell'URL (e dei relativi elementi figlio) dall'ambito della ricerca per indicizzazione.

Si supponga, ad esempio, di aver installato una nuova applicazione i cui file di dati si trovano nella cartella WorkteamA \\ ProjectFiles in un computer locale. Si supponga di voler indicizzare tutti gli elementi all'interno della cartella ProjectFiles, ad eccezione degli elementi nella sottocartella Prototypes. In questo caso, sono necessarie una regola di inclusione per myPH:///C: WorkteamA ProjectFiles e una regola di esclusione per \\ \\ \\ myPH:///C: \\ WorkteamA \\ ProjectFiles \\ Prototypes \\ .

Esistono tre tipi di regole, con l'ordine di precedenza seguente:

1.  Criteri di gruppo regole vengono impostate dagli amministratori e possono eseguire l'override di tutte le altre regole.
2.  Le regole utente vengono impostate dagli utenti che modificano l'ambito nell Windows utente delle opzioni di ricerca. Gli utenti o altre applicazioni possono rimuovere tutte le regole utente e ripristinare le regole predefinite.
3.  Le regole predefinite vengono in genere impostate da un'applicazione per definire un ambito predefinito. Ad esempio, le regole predefinite potrebbero essere impostate quando un nuovo gestore di protocollo o un nuovo contenitore viene aggiunto al sistema.

Insieme, questi tipi di regole comprendono il *set* di regole di lavoro da cui Gestione ambito ricerca per indicizzazione (CSM) genera l'elenco completo di URL per la ricerca per indicizzazione. Anche se le regole predefinite possono essere sostituite dalle regole di Criteri di gruppo e dalle regole utente, vengono mantenute nel proprio set di regole predefinito, che è possibile ripristinare in qualsiasi momento. L'indicizzatore esegue una ricerca per indicizzazione degli URL dal set di regole di lavoro e aggiunge elementi, proprietà e contenuto al catalogo.

> [!Note]  
> Gli utenti con accesso Pannello di controllo modificare le regole tramite tale interfaccia. Pertanto, le applicazioni che offrono la gestione dell'ambito devono sempre ottenere le regole direttamente dal CSM usando i metodi di enumerazione anziché basarsi su una copia salvata delle regole utente.

 

Le regole di esclusione possono definire gli URL dei modelli con il carattere jolly \* '', ad esempio: file:///C: \\ ProjectA \\ \* \\ . Una regola di esclusione che usa questo modello impedisce all'indicizzatore di eseguire ricerche per indicizzazione in qualsiasi cartella nella directory ProjectA. Per un esempio più complesso, si supponga che siano presenti una regola di inclusione per file:///C: ProjectA e una regola del modello di esclusione per \\ \\ file:///C: \\ dati ProjectA \\ \* \\ \\ \* . In questo caso, l'indicizzatore eseguirebbe una ricerca per indicizzazione degli elementi in:

-   C: \\ ProjectA\\
-   C: \\ File di test di ProjectA versione \\ **1** \\\\
-   C: \\ Dati temporanei di ProjectA versione \\ **\\ 1** \\\\

Tuttavia, l'indicizzatore non eseguirebbe la ricerca per indicizzazione degli elementi in:

-   C: \\ Dati projectA \\ **versione 1** \\\\

 

## <a name="before-you-begin"></a>Prima di iniziare

Prima di usare una delle interfacce Gestione ambito ricerca per indicizzazione, è necessario eseguire i passaggi dei prerequisiti seguenti:

1.  Creare **l'oggetto CSearchManager** e ottenere la **relativa interfaccia ISearchManager.**
2.  Chiamare **ISearchManager::GetCatalog** per "SystemIndex" per ottenere un'istanza **dell'interfaccia ISearchCatalogManager.**
3.  Chiamare **ISearchCatalogManager::GetCrawlScopeManager** per ottenere un'istanza **dell'interfaccia ISearchCrawlScopeManager.**

Dopo aver apportato le modifiche Gestione ambito ricerca per indicizzazione, è necessario chiamare il [**metodo ISearchCrawlScopeManager::SaveAll.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) Questo metodo non accetta parametri e restituisce S \_ OK in caso di esito positivo.

 

## <a name="adding-scope-rules"></a>Aggiunta di regole di ambito

Le regole di lavoro impostate per il CSM includono regole utente e predefinite, nonché tutte le regole forzate da Criteri di gruppo. Le regole utente vengono impostate dagli utenti in un'interfaccia utente e le regole predefinite possono essere impostate in uno dei modi seguenti:

-   Criteri di gruppo implementati da un amministratore di sistema (non usano [**l'interfaccia ISearchCrawlScopeManager).**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   L'installazione o l'aggiornamento di un'applicazione Windows ricerca o un gestore di protocollo
-   Un'applicazione di configurazione per l'aggiunta di un nuovo archivio dati o contenitore

[**ISearchCrawlScopeManager fornisce**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) due metodi per l'aggiunta di nuove regole di ambito, come descritto nella tabella seguente. I percorsi per le regole di inclusione per il file system devono terminare con una barra rovesciata ' ' (ad esempio, file:///C: file ) e i percorsi per le regole di esclusione devono terminare con un asterisco \\ \\ \\ (ad esempio, file:///c: \\ files \\ \* ). Solo le regole di esclusione possono contenere URL di criteri. Inoltre, è consigliabile includere gli ID di sicurezza (SID) degli utenti nei percorsi, per una maggiore sicurezza. I percorsi per utente sono più sicuri perché le query vengono quindi eseguite in un processo per utente, assicurando che un utente non possa visualizzare gli elementi indicizzati dalla posta in arrivo di un altro utente, ad esempio.

La tabella seguente descrive i metodi dell'interfaccia ISearchWlScopeManager usati per aggiungere nuove regole di ambito.



| Metodo                                                                              | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Aggiunge una regola per un URL, come specificato dall'utente. Queste regole sostituiscono le regole predefinite. Usare questo metodo se è stata implementata un'interfaccia utente che consente agli utenti di gestire gli URL e le regole di ambito.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Aggiunge una regola per un URL, come specificato da un'altra applicazione, ad esempio un gestore di protocollo. Usare questo metodo quando è stato implementato un nuovo gestore di protocollo o è stato aggiunto un nuovo archivio dati. Queste regole possono essere sostituite dalle regole utente. |



 

Ogni metodo accetta un URL in una posizione indicizzabile e i flag che determinano se l'URL deve essere incluso o escluso. Il *parametro fFollowFlags* è riservato per un uso futuro. Quando si aggiunge una nuova regola di ambito e il Gestione ambito ricerca per indicizzazione determina che la regola esiste già (in base all'URL o al modello fornito), il set di regole di lavoro viene aggiornato in modo che (1) la regola precedente venga sostituita dalla nuova regola e (2) le eventuali regole utente che la contraddicono vengono rimosse.

**Suggerimento:** Mentre la file:// radice è inclusa per impostazione predefinita nell'ambito della ricerca per indicizzazione, Programmi non è indicizzata per impostazione predefinita. Di conseguenza, le applicazioni con dati salvati nella directory Programmi devono aggiungere il percorso come regola predefinita.

### <a name="notes-on-user-rules"></a>Note sulle regole utente

Se una nuova regola utente corrisponde a una regola predefinita esistente, la nuova regola utente sostituisce la regola predefinita nel set di regole di lavoro. Se la nuova regola utente corrisponde a una regola utente esistente, la regola utente precedente viene sostituita.

L'impostazione del flag *fOverrideChildren* ha i risultati seguenti nel set di regole di lavoro:

-   **TRUE** comporta la rimozione di tutte le regole figlio dal set di regole di lavoro (regole utente e regole predefinite).
-   FALSE comporta la nuova aggiunta alle regole di lavoro che impostano tutte le regole predefinite figlio della nuova regola utente. Se una regola predefinita figlio è un'inclusione e la nuova regola utente è un'esclusione, la regola predefinita viene modificata in una regola utente di inclusione.

 

## <a name="removing-scope-rules"></a>Rimozione di regole di ambito

È possibile usare [**l'interfaccia ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per rimuovere una regola di ambito dal set di regole di lavoro. Questa interfaccia fornisce i due metodi seguenti per rimuovere le regole di ambito.



| Metodo                                                                                    | Descrizione                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Rimuove una regola utente per un URL specificato dal set di regole di lavoro. Se la regola utente è un duplicato di o sostituisce una regola predefinita, la regola predefinita rimane nel set di regole di lavoro.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Rimuove una regola predefinita per un URL specificato sia dal set di regole di lavoro che dal set di regole predefinito. Dopo aver chiamato questo metodo, non è possibile ripristinare questa regola predefinita usando RevertToDefaultScopes. |



 

Ogni metodo accetta un URL e un flag che indica se la regola da rimuovere è una regola di inclusione o esclusione. Questi metodi restituisce un errore se non viene trovata una regola con tale URL e flag di inclusione/esclusione.

**Suggerimento:** Se si vuole rimuovere completamente un ambito dall'ambito della ricerca per indicizzazione, usare il metodo [**RemoveRoot,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) che rimuove la radice di ricerca e tutte le regole di ambito associate. Questa operazione durante la disinstallazione, ad esempio, è considerata la procedura consigliata.

È anche possibile rimuovere tutte le sostituzioni impostate dall'utente di una radice di ricerca e ripristinare la radice di ricerca originale e le regole di ambito predefinite. Per altre informazioni, vedere la sezione successiva.

> [!Note]  
> In Windows Vista, se gli utenti vengono rimossi tramite Profili utente in Pannello di controllo, CSM rimuove tutte le regole e le radici che includono il RELATIVO SID e rimuove gli elementi indicizzati dal catalogo. In Windows XP è necessario rimuovere manualmente le radici e le regole degli utenti.

 

 

## <a name="reverting-to-default-rules"></a>Ripristino delle regole predefinite

Il ripristino delle regole predefinite rimuove tutte le regole utente per un URL o una radice e ripristina tutte le regole predefinite nel set di regole di lavoro. Non rimuove tuttavia le regole impostate da Criteri di gruppo. Il [**metodo RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) non accetta parametri e restituisce un codice di errore se non è in grado di ripristinare le regole predefinite.

 

## <a name="enumerating-scope-rules"></a>Enumerazione delle regole di ambito

Il CSM enumera le regole di ambito usando un'interfaccia di enumeratore di tipo COM standard, [**IEnumSearchScopeRules.**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) È possibile usare questa interfaccia per enumerare le regole di ambito per diversi scopi. Ad esempio, potrebbe essere necessario visualizzare l'intero set di regole di lavoro in un'interfaccia utente o scoprire se una regola o l'elemento figlio di una regola si trova già nell'ambito della ricerca per indicizzazione.

 

## <a name="tracing-scope-rules"></a>Regole di ambito di traccia

Il CSM consente inoltre di determinare se un URL specificato è incluso nell'ambito della ricerca per indicizzazione e se dispone di una regola di ambito padre o figlio. È anche possibile scoprire perché un URL viene incluso o escluso dall'ambito della ricerca per indicizzazione. Questi metodi non devono essere usati con GLI URL dei modelli.

La tabella seguente descrive i metodi di [**ISearchWlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) usati per aggiungere nuove regole di ambito.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Ottiene l'ID versione dell'URL di inclusione padre. È possibile usare questo metodo per verificare se l'ambito padre è stato modificato dopo l'ultima verifica.<br/> Esempio: se un'applicazione di posta elettronica usa notifiche gestite dal provider, potrebbe ottenere la versione dell'ambito padre prima della chiusura e controllare di nuovo la versione all'apertura. L'applicazione può quindi determinare se è necessario eseguire il push di un nuovo set di notifiche all'indicizzatore.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Restituisce **TRUE** se l'URL specificato ha una regola figlio (una regola che si applica a un elemento figlio a qualsiasi livello all'interno della gerarchia di URL). <br/> Esempio: se l'URL è file:///C: Cartella , questo metodo restituisce TRUE se il CSM ha una regola di ambito specifica per \\ \\ file:///C:  \\ Sottocartella cartella \\ \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Restituisce **TRUE** se l'URL specificato ha una regola padre (una regola che si applica a un elemento padre a qualsiasi livello della gerarchia di URL).<br/> Esempio: se l'URL è file:///C: Sottocartella cartella, questo metodo restituisce TRUE se il CSM ha una regola di ambito specifica per \\ \\ file:///C:  \\ Cartella \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Restituisce **TRUE se** l'URL specificato è incluso nell'ambito della ricerca per indicizzazione.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Restituisce un valore dall'enumerazione [**CLUSION \_ REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) che spiega perché l'URL è incluso o escluso dall'ambito della ricerca per indicizzazione e recupera il valore **TRUE** se l'URL è incluso nell'ambito della ricerca per indicizzazione. Questo metodo consente di identificare i conflitti nel set di regole di lavoro.                                                                                                                                       |



 

 

> [!Note]  
> I [**metodi IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) e [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) determinano se l'URL verrà sottoposto a ricerca per indicizzazione esclusivamente in base alle regole nel CSM. Esistono altri motivi per cui non viene eseguita la ricerca per indicizzazione di un URL, ad esempio il bit FANCI impostato, ovvero se un utente non ha consentito l'indicizzazione rapida nella finestra di dialogo Proprietà della cartella.

 

Se si ritiene che un percorso di file debba essere escluso, ma è elencato come incluso, assicurarsi che le regole di esclusione terminino con " <path> \\ \* ". Se si ritiene che un file o un percorso di file debba essere incluso ma non lo è, assicurarsi di controllare l'impostazione di bit FANCI per il file o il percorso. A tale scopo, fare clic con il pulsante destro del mouse sul file o sul percorso del file e scegliere Proprietà **,** quindi assicurarsi che la casella di controllo Per la ricerca **veloce,** consenti al servizio di indicizzazione di indicizzare questa cartella sia selezionata. Se il percorso del file o del file non è contrassegnato per l'indicizzazione, non verrà indicizzato anche se si trova in una regola di inclusione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Gestione delle radici di ricerca](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




