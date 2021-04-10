---
description: Un processo può monitorare un set di eventi che si verificano in una risorsa di comunicazione. Ad esempio, un'applicazione può usare il monitoraggio degli eventi per determinare quando i segnali CTS (Clear-to-Send) e DSR (Data-Set-Ready) cambiano lo stato.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventi di comunicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126804"
---
# <a name="communications-events"></a>Eventi di comunicazione

Un processo può monitorare un set di eventi che si verificano in una risorsa di comunicazione. Ad esempio, un'applicazione può usare il monitoraggio degli eventi per determinare quando i segnali CTS (Clear-to-Send) e DSR (Data-Set-Ready) cambiano lo stato.

Un processo può monitorare gli eventi in una determinata risorsa di comunicazione usando la funzione [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) per creare una maschera di eventi. Per determinare la maschera eventi corrente per una risorsa di comunicazione, un processo può usare la funzione [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) . I valori seguenti specificano gli eventi che possono essere monitorati.



| Valore           | Significato                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_Interrompi EV**   | È stata rilevata un'interruzione nell'input.                                                                                                                                                                                                                    |
| **\_CTS EV**     | Il segnale CTS (Clear-to-Send) ha modificato lo stato.                                                                                                                                                                                                     |
| **\_DSR EV**     | Lo stato del segnale DSR (Data-Set-Ready) è stato modificato.                                                                                                                                                                                                    |
| **\_errore EV**     | Si è verificato un errore di stato della riga. Gli errori di stato della riga sono **\_ Frame CE**, **\_ sovraccarico CE** e **CE \_ RXPARITY**.                                                                                                                                        |
| **\_anello EV**    | È stato rilevato un indicatore sonoro.                                                                                                                                                                                                                    |
| **\_RISD EV**    | Lo stato del segnale RISD (Receive-Line-Signal-Detect) è stato modificato.                                                                                                                                                                                       |
| **\_RXCHAR EV**  | È stato ricevuto un carattere ed è stato collocato nel buffer di input.                                                                                                                                                                                          |
| **\_RXFLAG EV**  | Il carattere evento è stato ricevuto e inserito nel buffer di input. Il carattere evento viene specificato nella struttura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) del dispositivo, che viene applicata a una porta seriale tramite la funzione [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) . |
| **\_TXEMPTY EV** | L'ultimo carattere nel buffer di output è stato inviato.                                                                                                                                                                                                 |



 

Dopo che è stato specificato un set di eventi, un processo usa la funzione [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) per attendere che si verifichi uno degli eventi. **WaitCommEvent** può essere utilizzato in modo sincrono o come operazione sovrapposta. Per ulteriori informazioni sull'esecuzione di una funzione come operazione sovrapposta, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).

Quando si verifica uno degli eventi specificati nella maschera di eventi, il processo completa l'operazione di attesa e imposta una variabile event mask per indicare il tipo di evento rilevato. Se [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) viene chiamato per una risorsa di comunicazione mentre è in sospeso un'attesa per tale risorsa, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) restituisce un errore.

La funzione [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) rileva gli eventi che si sono verificati dopo l'ultima chiamata a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) o **WaitCommEvent**. Se, ad esempio, si specifica l'evento **EV \_ RXCHAR** come evento di soddisfazione dell'attesa, verrà soddisfatta una chiamata a **WaitCommEvent** se sono presenti caratteri nel buffer di input del driver che sono arrivati dall'ultima chiamata a **WaitCommEvent** o **SetCommMask**. Pertanto, data la seguente pseudocodice, qualsiasi carattere ricevuto tra T1 e T2 soddisferà la chiamata successiva a **WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Quando si esegue il monitoraggio di un evento che si verifica quando un segnale (CTS, DSR e così via) cambia stato, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) segnala la modifica, ma non lo stato corrente. Per eseguire una query sullo stato corrente dei segnali CTS (Clear-to-Send), DSR (set di dati-Ready), RISD (Receive-Line-Signal-Detect) e indicatore Ring, un processo può usare la funzione [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) .

 

 
