---
description: Il Windows installer elabora le azioni personalizzate come thread separato dall'installazione principale.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Azioni personalizzate sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ffa9de75d81cfe0c824bab0580f0e6565567a187f768d99687169b47543a41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893611"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Azioni personalizzate sincrone e asincrone

Il Windows installer elabora le azioni personalizzate come thread separato dall'installazione principale. Durante l'esecuzione sincrona di un'azione personalizzata, il programma di installazione attende il completamento del thread dell'azione personalizzata prima di continuare l'installazione principale. Durante l'esecuzione asincrona, il programma di installazione esegue l'azione personalizzata simultaneamente mentre l'installazione corrente continua. Gli autori di azioni personalizzate devono pertanto essere a conoscenza di eventuali thread asincroni che potrebbero apportare modifiche al database di installazione tra le chiamate di funzione.

In particolare, le chiamate [**a MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devono essere evitate nelle azioni personalizzate asincrone. Usare invece [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) per ottenere un percorso di destinazione. Le operazioni bulk del database, ad esempio le operazioni di importazione, esportazione e trasformazione, devono essere evitate in qualsiasi tipo di azione personalizzata.

I flag di opzione possono essere impostati nel campo Tipo della tabella [CustomAction](customaction-table.md) per specificare che i thread di azione principale e personalizzata vengono eseguiti in modo sincrono o asincrono. Vedere [Opzioni di elaborazione per la restituzione di azioni personalizzate](custom-action-return-processing-options.md).

Il programma di installazione può eseguire [solo azioni personalizzate di rollback](rollback-custom-actions.md) e installazione [simultanea](concurrent-installations.md) come azioni personalizzate sincrone.

 

 



