---
title: Finestra Comandi vocali
description: Finestra Comandi vocali
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f4e5ce02ea9a964663efacbc19a3b302d6e58f0364d705491be26229b15f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245104"
---
# <a name="voice-commands-window"></a>Finestra Comandi vocali

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Nella finestra Comandi vocali vengono visualizzati i comandi vocali attivi correnti disponibili per il carattere. La finestra viene visualizzata quando si sceglie il comando Apri finestra comandi o la [**proprietà Visible**](visible-property.md) dell'oggetto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) è impostata su **True.** Se il motore di riconoscimento vocale non è ancora stato caricato, l'esecuzione di query o l'impostazione di questa proprietà causerà il tentativo di inizializzazione del motore da parte di Microsoft Agent. Se l'utente disabilita il riconoscimento vocale, la finestra può comunque essere visualizzata. Tuttavia, includerà un SMS che informa l'utente che la voce è attualmente disabilitata.

I comandi del client attivo per l'input vengono visualizzati nella finestra Comandi vocali in base alle [**impostazioni delle**](voice-property.md)proprietà Voice [**Caption**](caption-property.md) e **Voice** elencate nella [**raccolta VoiceCaption**](voicecaption-property.md) [**della raccolta Commands.**](/windows/desktop/lwef/the-commands-collection-object)

**Figura 1. Finestra Comandi vocali**

La finestra Comandi vocali viene visualizzata quando si sceglie il comando Apri finestra comandi. I comandi del client attivo per l'input vengono visualizzati  nella finestra Comandi vocali in base alle [**impostazioni delle**](voice-property.md)[](caption-property.md) proprietà Voce didascalia e Voce elencate in **Voce** della [**raccolta**](/windows/desktop/lwef/the-commands-collection-object) Comandi.

La finestra Comandi vocali elenca anche [**la voce VoiceCaption**](voicecaption-property.md) della raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) per altri client del carattere e i comandi vocali generati dal server seguenti per l'interazione generale nella voce Comandi globali:



| Didascalia vocale                       | Grammatica vocale                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aprire \| la finestra Chiudi comandi vocali | (open \| show) \[ la finestra dei comandi che cosa posso dire \] \[ \] \| \[ ora\] <br/> attiva/disattiva con: <br/> chiudere \[ la finestra dei \] \[ comandi\] <br/> |
| Nascondi                                | Nascondere \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Comandi globali                     | \[mostra \] \[ i comandi \] globali                                                                                                                          |



 

\* Un carattere è elencato qui solo se è attualmente visibile.

\*\* Vengono elencati tutti i caratteri caricati.

Pronunciando il comando vocale per la raccolta [**Commands**](/windows/desktop/lwef/the-commands-collection-object) di un altro client, si passa a tale client e nella finestra Comandi vocali vengono visualizzati i comandi del client. Non vengono espanse altre voci. Analogamente, se l'utente cambia carattere, la finestra Comandi vocali cambia per visualizzare i comandi del client attivo per l'input. Se il client è già attivo per l'input, pronunciare uno dei comandi vocali non ha alcun effetto. Se tuttavia l'utente comprime il sottoalbero del client attivo con il mouse, pronunciando il nome del client viene visualizzato nuovamente il sottoalbero del client.

Se un client dispone di [](voice-property.md) comandi vocali, ma nessuna impostazione Voce per il relativo oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (o nessuna didascalia [**vocale),**](caption-property.md)l'albero visualizza "(command undefined)" come voce padre, ma solo quando il client è attivo per l'input e il client ha comandi nella raccolta con le impostazioni **Didascalia** **e Voce.**

Il server visualizza automaticamente i comandi del client attivo di input corrente e, se necessario, scorre la finestra per visualizzare il maggior numero possibile di comandi del client, in base alle dimensioni della finestra. Se il carattere non contiene voci client, la voce Comandi globali viene espansa.

Se l'utente pronuncia "Comandi globali", nella finestra Comandi vocali vengono sempre visualizzate le voci del sottoalbero associate. Se sono già visualizzati, il comando non ha alcun effetto.

Anche se è anche possibile visualizzare o nascondere la finestra Comandi vocali dal codice dell'applicazione usando la proprietà [**Visible,**](visible-property.md) non è possibile modificare le dimensioni o la posizione della finestra comandi vocali. Il server mantiene le proprietà della finestra Comandi vocali in base all'interazione dell'utente con la finestra. La posizione iniziale è immediatamente adiacente all'icona della barra delle applicazioni del carattere.

La finestra Comandi vocali è inclusa nell'ordine della finestra ALT+TAB. Ciò consente a un utente di passare alla finestra per scorrere, ridimensionare o riposizionare la finestra con la tastiera.

-   [Suggerimento per l'ascolto](the-listening-tip.md)
-   [Finestra Opzioni carattere avanzate](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

