---
description: L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da pianificare.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversione priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345456"
---
# <a name="priority-inversion"></a>Inversione priorità

L'inversione della priorità si verifica quando due o più thread con priorità diverse sono in conflitto da pianificare. Si consideri un caso semplice con tre thread: thread 1, thread 2 e thread 3. Il thread 1 è con priorità alta e diventa pronto per essere pianificato. Il thread 2, un thread con priorità bassa, sta eseguendo il codice in una sezione critica. Thread 1, il thread con priorità alta, inizia ad attendere una risorsa condivisa dal thread 2. Il thread 3 ha priorità media. Il thread 3 riceve tutto il tempo del processore, perché il thread con priorità alta (thread 1) è in attesa di risorse condivise dal thread con priorità bassa (thread 2). Il thread 2 non lascerà la sezione critica, perché non ha la priorità più alta e non verrà pianificata.

L'utilità di pianificazione risolve questo problema, incrementando in modo casuale la priorità dei thread pronti, in questo caso i blocchi con priorità bassa. I thread con priorità bassa vengono eseguiti abbastanza a lungo per uscire dalla sezione critica e il thread con priorità alta può accedere alla sezione critica. Se il thread con priorità bassa non ha tempo sufficiente per uscire dalla sezione critica per la prima volta, si otterrà un'altra opportunità durante il ciclo di pianificazione successivo.

 

 



