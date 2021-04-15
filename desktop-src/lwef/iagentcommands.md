---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516762"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server Microsoft Agent gestisce un elenco di comandi attualmente disponibili per l'utente. Questo elenco include i comandi definiti dal server per l'interazione generale, ad esempio le proprietà Nascondi e agente Microsoft, l'elenco dei client disponibili, ma non di input, e i comandi definiti dal client attivo corrente. I primi due set di comandi sono comandi globali. ovvero sono disponibili in qualsiasi momento, indipendentemente dal client attivo di input. I comandi definiti dal client sono disponibili solo quando il client è attivo per l'input.

Recuperare un'interfaccia **IAgentCommands** eseguendo una query sull'interfaccia [**IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) per **IAgentCommands**. Ogni applicazione client di Microsoft Agent può definire una raccolta di comandi denominata raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Per aggiungere un [**comando**](/windows/desktop/lwef/the-command-object) alla raccolta, utilizzare il metodo [**Add**](add-method.md) o [**Insert**](insert-method.md) . Sebbene sia possibile specificare le **proprietà di un comando** usando i metodi [**IAgentCommand**](iagentcommand.md) , per ottenere prestazioni ottimali del codice, specificare tutte le proprietà di un **comando** nei metodi [**IAgentCommands:: Add**](iagentcommands--add.md) o [**IAgentCommands:: Insert**](iagentcommands--insert.md) quando inizialmente si impostano le proprietà per un nuovo **comando**. È possibile utilizzare i metodi **IAgentCommand** per eseguire una query o modificare le impostazioni delle proprietà.

Per ogni [**comando**](/windows/desktop/lwef/the-command-object) della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , è possibile determinare se il comando viene visualizzato nel menu di scelta rapida del carattere, nella finestra comandi vocali, in entrambi o in nessuno dei due. Ad esempio, se si desidera che un comando venga visualizzato nel menu a comparsa per il carattere, impostare la [**didascalia**](caption-property.md) del comando e le proprietà [**visibili**](visible-property.md) . Per visualizzare il comando nella **finestra comandi vocali**, impostare le proprietà **didascalia** e [**voce**](voice-property.md) del comando.

Un utente può accedere ai singoli comandi nella raccolta di comandi solo quando l'applicazione client è in input-attivo e il carattere è visibile. Pertanto, in genere si desidera impostare le proprietà [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) per l'oggetto Collection [**Commands**](/windows/desktop/lwef/the-commands-collection-object) , nonché per i comandi della raccolta, perché in questo modo viene inserita una voce per la raccolta di **comandi** nel menu di scelta rapida di un carattere e nella finestra dei comandi vocali. Quando l'utente passa al client scegliendo la voce **Commands** , il server rende automaticamente attivo l'input del client, inviando una notifica all'applicazione client usando [**IAgentNotifySink:: ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) e rende disponibili i **comandi** nella relativa raccolta. Il server invia inoltre una notifica al client che non è più in input-Active con l'evento **IAgentNotifySink:: ActivateInputState** . Ciò consente al server di presentare e accettare solo i **comandi** che si applicano al contesto del client attivo di input corrente. Serve anche per evitare conflitti tra i nomi di [**comando**](/windows/desktop/lwef/the-command-object)tra i client.

Un client può anche richiedere in modo esplicito di creare il client input-Active usando il metodo [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) . Questo metodo supporta anche l'impostazione dell'applicazione in modo che non sia il client di input-attivo. Si consiglia di usare questo metodo quando si condivide un carattere con un'altra applicazione, impostando l'applicazione come input-attivo quando la finestra dell'applicazione ottiene lo stato attivo e non l'input-attivo quando perde lo stato attivo.

Analogamente, è possibile usare [**IAgentCharacter:: Activate**](iagentcharacter--activate.md) per impostare l'applicazione in modo che sia (o meno) il client attivo del carattere. Il client attivo è il client che riceve l'input quando il carattere è il carattere superiore. Quando questo stato viene modificato, il server invia una notifica all'applicazione con l'evento [**IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md) .

Quando viene visualizzato il menu di scelta rapida di un carattere, le modifiche apportate alle proprietà di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) o ai comandi nella relativa raccolta non vengono visualizzate fino a quando l'utente non visualizza nuovamente il menu. Tuttavia, quando si apre, la finestra comandi vocali Visualizza le modifiche appena si verificano.

