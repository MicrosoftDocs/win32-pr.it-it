---
description: Le funzioni seguenti vengono utilizzate con le transazioni.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funzioni di gestione transazioni kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce98208b6ac78795be95b7255e9f263971ad6f08237e75ac0ef661c38a0878a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535281"
---
# <a name="kernel-transaction-manager-functions"></a>Funzioni di gestione transazioni kernel

Le funzioni seguenti vengono utilizzate con le transazioni.



| Funzione                                                            | Descrizione                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Richiede il commit della transazione specificata.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Richiede il commit della transazione specificata.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuovo oggetto transazione.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Ottiene l'ID per la transazione specificata.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Restituisce le informazioni richieste sulla transazione specificata.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Apre una transazione esistente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica che il gestore di risorse (RM) ha completato correttamente il rollback di una transazione. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Richiede il rollback della transazione specificata.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Richiede il rollback della transazione specificata. Questa funzione restituisce in modo asincrono.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Imposta le informazioni sulla transazione per la transazione specificata.                                 |



 

Le funzioni seguenti vengono usate con le integrazioni.



| Funzione                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica che un RM ha completato il commit di una transazione richiesta dalla gestione transazioni.                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Esegue il commit della transazione per l'integrazione specificata.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Ottiene l'ID per l'integrazione specificata.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea un'integrazione, ne imposta lo stato iniziale e apre un handle per l'integrazione con l'accesso specificato.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una struttura opaca dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un RM chiamando la [**funzione SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Dopo un errore, l'RM può usare [**la funzione GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Apre un oggetto di integrazione esistente e restituisce un handle per l'integrazione.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Chiamato da TM superiore per indicare che il lavoro di pre-preparazione è stato completato.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Chiamato da TM superiore per indicare che il lavoro di pre-preparazione è stato completato.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera lo stato di un'integrazione.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Richiede che l'integrazione specificata sia convertita in un'integrazione di sola lettura. Un'integrazione di sola lettura non può partecipare al risultato della transazione e non viene registrata in modo durevole per il recupero.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Esegue il rollback della transazione specificata associata a un'integrazione. Questa funzione non può essere chiamata per le integrazioni di sola lettura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Imposta una struttura opaca definita dall'utente dei dati di ripristino da KTM. Le informazioni di ripristino vengono archiviate in un log per conto di un RM chiamando [**SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Dopo un errore, l'RM può [**usare GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) per recuperare le informazioni.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica che l'RM sta rifiutando una richiesta a fase singola. Quando un TM riceve questa chiamata, avvia un commit in due fasi e invia una richiesta di preparazione a tutte le macchine virtuali integrate.                                                                                                                                                                                                             |



 

Le funzioni seguenti vengono usate con i gestori di risorse.



| Funzione                                                                           | Descrizione                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuovo oggetto RM e associa l'RM a una gestione transazioni.                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Richiede e riceve una notifica per RM. Questa funzione viene usata dal registro RM per ricevere notifiche quando lo stato di una transazione cambia.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Richiede e riceve una notifica asincrona per un RM. Questa funzione viene usata dall'RM per eseguire la registrazione per ricevere notifiche quando lo stato di una transazione cambia. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Apre un RM esistente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica che l'RM ha completato tutte le elaborazioni necessarie per garantire che un'operazione di commit o interruzione abbia esito positivo per la transazione specificata.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Segnala che l'RM ha completato il lavoro di preprepare, in modo che altre macchine virtuali di ripristino possano ora iniziare le operazioni di preparazione.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera lo stato di un RM dal relativo file di log.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Associa la porta di completamento I/O specificata all'RM specificato. Questa porta riceve tutte le notifiche per l'RM.                                             |



 

Le funzioni seguenti vengono utilizzate con i gestori transazioni.



| Funzione                                                                            | Descrizione                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuovo oggetto TM e restituisce un handle con l'accesso specificato.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Ottiene un valore di clock virtuale da un TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ottiene un identificatore per il TM specificato.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Apre una TM esistente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Apre una TM esistente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera lo stato di un TM dal relativo file di log.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Rinomina un TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera lo stato di TM dal file di log al valore di clock virtuale specificato. |



 

 

 



