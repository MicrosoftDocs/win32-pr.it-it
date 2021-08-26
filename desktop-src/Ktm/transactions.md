---
description: Una transazione è un oggetto che definisce un'unità logica di lavoro.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transazioni (Gestione transazioni kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471d2ece52d510c1a77baa59ee3af980c4e4630a17d0911fdcbe590bad78903f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913881"
---
# <a name="transactions"></a>Transazioni

Una transazione è un oggetto che definisce un'unità logica di lavoro. La transazione è attiva fino a quando esiste un handle che fa riferimento alla transazione e viene considerata attiva se non è ancora stato eseguito il commit o il rollback della transazione. Se viene creata una transazione e tutti gli handle sono stati chiusi prima che si verifichi un commit o un rollback, verrà eseguito il rollback della transazione.

Si consideri il caso di un client transazionale in modalità utente che crea una transazione per l'ambito delle operazioni, quindi esegue gli aggiornamenti in uno o più gestori delle risorse. Si verifica quanto segue:

1.  Il client chiama la [**funzione CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) per creare la transazione e riceve un handle per tale transazione come valore restituito.

    La transazione può essere aperta o ereditata da un numero qualsiasi di processi. ogni processo è quindi coinvolto nella transazione. L'errore di uno di questi processi causerà l'interruzione della transazione.

    Questa transazione potrebbe non essere ancora persistente. Solo le transazioni che hanno raggiunto lo stato preparato devono essere recuperate tra gli errori di sistema se la transazione usa la registrazione presunta-interruzione.

2.  Il client deve passare una transazione al gestore delle risorse in modo esplicito.
3.  Il client esegue tutte le operazioni transazionali con una o più macchine virtuali, ad esempio file system transazionali.
4.  Il client chiama la [**funzione CommitTransaction.**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
5.  Il gestore delle risorse riceve notifiche da KTM per preparare ed eseguire il commit dei dati.

## <a name="transactions-and-threads"></a>Transazioni e thread

Le transazioni non sono uguali ai thread. Più thread o processi possono far parte di una singola transazione. Al contrario, un thread può far parte di diverse transazioni in momenti diversi.

## <a name="transaction-functions"></a>Funzioni di transazione

Le funzioni seguenti vengono usate con le transazioni.



| Funzione                                                            | Descrizione                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Richiede il commit della transazione specificata.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Richiede il commit della transazione specificata.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuovo oggetto transazione.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Restituisce le informazioni richieste sulla transazione specificata.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Apre una transazione esistente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Richiede il rollback della transazione specificata.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Richiede il rollback della transazione specificata. Questa funzione restituisce in modo asincrono. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Imposta le informazioni sulla transazione per la transazione specificata.                               |



 

 

 



