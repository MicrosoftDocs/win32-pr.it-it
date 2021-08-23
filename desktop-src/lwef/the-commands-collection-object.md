---
title: Oggetto raccolta Commands
description: Oggetto raccolta Commands
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f7933bd973ae500b75abb51c47899fa60322444d49fe0835f6bfa3efab97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975661"
---
# <a name="the-commands-collection-object"></a>Oggetto raccolta Commands

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server Microsoft Agent gestisce un elenco di comandi attualmente disponibili per l'utente. Questo elenco include i comandi definiti dal server per l'interazione generale (ad esempio Nascondi e apri la finestra Comandi vocali), l'elenco dei client disponibili (ma non attivi per l'input) e i comandi definiti dal client attivo corrente. I primi due set di comandi sono comandi globali. in altre parole, sono disponibili in qualsiasi momento, indipendentemente dal client attivo di input. I comandi definiti dal client sono disponibili solo quando il client è attivo per l'input e il carattere è visibile.

Ogni applicazione client può definire una raccolta di comandi denominata [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) Per aggiungere un comando alla raccolta, usare il [**metodo Add**](add-method.md) [**o Insert.**](insert-method.md) Anche se è possibile specificare le proprietà di un comando con istruzioni separate, per ottenere prestazioni ottimali del codice, specificare tutte le proprietà di un comando nell'istruzione del metodo **Add** o **Insert.** Per ogni comando nella raccolta, è possibile determinare se l'accesso utente al comando viene visualizzato nel menu a comparsa del carattere, nella finestra Comandi vocali, in entrambi o in nessuno dei due. Ad esempio, se si vuole che un comando venga visualizzato nel menu a comparsa per il carattere, impostare le proprietà [**Caption**](caption-property.md) e [**Visible del**](visible-property.md) comando. Per visualizzare il comando nella finestra Comandi vocali, impostare le proprietà [**VoiceCaption**](voicecaption-property.md) [**e Voice del**](voice-property.md) comando.

Un utente può accedere ai singoli comandi comm [**e**](/windows/desktop/lwef/the-commands-collection-object)nella raccolta solo quando l'applicazione client è attiva per l'input. Pertanto, quando si condivide il carattere con altre applicazioni client è in genere necessario impostare le proprietà [**Caption,**](caption-property.md) [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) per l'oggetto raccolta **Commands** e per i comandi nella raccolta. Questa operazione inserisce una voce **per la** raccolta Commands nel menu a comparsa di un carattere e nella finestra Comandi vocali.

Quando l'utente passa al client scegliendo la voce [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (Comandi), il server rende automaticamente attivo l'input del client, inviando una notifica all'applicazione client tramite l'evento [**ActivateInput**](activateinput-event.md) e rende disponibili i comandi nella raccolta. Il server notifica inoltre al client che non è più attivo per l'input con [**l'evento DeActivateInput.**](deactivateinput-event.md) In questo modo il server può presentare e accettare solo i comandi che si applicano al contesto del client attivo-input corrente. Serve anche per evitare conflitti di nomi di comando tra i client.

Un client può anche richiedere in modo esplicito di impostare se stesso come client attivo di input usando il [**metodo Activate.**](activate-method.md) Questo metodo supporta anche l'impostazione dell'applicazione in modo che non sia il client attivo per l'input. È possibile usare questo metodo quando si condivide un carattere con un'altra applicazione, impostando l'applicazione come attiva per l'input quando la finestra dell'applicazione ottiene lo stato attivo e non l'input attivo quando perde lo stato attivo.

Analogamente, è possibile usare il [**metodo Activate**](activate-method.md) per impostare l'applicazione come (o non essere) il client attivo del carattere. Il client attivo è il client che riceve l'input quando il relativo carattere è il carattere in primo piano. Quando questo stato cambia, il server invia una notifica all'applicazione con [**l'evento ActiveClientChange.**](activeclientchange-event.md)

Quando viene visualizzato il menu a comparsa di un carattere, le modifiche apportate alle proprietà di una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) o ai comandi nella raccolta non vengono visualizzate finché l'utente non visualizza nuovamente il menu. Tuttavia, la finestra Comandi visualizza le modifiche non appena si verificano.

-   [Metodi dell'oggetto Commands](commands-object-methods.md)
-   [Proprietà dell'oggetto Commands](commands-object-properties.md)

 

 