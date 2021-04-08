---
description: Operazioni di amministrazione COM+ all'interno delle transazioni
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operazioni di amministrazione COM+ all'interno delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21612ffec1b9f082dc6a91861882a71f18fb07be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749095"
---
# <a name="com-administration-operations-within-transactions"></a><span data-ttu-id="87616-103">Operazioni di amministrazione COM+ all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="87616-103">COM+ Administration Operations Within Transactions</span></span>

<span data-ttu-id="87616-104">Il database di registrazione COM+ (RegDB) è un gestore di risorse transazionale che può partecipare alle transazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="87616-104">The COM+ registration database (RegDB) is a transacted resource manager that can participate in COM+ transactions.</span></span> <span data-ttu-id="87616-105">Questo consente di eseguire operazioni di amministrazione all'interno di una transazione e di eseguire il commit o l'interruzione di tutte le modifiche di configurazione come operazione atomica, anche in più computer.</span><span class="sxs-lookup"><span data-stu-id="87616-105">This enables you to perform administration operations within a transaction and have all configuration changes committed or aborted as an atomic operation, even across multiple computers.</span></span> <span data-ttu-id="87616-106">In alcune circostanze, può essere molto vantaggioso eseguire questa operazione, sebbene esista un comportamento di isolamento e blocco da tenere in considerazione e l'esecuzione di attività amministrative all'interno delle transazioni comporta lievi modifiche al normale modello di programmazione di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="87616-106">In some circumstances, it can be very beneficial to do this, although there is isolation and blocking behavior that you should take into account, and performing administration tasks within transactions does involve slight changes to the normal administration programming model.</span></span>

## <a name="benefits-of-doing-administration-operations-within-transactions"></a><span data-ttu-id="87616-107">Vantaggi delle operazioni di amministrazione all'interno delle transazioni</span><span class="sxs-lookup"><span data-stu-id="87616-107">Benefits of Doing Administration Operations Within Transactions</span></span>

-   <span data-ttu-id="87616-108">**Coerenza dei dati:** Le operazioni di amministrazione eseguite all'interno di una transazione vengono sottoposte a commit o interrotte nel suo complesso, sebbene esistano alcune risorse di catalogo COM+ non transazionali per le quali questa situazione potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="87616-108">**Consistency of data—** Administration operations performed within a transaction are committed or aborted as a whole, although there are some non-transactional COM+ catalog resources for which this may not be the case.</span></span> <span data-ttu-id="87616-109">Vedere le risorse di catalogo COM+ non transazionali.</span><span class="sxs-lookup"><span data-stu-id="87616-109">(See Non-Transactional COM+ Catalog Resources below.)</span></span>
-   <span data-ttu-id="87616-110">**Distribuzione coerente tra più computer:** Se si distribuiscono applicazioni COM+ su più server, è possibile garantire che tutti i server rimangano con configurazioni identiche.</span><span class="sxs-lookup"><span data-stu-id="87616-110">**Consistent deployment across multiple machines—** If you are deploying COM+ applications across multiple servers, you can guarantee that all servers are left with identical configurations.</span></span>
-   <span data-ttu-id="87616-111">**Scalabilità e prestazioni:** Quando si eseguono più operazioni all'interno di una transazione, tutte le Scritture in RegDB vengono eseguite contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="87616-111">**Scaling and performance—** When you do multiple operations within a transaction, all writes to RegDB are performed at once.</span></span> <span data-ttu-id="87616-112">Le Scritture rese permanente in RegDB sono un'operazione relativamente costosa; Se si effettuano molte operazioni di scrittura in RegDB, è possibile ottenere un notevole vantaggio in termini di prestazioni, anziché ogni volta che si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span><span class="sxs-lookup"><span data-stu-id="87616-112">Persisted writes to RegDB are a relatively expensive operation; if you are making many writes to RegDB, you can get a big performance benefit from doing them all at once instead of every time you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).</span></span>

