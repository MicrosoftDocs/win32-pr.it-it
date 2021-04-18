---
title: Finestra comandi vocali
description: Finestra comandi vocali
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299722"
---
# <a name="voice-commands-window"></a>Finestra comandi vocali

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Nella finestra comandi vocali vengono visualizzati i comandi vocali attivi correnti disponibili per il carattere. La finestra viene visualizzata quando si sceglie il comando Apri finestra comandi o la proprietà [**Visible**](visible-property.md) dell'oggetto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) è impostata su **true**. Se il motore vocale non è ancora stato caricato, l'esecuzione di una query o l'impostazione di questa proprietà provocherà l'inizializzazione del motore da parte di Microsoft Agent. Se l'utente disabilita la voce vocale, la finestra può comunque visualizzare; Tuttavia, verrà incluso un messaggio di testo che informa l'utente che la voce è attualmente disabilitata.

I comandi del client di input-attivo vengono visualizzati nella finestra comandi vocali in base alle impostazioni relative alla [**didascalia**](caption-property.md) [**vocale**](voice-property.md)e alla proprietà **voce** elencate in [**VoiceCaption**](voicecaption-property.md) della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

**Figura 1. Finestra comandi vocali**

La finestra comandi vocali viene visualizzata quando si sceglie il comando Apri finestra comandi. I comandi del client di input-attivo vengono visualizzati nella finestra comandi vocali in base alle impostazioni [**relative alla**](voice-property.md)[**didascalia**](caption-property.md) vocale e alla proprietà **voce** elencate sotto la **voce** della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) .

Nella finestra comandi vocali sono inoltre elencati i [**VoiceCaption**](voicecaption-property.md) della raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) per altri client del carattere e i seguenti comandi vocali generati dal server per l'interazione generale con la voce comandi globali:



| Didascalia vocale                       | Grammatica vocale                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Apri \| finestra comandi di chiusura vocale | (aprire \| Mostra) \[ la \] finestra dei comandi \[ \] \| che cosa si può dire \[ ora\] <br/> consente di selezionare: <br/> chiudere \[ la \] \[ finestra comandi\] <br/> |
| Nascondi                                | nascondere \*                                                                                                                                                  |
| *CharacterName*                     | *CharacterName*\*\*                                                                                                                                      |
| Comandi globali                     | \[Mostra \] \[ \] comandi globali                                                                                                                          |



 

\* Un carattere è elencato qui solo se è attualmente visibile.

\*\* Sono elencati tutti i caratteri caricati.

Pronunciando il comando Voice per la raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) di un altro client si passa a tale client e nella finestra comandi vocali vengono visualizzati i comandi di tale client. Non vengono espanse altre voci. Analogamente, se l'utente passa i caratteri, la finestra dei comandi vocali cambia per visualizzare i comandi del client attivo di input. Se il client è già attivo per l'input, la pronuncia di uno dei comandi vocali non ha alcun effetto. Tuttavia, se l'utente comprime il sottoalbero del client attivo con il mouse, il nome del client rivisualizzerà il sottoalbero del client.

Se un client dispone di comandi vocali, ma nessuna impostazione [**vocale**](voice-property.md) per il relativo oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) (o nessuna [**didascalia**](caption-property.md) **vocale**), nell'albero viene visualizzato "(Command undefined)" come voce padre, ma solo quando il client è input-Active e il client dispone di comandi nella relativa raccolta con impostazioni di **didascalia** e **voce** .

Il server Visualizza automaticamente i comandi del client di input attivo corrente e, se necessario, scorre la finestra per visualizzare il maggior numero possibile di comandi del client, in base alle dimensioni della finestra. Se il carattere non contiene voci client, la voce dei comandi globali viene espansa.

Se l'utente parla di "comandi globali", la finestra comandi vocali Visualizza sempre le voci del sottoalbero associate. Se sono già visualizzati, il comando non ha alcun effetto.

Sebbene sia anche possibile visualizzare o nascondere la finestra dei comandi vocali dal codice dell'applicazione usando la proprietà [**Visible**](visible-property.md) , non è possibile modificare le dimensioni o la posizione della finestra dei comandi vocali. Il server gestisce le proprietà della finestra comandi vocali in base all'interazione dell'utente con la finestra. La posizione iniziale è immediatamente adiacente all'icona della barra delle applicazioni del carattere.

La finestra comandi vocali è inclusa nell'ordine della finestra ALT + TAB. Ciò consente a un utente di passare alla finestra per scorrere, ridimensionare o riposizionare la finestra con la tastiera.

-   [Il suggerimento di ascolto](the-listening-tip.md)
-   [Finestra Opzioni carattere avanzato](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)

 

