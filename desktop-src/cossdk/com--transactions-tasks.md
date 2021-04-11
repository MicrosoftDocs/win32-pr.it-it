---
description: Attività delle transazioni COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Attività delle transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127154"
---
# <a name="com-transactions-tasks"></a>Attività delle transazioni COM+

Mentre l'elaborazione automatica delle transazioni in COM+ consente di impiegare un tempo di sviluppo più produttivo per la creazione e la configurazione di oggetti che si desidera includere nelle transazioni automatiche, è possibile eseguire alcune attività di programmazione per adattare il comportamento delle transazioni ai requisiti dell'applicazione.

Negli argomenti seguenti vengono illustrate le opzioni di programmazione specifiche relative all'elaborazione delle transazioni.



| Argomento                                                                                             | Descrizione                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Impostazione dell'attributo Transaction](setting-the-transaction-attribute.md)<br/>             | Viene descritto come impostare i valori degli attributi di transazione per gli oggetti della transazione.<br/>         |
| [Impostazione del livello di isolamento delle transazioni](setting-the-transaction-isolation-level.md)<br/> | Viene descritto come impostare i livelli di isolamento delle transazioni per gli oggetti della transazione.<br/>     |
| [Impostazione del timeout della transazione](setting-the-transaction-time-out.md)<br/>               | Viene descritto come impostare gli intervalli di timeout per le transazioni.<br/>                          |
| [Impostazione dei flag coerenti e done](setting-the-consistent-and-done-flags.md)<br/>     | Viene illustrato come utilizzare i flag coerenti e done per controllare il risultato di una transazione.<br/> |
| [Creazione di oggetti BYOT](creating-byot-objects.md)<br/>                                     | Viene descritto come creare oggetti in modo che sia possibile eseguire una transazione personalizzata (BYOT).<br/>           |



 

> [!Note]  
> Come regola generale, qualsiasi componente che aggiorna lo stato persistente deve supportare le transazioni. I componenti che combinano le operazioni di due o più oggetti in una singola attività devono utilizzare le transazioni per semplificare il ripristino degli errori. Inoltre, per rilasciare le risorse, ad esempio le connessioni al database, le transazioni in COM+ dovrebbero essere le più brevi possibile.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti sulle transazioni COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




