---
title: Microsoft Agent Animations for Genie Character
description: Microsoft Agent Animations for Genie Character
ms.assetid: 56c42d7a-32af-47cb-8578-0a89507a41ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204da244b74e96e239d540662dabf73af82001748b395da8e660f53fe4cf85e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976101"
---
# <a name="microsoft-agent-animations-for-genie-character"></a>Microsoft Agent Animations for Genie Character

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft [Agent Genie Character](https://www.microsoft.com/downloads/details.aspx?FamilyID=da86ba4e-bc2d-4c1d-b5a0-3183fe206414) è un'opera di Microsoft Corporation.

Genie supporta le animazioni elencate nella tabella seguente. Per informazioni su come chiamare [le animazioni del](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) carattere, vedere Programmazione dell'interfaccia server di Microsoft Agent e Programmazione del controllo Microsoft [Agent.](programming-the-microsoft-agent-control.md)

Se si accede a queste animazioni di caratteri usando il protocollo HTTP e il metodo [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo, valutare come verranno scaricate. Invece di scaricare tutte le animazioni contemporaneamente, è possibile recuperare prima le animazioni di stato **Showing** e **Speaking.** In questo modo sarà possibile visualizzare rapidamente il carattere e farlo parlare mentre altre animazioni vengono visualizzate in modo asincrono. Inoltre, per assicurarsi che i dati dei caratteri e delle animazioni siano caricati correttamente, usare [**l'evento RequestComplete.**](requestcomplete-event.md) Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se le animazioni **Return** di un'animazione vengono definite usando rami Exit, non è necessario chiamarle in modo esplicito. Agent riproduce automaticamente **l'animazione Return** prima dell'animazione successiva. Tuttavia, se è **elencata** un'animazione Return, è necessario chiamare l'animazione usando il [**metodo Play**](play-method.md) prima di un'altra animazione per fornire una transizione uniforme. Se non è **elencata** alcuna animazione Return, l'animazione termina in genere senza la necessità di un'animazione di transizione.

Il file di caratteri include gli effetti sonori per alcune animazioni, come illustrato nella tabella seguente. Gli effetti sonori vengono riprodotti solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti sonori nell'applicazione.



| Animazione                 | Restituire un'animazione         | Supporta Speaking | Effetti sonori | Assegnato allo stato                            | Descrizione                                                    |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|----------------------------------------------------------------|
| **Riconoscere**           | Nessuno                     | No                | **No**        | Nessuno                                         | Nods head                                                      |
| **Avviso**                 | Sì, con i rami exit | Sì               | **No**        | **Ascolto**                                | Raddrizza e alza le ciglia                                |
| **Annunciare**              | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Alza la mano                                                    |
| **Blink**                 | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Lampeggia gli occhi                                                    |
| **Confusione**              | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Testina dei scratch                                                 |
| **Congratularmi con**          | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Applaude                                                       |
| **Congratulazioni \_ 2**       | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Offre un movimento di scorrimento verso l'alto                                        |
| **Non accetto**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Alza le mani e scuote la testa                                   |
| **DoMagic1**              | Nessuno                     | Sì               | **No**        | Nessuno                                         | Si volta a lato e alza le mani                                 |
| **DoMagic2**              | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Abbassa le mani, vengono visualizzati i cloud                                    |
| **DontRecognize**         | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano all'udito                                              |
| **Explain**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Estende le bracci laterali                                           |
| **GestureDown**           | Sì, con i rami exit | Sì               | **No**        | **GesturingDown**                            | Movimenti verso il basso                                                  |
| **GestureLeft**           | Sì, con i rami exit | Sì               | **No**        | **GesturingLeft**                            | Movimenti a sinistra                                                  |
| **GestureRight**          | Sì, con i rami exit | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                                 |
| **GestureUp**             | Sì, con i rami exit | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                                    |
| **GetAttention**          | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Onde di bracci                                                     |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Ondate di nuovo le bracci                                               |
| **GetAttentionReturn**    | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **Greet**                 | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Archi                                                           |
| **Udito \_ 1**            | Nessuno                     | No                | **No**        | **Udito**                                  | Estensione delle orecchini \* (animazione a ciclo continuo)                              |
| **Udito \_ 2**            | Nessuno                     | No                | **No**        | **Udito**                                  | Inclina la testa a sinistra \* (animazione a ciclo continuo)                          |
| **Udito \_ 3**            | Nessuno                     | No                | **No**        | **Udito**                                  | Ruota la parte superiore sinistra \* (animazione a ciclo continuo)                          |
| **Udito \_ 4**            | Nessuno                     | No                | **No**        | **Udito**                                  | Ruota la parte superiore destra \* (animazione a ciclo continuo)                         |
| **Nascondi**                  | Nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare nel fumo                                          |
| **Inattivo 1 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel1** IdlingLevel2                | Prende il soffio                                                   |
| **Inattivo 1 \_ 2**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi a destra e lampeggia                                       |
| **Inattivo1 \_ 3**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso sinistra e lampeggia                                        |
| **Inattivo 1 \_ 4**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso destra e lampeggia                             |
| **Inattivo1 \_ 5**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso il basso e lampeggia                                        |
| **Inattivo1 \_ 6**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso l'alto e lampeggia                                          |
| **Inattivo 2 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel2**                             | Serpenti Wisp                                                    |
| **Inattivo \_ 2 2**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel2**                             | Visualizza lo scorrimento e le operazioni di lettura                                       |
| **Inattivo 2 \_ 3**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel2**                             | Visualizza lo scorrimento e le scritture                                      |
| **Inattivo3 \_ 1**              | Nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Sbadiglia                                                          |
| **Inattivo3 \_ 2**              | Sì, con i rami exit | No                | **Sì**       | **IdlingLevel3**                             | Si addormenta \* (animazione a ciclo continuo)                             |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | Nessuno                                         | Cerca in basso                                                     |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | Nessuno                                         | Lampeggia verso il basso                                            |
| **LookDownReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | Nessuno                                         | Sembra a sinistra                                                     |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | Nessuno                                         | Lampeggia verso sinistra                                            |
| **LookLeftReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | Nessuno                                         | Sembra a destra                                                    |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | Nessuno                                         | Lampeggia verso destra                                           |
| **LookRightReturn**       | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **Ricerca**                | **LookUpReturn**         | No                | **No**        | Nessuno                                         | Cerca                                                       |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | Nessuno                                         | Lampeggia verso l'alto                                              |
| **LookUpReturn**          | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **MoveDown**              | Sì, con i rami exit | No                | **Sì**       | **MovingDown**                               | Vola verso il basso                                                     |
| **MoveLeft**              | Sì, con i rami exit | No                | **Sì**       | **Spostamentoleft**                               | Flies left (Vola a sinistra)                                                     |
| **MoveRight**             | Sì, con i rami exit | No                | **Sì**       | **MovingRight**                              | Voli a destra                                                    |
| **MoveUp**                | Sì, con i rami exit | No                | **Sì**       | **Spostamento in avanti**                                 | Vola verso l'alto                                                       |
| **Contento**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Sorride e tiene le mani insieme                                |
| **Processo**               | No                       | No                | **No**        | Nessuno                                         | Si trasforma in un cloud                                             |
| **Elaborazione in corso**            | Sì, con i rami exit | No                | **No**        | Nessuno                                         | Ruota in un cloud \* (animazione a ciclo continuo)                       |
| **Lettura**                  | **ReadReturn**           | Sì               | **Sì**       | Nessuno                                         | Visualizza lo scorrimento, la lettura e la ricerca                             |
| **ReadContinued**         | **ReadReturn**           | Sì               | **No**        | Nessuno                                         | Legge e cerca                                             |
| **ReadReturn**            | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **Lettura**               | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Reveal scroll and reads \* (animazione a ciclo continuo)                  |
| **RestPose**              | Nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                               |
| **Triste**                   | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Espressione non valida                                                 |
| **Ricerca**                | No                       | No                | **No**        | Nessuno                                         | Rivela binocoli e turni                                   |
| **Ricerca**             | Sì, con i rami exit | No                | **No**        | Nessuno                                         | Visualizza binocolo e turni \* (animazione a ciclo continuo)             |
| **Mostra**                  | Nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Appare fuori dal smoke                                           |
| **Elenco di avvio**        | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette la mano all'ascolto                                               |
| **Elenco di arresto**         | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette le mani sopra le mani                                           |
| **Suggerisci**               | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Visualizza la lampadina                                             |
| **Sorpreso**             | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Sembra disdato                                                |
| **Pensare**                 | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Cerca con la mano sul chin                                     |
| **Pensando**              | No                       | No                | **No**        | Nessuno                                         | Cerca con la mano sul chin \* (animazione a ciclo continuo)               |
| **Incerto**             | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Sposta una mano sulchin, l'altra all'anca e alza le oculare destra |
| **Onda**                  | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Onde                                                          |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Visualizza lo scorrimento, scrive e cerca                            |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Scrive e cerca                                            |
| **WriteReturn**           | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                    |
| **Scrittura**               | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Visualizza scorrimento, scritture \* (animazione a ciclo continuo)                   |



 

\* Se si riproduce un'animazione a ciclo continuo, è necessario usare [**Arresta**](stop-method.md) per cancellarla prima che altre animazioni nella coda del carattere verranno riprodotte.

 

