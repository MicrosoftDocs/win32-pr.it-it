---
description: Attività delle transazioni COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Attività delle transazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102b0ec6ae54430be5499c67b5041ee26035eb077e27b1b860377cd728e3e42d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307591"
---
# <a name="com-transactions-tasks"></a>Attività delle transazioni COM+

Anche se l'elaborazione automatica delle transazioni in COM+ consente di dedicare più tempo di sviluppo alla creazione e alla configurazione di oggetti che si desidera partecipare alle transazioni automatiche, esistono alcune attività di programmazione che è possibile eseguire per adattare il comportamento delle transazioni ai requisiti dell'applicazione.

Negli argomenti seguenti vengono illustrate opzioni di programmazione specifiche correlate all'elaborazione delle transazioni.



| Argomento                                                                                             | Descrizione                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Impostazione dell'attributo della transazione](setting-the-transaction-attribute.md)<br/>             | Viene descritto come impostare i valori degli attributi della transazione per gli oggetti transazione.<br/>         |
| [Impostazione del livello di isolamento delle transazioni](setting-the-transaction-isolation-level.md)<br/> | Viene descritto come impostare i livelli di isolamento delle transazioni per gli oggetti transazione.<br/>     |
| [Impostazione del timeout della transazione](setting-the-transaction-time-out.md)<br/>               | Viene descritto come impostare gli intervalli di timeout per le transazioni.<br/>                          |
| [Impostazione dei flag Coerenti e Done](setting-the-consistent-and-done-flags.md)<br/>     | Viene illustrato come usare i flag coerenti e non evasi per controllare il risultato di una transazione.<br/> |
| [Creazione di oggetti BYOT](creating-byot-objects.md)<br/>                                     | Viene descritto come creare oggetti in modo da poter usare bring your own transaction (BYOT).<br/>           |



 

> [!Note]  
> Come regola generale, qualsiasi componente che aggiorna lo stato permanente deve supportare le transazioni. I componenti che combinano le operazioni di due o più oggetti in una singola attività devono usare le transazioni per semplificare il ripristino degli errori. Inoltre, per rilasciare risorse, ad esempio connessioni di database, le transazioni in COM+ devono essere brevi quanto è possibile creare.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi alle transazioni COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




