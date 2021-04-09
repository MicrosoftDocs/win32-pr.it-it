---
title: Interfaccia utente della finestra MCIWnd
description: Interfaccia utente della finestra MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044330"
---
# <a name="mciwnd-window-user-interface"></a>Interfaccia utente della finestra MCIWnd

MCIWnd fornisce funzionalità aggiuntive per regolare l'aspetto della finestra MCIWnd, personalizzare il comportamento dell'applicazione e ottimizzare le prestazioni di riproduzione. Nella finestra MCIWnd sono incluse le funzionalità seguenti:

-   Barra degli strumenti con pulsanti di **riproduzione**, **arresto**, **record** e **menu**
-   TrackBar che controlla il posizionamento all'interno del contenuto di riproduzione
-   Menu di scelta rapida contenente i comandi comuni
-   Area di riproduzione per video e altri dispositivi che visualizzano immagini

Nella figura seguente viene illustrato lo stato iniziale della riproduzione video controllata dall'utente. Il file di esempio usato è CLOCK.AVI.

![Immagine di clock.avi](images/mciwnd1.gif)

La finestra MCIWnd include un'area di riproduzione per video e altri dispositivi che visualizzano immagini durante la riproduzione. MCIWnd omette l'area di riproduzione dai dispositivi audio e della forma d'onda, i sequencer MIDI e altri dispositivi che non scrivono sullo schermo. Nell'illustrazione seguente viene mostrata l'area di riproduzione dell'audio e della forma d'onda.

![immagine della finestra MCIWnd](images/mciwnd4.gif)

Il pulsante **Play** si trova nell'angolo inferiore sinistro della finestra MCIWnd. Viene visualizzato quando il contenuto viene arrestato. L'utente può riprodurre il contenuto nei modi seguenti:

-   Per riprodurre il contenuto dalla posizione di riproduzione corrente, selezionare il pulsante **Riproduci** .
-   Per riprodurre il contenuto a schermo intero dalla posizione di riproduzione corrente, selezionare il pulsante **Play** tenendo premuto il tasto CTRL.
-   Per riprodurre il contenuto indietro rispetto alla posizione di riproduzione corrente, selezionare il pulsante **Riproduci** tenendo premuto il tasto MAIUSC.

Il pulsante di **menu** , situato accanto al pulsante **Riproduci** , attiva un menu che consente all'utente di aprire e chiudere i file audio-video con interfoliazione (AVI) e di regolare le dimensioni dell'immagine, la velocità di riproduzione e il volume. L'utente può anche attivare il menu facendo clic con il pulsante destro del mouse quando il cursore si trova nell'area client della finestra. Il menu include anche i comandi per modificare la configurazione del dispositivo corrente, per copiare il contenuto della riproduzione negli Appunti e per emettere i comandi MCI.

Il TrackBar a destra del pulsante di **menu** rappresenta la durata del contenuto di riproduzione (o registrato). Il dispositivo di scorrimento nel TrackBar rappresenta la posizione di riproduzione corrente all'interno del contenuto. Quando il dispositivo di scorrimento è posizionato all'estremità sinistra del TrackBar, la posizione di riproduzione corrente è l'inizio del contenuto. L'utente può spostarsi in posizioni diverse nel contenuto trascinando il dispositivo di scorrimento lungo il TrackBar. Il pulsante **Arresta** si trova nell'angolo inferiore sinistro della finestra MCIWnd. Viene visualizzato quando viene riprodotto il contenuto. La figura seguente mostra la riproduzione video in corso.

![immagine di riproduzione video](images/mciwnd2.gif)

I controlli MCIWnd possono includere anche un pulsante di **registrazione** per i dispositivi che possono registrare. Il pulsante **record** è contrassegnato da un cerchio rosso e viene visualizzato solo quando il dispositivo è in grado di registrare.

> [!Note]  
> La finestra di riproduzione deve essere allineata su un limite di quattro pixel per ottenere prestazioni migliori per la riproduzione video. In genere, Windows allinea automaticamente la finestra al momento della creazione. Se un utente sposta o estende la finestra dalla posizione iniziale, la velocità di riproduzione del video potrebbe essere ridotta di metà.

 

 

 




