---
description: Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vantaggi del collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a35e254ae14f74d5e2ed4c260f3ee201e2fd1f62efd8aa953b708256e437c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632281"
---
# <a name="advantages-of-dynamic-linking"></a>Vantaggi del collegamento dinamico

Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico:

-   Più processi che caricano la stessa DLL allo stesso indirizzo di base condividono una singola copia della DLL nella memoria fisica. In questo modo si risparmia memoria di sistema e si riduce lo scambio.
-   Quando le funzioni in una DLL cambiano, le applicazioni che le usano non devono essere ricompilate o ricollegate purché gli argomenti della funzione, le convenzioni di chiamata e i valori restituiti non cambino. Al contrario, il codice oggetto collegato in modo statico richiede che l'applicazione sia ricollegata quando le funzioni cambiano.
-   Una DLL può fornire supporto dopo il mercato. Ad esempio, una DLL del driver di visualizzazione può essere modificata per supportare una visualizzazione che non era disponibile quando l'applicazione è stata inizialmente spedita.
-   I programmi scritti in linguaggi di programmazione diversi possono chiamare la stessa funzione DLL purché seguano la stessa convenzione di chiamata utilizzata dalla funzione. La convenzione di chiamata (ad esempio C, Pascal o chiamata standard) controlla l'ordine in cui la funzione chiamante deve eseguire il push degli argomenti nello stack, se la funzione o la funzione chiamante è responsabile della pulizia dello stack e se vengono passati argomenti nei registri. Per altre informazioni, vedere la documentazione inclusa nel compilatore.

Un potenziale svantaggio dell'uso delle DLL è che l'applicazione non è autonoma. dipende dall'esistenza di un modulo DLL separato. Il sistema termina i processi usando il collegamento dinamico in fase di caricamento se richiedono una DLL che non viene trovata all'avvio del processo e restituisce un messaggio di errore all'utente. Il sistema non termina un processo usando il collegamento dinamico in fase di esecuzione in questa situazione, ma le funzioni esportate dalla DLL mancante non sono disponibili per il programma.

 

 



