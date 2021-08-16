---
description: Operazioni di amministrazione COM+ all'interno delle transazioni
ms.assetid: 832f2e6d-26ff-416e-a92e-ebaa33d4e7e5
title: Operazioni di amministrazione COM+ all'interno delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4182b143de38d838aea7c5aabd2d91bdb84f94480b2bed4c4441e204412ac834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308250"
---
# <a name="com-administration-operations-within-transactions"></a>Operazioni di amministrazione COM+ all'interno delle transazioni

Il database di registrazione COM+ (RegDB) è un gestore di risorse transazionale che può partecipare alle transazioni COM+. Ciò consente di eseguire operazioni di amministrazione all'interno di una transazione e di eseguire il commit o l'interruzione di tutte le modifiche di configurazione come operazione atomica, anche in più computer. In alcuni casi, può essere molto utile eseguire questa operazione, anche se è necessario prendere in considerazione il comportamento di isolamento e blocco e l'esecuzione di attività di amministrazione all'interno delle transazioni comporta lievi modifiche al normale modello di programmazione di amministrazione.

## <a name="benefits-of-doing-administration-operations-within-transactions"></a>Vantaggi dell'esecuzione di operazioni di amministrazione all'interno delle transazioni

-   **Coerenza dei dati:** Il commit o l'interruzione delle operazioni di amministrazione eseguite all'interno di una transazione viene eseguito nel suo complesso, anche se esistono alcune risorse del catalogo COM+ non transazionali per le quali questo potrebbe non essere il caso. Vedere le risorse del catalogo COM+ non transazionali di seguito.
-   **Distribuzione coerente tra più computer:** Se si distribuiscono applicazioni COM+ in più server, è possibile garantire che tutti i server siano rimasti con configurazioni identiche.
-   **Ridimensionamento e prestazioni:** Quando si eseguiti più operazioni all'interno di una transazione, tutte le operazioni di scrittura in RegDB vengono eseguite contemporaneamente. Le scritture persistenti in RegDB sono un'operazione relativamente costosa. se si effettuano molte operazioni di scrittura in RegDB, è possibile ottenere un grande vantaggio in termini di prestazioni dall'esecuzione di tutte le operazioni contemporaneamente anziché ogni volta che si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges).

## <a name="isolation-behavior-of-regdb"></a>Comportamento di isolamento di RegDB

Per garantire la coerenza dei dati e le transazioni serializzabili, RegDB applica un particolare comportamento di blocco e isolamento quando vengono eseguite operazioni di amministrazione all'interno delle transazioni.

Ogni volta che un componente che esegue operazioni all'interno di una transazione chiama qualsiasi metodo che causerà una scrittura nel catalogo COM+, ad esempio [**SaveChanges,**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) [**InstallApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installapplication)o [**InstallComponent,**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent)viene eseguito un blocco del writer sul codice del server di catalogo COM+ che bloccherà l'ingresso di qualsiasi altro writer fino al commit o all'interruzione della transazione corrente. In altre informazioni, i writer possono accedere solo se hanno l'affinità di transazione corretta e partecipano alla transazione corrente.

I lettori non sono bloccati. Tuttavia, i dati visualizzati dai lettori non riflettono le modifiche provvisorie apportate all'interno della transazione fino al commit della transazione. Tutti i componenti che partecipano a tale transazione visualizzano gli stati dei dati provvisori quando leggono i dati, ma tutti i componenti esterni alla transazione visualizzano tali modifiche solo dopo il completamento della transazione.

## <a name="savechanges-behavior"></a>Comportamento di SaveChanges

Per ottenere il comportamento di isolamento descritto in precedenza, RegDB fornisce in modo efficace una cache su cui agivano i componenti all'interno della transazione. In questo modo viene modificato il comportamento [**del metodo SaveChanges.**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)

In genere, senza la presenza di una transazione, le modifiche in sospeso vengono scritte nel catalogo quando si chiama [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)e **SaveChanges** non viene restituito fino al completamento di tutte le scritture. Ciò garantisce che se una chiamata a **SaveChanges** viene restituita correttamente, è possibile chiamare [**StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) per attivare l'applicazione con dati nuovi.

Tuttavia, all'interno di una transazione, [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) influisce solo sulla cache, non sul RegDB stesso, e **SaveChanges** restituisce immediatamente se è stato eseguito il commit transazionale di tutte le modifiche in RegDB. Non è garantito che [**StartApplication utilizzi**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) dati nuovi dopo la restituzione **di SaveChanges.** Se è necessario chiamare **StartApplication** in questo contesto, è consigliabile attendere un certo periodo di tempo prima di eseguire questa operazione.

## <a name="transaction-time-out-period"></a>Periodo di Time-Out transazione

Se si eseguono numerose operazioni di amministrazione all'interno di una transazione, potrebbe trattarsi di una transazione a esecuzione lunga. In questo caso, il valore di timeout della transazione può essere un problema. Ciò è determinato dal valore di timeout della transazione impostato per il componente che avvia la transazione o dall'impostazione di timeout a livello di computer per il computer in cui è in esecuzione tale componente. Se vengono eseguite numerose operazioni all'interno di una transazione, è consigliabile impostare il periodo di timeout della transazione appropriato su un valore sufficientemente lungo e, se necessario, ripristinare l'impostazione originale al termine.

## <a name="non-transactional-com-catalog-resources"></a>Risorse del catalogo COM+ non transazionali

Il Registro di sistema, file system e Windows Installer (MSI) sono risorse del catalogo COM+ non transazionali.

> [!Note]  
> Se si verifica un errore che interrompe una transazione, è possibile che non venga eseguito il rollback delle modifiche a queste risorse.

 

Se si verifica un errore durante l'installazione di un'applicazione COM+ esistente da un file .msi, l'applicazione non viene visualizzata nello snap-in Servizi componenti, ma potrebbe essere visualizzata in Installazione applicazioni, nel qual caso è necessario rimuoverla manualmente.

## <a name="recovering-in-the-event-of-system-hangs"></a>Ripristino in caso di blocco del sistema

Se un componente che effettua operazioni di amministrazione all'interno di una transazione si blocca mentre contiene un blocco del writer sul codice del server di catalogo, impedirebbe a tutti gli altri utenti di apportare modifiche al catalogo. In questo caso, è possibile cancellare il blocco sul catalogo arrestando e riavviando l'applicazione Di sistema.

## <a name="scripting-with-a-transactioncontext-object"></a>Creazione di script con un oggetto TransactionContext

Un modo semplice per eseguire operazioni di amministrazione all'interno delle transazioni è usare un [**oggetto TransactionContext**](transactioncontext.md) per controllare la transazione. Ad esempio, lo script Visual Basic seguente illustra come aggiungere due nuove applicazioni in modo transazionale in modo che entrambe le applicazioni o nessuna delle due applicazioni vengono create:


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

[Esempio introduttivo sull'uso del catalogo di amministrazione COM+](introductory-example-using-the-com--administration-catalog.md)
</dt> <dt>

[Panoramica degli oggetti COMAdmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Recupero di raccolte nel catalogo COM+](retrieving-collections-on-the-com--catalog.md)
</dt> <dt>

[Impostazione delle proprietà e salvataggio delle modifiche nel catalogo COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
</dt> </dl>

 

 



