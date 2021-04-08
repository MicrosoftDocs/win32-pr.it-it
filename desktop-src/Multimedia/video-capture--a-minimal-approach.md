---
title: Acquisizione video un approccio minimo
description: Acquisizione video un approccio minimo
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Video per Windows (VFW), acquisizione video
- VFW (video per Windows), acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872401"
---
# <a name="video-capture-a-minimal-approach"></a>Acquisizione video: approccio minimo

Acquisizione video digitalizza un flusso di dati video e audio e lo archivia in un disco rigido o in un altro tipo di dispositivo di archiviazione permanente. In questa sezione viene descritto come aggiungere un semplice modulo di acquisizione video a un'applicazione utilizzando tre istruzioni di codice. Viene inoltre descritto come terminare o interrompere una sessione di acquisizione inviando messaggi alla finestra di acquisizione.

Una finestra di acquisizione di AVICap gestisce i dettagli dell'acquisizione audio e video di streaming in file AVI. Questo consente di liberare l'applicazione dal coinvolgimento del formato di file AVI, della gestione del buffer audio e video e dell'accesso di basso livello ai driver di dispositivo audio e video. AVICap fornisce un'interfaccia flessibile per le applicazioni. È possibile aggiungere l'acquisizione video all'applicazione usando solo le righe di codice seguenti:


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



È disponibile anche un'interfaccia macro che fornisce un'alternativa all'uso della funzione [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) e migliora la leggibilità di un'applicazione. Nell'esempio seguente viene usata l'interfaccia macro per aggiungere un'acquisizione video a un'applicazione.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Dopo che l'applicazione crea una finestra di acquisizione della classe della finestra AVICap e la connette a un driver video, la finestra di acquisizione è pronta per l'acquisizione dei dati. A questo punto, l'applicazione può semplicemente inviare il messaggio di [**\_ \_ sequenza Cap WM**](wm-cap-sequence.md) (o la macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) per avviare l'acquisizione.

Con le impostazioni predefinite, WM \_ Cap \_ Sequence avvia l'acquisizione di input audio e video in un file denominato CAPTURE.AVI. L'acquisizione continua fino a quando non si verifica uno degli eventi seguenti:

-   L'utente preme il tasto ESC o il pulsante del mouse.
-   L'applicazione interrompe o interrompe l'operazione di acquisizione.
-   Il disco diventa pieno.

In un'applicazione, è possibile arrestare il flusso di dati acquisiti in un file inviando il messaggio di [**\_ \_ arresto del Cap WM**](wm-cap-stop.md) (o la macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) a una finestra di acquisizione. È anche possibile interrompere l'operazione di acquisizione inviando il messaggio [**WM \_ Cap \_ Abort**](wm-cap-abort.md) (o la macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) a una finestra di acquisizione.

 

 