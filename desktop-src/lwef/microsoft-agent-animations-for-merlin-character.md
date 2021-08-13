---
title: Microsoft Agent Animations for Merlin Character
description: Microsoft Agent Animations for Merlin Character
ms.assetid: 4563a464-2c1a-4928-a471-e3f0fdfe85c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 797002897f0e3bdb7efb309de8b73a33df8bdf399279895be8daa2b47d8ec084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247474"
---
# <a name="microsoft-agent-animations-for-merlin-character"></a>Microsoft Agent Animations for Merlin Character

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft [Agent Merlin Character](https://www.microsoft.com/downloads/details.aspx?FamilyID=fee1dadd-2f23-41d0-8a81-2affd74c0aa5) è un'opera di Microsoft Corporation.

Merlin supporta le animazioni elencate nella tabella seguente. Per informazioni su come chiamare [le animazioni del](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) carattere, vedere Programmazione dell'interfaccia server di Microsoft Agent e Programmazione del controllo Microsoft [Agent.](programming-the-microsoft-agent-control.md)

Se si accede a queste animazioni di caratteri usando il protocollo HTTP e il metodo [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo, valutare come verranno scaricate. Invece di scaricare tutte le animazioni contemporaneamente, è possibile recuperare prima le animazioni di stato **Showing** e **Speaking.** In questo modo sarà possibile visualizzare rapidamente il carattere e farlo parlare mentre altre animazioni vengono visualizzate in modo asincrono. Inoltre, per assicurarsi che i dati dei caratteri e delle animazioni siano caricati correttamente, usare [**l'evento RequestComplete.**](requestcomplete-event.md) Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se l'animazione **Return** di un'animazione viene definita usando rami Exit, non è necessario chiamarla in modo esplicito. Agent riproduce automaticamente **l'animazione Return** prima dell'animazione successiva. Tuttavia, se è **elencata** un'animazione Return, è necessario chiamare l'animazione usando il [**metodo Play**](play-method.md) prima di un'altra animazione per fornire una transizione uniforme. Se non è **elencata** alcuna animazione Return, l'animazione termina in genere senza la necessità di un'animazione di transizione.

Il file di caratteri include gli effetti sonori per alcune animazioni, come illustrato nella tabella seguente. Gli effetti sonori vengono riprodotti solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti sonori nell'applicazione.



| Animazione                 | Restituire un'animazione         | Supporta Speaking | Effetti sonori | Assegnato allo stato                            | Descrizione                                      |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------|
| **Riconoscere**           | Nessuno                     | No                | **No**        | Nessuno                                         | Nods head                                        |
| **Avviso**                 | Sì, con i rami exit | Sì               | **No**        | **Ascolto**                                | Raddrizza e alza le ciglia                  |
| **Annunciare**              | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Genera tromba e giochi                         |
| **Blink**                 | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Lampeggia gli occhi                                      |
| **Confusione**              | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Testina dei scratch                                   |
| **Congratularmi con**          | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Visualizza il trofeo                                  |
| **Congratulazioni \_ 2**       | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Applaude                                         |
| **Non accetto**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Alza le mani e scuote la testa                     |
| **DoMagic1**              | Nessuno                     | Sì               | **No**        | Nessuno                                         | Alza la wand magic                                |
| **DoMagic2**              | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Abbassa la wand, vengono visualizzati i cloud                       |
| **DontRecognize**         | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano all'udito                                |
| **Explain**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Estende le bracci laterali                             |
| **GestureDown**           | Sì, con i rami exit | Sì               | **No**        | **GesturingDown**                            | Movimenti verso il basso                                    |
| **GestureLeft**           | Sì, con i rami exit | Sì               | **No**        | **GesturingLeft**                            | Movimenti a sinistra                                    |
| **GestureRight**          | Sì, con i rami exit | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                   |
| **GestureUp**             | Sì, con i rami exit | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                      |
| **GetAttention**          | **GetAttentionReturn**   | Sì               | **Sì**       | Nessuno                                         | Si china in avanti e bussa                         |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **Sì**       | Nessuno                                         | In avanti, bussa di nuovo                    |
| **GetAttentionReturn**    | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                      |
| **Greet**                 | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Archi                                             |
| **Udito \_ 1**            | Nessuno                     | No                | **No**        | **Udito**                                  | Estensione delle orecchini \* (animazione a ciclo continuo)                |
| **Udito \_ 2**            | Nessuno                     | No                | **No**        | **Udito**                                  | Inclina la testa a sinistra \* (animazione a ciclo continuo)            |
| **Udito \_ 3**            | Nessuno                     | No                | **No**        | **Udito**                                  | Ruota la parte superiore sinistra \* (animazione a ciclo continuo)            |
| **Udito \_ 4**            | Nessuno                     | No                | **No**        | **Udito**                                  | Ruota la parte superiore destra \* (animazione a ciclo continuo)           |
| **Nascondi**                  | Nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare sotto il limite                             |
| **Inattivo 1 \_ 1**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Prende il soffio                                     |
| **Inattivo 1 \_ 2**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso sinistra e lampeggia                          |
| **Inattivo1 \_ 3**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi a destra                                    |
| **Inattivo 1 \_ 4**              | Sì, con i rami exit | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso destra e lampeggia               |
| **Inattivo 2 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel2**                             | Esamina la wand e lampeggia                         |
| **Inattivo \_ 2 2**              | Nessuno                     | No                | **No**        | **IdlingLevel2**                             | Tiene le mani e lampeggia                           |
| **Inattivo3 \_ 1**              | Nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Sbadiglia                                            |
| **Inattivo3 \_ 2**              | Sì, uso dei rami exit | No                | **Sì**       | **IdlingLevel3**                             | Sospensione \* (animazione a ciclo continuo)               |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | Nessuno                                         | Cerca in basso                                       |
| **LookDownBlink**         | **LookDownReturn**       | No                | **No**        | Nessuno                                         | Lampeggia verso il basso                              |
| **LookDownReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                      |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | Nessuno                                         | Sembra a sinistra                                       |
| **LookLeftBlink**         | **LookLeftReturn**       | No                | **No**        | Nessuno                                         | Lampeggia verso sinistra                              |
| **LookLeftReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                      |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | Nessuno                                         | Sembra a destra                                      |
| **LookRightBlink**        | **LookRightReturn**      | No                | **No**        | Nessuno                                         | Lampeggia verso destra                             |
| **LookRightReturn**       | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                      |
| **Ricerca**                | **LookUpReturn**         | No                | **No**        | Nessuno                                         | Cerca                                         |
| **LookUpBlink**           | **LookUpReturn**         | No                | **No**        | Nessuno                                         | Lampeggia la ricerca                                |
| **LookUpReturn**          | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                      |
| **MoveDown**              | Sì, uso dei rami exit | No                | **Sì**       | **MovingDown**                               | In basso                                       |
| **MoveLeft**              | Sì, uso dei rami exit | No                | **Sì**       | **MovingLeft**                               | 1000 a sinistra                                       |
| **MoveRight**             | Sì, uso dei rami exit | No                | **Sì**       | **MovingRight**                              | Diritto di controllo                                      |
| **MoveUp**                | Sì, uso dei rami exit | No                | **Sì**       | **MovingUp**                                 | Res up                                         |
| **Contento**               | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Fa smile e tiene le mani insieme                  |
| **Processo**               | No                       | No                | **Sì**       | Nessuno                                         | Caldron Di Caldron                                    |
| **Elaborazione in corso**            | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Caldron a forma di caldron \* (animazione a ciclo continuo)              |
| **Lettura**                  | **ReadReturn**           | Sì               | **Sì**       | Nessuno                                         | Apre un libro, legge e cerca                   |
| **ReadContinued**         | **ReadReturn**           | Sì               | **Sì**       | Nessuno                                         | Legge e cerca                               |
| **ReadReturn**            | Nessuno                     | No                | **Sì**       | Nessuno                                         | Torna alla posizione neutra                      |
| **Lettura**               | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Operazioni di lettura \* (animazione a ciclo continuo)                      |
| **RestPose**              | Nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                 |
| **Triste**                   | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Espressione tristia                                   |
| **Ricerca**                | No                       | No                | **Sì**       | Nessuno                                         | Esamina la palla a sfera                          |
| **Ricerca**             | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Esamina la palla a forma di sfera \* (animazione a ciclo continuo)    |
| **Mostra**                  | Nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Viene visualizzato fuori limite                               |
| **Elenco di avvio**        | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette la mano all'ascolto                                 |
| **Elenco di arresto**         | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette le mani sulle orecchini                             |
| **Suggerisci**               | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Visualizza lampadina                               |
| **Sorpreso**             | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Sembra sorpresa                                  |
| **Pensare**                 | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Cerca con la mano sul chin                       |
| **Pensando**              | No                       | No                | **No**        | Nessuno                                         | Cerca con la mano sul chin \* (animazione a ciclo continuo) |
| **Incerto**             | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Si china in avanti e alza il sopracciglio                 |
| **Onda**                  | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Onde                                            |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Apre un libro, scrive e cerca                  |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Scrive e cerca                              |
| **WriteReturn**           | Nessuno                     | No                | **Sì**       | Nessuno                                         | Torna alla posizione neutra                      |
| **Scrittura**               | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Scritture \* (animazione a ciclo continuo)                     |



 

\* Se si riproduce un'animazione a ciclo continuo, è necessario usare [**Arresta**](stop-method.md) per cancellarla prima che altre animazioni nella coda del carattere verranno riprodotte.

 

