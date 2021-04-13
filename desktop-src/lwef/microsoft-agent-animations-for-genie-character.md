---
title: Animazioni degli agenti Microsoft per il carattere Genie
description: Animazioni degli agenti Microsoft per il carattere Genie
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4f583fc6540b5fe13cc157542d69352a8ea5b31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399023"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Animazioni degli agenti Microsoft per il carattere Genie

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il [carattere Microsoft Agent Genie](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) è un lavoro di copyright di Microsoft Corporation.

Genie supporta le animazioni elencate nella tabella seguente. Vedere [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programming the Microsoft Agent Control](programming-the-microsoft-agent-control.md) per informazioni su come chiamare le animazioni del carattere.

Se si accede a queste animazioni di caratteri utilizzando il protocollo HTTP e il metodo di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo [**Get**](get-method.md) o del server, valutare il modo in cui eseguirne il download. Anziché scaricare contemporaneamente tutte le animazioni, è possibile recuperare prima le animazioni dello stato di **visualizzazione** e di **pronuncia** . In questo modo sarà possibile visualizzare il carattere rapidamente e fare in modo che parli mentre si disattivano le altre animazioni in modo asincrono. Per assicurarsi che il caricamento dei dati di tipo carattere e animazione venga eseguito correttamente, utilizzare l'evento [**RequestComplete**](requestcomplete-event.md) . Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se le animazioni **restituite** di un'animazione vengono definite usando i rami di uscita, non è necessario chiamarle in modo esplicito; Agent esegue automaticamente l'animazione **restituita** prima dell'animazione successiva. Tuttavia, se viene elencata un'animazione **restituita** , è necessario chiamare l'animazione utilizzando il metodo [**Play**](play-method.md) prima di un'altra animazione per fornire una transizione senza problemi. Se non è presente alcuna animazione **restituita** , l'animazione termina in genere senza che sia necessaria un'animazione di transizione.

Il file di caratteri include effetti audio per alcune animazioni, come indicato nella tabella seguente. Gli effetti audio Riproduci solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti audio nell'applicazione.



