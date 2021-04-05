---
title: Animazioni degli agenti Microsoft per il carattere Robby
description: Animazioni degli agenti Microsoft per il carattere Robby
ms.assetid: 05baf1ab-3217-4da4-9562-6719c58cd744
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347c95fd6a29af72041d3b9e1192167d34602260
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725919"
---
# <a name="microsoft-agent-animations-for-robby-character"></a>Animazioni degli agenti Microsoft per il carattere Robby

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il [carattere di Microsoft Agent Robby](https://www.microsoft.com/downloads/details.aspx?FamilyID=fa36d1d5-d828-494a-ad0a-7b571db5bd2e) è un lavoro di copyright di Microsoft Corporation.

Robby supporta le animazioni elencate nella tabella seguente. Vedere [Programming the Microsoft Agent Server Interface](/windows/desktop/lwef/programming-the-microsoft-agent-server-interface) e [Programming the Microsoft Agent Control](programming-the-microsoft-agent-control.md) per informazioni su come chiamare le animazioni del carattere.

Se si accede a queste animazioni di caratteri utilizzando il protocollo HTTP e il metodo di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) del controllo [**Get**](get-method.md) o del server, valutare il modo in cui eseguirne il download. Anziché scaricare contemporaneamente tutte le animazioni, è possibile recuperare prima le animazioni dello stato di **visualizzazione** e di **pronuncia** . In questo modo sarà possibile visualizzare il carattere rapidamente e fare in modo che parli mentre si disattivano le altre animazioni in modo asincrono. Per assicurarsi che il caricamento dei dati di tipo carattere e animazione venga eseguito correttamente, utilizzare l'evento [**RequestComplete**](requestcomplete-event.md) . Se una richiesta di caricamento ha esito negativo, è possibile riprovare a caricare i dati o visualizzare un messaggio appropriato.

Se un'animazione **restituisce** un'animazione viene definita usando i rami di uscita, non è necessario chiamarla in modo esplicito; Agent esegue automaticamente l'animazione **restituita** prima dell'animazione successiva. Tuttavia, se viene elencata un'animazione **restituita** , è necessario chiamare l'animazione utilizzando il metodo [**Play**](play-method.md) prima di un'altra animazione per fornire una transizione senza problemi. Se non è presente alcuna animazione **restituita** , l'animazione termina in genere senza che sia necessaria un'animazione di transizione.

Il file di caratteri include effetti audio per alcune animazioni, come indicato nella tabella seguente. Gli effetti audio Riproduci solo se questa opzione è abilitata nella finestra delle proprietà di Microsoft Agent. È anche possibile disabilitare gli effetti audio nell'applicazione.