## <a name="isolation-behavior-of-regdb"></a><span data-ttu-id="87616-113">Comportamento di isolamento di RegDB</span><span class="sxs-lookup"><span data-stu-id="87616-113">Isolation Behavior of RegDB</span></span>

<span data-ttu-id="87616-114">Per garantire la coerenza dei dati e le transazioni serializzabili, RegDB impone un comportamento particolare di blocco e isolamento quando le operazioni di amministrazione vengono eseguite all'interno delle transazioni.</span><span class="sxs-lookup"><span data-stu-id="87616-114">To ensure proper data consistency and serializable transactions, RegDB enforces particular blocking and isolation behavior when administration operations are being performed within transactions.</span></span>

<span data-ttu-id="87616-115">Ogni volta che un componente che esegue operazioni all'interno di una transazione chiama qualsiasi metodo che provocherà una scrittura nel catalogo COM+, ad esempio [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent), viene eseguito un blocco del writer sul codice del server di catalogo COM+ che blocca qualsiasi altro writer fino a quando non viene eseguito il commit o l'interruzione della transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="87616-115">Whenever a component that is doing work within a transaction calls any method that will cause a write to the COM+ catalog—such as [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication), or [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)—a writer lock is taken on COM+ catalog server code that will block any other writers from coming in until the current transaction commits or aborts.</span></span> <span data-ttu-id="87616-116">Ovvero, i writer possono entrare solo se hanno l'affinità di transazione corretta e partecipano alla transazione corrente.</span><span class="sxs-lookup"><span data-stu-id="87616-116">That is, writers can come in only if they have the correct transaction affinity and are participating in the current transaction.</span></span>

<span data-ttu-id="87616-117">I lettori non sono bloccati.</span><span class="sxs-lookup"><span data-stu-id="87616-117">Readers are not blocked.</span></span> <span data-ttu-id="87616-118">Tuttavia, i dati visualizzati dai lettori non riflettono alcuna modifica provvisoria apportata all'interno della transazione finché non viene effettivamente eseguito il commit della transazione.</span><span class="sxs-lookup"><span data-stu-id="87616-118">However, the data that readers see does not reflect any interim changes made within the transaction until that transaction actually commits.</span></span> <span data-ttu-id="87616-119">Tutti i componenti che partecipano alla transazione vedono gli Stati dei dati provvisori durante la lettura dei dati, ma tutti i componenti esterni alla transazione visualizzano tali modifiche solo dopo il completamento della transazione.</span><span class="sxs-lookup"><span data-stu-id="87616-119">Any components participating in that transaction sees interim data states when they read data, but all components outside the transaction see those changes only after the transaction has completed.</span></span>

## <a name="savechanges-behavior"></a><span data-ttu-id="87616-120">Comportamento di SaveChanges</span><span class="sxs-lookup"><span data-stu-id="87616-120">SaveChanges Behavior</span></span>

<span data-ttu-id="87616-121">Per ottenere il comportamento di isolamento descritto in precedenza, RegDB fornisce efficacemente una cache che agisce dai componenti all'interno della transazione.</span><span class="sxs-lookup"><span data-stu-id="87616-121">To achieve the isolation behavior described above, RegDB effectively provides a cache that is acted on by components within the transaction.</span></span> <span data-ttu-id="87616-122">In questo modo viene modificato il comportamento del metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .</span><span class="sxs-lookup"><span data-stu-id="87616-122">This changes the behavior of the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method.</span></span>

<span data-ttu-id="87616-123">In genere, senza la presenza di una transazione, tutte le modifiche in sospeso vengono scritte nel catalogo quando si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)e **SaveChanges** non viene restituito finché non vengono completate tutte le Scritture.</span><span class="sxs-lookup"><span data-stu-id="87616-123">Normally, without the presence of a transaction, any pending changes are written to the catalog when you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), and **SaveChanges** doesn't return until all writes are completed.</span></span> <span data-ttu-id="87616-124">In questo modo si garantisce che se una chiamata a **SaveChanges** restituisce correttamente, è possibile chiamare [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) e l'applicazione verrà attivata con dati aggiornati.</span><span class="sxs-lookup"><span data-stu-id="87616-124">This guarantees that if a call to **SaveChanges** returns successfully, you can call [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) and it will activate the application with fresh data.</span></span>

