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

Il [carattere robby di Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) è un'opera con copyright di Microsoft Corporation.

Robby supporta le animazioni elencate nella tabella seguente. Per informazioni su come chiamare le animazioni del carattere, vedere Programming the Microsoft Agent Server Interface (Programmazione dell'interfaccia server di [Microsoft Agent)](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e Programming the Microsoft Agent Control (Programmazione del controllo [Microsoft Agent).](programming-the-microsoft-agent-control.md)

Se si accede a queste animazioni di caratteri usando il protocollo HTTP e il metodo [**Get**](get-method.md) o [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo, prendere in considerazione il modo in cui verranno scaricate. Invece di scaricare tutte le animazioni contemporaneamente, è possibile recuperare prima le animazioni di stato **Showing** (Visualizzazione) e **Speaking** (Pronuncia). In questo modo sarà possibile visualizzare rapidamente il carattere e farlo parlare mentre altre animazioni vengono avviate in modo asincrono. Inoltre, per assicurarsi che i dati dei caratteri e delle animazioni siano caricati correttamente, usare [**l'evento RequestComplete.**](requestcomplete-event.md) Se una richiesta di caricamento non riesce, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se l'animazione **Return** di un'animazione viene definita usando rami Exit, non è necessario chiamarla in modo esplicito. Agent riproduce automaticamente **l'animazione Return** prima dell'animazione successiva. Tuttavia, se è **elencata** un'animazione Return, è necessario chiamare l'animazione usando il metodo [**Play**](play-method.md) prima di un'altra animazione per fornire una transizione uniforme. Se non è **elencata** alcuna animazione Return, l'animazione termina in genere senza che sia necessaria un'animazione di transizione.

Il file di caratteri include effetti audio per alcune animazioni, come illustrato nella tabella seguente. Gli effetti sonori vengono riprodotti solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti audio nell'applicazione.



| Animazione                 | Restituire un'animazione         | Supporto per la pronuncia | Effetti sonori | Assegnato allo stato                            | Descrizione                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Riconoscere**           | Nessuno                     | No                | **No**        | Nessuno                                         | Nods head                                                  |
| **Avviso**                 | Sì, uso dei rami exit | Sì               | **No**        | **Ascolto**                                | Raddrizza                                                |
| **Annunciare**              | Sì, uso dei rami exit | Sì               | **Sì**       | Nessuno                                         | Stampa carta e report                               |
| **Blink**                 | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Lampeggia gli occhi                                                |
| **Confusione**              | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Scratches head                                             |
| **Congratularmi con**          | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Alza le mani e quindi stringe le mani                             |
| **Non accetto**               | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Alza la mano e trema la testa                                |
| **DoMagic1**              | Nessuno                     | Sì               | **No**        | Nessuno                                         | Rimuove il dispositivo                                             |
| **DoMagic2**              | Sì, uso dei rami exit | No                | **Sì**       | Nessuno                                         | Preme il pulsante e viene visualizzato il trave                            |
| **DontRecognize**         | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano all'ascolto                                          |
| **Explain**               | Sì, uso dei rami exit | Sì               | **No**        | Nessuno                                         | Movimenti con le mani                                         |
| **GestureDown**           | Sì, uso dei rami exit | Sì               | **No**        | **GesturingDown**                            | Movimenti in basso                                              |
| **GestureLeft**           | Sì, uso dei rami exit | Sì               | **No**        | **GesturingLeft**                            | Movimenti a sinistra                                              |
| **GestureRight**          | Sì, con i rami exit | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                             |
| **GestureUp**             | Sì, con i rami exit | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                                |
| **GetAttention**          | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Onde di bracci                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **No**        | Nessuno                                         | Ondate di nuovo le bracci                                           |
| **GetAttentionReturn**    | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **Greet**                 | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Tiene la mano                                              |
| **Udito \_ 1**            | Sì, con i rami exit | No                | **No**        | **Udito**                                  | Inclina la testa a destra \* (animazione a ciclo continuo)                     |
| **Udito \_ 2**            | Sì, con i rami exit | No                | **No**        | **Udito**                                  | Inclina la testa a sinistra \* (animazione a ciclo continuo)                      |
| **Udito \_ 3**            | Sì, con i rami exit | No                | **No**        | **Udito**                                  | Testa a sinistra \* (animazione a ciclo continuo)                      |
| **Udito \_ 4**            | Sì, con i rami exit | No                | **No**        | **Udito**                                  | Inclina verso il basso \* (animazione a ciclo continuo)                      |
| **Nascondi**                  | Nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare attraverso la porta                                    |
| **Inattivo 1 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi a destra                                              |
| **Inattivo 1 \_ 2**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso l'alto e lampeggia                                      |
| **Inattivo1 \_ 3**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso il basso e lampeggia                                    |
| **Inattivo1 \_ 4**              | Nessuno                     | No                | **No**        | **IdlingLevel1** **IdlingLevel2**<br/> | Sguardi verso sinistra e lampeggia                                    |
| **Inattivo 2 \_ 1**              | Nessuno                     | No                | **No**        | **IdlingLevel2**                             | Incrocia le bracci                                                 |
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
| **Onda**                  | Sì, con i rami exit | Sì               | **No**        | Nessuno                                         | Onde                                                      |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Visualizza matita e Appunti, scrive e cerca          |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | Nessuno                                         | Scrive e cerca                                        |
| **WriteReturn**           | Nessuno                     | No                | **No**        | Nessuno                                         | Torna alla posizione neutra                                |
| **Scrittura**               | Sì, con i rami exit | No                | **Sì**       | Nessuno                                         | Visualizza matita e Appunti, scrive \* (animazione a ciclo continuo) |



 

\* Se si riproduce un'animazione a ciclo continuo, è necessario usare [**Arresta**](stop-method.md) per cancellarla prima che altre animazioni nella coda del carattere verranno riprodotte.

 

