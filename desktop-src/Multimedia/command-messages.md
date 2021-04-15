---
title: Messaggi di comando
description: Messaggi di comando
ms.assetid: 29b40f35-d390-49c3-99bd-c648c7c50504
keywords:
- Messaggi di comando MCI, informazioni
- Messaggi di comando MCI, sintassi
- mciSendCommand (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc92b960e646ee1e452c7a356d0291c080d0162
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516714"
---
# <a name="command-messages"></a>Messaggi di comando

L'interfaccia del messaggio di comando è progettata per essere utilizzata dalle applicazioni che richiedono un'interfaccia del linguaggio C per il controllo dei dispositivi multimediali. Usa un paradigma di passaggio dei messaggi per comunicare con i dispositivi MCI. È possibile inviare un comando tramite la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

La funzione **mciSendCommand** restituisce zero in caso di esito positivo. Se la funzione ha esito negativo, la parola di ordine inferiore del valore restituito contiene un codice di errore. È possibile passare questo codice di errore alla funzione [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) per ottenere una descrizione di testo dell'errore.

## <a name="syntax-of-command-messages"></a>Sintassi dei messaggi di comando

I messaggi di comando MCI sono costituiti dagli elementi seguenti:

-   Valore costante del messaggio
-   Struttura che contiene i parametri per il comando.
-   Set di flag che specificano le opzioni per il comando e i campi di convalida nel blocco di parametri

Nell'esempio seguente viene usata la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare il comando [**MCI \_ Play**](mci-play.md) al dispositivo identificato da un identificatore di dispositivo.


```C++
mciSendCommand(wDeviceID,            // device identifier 
    MCI_PLAY,                        // command message 
    0,                               // flags 
    (DWORD)(LPVOID) &mciPlayParms);  // parameter block 
```



L'identificatore del dispositivo specificato nel primo parametro viene recuperato quando il dispositivo viene aperto usando il comando [**MCI \_ Open**](mci-open.md) . L'ultimo parametro è l'indirizzo di una [**struttura \_ \_ parametri di MCI Play**](mci-play-parms.md) , che può contenere informazioni sul punto in cui iniziare e terminare la riproduzione. Molti messaggi di comando MCI usano una struttura per contenere parametri di questo tipo. Il primo membro di ognuna di queste strutture identifica la finestra che riceve un [**messaggio \_ MCINOTIFY mm**](mm-mcinotify.md) al termine dell'operazione.

 

 