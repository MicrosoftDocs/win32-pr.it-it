---
description: Una gestione transazioni (TM) è un'istanza di un log. In KTM gli oggetti TM specificano il log e alcune delle funzionalità della TM. In un nodo specifico sono in genere presenti molti oggetti TM. I gestori di risorse (RMs) devono essere associati a una specifica TM.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Gestori transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311127"
---
# <a name="transaction-managers"></a>Gestori transazioni

Una gestione transazioni (TM) è un'istanza di un log. In KTM gli oggetti TM specificano il log e alcune delle funzionalità della TM. In un nodo specifico sono in genere presenti molti oggetti TM. I gestori di risorse (RMs) devono essere associati a una specifica TM. Sono disponibili tre tipi di TMs:

-   Una TM volatile, che non ha log.
-   Un TM regolare, che ha un log e viene usato per coordinare le transazioni di uno o più RMs.
-   Una gestione transazioni superiore.

## <a name="volatile-transaction-managers"></a>Gestori transazioni volatili

Una TM volatile è una TM per la sola lettura o per RMs volatile. Non dispone di un log e non rende persistente lo stato delle transazioni tra i riavvii del sistema.

## <a name="transaction-managers"></a>Gestori transazioni

Le TMs includono un log, uno o più RMs durevole o volatile o entrambi. Il TM renderà permanente lo stato di una transazione tra i riavvii del sistema finché le transazioni non vengono completate. Viene usato un modello presunto di interruzione, quindi le transazioni che erano attive ma non preparate quando l'oggetto TM viene arrestato viene eseguito il rollback. Quando si apre una TM per la prima volta, è necessario recuperare la TM chiamando la funzione [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) .

## <a name="superior-transaction-managers"></a>Gestori transazioni superiori

Una TM superiore è una TM per le altre TM. Coordina le transazioni. Genera inoltre notifiche per la **\_ \_ preparazione della notifica di transazione** a gestione transazioni kernel. Un esempio di TM superiore è Microsoft Distributed Transaction Coordinator (DTC). Questa possibilità viene fornita con una responsabilità aggiuntiva in fase di ripristino. Durante il ripristino, RM deve prima chiamare la funzione [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) per riaprire l'integrazione. Deve inoltre recapitare o recapitare il risultato della transazione se è stato eseguito il commit della transazione. è possibile recapitare un risultato chiamando la funzione [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) o [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) . Questo obbligo non termina fino a quando non viene ricevuto un evento di notifica del commit della transazione di notifica **\_ \_ \_ completato** o di notifica di **transazione \_ \_ \_** . Se una TM superiore non riesce a eseguire queste operazioni al momento del ripristino, la KTM eliminerà tutte le transazioni che non hanno ricevuto risultati al termine della fase di recupero. Tuttavia, ciò può comportare risultati di transazione incoerenti.

## <a name="transaction-manager-functions"></a>Funzioni di gestione transazioni

Con i gestori delle transazioni vengono utilizzate le funzioni seguenti.



| Funzione                                                                            | Descrizione                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuovo oggetto di gestione transazioni (TM) e restituisce un handle con l'accesso specificato.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Ottiene un valore di clock virtuale da una gestione transazioni.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ottiene un identificatore per la gestione transazioni specificata.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Apre una gestione transazioni esistente.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera lo stato di una gestione transazioni dal relativo file di log.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera lo stato di una gestione transazioni dal relativo file di log al valore di clock virtuale specificato. |



 

 

 