<span data-ttu-id="87616-125">Tuttavia, all'interno di una transazione, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) influiscono solo sulla cache, non sul regdb stesso e **SaveChanges** restituisce immediatamente se tutte le modifiche sono state sottoposte a commit transazionale in regdb.</span><span class="sxs-lookup"><span data-stu-id="87616-125">However, within a transaction, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) affects only the cache, not the RegDB itself, and **SaveChanges** returns immediately whether all changes have been transactionally committed to RegDB.</span></span> <span data-ttu-id="87616-126">Non vi è alcuna garanzia che [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) usi dati aggiornati successivi alla restituzione di **SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="87616-126">There is no guarantee that [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) is using fresh data subsequent to **SaveChanges** returning.</span></span> <span data-ttu-id="87616-127">Se è necessario chiamare **StartApplication** in questo contesto, è consigliabile attendere un certo periodo di tempo prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="87616-127">If you need to call **StartApplication** in this context, it is advisable to wait for some period of time before doing so.</span></span>

## <a name="transaction-time-out-period"></a><span data-ttu-id="87616-128">Periodo di Time-Out transazione</span><span class="sxs-lookup"><span data-stu-id="87616-128">Transaction Time-Out Period</span></span>

<span data-ttu-id="87616-129">Se si eseguono numerose operazioni di amministrazione all'interno di una transazione, potrebbe trattarsi di una transazione a esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="87616-129">If you are doing numerous administration operations within a transaction, it may be a long running transaction.</span></span> <span data-ttu-id="87616-130">In questo caso, il valore di timeout della transazione può essere un problema.</span><span class="sxs-lookup"><span data-stu-id="87616-130">In this case, the transaction time-out value can be an issue.</span></span> <span data-ttu-id="87616-131">Questo è determinato dal valore di timeout della transazione impostato per il componente che avvia la transazione o dall'impostazione di timeout a livello di computer per il computer in cui è in esecuzione il componente.</span><span class="sxs-lookup"><span data-stu-id="87616-131">This is determined either by the transaction time-out value set for the component initiating the transaction or by the machine-wide time-out setting for the machine where that component is running.</span></span> <span data-ttu-id="87616-132">Se si eseguono numerose operazioni all'interno di una transazione, è consigliabile impostare il periodo di timeout della transazione appropriato su un valore sufficientemente lungo e, se necessario, ripristinare l'impostazione originale al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="87616-132">If you are doing numerous operations within a transaction, it is advisable to set the appropriate transaction time-out period to a sufficiently long value and, if necessary, to restore the original setting when you are finished.</span></span>

## <a name="non-transactional-com-catalog-resources"></a><span data-ttu-id="87616-133">Risorse del catalogo COM+ non transazionali</span><span class="sxs-lookup"><span data-stu-id="87616-133">Non-Transactional COM+ Catalog Resources</span></span>

<span data-ttu-id="87616-134">Il registro di sistema, il file system e il Windows Installer (MSI) sono risorse del catalogo COM+ che non sono transazionali.</span><span class="sxs-lookup"><span data-stu-id="87616-134">The registry, the file system, and Windows Installer (MSI) are COM+ catalog resources that are not transactional.</span></span>

> [!Note]  
> <span data-ttu-id="87616-135">Se si verifica un errore che interrompe una transazione, è possibile che non venga eseguito il rollback delle modifiche apportate a tali risorse.</span><span class="sxs-lookup"><span data-stu-id="87616-135">If there is an error that aborts a transaction, changes to these resources may not be rolled back.</span></span>

 

