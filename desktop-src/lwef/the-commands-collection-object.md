---
title: Oggetto raccolta di comandi
description: Oggetto raccolta di comandi
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2367035d86f92d57dc459564943b9e7797ecb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398862"
---
# <a name="the-commands-collection-object"></a>Oggetto raccolta di comandi

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server Microsoft Agent gestisce un elenco di comandi attualmente disponibili per l'utente. Questo elenco include i comandi definiti dal server per l'interazione generale (ad esempio Hide e Open The Voice Commands window), l'elenco di client disponibili, ma non di input, e i comandi definiti dal client attivo corrente. I primi due set di comandi sono comandi globali. ovvero sono disponibili in qualsiasi momento, indipendentemente dal client attivo di input. I comandi definiti dal client sono disponibili solo quando il client è di input-attivo e il carattere è visibile.

Ogni applicazione client può definire una raccolta di comandi denominata raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Per aggiungere un comando alla raccolta, utilizzare il metodo [**Add**](add-method.md) o [**Insert**](insert-method.md) . Sebbene sia possibile specificare le proprietà di un comando con istruzioni separate, per prestazioni ottimali del codice specificare tutte le proprietà di un comando nell'istruzione **Add** o **Insert** Method. Per ogni comando della raccolta, è possibile determinare se l'accesso utente al comando viene visualizzato nel menu di scelta rapida del carattere, nella finestra comandi vocali, in entrambi o in nessuno dei due. Ad esempio, se si desidera che un comando venga visualizzato nel menu a comparsa per il carattere, impostare la [**didascalia**](caption-property.md) del comando e le proprietà [**visibili**](visible-property.md) . Per visualizzare il comando nella finestra comandi vocali, impostare le proprietà [**VoiceCaption**](voicecaption-property.md) e [**Voice**](voice-property.md) del comando.

Un utente può accedere ai singoli [**comandi**](/windows/desktop/lwef/the-commands-collection-object)comm nella raccolta solo quando l'applicazione client è di input-attivo. Pertanto, quando è possibile condividere il carattere con altre applicazioni client, in genere si desidera impostare le proprietà [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) per l'oggetto raccolta **Commands** , nonché per i comandi nella raccolta. In questo modo viene inserita una voce per la raccolta di **comandi** nel menu di scelta rapida di un carattere e nella finestra dei comandi vocali.

Quando l'utente passa al client scegliendo la voce [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , il server rende automaticamente attivo l'input del client, inviando una notifica all'applicazione client usando l'evento [**ActivateInput**](activateinput-event.md) e rende disponibili i comandi nella relativa raccolta. Il server informa inoltre il client che non è più attivo per l'input con l'evento [**DeActivateInput**](deactivateinput-event.md) . Ciò consente al server di presentare e accettare solo i comandi che si applicano al contesto del client attivo di input corrente. Serve anche per evitare conflitti tra i nomi di comando tra i client.

Un client può anche richiedere in modo esplicito di creare il client input-Active usando il metodo [**Activate**](activate-method.md) . Questo metodo supporta anche l'impostazione dell'applicazione in modo che non sia il client di input-attivo. Si consiglia di usare questo metodo quando si condivide un carattere con un'altra applicazione, impostando l'applicazione come input-attivo quando la finestra dell'applicazione ottiene lo stato attivo e non l'input-attivo quando perde lo stato attivo.

Analogamente, è possibile usare il metodo [**Activate**](activate-method.md) per impostare l'applicazione in modo che sia (o meno) il client attivo del carattere. Il client attivo è il client che riceve l'input quando il carattere è il carattere superiore. Quando questo stato viene modificato, il server invia una notifica all'applicazione con l'evento [**ActiveClientChange**](activeclientchange-event.md) .

Quando viene visualizzato il menu di scelta rapida di un carattere, le modifiche apportate alle proprietà di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) o ai comandi nella relativa raccolta non vengono visualizzate fino a quando l'utente non visualizza nuovamente il menu. Tuttavia, nella finestra comandi vengono visualizzate le modifiche appena si verificano.

-   [Metodi dell'oggetto Commands](commands-object-methods.md)
-   [Proprietà degli oggetti Commands](commands-object-properties.md)

 

 