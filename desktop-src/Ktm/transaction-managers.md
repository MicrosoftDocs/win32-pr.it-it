---
description: Una gestione transazioni è un'istanza di un log. In KTM gli oggetti TM specificano il log e alcune delle funzionalità del TM. In genere sono presenti molti oggetti TM in un determinato nodo. I gestori di risorse (RM) devono essere associati a una TM specifica.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Gestori transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ea492a3eb10d95002d4e0a61500e7f1e74e87da21bc90daf680a2899e3fa67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424441"
---
# <a name="transaction-managers"></a>Gestori transazioni

Una gestione transazioni è un'istanza di un log. In KTM gli oggetti TM specificano il log e alcune delle funzionalità del TM. In genere sono presenti molti oggetti TM in un determinato nodo. I gestori di risorse (RM) devono essere associati a una TM specifica. Esistono tre tipi di TM:

-   TM volatile, senza log.
-   Un TM normale, che ha un log e viene usato per coordinare le transazioni di uno o più RM.
-   Gestione transazioni superiore.

## <a name="volatile-transaction-managers"></a>Gestori transazioni volatili

Un TM volatile è un TM per le macchine virtuali di sola lettura o volatili. Non dispone di un log e non rende persistente lo stato delle transazioni tra i riavvii del sistema.

## <a name="transaction-managers"></a>Gestori transazioni

Le macchine virtuali hanno un log, una o più macchine virtuali durevoli o volatili o entrambe. Il TM rende persistente lo stato di una transazione tra i riavvii del sistema fino al completamento delle transazioni. Viene usato un modello di interruzione presunta, quindi viene eseguito il rollback delle transazioni attive ma non preparate quando l'oggetto TM viene arrestato. Quando si apre un TM per la prima volta, è necessario recuperare il TM chiamando la [**funzione RecoverTransactionManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)

## <a name="superior-transaction-managers"></a>Gestori transazioni superiori

Un TM superiore è un TM per altre TM. Coordina le transazioni. Invia inoltre notifiche **TRANSACTION \_ NOTIFY \_ PREPARE** al gestore delle transazioni del kernel. Un esempio di TM superiore è il Microsoft Distributed Transaction Coordinator (DTC). Questa possibilità ha una responsabilità in più in fase di ripristino. Durante il ripristino, l'RM deve prima chiamare la [**funzione OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) per aprire nuovamente l'integrazione. Deve inoltre recapitare (o recapitare nuovamente) il risultato della transazione se è stato eseguito il commit della transazione; è possibile fornire un risultato chiamando la funzione [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) o [**la funzione RollbackTransaction.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) Questo vincolo non termina finché non riceve un evento di notifica **TRANSACTION \_ NOTIFY COMMIT \_ \_ COMPLETE** o **TRANSACTION NOTIFY ROLLBACK \_ \_ \_ COMPLETE** associato. Se un TM superiore non riesce a eseguire queste operazioni in fase di recupero, il KTM pulirà tutte le transazioni che non hanno ricevuto risultati entro la fine della fase di recupero. Tuttavia, ciò può comportare risultati di transazione incoerenti.

## <a name="transaction-manager-functions"></a>Funzioni di gestione transazioni

Le funzioni seguenti vengono utilizzate con i gestori transazioni.



| Funzione                                                                            | Descrizione                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuovo oggetto di gestione transazioni e restituisce un handle con l'accesso specificato.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Ottiene un valore di clock virtuale da una gestione transazioni.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ottiene un identificatore per la gestione transazioni specificata.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Apre una gestione transazioni esistente.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera lo stato di una gestione transazioni dal relativo file di log.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera lo stato di una gestione transazioni dal relativo file di log al valore di clock virtuale specificato. |



 

 

 