<span data-ttu-id="87616-136">Se si verifica un errore durante l'installazione di un'applicazione COM+ esistente da un file con estensione msi, l'applicazione non viene visualizzata nello snap-in Servizi componenti, ma potrebbe essere visualizzata in Installazione applicazioni, nel qual caso è necessario rimuoverla manualmente.</span><span class="sxs-lookup"><span data-stu-id="87616-136">If there is an error while installing an existing COM+ application from an .msi file, the application doesn't appear in the Component Services snap-in but it might appear in Add/Remove programs, in which case you need to manually remove it.</span></span>

## <a name="recovering-in-the-event-of-system-hangs"></a><span data-ttu-id="87616-137">Ripristino in caso di blocchi di sistema</span><span class="sxs-lookup"><span data-stu-id="87616-137">Recovering in the Event of System Hangs</span></span>

<span data-ttu-id="87616-138">Se un componente che esegue le operazioni di amministrazione all'interno di una transazione si blocca mentre è presente un blocco del writer sul codice del server di catalogo, tutti gli altri elementi non possono apportare modifiche al catalogo.</span><span class="sxs-lookup"><span data-stu-id="87616-138">If a component doing administration operations within a transaction were to hang while it holds a writer lock on the catalog server code, it would block everyone else from making any changes to the catalog.</span></span> <span data-ttu-id="87616-139">In tal caso, è possibile cancellare il blocco sul catalogo arrestando e riavviando l'applicazione di sistema.</span><span class="sxs-lookup"><span data-stu-id="87616-139">Should this happen, you can clear the lock on the catalog by shutting down and restarting the System application.</span></span>

## <a name="scripting-with-a-transactioncontext-object"></a><span data-ttu-id="87616-140">Creazione di script con un oggetto TransactionContext</span><span class="sxs-lookup"><span data-stu-id="87616-140">Scripting with a TransactionContext Object</span></span>

<span data-ttu-id="87616-141">Un modo semplice per eseguire operazioni di amministrazione all'interno delle transazioni consiste nell'usare un oggetto [**TransactionContext**](transactioncontext.md) per controllare la transazione.</span><span class="sxs-lookup"><span data-stu-id="87616-141">A simple way to do administration operations within transactions is to use a [**TransactionContext**](transactioncontext.md) object to control the transaction.</span></span> <span data-ttu-id="87616-142">Ad esempio, lo script di Visual Basic seguente illustra come aggiungere due nuove applicazioni in modo transazionale in modo da creare entrambe le applicazioni o nessuna delle due applicazioni:</span><span class="sxs-lookup"><span data-stu-id="87616-142">For example, the following Visual Basic script demonstrates how to transactionally add two new applications so that either both applications or neither application is created:</span></span>


```VB
Dim txctx
Dim cat
Dim apps
Dim app1
Dim app2
  
WScript.Echo "Starting"
Set txctx = CreateObject("TxCtx.TransactionContext")
Set cat = txctx.CreateInstance("COMAdmin.COMAdminCatalog")
Set apps = cat.GetCollection("Applications")
Set app1 = apps.Add
app1.Value("Name") = "Test App #1"
apps.SaveChanges
Set app2 = apps.Add
app2.Value("Name") = "Test App #2"
apps.SaveChanges
  
WScript.Echo "Ending"
txctx.Commit

```



## <a name="related-topics"></a><span data-ttu-id="87616-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87616-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87616-144">Gestione degli errori di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="87616-144">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
</dt> <dt>

[<span data-ttu-id="87616-145">Esempio introduttivo di utilizzo del catalogo di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="87616-145">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[<span data-ttu-id="87616-146">Panoramica degli oggetti COMAdmin</span><span class="sxs-lookup"><span data-stu-id="87616-146">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> <dt>

[<span data-ttu-id="87616-147">Recupero di raccolte nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="87616-147">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="87616-148">Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+</span><span class="sxs-lookup"><span data-stu-id="87616-148">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



