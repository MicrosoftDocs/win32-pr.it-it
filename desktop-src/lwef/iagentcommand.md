---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e2288a7b913becc54e2c0baa43eb14903e65fb7eddf6620d5cefbd78968026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665481"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un [**oggetto Command**](/windows/desktop/lwef/the-command-object) è un elemento di una raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Il server fornisce all'utente l'accesso ai comandi che l'applicazione client diventa attiva per l'input. Per recuperare un **oggetto Command,** chiamare [**IAgentCommands::GetCommand**](iagentcommands--getcommand.md).

**IAgentCommand** definisce un'interfaccia che consente alle applicazioni di impostare ed eseguire query su proprietà per gli oggetti [**Command**](/windows/desktop/lwef/the-command-object) che possono essere visualizzati nel menu a comparsa di un carattere e nella finestra Comandi vocali. Queste funzioni sono disponibili anche da [**IAgentCommandEx.**](iagentcommandex.md) Un **oggetto Command** è un elemento di una raccolta [**Commands.**](/windows/desktop/lwef/the-commands-collection-object) Il server fornisce all'utente l'accesso ai comandi quando l'applicazione client diventa attiva per l'input.

Un [**comando**](/windows/desktop/lwef/the-command-object) può essere visualizzato in uno o entrambi i menu a comparsa del carattere e nella finestra comandi vocali. Per essere visualizzato nel menu a comparsa, deve avere [**una**](caption-property.md) didascalia e la [**proprietà Visible**](visible-property.md) impostata su **True.** Anche **la proprietà Visible** per l'oggetto raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) deve essere impostata su **True** perché il comando venga visualizzato nel menu a comparsa quando l'applicazione client è attiva per l'input. Per essere visualizzato nella finestra Comandi vocali, un **comando** deve avere le [**proprietà VoiceCaption**](voicecaption-property.md) [**e Voice**](voice-property.md) impostate. Per la compatibilità con le versioni precedenti, se non è presente **VoiceCaption,** viene **usata l'impostazione Didascalia.**

Le voci di menu popup di un carattere non cambiano quando viene visualizzato il menu. Se si aggiungono o rimuovono comandi o si modificano le proprietà mentre viene visualizzato il menu popup del carattere, tali modifiche vengono visualizzate quando vengono visualizzate nuovamente. Tuttavia, la finestra Comandi vocali visualizza le modifiche non appena vengono apportate.

La tabella seguente riepiloga in che modo le proprietà di un comando influiscono sulla relativa presentazione.



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
| Sì              | No¹                    | Sì            | False            | No                                             | Sì, usando [ **Didascalia**](caption-property.md)           |
| Sì              | No¹                    | No¹            | False            | No                                             | No                                                       |
| No¹              | No¹                    | Sì            | True             | No                                             | No²                                                      |
| No¹              | No¹                    | Sì            | False            | No                                             | No²                                                      |
| No¹              | No¹                    | No¹            | True             | No                                             | No                                                       |
| No¹              | No¹                    | No¹            | False            | No                                             | No                                                       |



 

¹Se l'impostazione della proprietà è Null. In alcuni linguaggi di programmazione una stringa vuota non può essere interpretata come una stringa Null.

²Il comando è ancora accessibile dalla voce.

In genere, se si definisce un [**comando**](/windows/desktop/lwef/the-command-object) con [**un'impostazione**](voice-property.md) Voce, si definiscono anche le [**impostazioni didascalia**](caption-property.md) **e** voce per la raccolta [**comandi**](/windows/desktop/lwef/the-commands-collection-object) associata. Se  la raccolta Comandi per un set di comandi non ha l'impostazione  Voce o  Nessuna didascalia ed è attualmente attiva per l'input, ma i comandi hanno le impostazioni Didascalia e Voce, i comandi vengono visualizzati nella visualizzazione albero della finestra Comandi vocali in "(comando non definito)" quando l'applicazione client diventa attiva per l'input.    

Quando il server riceve input che corrisponde a uno degli oggetti [**Command**](/windows/desktop/lwef/the-command-object) definiti per la raccolta [**Commands,**](/windows/desktop/lwef/the-commands-collection-object) invia un evento [**IAgentNotifySink::Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) e restituisce l'ID del comando come attributo dell'oggetto [**IAgentUserInput.**](https://www.bing.com/search?q=**IAgentUserInput**) È quindi possibile usare istruzioni condizionali per trovare corrispondenze ed elaborare il comando.

**Metodi nell'ordine Vtable**



| Metodi di IAgentCommand                                                   | Descrizione                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Imposta il valore della [**didascalia per**](caption-property.md) un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Restituisce il valore della [**proprietà Caption**](caption-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | Imposta il valore per il [**testo voce**](voice-property.md) per un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | Restituisce il valore della [**proprietà Voice**](voice-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Imposta il valore della proprietà [**Enabled**](enabled-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)                 |
| [**Getenabled**](iagentcommand--getenabled.md)                         | Restituisce il valore della [**proprietà Enabled**](enabled-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Imposta il valore della [**proprietà Visible**](visible-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Restituisce il valore della [**proprietà Visible**](visible-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Imposta il valore della proprietà [**Confidence**](confidence-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Restituisce il valore della [**proprietà Confidence**](confidence-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Imposta il valore della [**proprietà ConfidenceText**](confidencetext-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Restituisce il valore della [**proprietà ConfidenceText**](confidencetext-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object) |
| [**getID**](iagentcommand--getid.md)                                   | Restituisce l'ID di un [**oggetto**](/windows/desktop/lwef/the-command-object) Command.                                                                      |



 

 

 