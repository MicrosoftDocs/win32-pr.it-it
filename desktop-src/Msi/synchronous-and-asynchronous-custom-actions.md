---
description: Il Windows Installer elabora le azioni personalizzate come thread separato dall'installazione principale.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Azioni personalizzate sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308675"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a>Azioni personalizzate sincrone e asincrone

Il Windows Installer elabora le azioni personalizzate come thread separato dall'installazione principale. Durante l'esecuzione sincrona di un'azione personalizzata, il programma di installazione attende il completamento del thread dell'azione personalizzata prima di continuare l'installazione principale. Durante l'esecuzione asincrona, il programma di installazione esegue l'azione personalizzata contemporaneamente mentre l'installazione corrente continua. Gli autori di azioni personalizzate devono pertanto essere a conoscenza di eventuali thread asincroni che possono apportare modifiche al database di installazione tra le chiamate di funzione.

In particolare, le chiamate a [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) e [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) devono essere evitate in azioni personalizzate asincrone. Usare invece [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) per ottenere un percorso di destinazione. Le operazioni di database bulk, ad esempio le operazioni di importazione, esportazione e trasformazione, devono essere evitate in qualsiasi tipo di azione personalizzata.

I flag di opzione possono essere impostati nel campo Type della [tabella CustomAction](customaction-table.md) per specificare che i thread delle azioni principale e personalizzata vengono eseguiti in modo sincrono o asincrono. Vedere [Opzioni di elaborazione della restituzione dell'azione personalizzata](custom-action-return-processing-options.md).

Il programma di installazione può eseguire azioni [personalizzate di rollback](rollback-custom-actions.md) e azioni di [installazione simultanee](concurrent-installations.md) come azioni personalizzate sincrone.

 

 



