---
description: Il Windows installer può eseguire un'installazione amministrativa di un'applicazione o di un prodotto in una rete per l'uso da parte di un gruppo di lavoro.
ms.assetid: 5840cfab-a127-4b1f-a7af-a2d8e2786928
title: Installazione amministrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26968b6b81c1c2aafedfd74151b139f61062baa29c44b04977a119b14ab1a8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381851"
---
# <a name="administrative-installation"></a>Installazione amministrativa

Il Windows installer può eseguire un'installazione amministrativa di un'applicazione o di un prodotto in una rete per l'uso da parte di un gruppo di lavoro. Un'installazione amministrativa installa un'immagine di origine dell'applicazione nella rete simile a un'immagine di origine in un CD-ROM. Gli utenti di un gruppo di lavoro che hanno accesso a questa immagine amministrativa possono quindi installare il prodotto da questa origine. Un utente deve prima installare il prodotto dalla rete per eseguire l'applicazione. L'utente può scegliere di eseguire dall'origine quando installa e il programma di installazione usa la maggior parte del file del prodotto direttamente dalla rete.

Gli amministratori possono eseguire un'installazione amministrativa dalla riga di comando usando l'opzione della riga di [comando](command-line-options.md)/a .

[L'azione ADMIN](admin-action.md) è l'azione di primo livello usata per avviare un'installazione amministrativa. Quando questa azione viene eseguita, il programma di installazione chiama le azioni nelle tabelle [AdminExecuteSequence](adminexecutesequence-table.md) e [AdminUISequence](adminuisequence-table.md) per eseguire l'installazione amministrativa.

La [**proprietà AdminProperties**](adminproperties.md) è un elenco delimitato da punto e virgola di proprietà impostate al momento di un'installazione amministrativa. Il programma di installazione usa queste proprietà durante un'installazione post-amministrazione dell'applicazione dall'immagine amministrativa.

Gli utenti che non hanno accesso continuo alla rete possono installare un'applicazione da un'immagine amministrativa e quindi a volte devono basarsi su supporti, ad esempio dischi CD-ROM, come origine di backup. In questi casi la lunghezza dei nomi di file nell'immagine amministrativa e nei supporti deve corrispondere. Entrambi devono usare nomi di file lunghi oppure entrambi devono usare nomi di file brevi. Ad esempio, un CD-ROM che supporta solo nomi di file brevi può fornire sia il supporto originale per l'installazione dell'immagine amministrativa che un'origine di backup.

Se la [**proprietà SHORTFILENAMES**](shortfilenames.md) viene impostata durante un'installazione amministrativa, potrebbe essere necessario impostare nuovamente questa proprietà da un utente che successivamente applica una patch all'immagine amministrativa. Quando si Windows installer per applicare la patch, il programma di installazione imposta automaticamente la **proprietà SHORTFILENAMES** se l'immagine amministrativa usa nomi di file brevi.

Se un amministratore usa un pacchetto con una proprietà [**Riepilogo**](word-count-summary.md) conteggio parole 2 o 3 per eseguire un'installazione amministrativa, gli utenti dell'immagine amministrativa non possono reinstallare automaticamente dall'origine del supporto originale. Se l'immagine amministrativa non è più disponibile, agli utenti che sono stati installati dall'immagine amministrativa non viene impedito di ripristinare il supporto originale.

L'applicazione [*di trasformazioni durante*](t-gly.md) la creazione di un'immagine amministrativa non ha alcun effetto valido. Per rendere disponibile una versione personalizzata di un prodotto a un gruppo di lavoro, applicare la trasformazione durante l'installazione del prodotto dall'immagine amministrativa.

Durante un'installazione amministrativa, il programma di installazione crea un'immagine di origine per tutte le funzionalità del prodotto, ad eccezione di quelle con 0 nella colonna Livello della [tabella Funzionalità](feature-table.md).

 

 



