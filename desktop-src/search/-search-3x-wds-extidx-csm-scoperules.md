---
description: Il gestore dell'ambito di ricerca per indicizzazione consente di definire regole di ambito che includono o escludono URL dall'ambito di ricerca per indicizzazione di Windows Search.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Gestione delle regole di ambito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d45199726cfe36dc1c4936e9ac7699a288c3ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128614"
---
# <a name="managing-scope-rules"></a>Gestione delle regole di ambito

Il gestore dell'ambito di ricerca per indicizzazione consente di definire regole di ambito che includono o escludono URL dall'ambito di ricerca per indicizzazione di Windows Search.

Il CSM consente di eseguire le operazioni seguenti:

-   Aggiungere nuove regole di ambito al set di regole di lavoro
-   Rimuovi regole ambito esistenti
-   Enumera regole ambito predefinite
-   Individuare se un particolare URL è incluso o escluso dall'ambito della ricerca per indicizzazione o ha una regola di ambito padre o figlio

 

Vengono inoltre presentati gli argomenti seguenti:

-   [Informazioni sulle regole di ambito](#about-scope-rules)
-   [Prima di iniziare](#before-you-begin)
-   [Aggiunta di regole di ambito](#adding-scope-rules)
    -   [Note sulle regole utente](#notes-on-user-rules)
-   [Rimozione delle regole dell'ambito](#removing-scope-rules)
-   [Ripristino di regole predefinite](#reverting-to-default-rules)
-   [Enumerazione delle regole dell'ambito](#enumerating-scope-rules)
-   [Traccia regole ambito](#tracing-scope-rules)
-   [Argomenti correlati](#related-topics)

## <a name="about-scope-rules"></a>Informazioni sulle regole di ambito

Una regola di ambito è una regola che include o esclude gli URL all'interno di una radice di ricerca dalla ricerca per indicizzazione e l'indicizzazione. Le regole di inclusione fanno sì che l'indicizzatore includa tale URL nell'ambito dello scarabocchio, mentre le regole di esclusione provocano l'esclusione dell'URL (e dei relativi elementi figlio) da parte dell'indicizzatore.

Si supponga, ad esempio, di aver installato una nuova applicazione i cui file di dati si trovano nella cartella WorkteamA \\ ProjectFiles in un computer locale. Si supponga di voler indicizzare tutti gli elementi all'interno della cartella ProjectFiles, ad eccezione degli elementi nei prototipi della sottocartella. In questa situazione è necessaria una regola di inclusione per myPH:///C: \\ WorkteamA \\ ProjectFiles \\ e una regola di esclusione per i \\ prototipi myPH:///C: WorkteamA \\ ProjectFiles \\ \\ .

Esistono tre tipi di regole, con il seguente ordine di precedenza:

1.  Criteri di gruppo regole vengono impostate dagli amministratori e possono eseguire l'override di tutte le altre regole.
2.  Le regole utente sono impostate dagli utenti che modificano l'ambito nell'interfaccia utente delle opzioni di ricerca di Windows. Gli utenti o le altre applicazioni possono rimuovere tutte le regole utente e ripristinare le regole predefinite.
3.  Le regole predefinite vengono in genere impostate da un'applicazione per definire un ambito predefinito. Ad esempio, le regole predefinite potrebbero essere impostate quando un nuovo gestore di protocollo o contenitore viene aggiunto al sistema.

Insieme, questi tipi di regole costituiscono il *set di regole di lavoro* da cui il gestore dell'ambito di ricerca per indicizzazione (CSM) genera l'elenco completo degli URL da ricercare. Mentre le regole predefinite possono essere sostituite da regole di criteri di gruppo e da regole utente, vengono mantenute nel set di regole predefinito, che è possibile ripristinare in qualsiasi momento. L'indicizzatore esegue la ricerca per indicizzazione degli URL dal set di regole di lavoro e aggiunge elementi, proprietà e contenuto al catalogo.

> [!Note]  
> Gli utenti con accesso al pannello di controllo possono modificare le regole tramite tale interfaccia. Pertanto, le applicazioni che offrono la gestione degli ambiti devono sempre ottenere le regole direttamente da CSM usando i metodi di enumerazione invece di basarsi su una copia salvata delle regole utente.

 

Le regole di esclusione possono definire URL di pattern con il carattere jolly ' \* ', ad esempio: file:///C: \\ ProjectA \\ \* \\ . Una regola di esclusione che usa questo modello impedisce all'indicizzatore di eseguire la ricerca per indicizzazione di tutte le cartelle nella directory NomeProgetto. Per un esempio più complesso, si supponga che esista una regola di inclusione per file:///C: \\ ProjectA \\ e una regola di modello di esclusione per file:///C: \\ ProjectA \\ \* \\ data \\ \* . In questo caso, l'indicizzatore esegue la ricerca per indicizzazione degli elementi in:

-   C: \\ PROJECTA\\
-   C: \\ ProjectA \\ **Version1** \\ testfiles\\
-   C: \\ ProjectA \\ **Version1 \\ Temp** \\ Data\\

Tuttavia, l'indicizzatore non esegue la ricerca per indicizzazione degli elementi in:

-   C: \\ ProjectA \\ **Version1** \\ dati\\

 

## <a name="before-you-begin"></a>Prima di iniziare

Prima di usare una delle interfacce di gestione degli ambiti di ricerca per indicizzazione, è necessario eseguire i passaggi dei prerequisiti seguenti:

1.  Creare l'oggetto **CSearchManager** e ottenere la relativa interfaccia **ISearchManager** .
2.  Chiamare **ISearchManager:: getCatalog** per "SystemIndex" per ottenere un'istanza dell'interfaccia **ISearchCatalogManager** .
3.  Chiamare **ISearchCatalogManager:: GetCrawlScopeManager** per ottenere un'istanza dell'interfaccia **ISearchCrawlScopeManager** .

Dopo aver apportato modifiche al gestore dell'ambito di ricerca per indicizzazione, è necessario chiamare il metodo [**ISearchCrawlScopeManager:: SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) . Questo metodo non accetta parametri e restituisce \_ OK in seguito all'esito positivo.

 

## <a name="adding-scope-rules"></a>Aggiunta di regole di ambito

Le regole di lavoro impostate per CSM includono regole utente e predefinite, nonché qualsiasi regola forzata da criteri di gruppo. Le regole utente vengono configurate dagli utenti in un'interfaccia utente e le regole predefinite possono essere impostate in uno dei seguenti elementi:

-   Criteri di gruppo implementati da un amministratore di sistema (che non utilizzano l'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) ).
-   Installazione o aggiornamento di un'applicazione come Windows Search o un gestore di protocollo
-   Un'applicazione di installazione per l'aggiunta di un nuovo archivio dati o contenitore

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) fornisce due metodi per l'aggiunta di nuove regole di ambito, come descritto nella tabella seguente. I percorsi per le regole di inclusione per il file system devono terminare con una barra rovesciata ' \\ ' (ad esempio, file:///C: \\ files \\ ) e i percorsi per le regole di esclusione devono terminare con un asterisco (ad esempio, file:///c: \\ files \\ \* ). Solo le regole di esclusione possono contenere URL del modello. Inoltre, è consigliabile includere gli identificatori di sicurezza (SID) degli utenti nei percorsi, per una maggiore sicurezza. I percorsi per utente sono più sicuri quando le query vengono eseguite in un processo per utente, assicurando che un utente non possa visualizzare gli elementi indicizzati dalla posta in arrivo di un altro utente, ad esempio.

Nella tabella seguente vengono descritti i metodi dell'interfaccia ISearchCrawlScopeManager utilizzata per l'aggiunta di nuove regole di ambito.



| Metodo                                                                              | Descrizione                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Aggiunge una regola per un URL, come specificato dall'utente. Queste regole sostituiscono le regole predefinite. Utilizzare questo metodo se è stata implementata un'interfaccia utente che consente agli utenti di gestire le proprie regole di ambito e URL.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Aggiunge una regola per un URL, come specificato da un'altra applicazione come un gestore di protocollo. Utilizzare questo metodo quando è stato implementato un nuovo gestore di protocollo o è stato aggiunto un nuovo archivio dati. È possibile eseguire l'override di queste regole tramite regole utente. |



 

Ogni metodo accetta un URL per una posizione indicizzabile e i flag che determinano se l'URL deve essere incluso o escluso. Il parametro *fFollowFlags* è riservato per un utilizzo futuro. Quando si aggiunge una nuova regola di ambito e il gestore dell'ambito di ricerca per indicizzazione determina che la regola esiste già (in base all'URL o al modello fornito), il set di regole di lavoro viene aggiornato in modo che (1) la regola precedente venga sostituita dalla nuova regola e (2) eventuali regole utente che lo contraddicono vengano rimosse.

**Suggerimento:** Mentre la radice file://è inclusa per impostazione predefinita nell'ambito della ricerca per indicizzazione, i file di programma non vengono indicizzati per impostazione predefinita. Pertanto, le applicazioni con i dati salvati nella directory dei file di programma devono aggiungere il proprio percorso come una regola predefinita.

### <a name="notes-on-user-rules"></a>Note sulle regole utente

Se una nuova regola utente corrisponde a una regola predefinita esistente, la nuova regola utente sostituisce quella predefinita nel set di regole di lavoro. Se la nuova regola utente corrisponde a una regola utente esistente, la regola utente precedente viene sostituita.

L'impostazione del flag *fOverrideChildren* presenta i risultati seguenti nel set di regole di lavoro:

-   **True** comporta la rimozione di tutte le regole figlio dal set di regole di lavoro (regole utente e regole predefinite).
-   FALSE comporta un nuovo tentativo di aggiunta alle regole di lavoro per impostare tutte le regole predefinite figlio della nuova regola utente. Se una regola predefinita figlio è un'inclusione e la nuova regola utente è un'esclusione, la regola predefinita viene modificata in una regola utente di inclusione.

 

## <a name="removing-scope-rules"></a>Rimozione delle regole dell'ambito

È possibile utilizzare l'interfaccia [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) per rimuovere una regola di ambito dal set di regole di lavoro. Questa interfaccia fornisce i due metodi seguenti per rimuovere le regole di ambito.



| Metodo                                                                                    | Descrizione                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Rimuove una regola utente per un URL specificato dal set di regole di lavoro. Se la regola utente è un duplicato di o sostituisce una regola predefinita, la regola predefinita rimane nel set di regole di lavoro.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Rimuove una regola predefinita per un URL specificato sia dal set di regole di lavoro che dal set di regole predefinito. Dopo aver chiamato questo metodo, non è possibile ripristinare questa regola predefinita usando RevertToDefaultScopes. |



 

Ogni metodo accetta un URL e un flag che indica se la regola da rimuovere è una regola di inclusione o di esclusione. Questi metodi restituiscono un errore se non viene trovata una regola con tale URL e il flag di inclusione/esclusione.

**Suggerimento:** Se si desidera rimuovere completamente un ambito dall'ambito della ricerca per indicizzazione, utilizzare il metodo [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) , che rimuove la radice di ricerca e tutte le regole di ambito associate. Questa operazione durante la disinstallazione di, ad esempio, viene considerata una procedura consigliata.

È anche possibile rimuovere tutte le sostituzioni impostate dall'utente di una radice di ricerca e ripristinare le regole dell'ambito di ricerca originale e dell'ambito predefinito. Per ulteriori informazioni, fare riferimento alla sezione successiva.

> [!Note]  
> In Windows Vista, se gli utenti vengono rimossi tramite profili utente nel pannello di controllo, CSM rimuove tutte le regole e le radici che includono il SID e rimuove gli elementi indicizzati dal catalogo. In Windows XP è necessario rimuovere manualmente le radici e le regole degli utenti.

 

 

## <a name="reverting-to-default-rules"></a>Ripristino di regole predefinite

Ripristinando le regole predefinite vengono rimosse tutte le regole utente per un URL o una radice e vengono ripristinate tutte le regole predefinite per il set di regole di lavoro. Tuttavia, non rimuove le regole impostate da criteri di gruppo. Il metodo [**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) non accetta parametri e restituisce un codice di errore se non è in grado di ripristinare le regole predefinite.

 

## <a name="enumerating-scope-rules"></a>Enumerazione delle regole dell'ambito

CSM enumera le regole di ambito usando un'interfaccia di enumeratore di tipo COM standard, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) . È possibile utilizzare questa interfaccia per enumerare le regole di ambito per diversi scopi. Ad esempio, è possibile visualizzare l'intero set di regole di lavoro in un'interfaccia utente o scoprire se una regola o l'elemento figlio di una regola si trova già nell'ambito della ricerca per indicizzazione.

 

## <a name="tracing-scope-rules"></a>Traccia regole ambito

Il CSM consente inoltre di determinare se un URL specificato è incluso nell'ambito della ricerca per indicizzazione e se dispone di una regola di ambito padre o figlio. È anche possibile scoprire perché un URL è incluso o escluso dall'ambito della ricerca per indicizzazione. Questi metodi non sono progettati per essere usati con gli URL del modello.

Nella tabella seguente vengono descritti i metodi di [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) utilizzati per l'aggiunta di nuove regole di ambito.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Ottiene l'ID versione dell'URL di inclusione padre. È possibile usare questo metodo per verificare se l'ambito padre è stato modificato dall'ultima volta che è stato verificato.<br/> Esempio: se un'applicazione di posta elettronica utilizza notifiche gestite dal provider, potrebbe ottenere la versione dell'ambito padre prima di chiuderla e controllare di nuovo la versione all'apertura. Quindi, l'applicazione può determinare se è necessario eseguire il push di un nuovo set di notifiche all'indicizzatore.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Restituisce **true** se l'URL specificato dispone di una regola figlio (regola applicata a un elemento figlio a qualsiasi livello all'interno della gerarchia degli URL). <br/> Esempio: se l'URL è file:///C: \\ Folder \\ , questo metodo restituisce **true** se CSM ha una regola di ambito specificatamente per la \\ sottocartella file:///C: Folder \\ \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Restituisce **true** se l'URL specificato dispone di una regola padre, ovvero una regola applicata a un elemento padre a qualsiasi livello della gerarchia URL.<br/> Esempio: se l'URL è file:///C: \\ Folder \\ sottocartella, questo metodo restituisce **true** se CSM ha una regola di ambito specifica per file:///C: \\ Folder \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Restituisce **true** se l'URL specificato è incluso nell'ambito della ricerca per indicizzazione.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Restituisce un valore dall'enumerazione [**del \_ motivo di isolamento**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) che spiega perché l'URL è incluso o escluso dall'ambito della ricerca per indicizzazione e recupera il valore **true** se l'URL è incluso nell'ambito della ricerca per indicizzazione. Questo metodo consente di identificare i conflitti nel set di regole di lavoro.                                                                                                                                       |



 

 

> [!Note]  
> I metodi [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) e [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) determinano se l'URL verrà sottoposto a ricerca per indicizzazione solo in base alle regole del CSM. Ci possono essere altri motivi per cui un URL non viene sottoposto a ricerca per indicizzazione, ad esempio il bit da impostare, ovvero un utente non ha consentito l'indicizzazione rapida nella finestra di dialogo delle proprietà della cartella.

 

Se si ritiene che un percorso di file debba essere escluso, ma sia elencato come incluso, assicurarsi che le regole di esclusione terminino con " <path> \\ \* ". Se si ritiene che un file o un percorso file debba essere incluso, ma non lo è, assicurarsi di controllare l'impostazione di bit per il file o il percorso. A tale scopo, fare clic con il pulsante destro del mouse sul percorso del file o del file e scegliere **Proprietà**, quindi verificare che la casella di controllo per la ricerca rapida, Consenti l'indicizzazione del **servizio indicizzare questa cartella** sia selezionata. Se il percorso del file o del file non è contrassegnato per l'indicizzazione, non verrà indicizzato anche se si trova in una regola di inclusione.

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

 

 




