---
title: Animazioni degli agenti Microsoft per il carattere di pipì
description: Animazioni degli agenti Microsoft per il carattere di pipì
ms.assetid: 335d915c-9cae-4850-a6bf-66ad78d533ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e064063b322bc6549d91b5fce35bdbc491a5a3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727034"
---
# <a name="microsoft-agent-animations-for-peedy-character"></a>Animazioni degli agenti Microsoft per il carattere di pipì

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il carattere di inattività di [Microsoft Agent](https://www.microsoft.com/downloads/details.aspx?FamilyID=bd3c4655-79e4-4791-ab9d-abc7bbd133ef) è una società con copyright di Microsoft Corporation.

La pipì supporta le animazioni elencate nella tabella seguente. Vedere [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programming the Microsoft Agent Control](programming-the-microsoft-agent-control.md) per informazioni su come chiamare le animazioni del carattere.

Se si accede a queste animazioni di caratteri utilizzando il protocollo HTTP e il metodo di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo [**Get**](get-method.md) o del server, valutare il modo in cui eseguirne il download. Anziché scaricare contemporaneamente tutte le animazioni, è possibile recuperare prima le animazioni dello stato di **visualizzazione** e di **pronuncia** . In questo modo sarà possibile visualizzare il carattere rapidamente e fare in modo che parli mentre si disattivano le altre animazioni in modo asincrono. Per assicurarsi che il caricamento dei dati di tipo carattere e animazione venga eseguito correttamente, utilizzare l'evento [**RequestComplete**](requestcomplete-event.md) . Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se un'animazione **restituisce** un'animazione viene definita usando i rami di uscita, non è necessario chiamarla in modo esplicito; Agent esegue automaticamente l'animazione **restituita** prima dell'animazione successiva. Tuttavia, se viene elencata un'animazione **restituita** , è necessario chiamare l'animazione utilizzando il metodo [**Play**](play-method.md) prima di un'altra animazione per fornire una transizione senza problemi. Se non è presente alcuna animazione **restituita** , l'animazione termina in genere senza che sia necessaria un'animazione di transizione.

Se si accede a queste animazioni di caratteri utilizzando il protocollo HTTP e il metodo di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo [**Get**](get-method.md) o del server, valutare il modo in cui eseguirne il download. Anziché scaricare contemporaneamente tutte le animazioni, è possibile recuperare prima le animazioni dello stato di **visualizzazione** e di **pronuncia** . In questo modo sarà possibile visualizzare il carattere rapidamente e fare in modo che parli mentre si disattivano le altre animazioni in modo asincrono. Per assicurarsi che il caricamento dei dati di tipo carattere e animazione venga eseguito correttamente, utilizzare l'evento [**RequestComplete**](requestcomplete-event.md) . Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Il file di caratteri include effetti audio per alcune animazioni, come indicato nella tabella seguente. Gli effetti audio Riproduci solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti audio nell'applicazione.



| Animazione                  | Restituisci animazione         | Supporta l'espressione | Effetti audio | Assegnato a stato                            | Descrizione                                            |
|----------------------------|--------------------------|-------------------|---------------|----------------------------------------------|--------------------------------------------------------|
| **Riconoscere**            | nessuno                     | No                | **No**        | nessuno                                         | Cenni Head                                              |
| **Avviso**                  | Sì, uso di rami di uscita | Sì               | **No**        | **In ascolto**                                | Raddrizza e genera sopracciglia                        |
| **Annunciare**               | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Paper Airplane Vola in e si apre                    |
| **Blink**                  | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Lampeggia gli occhi                                            |
| **Confusione**               | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Gli occhi girano                                       |
| **Congratularmi**           | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Visualizza la barra multifunzione blu                                   |
| **Non accetto**                | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Agita la testa                                            |
| **DoMagic1**               | nessuno                     | Sì               | **Sì**       | nessuno                                         | Genera bacchetta magica                                      |
| **DoMagic2**               | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Abbassa bacchetta, vengono visualizzati i cloud                             |
| **DontRecognize**          | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Scuote la testa e si aggrappa ala a orecchio                      |
| **Explain**                | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Estende le armi al lato                                   |
| **GestureDown**            | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingDown**                            | Movimenti in basso                                          |
| **GestureLeft**            | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingLeft**                            | Movimenti rimasti                                          |
| **GestureRight**           | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                         |
| **GestureUp**              | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                            |
| **Getattenzione**           | **GetAttentionReturn**   | Sì               | **Sì**       | nessuno                                         | Salta con le ali estesi                       |
| **GetAttentionContinued**  | **GetAttentionReturn**   | Sì               | **Sì**       | nessuno                                         | Salta di nuovo con le ali estesi                 |
| **GetAttentionReturn**     | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **Greet**                  | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Archi                                                   |
| **Udienza \_ 1**             | nessuno                     | No                | **No**        | **Udito**                                  | Inclina la testa a destra ( \* animazione ciclo)                 |
| **Udienza \_ 2**             | nessuno                     | No                | **No**        | **Udito**                                  | Inclina il capo a sinistra ( \* animazione ciclo)                  |
| **Udienza \_ 3**             | nessuno                     | No                | **No**        | **Udito**                                  | Ruota verso destra a sinistra ( \* animazione ciclo)       |
| **Nascondi**                   | nessuno                     | No                | **Sì**       | **Nascondere**                                   | Vola fuori                                             |
| **Idle1 \_ 1**               | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Si respira                                           |
| **Idle1 \_ 2**               | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi giusti e lampeggianti                               |
| **Idle1 \_ 3**               | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi a sinistra e a lampeggiamento                                |
| **Idle1 \_ 4**               | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi e lampeggi                                  |
| **Idle1 \_ 5**               | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi in basso e lampeggia                                |
| **Idle2 \_ 1**               | Sì, uso di rami di uscita | No                | **No**        | **IdlingLevel2**                             | Mette in occhiali                                     |
| **Idle2 \_ 2**               | nessuno                     | No                | **Sì**       | **IdlingLevel2**                             | Mangia un cracker                                         |
| **Idle3 \_ 1**               | nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Noia                                                  |
| **Idle3 \_ 2**               | Sì, uso di rami di uscita | No                | **Sì**       | **IdlingLevel3**                             | Cade in sospensione ( \* animazione ciclo)                     |
| **Idle3 \_ 3**               | Sì, uso di rami di uscita | No                | **No**        | **IdlingLevel3**                             | Ascolta musica ( \* animazione ciclo)                 |
| **LookDownLookDownReturn** |                          | No                | **No**        | nessuno                                         | Cerca giù                                             |
| **LookDownBlink**          | **LookDownReturn**       | No                | **Sì**       | nessuno                                         | Lampeggiare alla ricerca                                    |
| **LookDownReturn**         | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookDownLeft**           | **LookDownLeftReturn**   | No                | **No**        | nessuno                                         | Cerca in basso a sinistra                                        |
| **LookDownLeftBlink**      | **LookDownLeftReturn**   | No                | **Sì**       | nessuno                                         | Lampeggia alla ricerca verso il basso a sinistra                               |
| **LookDownLeftReturn**     | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookDownRight**          | **LookDownRightReturn**  | No                | **No**        | nessuno                                         | Cerca in basso a destra                                       |
| **LookDownRightBlink**     | **LookDownRightReturn**  | No                | **Sì**       | nessuno                                         | Lampeggia la ricerca verso il basso a destra                              |
| **LookDownRightReturn**    | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookLeft**               | **LookLeftReturn**       | Sì               | **No**        | nessuno                                         | A sinistra                                             |
| **LookLeftBlink**          | **LookLeftReturn**       | Sì               | **Sì**       | nessuno                                         | Lampeggia a sinistra                                    |
| **LookLeftReturn**         | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookRight**              | **LookRightReturn**      | Sì               | **No**        | nessuno                                         | A destra                                            |
| **LookRightBlink**         | **LookRightReturn**      | Sì               | **Sì**       | nessuno                                         | Lampeggia a destra                                   |
| **LookRightReturn**        | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **Ricerca**                 | **LookUpReturn**         | No                | **No**        | nessuno                                         | Cerca                                               |
| **LookUpBlink**            | **LookUpReturn**         | No                | **Sì**       | nessuno                                         | Lampeggia la ricerca                                      |
| **LookUpReturn**           | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookUpLeft**             | **LookUpLeftReturn**     | No                | **No**        | nessuno                                         | Cerca in alto a sinistra                                          |
| **LookUpLeftBlink**        | **LookUpLeftReturn**     | No                | **Sì**       | nessuno                                         | Lampeggia la ricerca verso sinistra                                 |
| **LookUpLeftReturn**       | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **LookUpRight**            | **LookUpRightReturn**    | No                | **No**        | nessuno                                         | Cerca in alto a destra                                         |
| **LookUpRightBlink**       | **LookUpRightReturn**    | No                | **Sì**       | nessuno                                         | Lampeggia la ricerca a destra                                |
| **LookUpRightReturn**      | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **MoveDown**               | Sì, uso di rami di uscita | No                | **Sì**       | **MovingDown**                               | Vola giù                                             |
| **MoveLeft**               | Sì, uso di rami di uscita | No                | **Sì**       | **MovingLeft**                               | Mosche a sinistra                                             |
| **MoveRight**              | Sì, uso di rami di uscita | No                | **Sì**       | **MovingRight**                              | Vola a destra                                            |
| **MoveUp**                 | Sì, uso di rami di uscita | No                | **Sì**       | **MovingUp**                                 | Vola su                                               |
| **Lieti**                | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | I                                                 |
| **Processo**                | nessuno                     | No                | **Sì**       | nessuno                                         | Usa il calcolatore                                        |
| **Elaborazione in corso**             | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | USA Calculator ( \* animazione ciclo)                  |
| **Lettura**                   | **ReadReturn**           | Sì               | **Sì**       | nessuno                                         | Apre Magazine, legge e cerca                     |
| **ReadContinued**          | **ReadReturn**           | Sì               | **Sì**       | nessuno                                         | Letture e ricerca                                     |
| **ReadReturn**             | nessuno                     | No                | **Sì**       | nessuno                                         | Torna alla posizione neutra                            |
| **Lettura**                | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Letture ( \* animazione ciclo)                            |
| **RestPose**               | nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                       |
| **Triste**                    | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Espressione triste                                         |
| **Ricerca**                 | nessuno                     | No                | **Sì**       | nessuno                                         | Rivela il teletelescopio e ruota                          |
| **Ricerca**              | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Rivela il teletelescopio e ruota ( \* animazione ciclo)    |
| **Mostra**                   | nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Vola in                                               |
| **StartListening**         | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Passa a orecchio                                       |
| **StopListening**          | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Inserisce le orecchie                                     |
| **Suggerisci**                | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Visualizza lampadina                                    |
| **Sorprendente**              | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Sembra sorpreso                                        |
| **Pensare**                  | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Cerca con ala sulla faccia                             |
| **Pensare**               | nessuno                     | No                | **No**        | nessuno                                         | Cerca con ala sulla faccia ( \* animazione ciclo)       |
| **Incerto**              | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Si avvicina a destra e alle spalle                              |
| **Onda**                   | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Diverse fasi                                                  |
| **Scrittura**                  | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Estrae matita e riempimento, scrive e cerca          |
| **WriteContinued**         | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Scrive e cerca                                    |
| **WriteReturn**            | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                            |
| **Scrittura**                | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Estrae matita e riempimento, Scritture ( \* animazione ciclo) |



 

\* Se si riproduce un'animazione di ciclo, è necessario usare [**Stop**](stop-method.md) per cancellarla prima che vengano riprodotte altre animazioni nella coda del carattere.

 

