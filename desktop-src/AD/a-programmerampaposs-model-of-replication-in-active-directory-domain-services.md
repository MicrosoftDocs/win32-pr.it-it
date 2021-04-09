---
title: Modello di replica di un programmatore in Active Directory Domain Services
description: Di seguito è riportata una descrizione del modello di replica per Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Modello di programmatore di Active Directory Active Directory Replication
- Modello di replica di un programmatore in Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ada20bc07411528eaea4b7ff8c773c50ae8b6ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044021"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Modello di replica di un programmatore in Active Directory Domain Services

Di seguito è riportata una descrizione del modello di replica per Active Directory Domain Services.

Tutti gli aggiornamenti per il controller di Dominio di Active Directory (DC) vengono eseguiti tramite richieste LDAP che creano, modificano o eliminano un oggetto per ogni richiesta. Una singola richiesta può impostare o modificare più attributi in un oggetto.

Una richiesta di aggiornamento viene elaborata come transazione atomica in un controller di dominio. L'intero aggiornamento viene eseguito o nessuno di essi. Se il richiedente riceve una risposta corretta a una richiesta di aggiornamento, l'intera richiesta ha avuto esito positivo (eseguito il commit). Questa operazione viene definita "scrittura di origine". Non è possibile raggruppare più richieste LDAP in un'unica transazione di dimensioni maggiori.

In una scrittura di origine, un controller di dominio calcola un "timbro" per ogni valore di attributo nuovo o modificato e connette questo timbro al valore in modo che, quando il valore viene replicato, il timbro viene replicato. Il nuovo timbro è univoco e, nel caso di un aggiornamento, il nuovo timbro è più grande del timbro sul valore precedente del controller di dominio.

In alcuni casi, un controller di dominio seleziona il set di oggetti che sono stati modificati dall'ultima volta in cui il controller di dominio ha eseguito la replica. Quindi, per ogni oggetto, invia un singolo messaggio a tutti gli altri controller di dominio che contengono tutti i valori correnti degli attributi modificati dall'ultima volta in cui l'oggetto è stato replicato. I messaggi di replica sono affidabili e vengono recapitati in ordine, ma possono richiedere più tempo per essere recapitati.

Quando un controller di dominio riceve un messaggio di replica da un altro controller di dominio, lo elabora come segue: per ogni attributo modificato, se il timbro sul valore nel messaggio di replica è maggiore del timbro sul valore corrente, il controller di dominio applica l'aggiornamento; in caso contrario, il controller di dominio ignora l'aggiornamento. Ogni messaggio di replica viene applicato come transazione atomica, proprio come una scrittura di origine.

Si tratta del modello di replica Active Directory Domain Services. Le proprietà chiave di questo modello includono:

-   Una scrittura di origine in un singolo oggetto è atomica.
-   Quando si replicano le modifiche, vengono inviate tutte le modifiche apportate da una scrittura di origine o nessuna di esse.
-   Una scrittura replicata in un singolo oggetto è atomica, ma i conflitti vengono risolti in base all'attributo.

Il modello non garantisce l'ordine di replica delle modifiche apportate a oggetti diversi. Non scrivere applicazioni che presuppongono che le modifiche vengano replicate nell'ordine di scrittura di origine. Il modello non garantisce che se un attributo di un oggetto viene modificato due volte, verranno replicati entrambi i valori. La replica invia solo il valore corrente al momento della replica.

Il modello è diverso dalla realtà in diversi modi che influiscono solo sulle prestazioni. Ad esempio, il server Active Directory Invia messaggi di replica contenenti le modifiche a più oggetti, ma elabora il contenuto di un messaggio multioggetto come se fosse una serie di messaggi a oggetto singolo. Il server Active Directory non esegue la replica Point-to-Point come descritto nel modello, ma esegue invece una replica transitiva più complessa e più efficiente, funzionalmente equivalente al modello.

 

 




