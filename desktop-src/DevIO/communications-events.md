---
description: Un processo può monitorare un set di eventi che si verificano in una risorsa di comunicazione. Ad esempio, un'applicazione può usare il monitoraggio eventi per determinare quando cambia lo stato dei segnali CTS (clear-to-send) e DSR (data-set-ready).
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventi di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bcb257652723a2464ff66c862f574f6aeae621bc6459b55d250f785d0b0895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815491"
---
# <a name="communications-events"></a>Eventi di comunicazione

Un processo può monitorare un set di eventi che si verificano in una risorsa di comunicazione. Ad esempio, un'applicazione può usare il monitoraggio eventi per determinare quando cambia lo stato dei segnali CTS (clear-to-send) e DSR (data-set-ready).

Un processo può monitorare gli eventi in una determinata risorsa di comunicazione usando la [**funzione SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) per creare una maschera di evento. Per determinare la maschera di evento corrente per una risorsa di comunicazione, un processo può usare la [**funzione GetCommMask.**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) I valori seguenti specificano gli eventi che possono essere monitorati.



| Valore           | Significato                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **INTERRUZIONE \_ EV**   | È stata rilevata un'interruzione nell'input.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | Lo stato del segnale CTS (clear-to-send) è stato modificato.                                                                                                                                                                                                     |
| **EV \_ DSR**     | Lo stato del segnale DSR (data-set-ready) è stato modificato.                                                                                                                                                                                                    |
| **EV \_ ERR**     | Si è verificato un errore di stato della riga. Gli errori di stato della riga **sono CE \_ FRAME,** **CE \_ OVERRUN** e **CE \_ RXPARITY.**                                                                                                                                        |
| **ANELLO \_ EV**    | È stato rilevato un indicatore sonoro.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | Lo stato del segnale RLSD (receive-line-signal-detect) è stato modificato.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | È stato ricevuto un carattere ed è stato collocato nel buffer di input.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | Il carattere dell'evento è stato ricevuto e inserito nel buffer di input. Il carattere dell'evento viene specificato nella struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) del dispositivo, che viene applicata a una porta seriale usando la [**funzione SetCommState.**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) |
| **EV \_ TXEMPTY** | L'ultimo carattere nel buffer di output è stato inviato.                                                                                                                                                                                                 |



 

Dopo aver specificato un set di eventi, un processo usa la [**funzione WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) per attendere il verificarsi di uno degli eventi. **WaitCommEvent** può essere usato in modo sincrono o come operazione sovrapposta. Per altre informazioni sull'esecuzione di una funzione come operazione sovrapposta, vedere [Sincronizzazione](/windows/desktop/Sync/synchronization).

Quando si verifica uno degli eventi specificati nella maschera eventi, il processo completa l'operazione di attesa e imposta una variabile della maschera di evento per indicare il tipo di evento rilevato. Se [**setCommMask viene**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) chiamato per una risorsa di comunicazione mentre è in sospeso un'attesa per tale risorsa, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) restituisce un errore.

La [**funzione WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) rileva gli eventi che si sono verificati dopo l'ultima chiamata a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) **o WaitCommEvent**. Ad esempio, se si specifica l'evento **\_ EV RXCHAR** come evento di attesa, una chiamata a **WaitCommEvent** verrà soddisfatta se sono presenti caratteri nel buffer di input del driver che sono arrivati dopo l'ultima chiamata a **WaitCommEvent** o **SetCommMask**. Di conseguenza, dato lo pseudocodice seguente, tutti i caratteri ricevuti tra T1 e T2 soddisferanno la chiamata successiva **a WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Quando si monitora un evento che si verifica quando un segnale (CTS, DSR e così via) cambia stato, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) segnala la modifica, ma non lo stato corrente. Per eseguire query sullo stato corrente dei segnali CTS (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect) e dell'indicatore circolare, un processo può usare la [**funzione GetCommModemStatus.**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)

 

 
