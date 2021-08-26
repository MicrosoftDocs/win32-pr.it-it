---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1bcc40f80e9a10301ec305fdc3e8f3e83984ceb0de5d36121e13c3d823b8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961891"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il server Microsoft Agent gestisce un elenco di comandi attualmente disponibili per l'utente. Questo elenco include i comandi definiti dal server per l'interazione generale, ad esempio Nascondi e Proprietà di Microsoft Agent, l'elenco di client disponibili (ma non attivi per l'input) e i comandi definiti dal client attivo corrente. I primi due set di comandi sono comandi globali. in altre parole, sono disponibili in qualsiasi momento, indipendentemente dal client attivo di input. I comandi definiti dal client sono disponibili solo quando il client è attivo per l'input.

Recuperare **un'interfaccia IAgentCommands** tramite query [**sull'interfaccia IAgentCharacter**](https://www.bing.com/search?q=**IAgentCharacter**) per **IAgentCommands**. Ogni applicazione client di Microsoft Agent può definire una raccolta di comandi denominata [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) Per aggiungere un [**oggetto Command**](/windows/desktop/lwef/the-command-object) alla raccolta, usare il [**metodo Add**](add-method.md) o [**Insert.**](insert-method.md) Anche se è  possibile specificare le proprietà di un comando usando i metodi [**IAgentCommand,**](iagentcommand.md) per ottenere prestazioni ottimali del codice, specificare tutte le proprietà di un comando nei metodi [**IAgentCommands::Add**](iagentcommands--add.md) o [**IAgentCommands::Insert**](iagentcommands--insert.md) quando si impostano inizialmente le proprietà per un nuovo **oggetto Command**. È possibile usare i **metodi IAgentCommand** per eseguire query o modificare le impostazioni delle proprietà.

Per ogni [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta [**Comandi**](/windows/desktop/lwef/the-commands-collection-object) è possibile determinare se il comando viene visualizzato nel menu a comparsa del carattere, nella finestra Comandi vocali, in entrambi o in nessuno dei due. Ad esempio, se si vuole visualizzare un comando nel menu a comparsa per il carattere, impostare le proprietà [**Caption**](caption-property.md) e [**Visible del**](visible-property.md) comando. Per visualizzare il comando nella **finestra Comandi vocali**, impostare le proprietà **Didascalia** [**e Voce del**](voice-property.md) comando.

Un utente può accedere ai singoli comandi nella raccolta Commands solo quando l'applicazione client è attiva per l'input e il carattere è visibile. Di conseguenza, in genere è necessario impostare le proprietà [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)e [**Voice**](voice-property.md) per l'oggetto raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) e per i comandi nella raccolta, perché in questo modo viene impostata una voce per la raccolta **Commands** nel menu a comparsa di un carattere e nella finestra Comandi vocali. Quando l'utente passa al client scegliendo la relativa voce **Commands,** il server rende automaticamente attivo l'input del client, inviando una notifica all'applicazione client usando [**IAgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) e rende disponibili i comandi nella raccolta.  Il server notifica inoltre al client che non è più attivo l'input con l'evento **IAgentNotifySink::ActivateInputState.** In questo modo il server può presentare e accettare solo i **comandi** che si applicano al contesto del client attivo di input corrente. Serve anche per evitare conflitti [**command-name**](/windows/desktop/lwef/the-command-object)tra i client.

Un client può anche richiedere in modo esplicito di rendere se stesso il client attivo di input usando il [**metodo IAgentCharacter::Activate.**](iagentcharacter--activate.md) Questo metodo supporta anche l'impostazione dell'applicazione in modo che non sia il client attivo per l'input. È possibile usare questo metodo quando si condivide un carattere con un'altra applicazione, impostando l'applicazione come attiva per l'input quando la finestra dell'applicazione ottiene lo stato attivo e non l'input attivo quando perde lo stato attivo.

Analogamente, è possibile usare [**IAgentCharacter::Activate**](iagentcharacter--activate.md) per impostare l'applicazione come (o non essere) il client attivo del carattere. Il client attivo è il client che riceve l'input quando il carattere è il carattere in primo piano. Quando questo stato cambia, il server invia una notifica all'applicazione con [**l'evento IAgentNotifySinkEx::ActiveClientChange.**](iagentnotifysinkex--activeclientchange.md)

Quando viene visualizzato il menu a comparsa di un carattere, le modifiche alle proprietà di una raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) o ai comandi nella raccolta non vengono visualizzate finché l'utente non visualizza nuovamente il menu. Tuttavia, quando si apre, la finestra Comandi vocali visualizza le modifiche non appena si verificano.