| Animazione                 | Restituisci animazione         | Supporta l'espressione | Effetti audio | Assegnato a stato                            | Descrizione                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Riconoscere**           | nessuno                     | No                | **No**        | nessuno                                         | Cenni Head                                                      |
| **Avviso**                 | Sì, uso di rami di uscita | Sì               | **No**        | **In ascolto**                                | Raddrizza e genera sopracciglia                                |
| **Annunciare**              | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Genera la mano                                                    |
| **Blink**                 | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Lampeggia gli occhi                                                    |
| **Confusione**              | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Testa graffi                                                 |
| **Congratularmi**          | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Applaude                                                       |
| **Congratulazioni \_ 2**       | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Fornisce un movimento Thumb-up                                        |
| **Non accetto**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Solleva la testa di mano e trema                                   |
| **DoMagic1**              | nessuno                     | Sì               | **No**        | nessuno                                         | Passa a lato e genera                                 |
| **DoMagic2**              | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Abbassa le mani, vengono visualizzati i cloud                                    |
| **DontRecognize**         | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Passa a orecchio                                              |
| **Explain**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Estende le armi al lato                                           |
| **GestureDown**           | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingDown**                            | Movimenti in basso                                                  |
| **GestureLeft**           | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingLeft**                            | Movimenti rimasti                                                  |
| **GestureRight**          | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                                 |
| **GestureUp**             | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                                    |
| **Getattenzione**          | **GetAttentionReturn**   | Sì               | **No**        | nessuno                                         | Bracci d'onda                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **No**        | nessuno                                         | Di nuovo Waves Arms                                               |
| **GetAttentionReturn**    | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **Greet**                 | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Archi                                                           |
| **Udienza \_ 1**            | nessuno                     | No                | **No**        | **Udito**                                  | Orecchie estesi ( \* animazione ciclo)                              |
| **Udienza \_ 2**            | nessuno                     | No                | **No**        | **Udito**                                  | Inclina il capo a sinistra ( \* animazione ciclo)                          |
| **Udienza \_ 3**            | nessuno                     | No                | **No**        | **Udito**                                  | Attiva l'intestazione sinistra ( \* animazione ciclo)                          |
| **Udienza \_ 4**            | nessuno                     | No                | **No**        | **Udito**                                  | Attiva l'intestazione a destra ( \* animazione ciclo)                         |
| **Nascondi**                  | nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare in fumo                                          |
| **Idle1 \_ 1**              | nessuno                     | No                | **No**        | **IdlingLevel1** IdlingLevel2                | Si respira                                                   |
| **Idle1 \_ 2**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi giusti e lampeggianti                                       |
| **Idle1 \_ 3**              | Sì, uso di rami di uscita | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi a sinistra e a lampeggiamento                                        |
| **Idle1 \_ 4**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi a destra e lampeggia                             |
| **Idle1 \_ 5**              | Sì, uso di rami di uscita | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi in basso e lampeggia                                        |
| **Idle1 \_ 6**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi e lampeggi                                          |
| **Idle2 \_ 1**              | nessuno                     | No                | **No**        | **IdlingLevel2**                             | Serpenti WISP                                                    |
| **Idle2 \_ 2**              | Sì, uso di rami di uscita | No                | **No**        | **IdlingLevel2**                             | Rivela scorrimento e letture                                       |
| **Idle2 \_ 3**              | Sì, uso di rami di uscita | No                | **No**        | **IdlingLevel2**                             | Rivela scorrimento e scritture                                      |
| **Idle3 \_ 1**              | nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Noia                                                          |
| **Idle3 \_ 2**              | Sì, uso di rami di uscita | No                | **Sì**       | **IdlingLevel3**                             | Cade in sospensione ( \* animazione ciclo)                             |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | nessuno                                         | Cerca giù                                                     |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | nessuno                                         | Lampeggiare alla ricerca                                            |
| **LookDownReturn**        | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | nessuno                                         | A sinistra                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | nessuno                                         | Lampeggia a sinistra                                            |
| **LookLeftReturn**        | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | nessuno                                         | A destra                                                    |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | nessuno                                         | Lampeggia a destra                                           |
| **LookRightReturn**       | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **Ricerca**                | **LookUpReturn**         | No                | **No**        | nessuno                                         | Cerca                                                       |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | nessuno                                         | Lampeggia la ricerca                                              |
| **LookUpReturn**          | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **MoveDown**              | Sì, uso di rami di uscita | No                | **Sì**       | **MovingDown**                               | Vola giù                                                     |
| **MoveLeft**              | Sì, uso di rami di uscita | No                | **Sì**       | **MovingLeft**                               | Mosche a sinistra                                                     |
| **MoveRight**             | Sì, uso di rami di uscita | No                | **Sì**       | **MovingRight**                              | Vola a destra                                                    |
| **MoveUp**                | Sì, uso di rami di uscita | No                | **Sì**       | **MovingUp**                                 | Vola su                                                       |
| **Lieti**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Sorride e stringe le mani insieme                                |
| **Processo**               | No                       | No                | **No**        | nessuno                                         | Spin in un cloud                                             |
| **Elaborazione in corso**            | Sì, uso di rami di uscita | No                | **No**        | nessuno                                         | Si inserisce in un cloud ( \* animazione ciclo)                       |
| **Lettura**                  | **ReadReturn**           | Sì               | **Sì**       | nessuno                                         | Rivela scorrimento, letture e ricerca                             |
| **ReadContinued**         | **ReadReturn**           | Sì               | **No**        | nessuno                                         | Letture e ricerca                                             |
| **ReadReturn**            | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **Lettura**               | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Rivela scorrimento e letture ( \* animazione ciclo)                  |
| **RestPose**              | nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                               |
| **Triste**                   | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Espressione triste                                                 |
| **Ricerca**                | No                       | No                | **No**        | nessuno                                         | Mostra i binocoli e le svolte                                   |
| **Ricerca**             | Sì, uso di rami di uscita | No                | **No**        | nessuno                                         | Mostra i binocoli e le svolte ( \* animazione ciclo)             |
| **Mostra**                  | nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Viene visualizzato fuori fumo                                           |
| **StartListening**        | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Passa a orecchio                                               |
| **StopListening**         | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Mette a disposizione gli orecchi                                           |
| **Suggerisci**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Visualizza lampadina                                             |
| **Sorprendente**             | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Sembra sorpreso                                                |
| **Pensare**                 | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Cerca con mano il mento                                     |
| **Pensare**              | No                       | No                | **No**        | nessuno                                         | Cerca la mano sul Chino ( \* animazione ciclo)               |
| **Incerto**             | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Sposta una mano su Chin, other to hip e solleva il sopracciglio destro |
| **Onda**                  | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Diverse fasi                                                          |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Rivela lo scorrimento, le Scritture e la ricerca                            |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Scrive e cerca                                            |
| **WriteReturn**           | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                    |
| **Scrittura**               | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Rivela Scroll, Scritture ( \* animazione ciclo)                   |



 

\* Se si riproduce un'animazione di ciclo, è necessario usare [**Stop**](stop-method.md) per cancellarla prima che vengano riprodotte altre animazioni nella coda del carattere.

 

