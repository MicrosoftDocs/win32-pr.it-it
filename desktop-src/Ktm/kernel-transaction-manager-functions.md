---
description: Le funzioni seguenti vengono utilizzate con le transazioni.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funzioni di gestione transazioni kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885121"
---
# <a name="kernel-transaction-manager-functions"></a>Funzioni di gestione transazioni kernel

Le funzioni seguenti vengono utilizzate con le transazioni.



| Funzione                                                            | Descrizione                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Richiede che venga eseguito il commit della transazione specificata.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Richiede che venga eseguito il commit della transazione specificata.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuovo oggetto transazione.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Ottiene l'ID per la transazione specificata.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Restituisce le informazioni richieste sulla transazione specificata.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Apre una transazione esistente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica che Gestione risorse (RM) ha completato correttamente il rollback di una transazione. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Richiede che venga eseguito il rollback della transazione specificata.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Richiede che venga eseguito il rollback della transazione specificata. Questa funzione restituisce in modo asincrono.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Imposta le informazioni sulla transazione per la transazione specificata.                                 |



 

Le funzioni seguenti vengono usate con gli elenchi.



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica che un RM ha completato il commit di una transazione richiesta da Transaction Manager (TM).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Viene eseguito il commit della transazione per l'integrazione specificata.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Ottiene l'ID per l'elenco specificato.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea un'integrazione, ne imposta lo stato iniziale e apre un handle per l'elenco con l'accesso specificato.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una struttura opaca dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un RM chiamando la funzione [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . In seguito a un errore, RM può utilizzare la funzione [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Apre un oggetto di integrazione esistente e restituisce un handle per l'integrazione.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Chiamato da Superior TM per indicare che è stata completata la preparazione del lavoro preliminare.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Chiamato da Superior TM per indicare che è stata completata la preparazione del lavoro preliminare.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera lo stato di un elenco.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Richiede che l'integrazione specificata venga convertita in un elenco di sola lettura. Un elenco di sola lettura non può partecipare al risultato della transazione e non viene registrato in modo durevole per il ripristino.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Esegue il rollback della transazione specificata associata a un'integrazione. Questa funzione non può essere chiamata per l'integrazione di sola lettura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Imposta una struttura opaca definita dall'utente dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un RM chiamando [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). In seguito a un errore, il gestore di risorse può utilizzare [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica che RM sta rifiutando una richiesta a fase singola. Quando una TM riceve questa chiamata, avvia un commit a due fasi e invia una richiesta di preparazione a tutti i RMs integrati.                                                                                                                                                                                                             |



 

Le funzioni seguenti vengono usate con i gestori di risorse.



| Funzione                                                                           | Descrizione                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuovo oggetto RM e associa RM a una gestione transazioni (TM).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Richiede e riceve una notifica per RM. Questa funzione viene utilizzata dal registro RM per ricevere notifiche quando lo stato di una transazione viene modificato.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Richiede e riceve una notifica asincrona per un RM. Questa funzione viene utilizzata da RM per la registrazione per ricevere notifiche quando lo stato di una transazione viene modificato. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Apre un RM esistente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica che RM ha completato tutte le operazioni di elaborazione necessarie per garantire l'esito positivo di un'operazione di commit o di interruzione per la transazione specificata.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Segnala che questo RM ha completato il lavoro di prepreparazione, in modo che altri RMs possano ora iniziare le operazioni di preparazione.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera lo stato di un RM dal relativo file di log.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa la porta di completamento I/O specificata con la RM specificata. Questa porta riceve tutte le notifiche per RM.                                             |



 

Con i gestori delle transazioni vengono utilizzate le funzioni seguenti.



| Funzione                                                                            | Descrizione                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuovo oggetto TM e restituisce un handle con l'accesso specificato.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Ottiene un valore di clock virtuale da una TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ottiene un identificatore per la TM specificata.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Apre una TM esistente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Apre una TM esistente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera lo stato di TM dal relativo file di log.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Rinomina una TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera lo stato di TM dal relativo file di log al valore di clock virtuale specificato. |



 

 

 



