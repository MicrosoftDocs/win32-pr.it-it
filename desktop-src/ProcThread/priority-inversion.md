---
description: L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da programmare.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversione priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a891655196b8f7e81c118d39fb8516a244411f1f4f6d9505e2fb40818d71f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031931"
---
# <a name="priority-inversion"></a>Inversione priorità

L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da programmare. Si consideri un caso semplice con tre thread: thread 1, thread 2 e thread 3. Il thread 1 ha priorità alta e diventa pronto per essere pianificato. Il thread 2, un thread con priorità bassa, esegue il codice in una sezione critica. Il thread 1, il thread con priorità alta, inizia l'attesa di una risorsa condivisa dal thread 2. Il thread 3 ha priorità media. Il thread 3 riceve tutto il tempo del processore, perché il thread ad alta priorità (thread 1) è in attesa di risorse condivise dal thread con priorità bassa (thread 2). Il thread 2 non lascia la sezione critica, perché non ha la priorità più alta e non verrà pianificato.

L'utilità di pianificazione risolve questo problema aumentando in modo casuale la priorità dei thread pronti (in questo caso, i titolari di blocchi con priorità bassa). I thread con priorità bassa vengono eseguiti per un tempo sufficiente per uscire dalla sezione critica e il thread con priorità alta può entrare nella sezione critica. Se il thread con priorità bassa non ottiene tempo di CPU sufficiente per uscire dalla sezione critica la prima volta, si otterrà un'altra possibilità durante il ciclo di pianificazione successivo.

 

 



