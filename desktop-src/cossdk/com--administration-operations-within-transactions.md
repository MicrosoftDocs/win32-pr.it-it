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
# <a name="com-administration-operations-within-transactions"></a>Operazioni di amministrazione COM+ all'interno delle transazioni

Il database di registrazione COM+ (RegDB) è un gestore di risorse transazionale che può partecipare alle transazioni COM+. Questo consente di eseguire operazioni di amministrazione all'interno di una transazione e di eseguire il commit o l'interruzione di tutte le modifiche di configurazione come operazione atomica, anche in più computer. In alcune circostanze, può essere molto vantaggioso eseguire questa operazione, sebbene esista un comportamento di isolamento e blocco da tenere in considerazione e l'esecuzione di attività amministrative all'interno delle transazioni comporta lievi modifiche al normale modello di programmazione di amministrazione.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Vantaggi delle operazioni di amministrazione all'interno delle transazioni

-   **Coerenza dei dati:** Le operazioni di amministrazione eseguite all'interno di una transazione vengono sottoposte a commit o interrotte nel suo complesso, sebbene esistano alcune risorse di catalogo COM+ non transazionali per le quali questa situazione potrebbe non essere possibile. Vedere le risorse di catalogo COM+ non transazionali.
-   **Distribuzione coerente tra più computer:** Se si distribuiscono applicazioni COM+ su più server, è possibile garantire che tutti i server rimangano con configurazioni identiche.
-   **Scalabilità e prestazioni:** Quando si eseguono più operazioni all'interno di una transazione, tutte le Scritture in RegDB vengono eseguite contemporaneamente. Le Scritture rese permanente in RegDB sono un'operazione relativamente costosa; Se si effettuano molte operazioni di scrittura in RegDB, è possibile ottenere un notevole vantaggio in termini di prestazioni, anziché ogni volta che si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportamento di isolamento di RegDB

Per garantire la coerenza dei dati e le transazioni serializzabili, RegDB impone un comportamento particolare di blocco e isolamento quando le operazioni di amministrazione vengono eseguite all'interno delle transazioni.

Ogni volta che un componente che esegue operazioni all'interno di una transazione chiama qualsiasi metodo che provocherà una scrittura nel catalogo COM+, ad esempio [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent), viene eseguito un blocco del writer sul codice del server di catalogo COM+ che blocca qualsiasi altro writer fino a quando non viene eseguito il commit o l'interruzione della transazione corrente. Ovvero, i writer possono entrare solo se hanno l'affinità di transazione corretta e partecipano alla transazione corrente.

I lettori non sono bloccati. Tuttavia, i dati visualizzati dai lettori non riflettono alcuna modifica provvisoria apportata all'interno della transazione finché non viene effettivamente eseguito il commit della transazione. Tutti i componenti che partecipano alla transazione vedono gli Stati dei dati provvisori durante la lettura dei dati, ma tutti i componenti esterni alla transazione visualizzano tali modifiche solo dopo il completamento della transazione.

## <a name="savechanges-behavior"></a>Comportamento di SaveChanges

Per ottenere il comportamento di isolamento descritto in precedenza, RegDB fornisce efficacemente una cache che agisce dai componenti all'interno della transazione. In questo modo viene modificato il comportamento del metodo [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) .

In genere, senza la presenza di una transazione, tutte le modifiche in sospeso vengono scritte nel catalogo quando si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)e **SaveChanges** non viene restituito finché non vengono completate tutte le Scritture. In questo modo si garantisce che se una chiamata a **SaveChanges** restituisce correttamente, è possibile chiamare [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) e l'applicazione verrà attivata con dati aggiornati.

Tuttavia, all'interno di una transazione, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) influiscono solo sulla cache, non sul regdb stesso e **SaveChanges** restituisce immediatamente se tutte le modifiche sono state sottoposte a commit transazionale in regdb. Non vi è alcuna garanzia che [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) usi dati aggiornati successivi alla restituzione di **SaveChanges** . Se è necessario chiamare **StartApplication** in questo contesto, è consigliabile attendere un certo periodo di tempo prima di procedere.

## <a name="transaction-time-out-period"></a>Periodo di Time-Out transazione

Se si eseguono numerose operazioni di amministrazione all'interno di una transazione, potrebbe trattarsi di una transazione a esecuzione prolungata. In questo caso, il valore di timeout della transazione può essere un problema. Questo è determinato dal valore di timeout della transazione impostato per il componente che avvia la transazione o dall'impostazione di timeout a livello di computer per il computer in cui è in esecuzione il componente. Se si eseguono numerose operazioni all'interno di una transazione, è consigliabile impostare il periodo di timeout della transazione appropriato su un valore sufficientemente lungo e, se necessario, ripristinare l'impostazione originale al termine dell'operazione.

## <a name="non-transactional-com-catalog-resources"></a>Risorse del catalogo COM+ non transazionali

Il registro di sistema, il file system e il Windows Installer (MSI) sono risorse del catalogo COM+ che non sono transazionali.

> [!Note]  
> Se si verifica un errore che interrompe una transazione, è possibile che non venga eseguito il rollback delle modifiche apportate a tali risorse.

 

Se si verifica un errore durante l'installazione di un'applicazione COM+ esistente da un file con estensione msi, l'applicazione non viene visualizzata nello snap-in Servizi componenti, ma potrebbe essere visualizzata in Installazione applicazioni, nel qual caso è necessario rimuoverla manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Ripristino in caso di blocchi di sistema

Se un componente che esegue le operazioni di amministrazione all'interno di una transazione si blocca mentre è presente un blocco del writer sul codice del server di catalogo, tutti gli altri elementi non possono apportare modifiche al catalogo. In tal caso, è possibile cancellare il blocco sul catalogo arrestando e riavviando l'applicazione di sistema.

## <a name="scripting-with-a-transactioncontext-object"></a>Creazione di script con un oggetto TransactionContext

Un modo semplice per eseguire operazioni di amministrazione all'interno delle transazioni consiste nell'usare un oggetto [**TransactionContext**](transactioncontext.md) per controllare la transazione. Ad esempio, lo script di Visual Basic seguente illustra come aggiungere due nuove applicazioni in modo transazionale in modo da creare entrambe le applicazioni o nessuna delle due applicazioni:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione degli errori di amministrazione COM+](handling-com--administration-errors.md)
</dt> <dt>

[Esempio introduttivo di utilizzo del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