| Animazione                 | Restituisci animazione         | Supporta l'espressione | Effetti audio | Assegnato a stato                            | Descrizione                                                |
|---------------------------|--------------------------|-------------------|---------------|----------------------------------------------|------------------------------------------------------------|
| **Riconoscere**           | nessuno                     | No                | **No**        | nessuno                                         | Cenni Head                                                  |
| **Avviso**                 | Sì, uso di rami di uscita | Sì               | **No**        | **In ascolto**                                | Raddrizza                                                |
| **Annunciare**              | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Stampa carta e report                               |
| **Blink**                 | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Lampeggia gli occhi                                                |
| **Confusione**              | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Testa graffi                                             |
| **Congratularmi**          | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Eleva le mani e quindi stringe le mani                             |
| **Non accetto**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Genera la mano e scuote la testa                                |
| **DoMagic1**              | nessuno                     | Sì               | **No**        | nessuno                                         | Rimuove il dispositivo                                             |
| **DoMagic2**              | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Viene visualizzata la pressione del pulsante e del raggio                            |
| **DontRecognize**         | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Passa a orecchio                                          |
| **Explain**               | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Movimenti con bracci                                         |
| **GestureDown**           | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingDown**                            | Movimenti in basso                                              |
| **GestureLeft**           | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingLeft**                            | Movimenti rimasti                                              |
| **GestureRight**          | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingRight**                           | Movimenti a destra                                             |
| **GestureUp**             | Sì, uso di rami di uscita | Sì               | **No**        | **GesturingUp**                              | Movimenti verso l'alto                                                |
| **Getattenzione**          | **GetAttentionReturn**   | Sì               | **No**        | nessuno                                         | Bracci d'onda                                                 |
| **GetAttentionContinued** | **GetAttentionReturn**   | Sì               | **No**        | nessuno                                         | Di nuovo Waves Arms                                           |
| **GetAttentionReturn**    | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **Greet**                 | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | In mano                                              |
| **Udienza \_ 1**            | Sì, uso di rami di uscita | No                | **No**        | **Udito**                                  | Inclina la testa a destra ( \* animazione ciclo)                     |
| **Udienza \_ 2**            | Sì, uso di rami di uscita | No                | **No**        | **Udito**                                  | Inclina il capo a sinistra ( \* animazione ciclo)                      |
| **Udienza \_ 3**            | Sì, uso di rami di uscita | No                | **No**        | **Udito**                                  | Cocks Head Left ( \* animazione loop)                      |
| **Udienza \_ 4**            | Sì, uso di rami di uscita | No                | **No**        | **Udito**                                  | Inclina l'intestazione verso il basso ( \* animazione ciclo)                      |
| **Nascondi**                  | nessuno                     | No                | **Sì**       | **Nascondere**                                   | Scompare dalla porta                                    |
| **Idle1 \_ 1**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi a destra                                              |
| **Idle1 \_ 2**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi e lampeggi                                      |
| **Idle1 \_ 3**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi in basso e lampeggia                                    |
| **Idle1 \_ 4**              | nessuno                     | No                | **No**        |  **IdlingLevel2** IdlingLevel1<br/> | Sguardi a sinistra e a lampeggiamento                                    |
| **Idle2 \_ 1**              | nessuno                     | No                | **No**        | **IdlingLevel2**                             | Riduzioni bracci                                                 |
| **Idle2 \_ 2**              | nessuno                     | No                | **Sì**       | **IdlingLevel2**                             | Rimuove la testa e apporta la regolazione                          |
| **Idle3 \_ 1**              | nessuno                     | No                | **No**        | **IdlingLevel3**                             | Noia                                                      |
| **Idle3 \_ 2**              | nessuno                     | No                | **Sì**       | **IdlingLevel3**                             | Arresta                                                 |
| **LookDown**              | **LookDownReturn**       | No                | **No**        | nessuno                                         | Cerca giù                                                 |
| **LookDownReturn**        | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **LookLeft**              | **LookLeftReturn**       | No                | **No**        | nessuno                                         | A sinistra                                                 |
| **LookLeftReturn**        | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **LookRight**             | **LookRightReturn**      | No                | **No**        | nessuno                                         | A destra                                                |
| **LookRightReturn**       | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **Ricerca**                | **LookUpReturn**         | No                | **No**        | nessuno                                         | Cerca                                                   |
| **LookUpReturn**          | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **MoveDown**              | Sì, uso di rami di uscita | No                | **Sì**       | **MovingDown**                               | Vola giù                                                 |
| **MoveLeft**              | Sì, uso di rami di uscita | No                | **Sì**       | **MovingLeft**                               | Mosche a sinistra                                                 |
| **MoveRight**             | Sì, uso di rami di uscita | No                | **Sì**       | **MovingRight**                              | Vola a destra                                                |
| **MoveUp**                | Sì, uso di rami di uscita | No                | **Sì**       | **MovingUp**                                 | Vola su                                                   |
| **Lieti**               | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Smile e raddrizzamento                                  |
| **Processo**               | No                       | No                | **Sì**       | nessuno                                         | Preme i pulsanti, stampa, letture, quindi esegue il lancio della stampa       |
| **Elaborazione in corso**            | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Preme i pulsanti, stampa, letture, quindi esegue il lancio della stampa       |
| **Lettura**                  | **ReadReturn**           | Sì               | **Sì**       | nessuno                                         | Stampa, letture e ricerca                                |
| **ReadContinued**         | **ReadReturn**           | Sì               | **Sì**       | nessuno                                         | Letture e ricerca                                         |
| **ReadReturn**            | nessuno                     | No                | **Sì**       | nessuno                                         | Torna alla posizione neutra                                |
| **Lettura**               | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Stampa, letture e ricerca ( \* animazione ciclo)          |
| **RestPose**              | nessuno                     | Sì               | **No**        | **Parlando**                                 | Posizione neutra                                           |
| **Triste**                   | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Espressione triste                                             |
| **Ricerca**                | No                       | No                | **Sì**       | nessuno                                         | Mostra la casella degli strumenti e rimuove lo strumento                           |
| **Ricerca**             | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Consente di visualizzare la casella degli strumenti e di rimuovere gli strumenti ( \* animazione ciclo)    |
| **Mostra**                  | nessuno                     | No                | **Sì**       | **Visualizzazione**                                  | Viene visualizzato attraverso la porta                                    |
| **StartListening**        | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Passa a orecchio                                           |
| **StopListening**         | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Mette a disposizione gli orecchi                                       |
| **Suggerisci**               | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Visualizza lampadina                                         |
| **Sorprendente**             | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Sembra sorpreso                                            |
| **Pensare**                 | Sì, uso di rami di uscita | Sì               | **Sì**       | nessuno                                         | Testa graffi                                             |
| **Pensare**              | No                       | No                | **Sì**       | nessuno                                         | Scratch Head ( \* animazione ciclo)                       |
| **Incerto**             | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Alza                                                     |
| **Onda**                  | Sì, uso di rami di uscita | Sì               | **No**        | nessuno                                         | Diverse fasi                                                      |
| **Scrittura**                 | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Rivela matita e appunti, scrive e cerca          |
| **WriteContinued**        | **WriteReturn**          | Sì               | **Sì**       | nessuno                                         | Scrive e cerca                                        |
| **WriteReturn**           | nessuno                     | No                | **No**        | nessuno                                         | Torna alla posizione neutra                                |
| **Scrittura**               | Sì, uso di rami di uscita | No                | **Sì**       | nessuno                                         | Rivela matita e appunti, Scritture ( \* animazione ciclo) |



 

\* Se si riproduce un'animazione di ciclo, è necessario usare [**Stop**](stop-method.md) per cancellarla prima che vengano riprodotte altre animazioni nella coda del carattere.

 

