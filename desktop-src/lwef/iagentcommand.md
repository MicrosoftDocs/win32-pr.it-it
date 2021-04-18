---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299704"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un oggetto [**Command**](/windows/desktop/lwef/the-command-object) è un elemento in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il server consente all'utente di accedere ai comandi in modo che l'applicazione client diventi attiva. Per recuperare un **comando**, chiamare [**IAgentCommands:: GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand** definisce un'interfaccia che consente alle applicazioni di impostare ed eseguire query sulle proprietà per gli oggetti [**Command**](/windows/desktop/lwef/the-command-object) che possono essere visualizzati nel menu di scelta rapida di un carattere e nella finestra dei comandi vocali. Queste funzioni sono disponibili anche da [**IAgentCommandEx**](iagentcommandex.md). Un oggetto **Command** è un elemento in una raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . Il server consente all'utente di accedere ai comandi quando l'applicazione client diventa attiva.

È possibile che venga visualizzato un [**comando**](/windows/desktop/lwef/the-command-object) sia nel menu popup del carattere che nella finestra dei comandi vocali. Per visualizzare nel menu a comparsa, deve avere una [**didascalia**](caption-property.md) e la proprietà [**Visible**](visible-property.md) è impostata su **true**. Anche la proprietà **Visible** per il relativo oggetto raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) deve essere impostata su **true** affinché il comando venga visualizzato nel menu a comparsa quando l'applicazione client è di input-attivo. Per visualizzare nella finestra comandi vocali, è necessario impostare le proprietà [**VoiceCaption**](voicecaption-property.md) e [**Voice**](voice-property.md) per un **comando** . (Per compatibilità con le versioni precedenti, se non esiste alcun **VoiceCaption**, viene utilizzata l'impostazione del **titolo** ).

Le voci del menu popup di un carattere non cambiano quando il menu viene visualizzato. Se si aggiungono o si rimuovono i comandi o se ne modificano le proprietà quando viene visualizzato il menu popup del carattere, il menu Visualizza tali modifiche quando vengono rivisualizzate. Tuttavia, nella finestra dei comandi vocali vengono visualizzate le modifiche apportate.

Nella tabella seguente viene riepilogato il modo in cui le proprietà di un comando influiscono sulla presentazione.



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

In genere, se si definisce un [**comando**](/windows/desktop/lwef/the-command-object) con un'impostazione [**vocale**](voice-property.md) , si definiscono anche le impostazioni relative alla [**didascalia**](caption-property.md) e alla **voce** per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) associati. Se la raccolta di **comandi** per un set di comandi non ha alcuna **voce** o nessuna impostazione di **didascalia** e attualmente è attiva, ma i **comandi** hanno le impostazioni **didascalia** e **vocale** , i **comandi** vengono visualizzati nella visualizzazione albero della finestra comandi vocali in "(comando non definito)" quando l'applicazione client diventa attiva.

Quando il server riceve un input che corrisponde a uno degli oggetti [**Command**](/windows/desktop/lwef/the-command-object) definiti per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) , invia un evento [**IAgentNotifySink:: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) e restituisce l'ID del comando come attributo dell'oggetto [**IAgentUserInput**](https://www.bing.com/search?q=**IAgentUserInput**) . È quindi possibile usare le istruzioni condizionali per trovare una corrispondenza ed elaborare il comando.

**Metodi nell'ordine Vtable**



| Metodi IAgentCommand                                                   | Descrizione                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Imposta il valore per la [**didascalia**](caption-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Restituisce il valore della proprietà [**Caption**](caption-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**Sevoice**](iagentcommand--setvoice.md)                             | Imposta il valore per il testo [**vocale**](voice-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                        |
| [**Getvoice**](iagentcommand--getvoice.md)                             | Restituisce il valore della proprietà [**Voice**](voice-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Imposta il valore della proprietà [**Enabled**](enabled-property.md) per un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Restituisce il valore della proprietà [**Enabled**](enabled-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Imposta il valore della proprietà [**Visible**](visible-property.md) per un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Restituisce il valore della proprietà [**Visible**](visible-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Imposta il valore della proprietà [**confidenza**](confidence-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Restituisce il valore della proprietà [**confidenza**](confidence-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) .         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Imposta il valore della proprietà [**ConfidenceText**](confidencetext-property.md) per un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Restituisce il valore della proprietà [**ConfidenceText**](confidencetext-property.md) di un oggetto [**Command**](/windows/desktop/lwef/the-command-object) . |
| [**getID**](iagentcommand--getid.md)                                   | Restituisce l'ID di un oggetto [**comando**](/windows/desktop/lwef/the-command-object) .                                                                      |



 

 

 