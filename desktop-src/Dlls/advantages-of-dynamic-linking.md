---
description: Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico.
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: Vantaggi del collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313386"
---
# <a name="advantages-of-dynamic-linking"></a>Vantaggi del collegamento dinamico

Il collegamento dinamico presenta i vantaggi seguenti rispetto al collegamento statico:

-   Più processi che caricano la stessa DLL nello stesso indirizzo di base condividono una singola copia della DLL nella memoria fisica. Questa operazione consente di risparmiare memoria di sistema e di ridurre lo scambio.
-   Quando le funzioni in una DLL cambiano, non è necessario ricompilare o ricollegare le applicazioni che le utilizzano finché gli argomenti della funzione, le convenzioni di chiamata e i valori restituiti non cambiano. Al contrario, il codice oggetto collegato staticamente richiede che l'applicazione venga ricollegata quando le funzioni cambiano.
-   Una DLL può fornire supporto After-Market. Ad esempio, è possibile modificare una DLL del driver di visualizzazione per supportare una visualizzazione che non era disponibile quando l'applicazione è stata inizialmente spedita.
-   I programmi scritti in linguaggi di programmazione diversi possono chiamare la stessa funzione DLL purché i programmi seguano la stessa convenzione di chiamata utilizzata dalla funzione. La convenzione di chiamata, ad esempio C, Pascal o chiamata standard, controlla l'ordine in cui la funzione chiamante deve effettuare il push degli argomenti nello stack, se la funzione o la funzione chiamante è responsabile della pulizia dello stack e se gli argomenti vengono passati nei registri. Per ulteriori informazioni, vedere la documentazione inclusa con il compilatore.

Un potenziale svantaggio nell'uso delle dll è che l'applicazione non è indipendente. dipende dall'esistenza di un modulo DLL separato. Il sistema termina i processi utilizzando il collegamento dinamico in fase di caricamento se richiedono una DLL non trovata all'avvio del processo e genera un messaggio di errore all'utente. Il sistema non termina un processo utilizzando il collegamento dinamico in fase di esecuzione in questa situazione, ma le funzioni esportate dalla DLL mancante non sono disponibili per il programma.

 

 