**IAgentCommands** definisce un'interfaccia che consente alle applicazioni di aggiungere, rimuovere, impostare ed eseguire query sulle proprietà per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Queste funzioni sono disponibili anche da [**IAgentCommandsEx**](iagentcommandsex.md).

Una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) può essere visualizzata come comando nel menu di scelta rapida e nella finestra dei comandi vocali per un carattere. Per visualizzare la raccolta di **comandi** , è necessario impostare la relativa proprietà [**Caption**](caption-property.md) . Nella tabella seguente viene riepilogato il modo in cui le proprietà di una raccolta di **comandi** influiscono sulla presentazione.



| Proprietà Caption | Proprietà Voice-Caption | Proprietà Voice | Visible (proprietà) | Viene visualizzato nel menu a comparsa del carattere             | Viene visualizzato nella finestra comandi vocali                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sì              | Sì                    | Sì            | Vero             | Sì, uso della [ **didascalia**](caption-property.md) | Sì, uso di [ **VoiceCaption**](voicecaption-property.md) |
| Sì              | Sì                    | No ¹            | Vero             | Sì, uso della [ **didascalia**](caption-property.md) | No                                                       |
| Sì              | Sì                    | Sì            | False            | No                                             | Sì, uso di [ **VoiceCaption**](voicecaption-property.md) |
| Sì              | Sì                    | No ¹            | False            | No                                             | No                                                       |
| No ¹              | Sì                    | Sì            | True             | No                                             | Sì, uso di [ **VoiceCaption**](voicecaption-property.md) |
| No ¹              | Sì                    | Sì            | False            | No                                             | Sì, uso di [ **VoiceCaption**](voicecaption-property.md) |
| No ¹              | Sì                    | No ¹            | True             | No                                             | No                                                       |
| No ¹              | Sì                    | No ¹            | False            | No                                             | No                                                       |
| Sì              | No ¹                    | Sì            | Vero             | Sì, uso della [ **didascalia**](caption-property.md) | Sì, uso della [ **didascalia**](caption-property.md)           |
| Sì              | No ¹                    | No ¹            | True             | Sì                                            | No                                                       |
| Sì              | No ¹                    | Sì            | False            | No                                             | Sì, uso della [ **didascalia**](caption-property.md)           |
| Sì              | No ¹                    | No ¹            | False            | No                                             | No                                                       |
| No ¹              | No ¹                    | Sì            | True             | No                                             | Nessun ²                                                      |
| No ¹              | No ¹                    | Sì            | False            | No                                             | Nessun ²                                                      |
| No ¹              | No ¹                    | No ¹            | True             | No                                             | No                                                       |
| No ¹              | No ¹                    | No ¹            | False            | No                                             | No                                                       |



 

¹ se l'impostazione della proprietà è null. In alcuni linguaggi di programmazione è possibile che una stringa vuota non venga interpretata come una stringa null.

² il comando è ancora accessibile tramite voce.

**Metodi nell'ordine Vtable**



| Metodi IAgentCommands                           | Descrizione                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Recupera un oggetto [**Command**](/windows/desktop/lwef/the-command-object) dalla raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .              |
| [**GetCount**](iagentcommands--getcount.md)     | Restituisce il valore del numero di [**comandi**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . |
| [**SetCaption**](iagentcommands--setcaption.md) | Imposta il valore della proprietà [**Caption**](caption-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetCaption**](iagentcommands--getcaption.md) | Restituisce il valore della proprietà [**Caption**](caption-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Sevoice**](iagentcommands--setvoice.md)     | Imposta il valore della proprietà [**Voice**](voice-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .        |
| [**Getvoice**](iagentcommands--getvoice.md)     | Restituisce il valore della proprietà [**Voice**](voice-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .      |
| [**SetVisible**](iagentcommands--setvisible.md) | Imposta il valore della proprietà [**Visible**](visible-property.md) per una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [**GetVisible**](iagentcommands--getvisible.md) | Restituisce il valore della proprietà [**Visible**](visible-property.md) di una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .  |
| [**Aggiungere**](iagentcommands--add.md)               | Aggiunge un oggetto [**Command**](/windows/desktop/lwef/the-command-object) a una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .                       |
| [**Insert**](iagentcommands--insert.md)         | Inserisce un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**Rimuovi**](iagentcommands--remove.md)         | Rimuove un oggetto [**Command**](/windows/desktop/lwef/the-command-object) in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Rimuove tutti gli oggetti [**Command**](/windows/desktop/lwef/the-command-object) da una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .               |



 

 

 