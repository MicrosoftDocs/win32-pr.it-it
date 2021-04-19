---
description: Una transazione è un oggetto che definisce un'unità logica di lavoro.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transazioni (gestione transazioni kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311126"
---
# <a name="transactions"></a>Transazioni

Una transazione è un oggetto che definisce un'unità logica di lavoro. La transazione è attiva finché è presente un handle che fa riferimento alla transazione e viene considerato attivo se non è ancora stato eseguito il commit o il rollback della transazione. Se viene creata una transazione e tutti gli handle sono stati chiusi prima del commit o del rollback, viene eseguito il rollback della transazione.

Si consideri il caso di un client transazionale in modalità utente che crea una transazione per definire l'ambito delle operazioni, quindi esegue gli aggiornamenti in uno o più gestori di risorse. Si verifica quanto segue:

1.  Il client chiama la funzione [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) per creare la transazione e riceve un handle per tale transazione come valore restituito.

    La transazione può essere aperta o ereditata da un numero qualsiasi di processi. ogni processo è quindi occupato dalla transazione. L'errore di uno di questi processi causerà l'interruzione della transazione.

    Questa transazione potrebbe non essere ancora persistente. Se la transazione utilizza la registrazione presunta-interruzione, è necessario recuperare solo le transazioni che hanno raggiunto lo stato preparato in tutti gli errori di sistema.

2.  Il client deve passare in modo esplicito una transazione a Resource Manager.
3.  Il client esegue tutte le operazioni transazionali con uno o più RMs, ad esempio i file system transazionali.
4.  Il client chiama la funzione [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .
5.  Resource Manager riceve le notifiche da KTM per preparare ed eseguire il commit dei dati.

## <a name="transactions-and-threads"></a>Transazioni e thread

Le transazioni non corrispondono ai thread. Più thread o processi possono far parte di una singola transazione. Viceversa, un thread può essere parte di diverse transazioni in momenti diversi.

## <a name="transaction-functions"></a>Funzioni di transazione

Le funzioni seguenti vengono utilizzate con le transazioni.



| Funzione                                                            | Descrizione                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Richiede che venga eseguito il commit della transazione specificata.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Richiede che venga eseguito il commit della transazione specificata.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuovo oggetto transazione.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Restituisce le informazioni richieste sulla transazione specificata.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Apre una transazione esistente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Richiede che venga eseguito il rollback della transazione specificata.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Richiede che venga eseguito il rollback della transazione specificata. Questa funzione restituisce in modo asincrono. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Imposta le informazioni sulla transazione per la transazione specificata.                               |



 

 

 