**IAgentCommands** definisce un'interfaccia che consente alle applicazioni di aggiungere, rimuovere, impostare ed eseguire query su proprietà per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) Queste funzioni sono disponibili anche da [**IAgentCommandsEx.**](iagentcommandsex.md)

Una [**raccolta**](/windows/desktop/lwef/the-commands-collection-object) Commands può essere visualizzata come comando sia nel menu a comparsa che nella finestra Comandi vocali per un carattere. Per visualizzare la **raccolta Commands,** è necessario impostarne la [**proprietà Caption.**](caption-property.md) La tabella seguente riepiloga in che modo le proprietà di una **raccolta Commands** influiscono sulla presentazione.



| Proprietà Caption | Voice-Caption proprietà | Proprietà Voice | Proprietà Visible | Viene visualizzato nel menu a comparsa del carattere             | Viene visualizzato nella finestra Comandi vocali                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Sì              | Sì                    | Sì            | Vero             | Sì, usando [ **Didascalia**](caption-property.md) | Sì, con [ **VoiceCaption**](voicecaption-property.md) |
| Sì              | Sì                    | No¹            | Vero             | Sì, usando [ **Didascalia**](caption-property.md) | No                                                       |
| Sì              | Sì                    | Sì            | False            | No                                             | Sì, con [ **VoiceCaption**](voicecaption-property.md) |
| Sì              | Sì                    | No¹            | False            | No                                             | No                                                       |
| No¹              | Sì                    | Sì            | True             | No                                             | Sì, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sì                    | Sì            | False            | No                                             | Sì, con [ **VoiceCaption**](voicecaption-property.md) |
| No¹              | Sì                    | No¹            | True             | No                                             | No                                                       |
| No¹              | Sì                    | No¹            | False            | No                                             | No                                                       |
| Sì              | No¹                    | Sì            | Vero             | Sì, usando [ **Didascalia**](caption-property.md) | Sì, usando [ **Didascalia**](caption-property.md)           |
| Sì              | No¹                    | No¹            | True             | Sì                                            | No                                                       |
| Sì              | No più                    | Sì            | False            | No                                             | Sì, usando [ **Caption**](caption-property.md)           |
| Sì              | No più                    | No più            | False            | No                                             | No                                                       |
| No più              | No più                    | Sì            | True             | No                                             | No più                                                      |
| No più              | No più                    | Sì            | False            | No                                             | No più                                                      |
| No più              | No più                    | No più            | True             | No                                             | No                                                       |
| No più              | No più                    | No più            | False            | No                                             | No                                                       |



 

¹Se l'impostazione della proprietà è Null. In alcuni linguaggi di programmazione una stringa vuota potrebbe non essere interpretata come una stringa Null.

I comandi sono ancora accessibili tramite voce.

**Metodi nell'ordine Vtable**



| Metodi IAgentCommands                           | Descrizione                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Recupera un [**oggetto Command**](/windows/desktop/lwef/the-command-object) dalla raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object)              |
| [**GetCount**](iagentcommands--getcount.md)     | Restituisce il valore del numero di [**comandi**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object) |
| [**SetCaption**](iagentcommands--setcaption.md) | Imposta il valore della proprietà [**Caption**](caption-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [**GetCaption**](iagentcommands--getcaption.md) | Restituisce il valore della proprietà [**Caption**](caption-property.md) di una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)  |
| [**SetVoice**](iagentcommands--setvoice.md)     | Imposta il valore della proprietà [**Voice**](voice-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)        |
| [**GetVoice**](iagentcommands--getvoice.md)     | Restituisce il valore della [**proprietà Voice**](voice-property.md) di una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)      |
| [**SetVisible**](iagentcommands--setvisible.md) | Imposta il valore della [**proprietà Visible**](visible-property.md) per una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [**GetVisible**](iagentcommands--getvisible.md) | Restituisce il valore della [**proprietà Visible**](visible-property.md) di una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)  |
| [**Add**](iagentcommands--add.md)               | Aggiunge un [**oggetto Command**](/windows/desktop/lwef/the-command-object) a una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)                       |
| [**Inserire**](iagentcommands--insert.md)         | Inserisce un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)                    |
| [**Rimuovi**](iagentcommands--remove.md)         | Rimuove un [**oggetto Command**](/windows/desktop/lwef/the-command-object) in una [**raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Rimuove tutti [**gli oggetti Command**](/windows/desktop/lwef/the-command-object) da una raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object)               |



 

 

 