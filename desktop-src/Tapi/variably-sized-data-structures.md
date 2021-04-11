---
description: Quando si usano strutture di dati di dimensioni variabili per trasmettere informazioni tra TAPI e l'applicazione, l'applicazione è responsabile dell'allocazione della memoria necessaria.
ms.assetid: f1e2e864-fa10-4058-ba56-faa0ba7363a1
title: Strutture di dati di dimensioni variabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873fcbaa1e4e3bda772d92ad2de9b1f6258363cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233255"
---
# <a name="variably-sized-data-structures"></a>Strutture di dati di dimensioni variabili

Quando si usano strutture di dati di dimensioni variabili per trasmettere informazioni tra TAPI e l'applicazione, l'applicazione è responsabile dell'allocazione della memoria necessaria. La quantità di memoria allocata deve essere almeno sufficientemente grande per la parte fissa della struttura dei dati e viene impostata dall'applicazione nel membro **dwTotalSize** della struttura dei dati. I membri **dwUsedSize** e **dwNeededSize** sono compilati da TAPI. Se **dwTotalSize** è minore della dimensione della parte fissa, viene restituito LINEERR/PHONEERR \_ STRUCTURETOOSMALL. Se una funzione restituisce l'esito positivo, tutti i campi nella parte fissa sono stati compilati. I membri **dwUsedSize** e **dwNeededSize** possono essere confrontati per determinare se tutte le parti variabili sono state compilate e la quantità di spazio necessaria per riempirle tutte.

Se **dwNeededSize** è uguale a **dwUsedSize**, tutte le parti fisse e variabili sono state compilate. Se **dwNeededSize** è maggiore di **dwUsedSize**, è possibile che alcune parti della variabile siano state compilate, ma che i campi con dimensioni identiche siano stati compilati in modo non definito. Non viene mai troncata alcuna parte variabile e le parti variabili che verrebbero troncate a causa di spazio insufficiente sono indicate con entrambe le parti "offset" e "size" corrispondenti impostate su zero. Se non sono entrambi zero (e non è stato restituito alcun errore), indicano l'offset e le dimensioni dei dati della parte variabile non troncati validi.

Un'applicazione può sempre garantire che tutte le parti variabili siano compilate allocando e indicando i byte **dwNeededSize** per la struttura e chiamando di nuovo la funzione "Get" fino a quando la funzione non restituisce Success e **dwNeededSize** è uguale a **dwUsedSize**. Questa operazione dovrebbe verificarsi nel secondo tentativo, ad eccezione delle race condition che comportano modifiche alle dimensioni delle parti variabili tra le chiamate, che dovrebbero essere un evento raro.

> [!Note]  
> Tutte le stringhe di testo, indipendentemente dalla codifica, in strutture di dimensioni variabili devono essere con terminazione **null** in base alle normali convenzioni di gestione delle stringhe C.

 

 

 



