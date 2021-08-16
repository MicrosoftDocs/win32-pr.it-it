---
title: Modello di replica per programmatori in Active Directory Domain Services
description: Di seguito è riportata una descrizione del modello di replica per Active Directory Domain Services.
ms.assetid: 45baf7ff-9474-4f86-81c8-03336901fec2
ms.tgt_platform: multiple
keywords:
- Modello per programmatori di Active Directory Replication AD
- Modello di replica per programmatori in Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b758a31913d0c306105d0d3ce51e72607530e314d79601e8e5230495458d9793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841231"
---
# <a name="a-programmers-model-of-replication-in-active-directory-domain-services"></a>Modello di replica per programmatori in Active Directory Domain Services

Di seguito è riportata una descrizione del modello di replica per Active Directory Domain Services.

Tutti gli aggiornamenti al controller Dominio di Active Directory (DC) vengono eseguiti usando richieste LDAP che creano, modificano o eliminano un oggetto per ogni richiesta. Una singola richiesta può impostare o modificare più attributi in un oggetto.

Una richiesta di aggiornamento viene elaborata come transazione atomica in alcuni controller di dominio. Viene eseguita l'intera operazione di aggiornamento o non viene eseguita nessuna di essa. Se il richiedente riceve una risposta corretta a una richiesta di aggiornamento, l'intera richiesta ha avuto esito positivo (commit). Questa operazione è detta "scrittura di origine". Non è possibile raggruppare più richieste LDAP in un'unica transazione più grande.

In una scrittura di origine, un controller di dominio calcola un "stamp" per ogni valore di attributo nuovo o modificato e allega tale indicatore al valore in modo che, quando il valore viene replicato, viene replicato anche lo stamp. Il nuovo timbro è univoco e, in caso di aggiornamento, il nuovo stamp è maggiore dello stamp sul valore precedente in tale controller di dominio.

In alcuni casi, un controller di dominio seleziona il set di oggetti che sono stati modificati dall'ultima volta in cui il controller di dominio ha eseguito la replica. Quindi, per ogni oggetto, invia un singolo messaggio a tutti gli altri controller di dominio che contengono tutti i valori correnti degli attributi modificati dall'ultima replica dell'oggetto. I messaggi di replica sono affidabili e vengono recapitati in ordine, ma possono richiedere più tempo per il recapito.

Quando un controller di dominio riceve un messaggio di replica da un altro controller di dominio, lo elabora come indicato di seguito: per ogni attributo modificato, se lo stamp sul valore nel messaggio di replica è maggiore dello stamp sul valore corrente, il controller di dominio applica l'aggiornamento. In caso contrario, il controller di dominio rimuove l'aggiornamento. Ogni messaggio di replica viene applicato come transazione atomica, proprio come una scrittura di origine.

Questo è il modello Active Directory Domain Services replica. Le proprietà principali di questo modello includono:

-   Una scrittura di origine in un singolo oggetto è atomica.
-   Quando si replicano le modifiche, vengono inviate tutte le modifiche apportate da una scrittura di origine o nessuna di esse.
-   Una scrittura replicata in un singolo oggetto è atomica, ma i conflitti vengono risolti attributo per attributo.

Il modello non garantisce l'ordine di replica delle modifiche apportate a oggetti diversi. Non scrivere applicazioni che presuppongono che le modifiche vengano replicate in ordine di origine/scrittura. Il modello non garantisce che se un attributo di un oggetto viene modificato due volte, entrambi i valori verranno replicati. La replica invia solo il valore corrente al momento della replica.

Il modello differisce dalla realtà in diversi modi che influiscono solo sulle prestazioni. Ad esempio, il server Active Directory invia messaggi di replica contenenti le modifiche a più oggetti, ma elabora il contenuto di tale messaggio multio object come se fosse una serie di messaggi a oggetto singolo. Il server Active Directory non esegue la replica da punto a punto come descritto nel modello, ma esegue invece una replica transitiva più complessa ed efficiente equivalente dal punto di vista funzionale al modello.

 

 




