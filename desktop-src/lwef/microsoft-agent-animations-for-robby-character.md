---
title: Microsoft Agent Animations for Robby Character
description: Microsoft Agent Animations for Robby Character
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef6cf0fc3d44f9783fe3d22f9f0d2b291e6acc51bd5bb72890af793ffe55156
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609101"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Microsoft Agent Animations for Robby Character

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Microsoft [Agent Robby Character](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) è un'opera di Microsoft Corporation.

Robby supporta le animazioni elencate nella tabella seguente. Per informazioni su come chiamare [le animazioni del](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) carattere, vedere Programmazione dell'interfaccia server di Microsoft Agent e Programmazione del controllo Microsoft [Agent.](programming-the-microsoft-agent-control.md)

Se si accede a queste animazioni di caratteri usando il protocollo HTTP e il metodo [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo, valutare come verranno scaricate. Invece di scaricare tutte le animazioni contemporaneamente, è possibile recuperare prima le animazioni di stato **Showing** e **Speaking.** In questo modo sarà possibile visualizzare rapidamente il carattere e farlo parlare mentre altre animazioni vengono visualizzate in modo asincrono. Inoltre, per assicurarsi che i dati dei caratteri e delle animazioni siano caricati correttamente, usare [**l'evento RequestComplete.**](requestcomplete-event.md) Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se l'animazione **Return** di un'animazione viene definita usando rami Exit, non è necessario chiamarla in modo esplicito. Agent riproduce automaticamente **l'animazione Return** prima dell'animazione successiva. Tuttavia, se è **elencata** un'animazione Return, è necessario chiamare l'animazione usando il [**metodo Play**](play-method.md) prima di un'altra animazione per fornire una transizione uniforme. Se non è **elencata** alcuna animazione Return, l'animazione termina in genere senza la necessità di un'animazione di transizione.

Il file di caratteri include gli effetti sonori per alcune animazioni, come illustrato nella tabella seguente. Gli effetti sonori vengono riprodotti solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti sonori nell'applicazione.



| Animazione                 | Restituire un'animazione         | Supporta Speaking | Effetti sonori | Assegnato allo stato                            | Descrizione                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Riconoscere**           | Nessuno                     | No                | **No**        | Nessuno                                         | Nods head                                                  |
| **Avviso**                 | Sì, con i rami exit | Sì               | **No**        | **Ascolto**                                | Raddrizza                                                |
| **Annunciare**              | Sì, con i rami exit | Sì               | **Sì**       | Nessuno                                         | Stampa carta e report                               |
| **Blink**                 | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Lampeggia gli occhi                                                |
| **Confusione**              | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Testa dei scratch                                             |
| **Congratularmi con**          | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Alza le mani e quindi stringe le mani                             |
| **Non accetto**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Alza la mano e scuote la testa                                |
| **DoMagic1**              | Nessuno                     | Sì               | **No**        | Nessuno                                         | Rimuove il dispositivo                                             |
| **DoMagic2**              | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Preme il pulsante e viene visualizzato il raggio                            |
| **DontRecognize**         | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano all'udito                                          |
| **Explain**               | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Movimenti con le braccia                                         |
| **GestureDown**           | Sì, con i rami exit | Sì               | **No**        | **GesturingDown**                            | Movimenti verso il basso                                              |
| **GestureLeft**           | Sì, con i rami exit | Sì               | **No**        | **GesturingLeft**                            | Movimenti a sinistra                                              |
| **GestureRight**          | Sì, uso dei rami exit | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                             |
| **GestureUp**             | Sì, uso dei rami exit | Sì               | **No**        | **GesturingUp**                              | Movimenti in alto                                                |
| **GetAttention**          | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Onde                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Onde di nuovo                                           |
| **GetAttentionReturn**    | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **Greet**                 | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano                                              |
| **Udito \_ 1**            | Sì, uso dei rami exit | No                | **No**        | **Udito**                                  | Inclina la testa verso destra \* (animazione a ciclo continuo)                     |
| **Udito \_ 2**            | Sì, uso dei rami exit | No                | **No**        | **Udito**                                  | Inclina la testa a sinistra \* (animazione a ciclo continuo)                      |
| **Udito \_ 3**            | Sì, uso dei rami exit | No                | **No**        | **Udito**                                  | Freccia a sinistra \* (animazione a ciclo continuo)                      |
| **Udito \_ 4**            | Sì, uso dei rami exit | No                | **No**        | **Udito**                                  | Inclina la testa verso il basso \* (animazione a ciclo continuo)                      |
| **Nascondi**                  | Nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare attraverso la porta                                    |
| **\_Inattivo1 1**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi a destra                                              |
| **Inattivo 1 \_ 2**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi in alto e lampeggia                                      |
| **Inattivo1 \_ 3**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi in basso e lampeggia                                    |
| **Inattivo 1 \_ 4**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi a sinistra e lampeggia                                    |
| **Inattivo \_ 2 1**              | Nessuno                     | No                | **No**        | **IdlingLevel2**                             | Folds arms                                                 |
| **Inattivo \_ 2 2**              | Nessuno                     | No                | **Sì**       | **IdlingLevel2**                             | Rimuove la testa ed esegue la regolazione                          |
| **Inattivo3 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel3**                             | Sbadiglia                                                      |
| **Inattivo3 \_ 2**              | Nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Spegne                                                 |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | Nessuno                                         | Cerca in basso                                                 |
| **LookDownReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | Nessuno                                         | Sembra a sinistra                                                 |
| **LookLeftReturn**        | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | Nessuno                                         | Sembra a destra                                                |
| **LookRightReturn**       | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **Ricerca**                | **LookUpReturn**         | No                | **No**        | Nessuno                                         | Cerca                                                   |
| **LookUpReturn**          | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **MoveDown**              | Sì, uso dei rami exit | No                | **Sì**       | **MovingDown**                               | In basso                                                 |
| **MoveLeft**              | Sì, uso dei rami exit | No                | **Sì**       | **MovingLeft**                               | 1000 a sinistra                                                 |
| **MoveRight**             | Sì, uso dei rami exit | No                | **Sì**       | **MovingRight**                              | Diritto di controllo                                                |
| **MoveUp**                | Sì, uso dei rami exit | No                | **Sì**       | **MovingUp**                                 | Res up                                                   |
| **Contento**               | Sì, uso dei rami exit | Sì               | **Sì**       | Nessuno                                         | Smile e raddrizza                                  |
| **Processo**               | No                       | No                | **Sì**       | Nessuno                                         | Preme i pulsanti, stampa, legge e quindi lancia la stampa       |
| **Elaborazione in corso**            | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Preme i pulsanti, stampa, legge e quindi lancia la stampa       |
| **Lettura**                  | **ReadReturn**           | Sì               | **Sì**       | Nessuno                                         | Stampa, legge e cerca                                |
| **ReadContinued**         | **ReadReturn**           | Sì               | **Sì**       | Nessuno                                         | Legge e cerca                                         |
| **ReadReturn**            | Nessuno                     | No                | **Sì**       | Nessuno                                         | Torna alla posizione neutra                                |
| **Lettura**               | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Stampa, legge e cerca \* (animazione a ciclo continuo)          |
| **RestPose**              | Nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                           |
| **Triste**                   | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Espressione tristia                                             |
| **Ricerca**                | No                       | No                | **Sì**       | Nessuno                                         | Visualizza la casella degli strumenti e rimuove lo strumento                           |
| **Ricerca**             | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Visualizza la casella degli strumenti e rimuove gli strumenti \* (animazione a ciclo continuo)    |
| **Mostra**                  | Nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Viene visualizzato attraverso l'ingresso                                    |
| **Elenco di avvio**        | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette la mano all'ascolto                                           |
| **Elenco di arresto**         | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Mette le mani sopra le mani                                       |
| **Suggerisci**               | Sì, uso dei rami exit | Sì               | **Sì**       | Nessuno                                         | Visualizza la lampadina                                         |
| **Sorpreso**             | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Sembra disdato                                            |
| **Pensare**                 | Sì, uso dei rami exit | Sì               | **Sì**       | Nessuno                                         | Scratches head                                             |
| **Pensando**              | No                       | No                | **Sì**       | Nessuno                                         | Scratches head \* (animazione a ciclo continuo)                       |
| **Incerto**             | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Shrugs                                                     |
| **Onda**                  | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Onde                                                      |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Visualizza matita e Appunti, scrive e cerca          |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Scrive e cerca                                        |
| **WriteReturn**           | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **Scrittura**               | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Visualizza matita e Appunti, scritture \* (animazione a ciclo continuo) |



 

\* Se si riproduce un'animazione a ciclo continuo, è necessario usare [**Arresta**](stop-method.md) per cancellarla prima che altre animazioni nella coda del carattere verranno riprodotte.

 

