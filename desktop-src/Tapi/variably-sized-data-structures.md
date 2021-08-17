---
description: Quando vengono usate strutture di dati di dimensioni variabili per trasmettere informazioni tra TAPI e l'applicazione, l'applicazione è responsabile dell'allocazione della memoria necessaria.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Strutture di dati con dimensioni variabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182e349079abbce93f533b1b6cd299ab7e0e883d71e9b845dfdaf52bf0275ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760196"
---
# <a name="variably-sized-data-structures"></a>Strutture di dati con dimensioni variabili

Quando vengono usate strutture di dati di dimensioni variabili per trasmettere informazioni tra TAPI e l'applicazione, l'applicazione è responsabile dell'allocazione della memoria necessaria. La quantità di memoria allocata deve essere almeno sufficiente per la parte fissa della struttura dei dati e viene impostata dall'applicazione nel membro **dwTotalSize** della struttura dei dati. I **membri dwUsedSize** **e dwNeededSize** vengono compilati da TAPI. Se **dwTotalSize** è minore delle dimensioni della parte fissa, viene restituito LINEERR/PHONEERR \_ STRUCTURETOOSMALL. Se una funzione restituisce l'esito positivo, tutti i campi nella parte fissa sono stati compilati. I **membri dwUsedSize** e **dwNeededSize** possono essere confrontati per determinare se tutte le parti variabili sono state compilate e la quantità di spazio necessaria per riempirle tutte.

Se **dwNeededSize** è uguale a **dwUsedSize**, tutte le parti fisse e variabili sono state compilate. Se **dwNeededSize** è maggiore di **dwUsedSize**, è possibile che alcune parti variabili siano state compilate, ma esattamente quali campi di dimensioni variabili sono stati compilati non sono definiti. Nessuna parte variabile viene troncata e le parti variabili che sarebbero state troncate a causa di spazio insufficiente sono indicate con entrambe le parti "Offset" e "Size" corrispondenti impostate su zero. Se non sono entrambi zero (e non è stato restituito alcun errore), indicano l'offset e le dimensioni dei dati validi della parte variabile nontruncated.

Un'applicazione può sempre garantire che tutte le parti variabili siano compilate allocando e indicando i byte **dwNeededSize** per la struttura e chiamando di nuovo la funzione "Get" fino a quando la funzione non restituisce l'esito positivo e **dwNeededSize è** uguale a **dwUsedSize**. Ciò dovrebbe verificarsi al secondo tentativo, ad eccezione delle race conditions che causano modifiche nelle dimensioni delle parti variabili tra le chiamate, che dovrebbero essere un evento raro.

> [!Note]  
> Tutte le stringhe di testo, indipendentemente dalla codifica, nelle strutture di dimensioni variabili devono essere **NULL**-terminate in base alle normali convenzioni di gestione delle stringhe C.

 

 

 



