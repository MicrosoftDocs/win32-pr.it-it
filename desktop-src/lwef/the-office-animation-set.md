---
title: Set Office animazione
description: Set Office animazione
ms.assetid: ea80d19b-bf4c-4f6e-bab0-424a9f78f457
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cfe8ffbfb9d54ee956c36dd6eb1b3d567f26ad8dc55cd182282db6a685f3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975551"
---
# <a name="the-office-animation-set"></a>Set Office animazione

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Nella tabella seguente sono elencate le animazioni definite per Microsoft Office 2000 caratteri. Se si intende usare il carattere in Microsoft Office, è necessario supportare tutte le animazioni in questa tabella. È anche possibile aggiungere qualsiasi altra animazione in tempo reale, ma tenere presente che Microsoft Office non le chiamerà. Le animazioni con asterischi ( \* ) devono essere a ciclo continuo al 100%. Altre animazioni devono essere brevi.



| Animazione               | Stato agente    | Esempio di quando viene usato                                                                                 | Esempi di animazione specifici                                                                                                               |
|-------------------------|----------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **Avviso**               | Nessuno           | Quando il carattere vuole avvisare l'utente                                                           | Il carattere cerca l'utente.                                                                                                              |
| **Controllo di un'attività\*** | Nessuno           | Controllo ortografico, controllo grammaticale                                                                            | Carattere cerca qualcosa in un libro di riferimento                                                                                          |
| **Congratularmi con**        | Nessuno           | Completare una procedura guidata                                                                                    | Big grin, sguardo di rilievo, affaticato ma contento                                                                                                 |
| **EmptyTrash**          | Nessuno           | Il cestino viene svuotato in Outlook                                                                          | Il cestino delle luci dei caratteri si accende                                                                                                        |
| **Explain**             | Nessuno           | Quando il carattere vuole spiegare qualcosa all'utente                                            | Guarda brevemente ma con attenzione all'utente, quindi guarda lontano                                                                                     |
| **GestureDown**         | GesturingDown  | Il carattere indica qualcosa sullo schermo                                                         | Il carattere esamina l'utente e quindi punta e guarda lo schermo                                                                           |
| **GestureLeft**         | GesturingLeft  | Character indica qualcosa sullo schermo, ad esempio un argomento della Guida o una parte dell'interfaccia utente                  | Il carattere esamina l'utente e quindi punta e guarda lo schermo                                                                           |
| **GestureRight**        | GesturingRight | "Presentazione" di un argomento o di una finestra di dialogo della Guida                                                                  | Il carattere esamina l'utente e quindi punta e guarda lo schermo                                                                           |
| **GestureUp**           | GesturingUp    | Il carattere indica qualcosa sullo schermo                                                         | Il carattere esamina l'utente e quindi punta e guarda lo schermo                                                                           |
| **GetArtsy\***          | Nessuno           | Formattazione automatica                                                                                           | Character mette in bava, mantiene la tavolozza e disegna                                                                                        |
| **GetAttention**        | Nessuno           | Suggerimento con priorità alta                                                                                    | Movimenti fortemente per ottenere l'attenzione dell'utente; ad esempio, salta su e giù alzando le bracci                                                 |
| **GetTechy**            | Nessuno           | Viene eseguito durante l'esecuzione nell'ambiente di programmazione                                                                | Il carattere estrae la calcolatrice o il ferro da venduto                                                                                          |
| **GetWizardy\***        | Nessuno           | Creazione guidata grafico in esecuzione mentre il carattere è visibile (azione ri triggerata con ogni nuovo pannello della procedura guidata)        | Il carattere mette il berretto e la wand delle onde della procedura guidata                                                                                               |
| **Addio**             | Nessuno           | Viene scelto un altro carattere                                                                          | Si tratta di un'elaborata scomparsa che inizia in **RestPose** e termina con un frame vuoto                                                      |
| **Greeting (Messaggio introduttivo)**            | Nessuno           | Viene scelto il carattere                                                                                  | Si tratta di un'immagine elaborata che inizia con un frame vuoto e termina in **RestPose**                                                      |
| **Udito \_ 1\***        | Nessuno           | File lungo aperto                                                                                    | Ear to the ground, listening to the computer (Ascolto del computer)                                                                                              |
| **Nascondi**                | Nascondere         | Il carattere lascia temporaneamente                                                                         | Lascia rapidamente in una nuvola di fumo                                                                                                         |
| **Inattivo \_ 1 1**            | Nessun input utente  | In ascolto attivo, quindi si arriccia e va in sospensione. (opportunità di mostrare la personalità del carattere) | Lampeggiare, guardarsi intorno, attendere pazientemente                                                                                               |
| **Inattivo2**               | Nessun input utente  | Periodi di inattività più lunghi                                                                                  | Il carattere sbadiglia e sembra assonnato                                                                                                          |
| **Inattivo3**               | Nessun input utente  | Inattività profonda (quando il carattere è rimasto inattivo per molto tempo)                                         | Il carattere passa alla sospensione                                                                                                                   |
| **IdleHit**             | Nessuno           | Si tratta di un esempio rappresentativo non mappato di animazioni Idle Level 1                                | Tutte le animazioni inattive                                                                                                                |
| **LookDown**            | Nessuno           | Guarda in basso brevemente                                                                                   | Nota che una riga viene inserita e la osserva con un'occhiata                                                                                               |
| **LookDownLeft**        | Nessuno           | Guarda in basso e a sinistra brevemente                                                                          | Nota che una riga viene inserita e la osserva con un'occhiata                                                                                               |
| **LookDownRight**       | Nessuno           | Guarda in basso e a destra brevemente                                                                         | Nota che una colonna viene inserita e la osserva con un'occhiata                                                                                            |
| **LookLeft**            | Nessuno           | Sembra a sinistra per un breve periodo                                                                                   | Nota che una tabella viene inserita e la osserva con un'occhiata                                                                                             |
| **LookRight**           | Nessuno           | L'aspetto è breve                                                                                  | Nota che una parola viene spostata e la osserva                                                                                                 |
| **Ricerca**              | Nessuno           | Cerca brevemente, come se qualcosa succede sopra il carattere sullo schermo                          | Si fa clic sul pulsante della barra degli strumenti Notices e lo si osserva con un'occhiata (il carattere non è di grande interesse)                                   |
| **LookUpLeft**          | Nessuno           | Sembra a sinistra e verso l'alto brevemente                                                                            | Si fa clic sul pulsante della barra degli strumenti Notices e lo si osserva con un'occhiata (il carattere non è di grande interesse)                                   |
| **LookUpRight**         | Nessuno           | Sembra a destra e in alto per un breve periodo                                                                           | Si fa clic sul pulsante della barra degli strumenti Notices e lo si osserva con un'occhiata (il carattere non è di grande interesse)                                   |
| **Stampa**               | Nessuno           | Stampa di una pagina di un processo di stampa                                                                       | Afferra un foglio di carta e lo invia alla stampante                                                                                 |
| **Elaborazione in corso\***        | Nessuno           | Azione generale per cui non è stata eseguita un'azione carattere specifica                                     | Il carattere ha un aspetto di concentrazione ed estrae un aceto. L'animazione deve avere una voce rapida in un ciclo, quindi un'uscita rapida |
| **RestPose**            | Nessuno           | Usato quando il carattere non riproduce un'animazione                                                   | Immagine dell'assistente                                                                                                                 |
| **Salva\***              | Nessuno           | Usato durante un'operazione di salvataggio file                                                                    | Il carattere inserisce qualcosa in un insieme di credenziali                                                                                                     |
| **Ricerca\***         | Nessuno           | Usato per la ricerca, il controllo ortografico e il controllo grammaticale                                                        | La testa ruota e esamina il documento. L'animazione deve avere una voce rapida in un ciclo, quindi un'uscita rapida                                 |
| **SendMail**            | Nessuno           | Invio di messaggi di posta elettronica                                                                                         | Estrae una lettera e la inserisce in una cassetta postale                                                                                             |
| **Mostra**                | Visualizzazione        | Il carattere viene restituito da un breve periodo di tempo                                                                   | Rapidamente sul stage                                                                                                         |
| **Pensando\***          | Nessuno           | Esecuzione di un calcolo complesso, ad esempio risolutore                                                          | Il carattere guarda verso l'alto e si gratta la testa. L'animazione deve avere una voce rapida in un ciclo, quindi un'uscita rapida                             |
| **Onda**                | Nessuno           | Avvisi relativi                                                                                  | Onda. Simile a Alert, ma non long o as frantic                                                                                     |
| **Scrittura\***           | Nessuno           | Il cliente cambia qualcosa in Strumenti Opzioni; richiesta IntelliSearch digitata dal cliente                   | Estrae il pad e avvia lo scribbling. L'animazione deve avere una voce rapida in un ciclo, quindi un'uscita rapida                                   |



 

 

 




