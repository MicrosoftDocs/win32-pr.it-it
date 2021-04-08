---
description: Un handle a una risorsa di comunicazione dispone di un set associato di parametri di timeout che influiscono sul comportamento delle operazioni di lettura e scrittura.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Timeout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db31fafc0f4d98832f1fb7fa5d22b32cba33d73
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748335"
---
# <a name="time-outs"></a>Timeout

Un handle a una risorsa di comunicazione dispone di un set associato di parametri di timeout che influiscono sul comportamento delle operazioni di lettura e scrittura. I timeout possono causare la conclusione di un'operazione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) quando scade un intervallo di timeout, anche se il numero di caratteri specificato non è stato letto o scritto. Non viene considerato un errore quando si verifica un timeout durante un'operazione di lettura o scrittura (ovvero il valore restituito della funzione di lettura o scrittura indica l'esito positivo). Il numero di byte effettivamente letti o scritti viene segnalato da **ReadFile** o **WriteFile** (o dalla funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**FileIOCompletionRoutine**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) , se l'i/o è stato eseguito come operazione sovrapposta).

Quando un'applicazione apre una risorsa di comunicazione, il sistema imposta i valori di timeout della risorsa sui valori in vigore quando la risorsa è stata usata per l'ultima volta. Se la risorsa di comunicazione non è mai stata aperta, il sistema imposta i valori di timeout su un valore predefinito. In entrambi i casi, un'applicazione deve sempre determinare i valori di timeout correnti dopo l'apertura della risorsa e quindi impostarli in modo esplicito per soddisfare i requisiti. Per determinare i valori di timeout correnti di una risorsa di comunicazione, usare la funzione [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) . Per modificare i valori di timeout, utilizzare la funzione [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) .

Due tipi di timeout sono abilitati dai parametri di timeout. Si verifica un timeout di intervallo quando il tempo che intercorre tra la ricezione di due caratteri è superiore a un numero specificato di millisecondi. L'intervallo di tempo inizia quando viene ricevuto il primo carattere e viene riavviato quando viene ricevuto ogni nuovo carattere. Si verifica un timeout totale quando la quantità totale di tempo utilizzata da un'operazione di lettura supera un numero calcolato di millisecondi. L'intervallo di tempo inizia immediatamente all'inizio dell'operazione di I/O. Le operazioni di scrittura supportano solo i timeout totali. Le operazioni di lettura supportano sia i timeout di intervallo che quelli totali, che possono essere usati separatamente o combinati.

Il tempo, in millisecondi, del periodo di timeout totale per un'operazione di lettura o scrittura viene calcolato usando il moltiplicatore e i valori costanti della struttura [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) specificata nella funzione [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) o [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) . Viene usata la formula seguente:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



L'utilizzo di un moltiplicatore e di una costante consente di variare il periodo di timeout totale, a seconda della quantità di dati richiesti. Un'applicazione può utilizzare solo la costante impostando il moltiplicatore su zero oppure utilizzare solo il moltiplicatore impostando la costante su zero. Se la costante e il moltiplicatore sono pari a zero, il timeout totale non viene utilizzato.

Se tutti i parametri di timeout di lettura sono pari a zero, i timeout di lettura non vengono usati e un'operazione di lettura non viene completata fino a quando non viene letto il numero di byte richiesto o si verifica un errore. Analogamente, se tutti i parametri di timeout di scrittura sono pari a zero, un'operazione di scrittura non viene completata fino a quando non viene scritto il numero di byte richiesto o si verifica un errore.

Se il parametro di timeout di lettura intervallo è il valore **MAXDWORD** ed entrambi i parametri di timeout di lettura totali sono pari a zero, un'operazione di lettura viene completata immediatamente dopo la lettura dei caratteri disponibili nel buffer di input, anche se è vuota.

Il tempo di intervallo forza la restituzione di un'operazione di lettura quando si verifica una pausa nella ricezione. Un processo che usa i timeout di intervallo può impostare un parametro di intervallo piuttosto breve, in modo che possa rispondere rapidamente a piccoli picchi isolati di uno o pochi caratteri, ma può comunque raccogliere buffer di grandi dimensioni di caratteri con una singola chiamata quando i dati vengono ricevuti in un flusso stabile.

I timeout per un'operazione di scrittura possono essere utili quando la trasmissione è bloccata da un tipo di controllo di flusso o quando è stata chiamata la funzione [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) per sospendere la trasmissione dei caratteri.

Nella tabella seguente viene riepilogato il comportamento delle operazioni di lettura in base ai valori specificati per i timeout totali e di intervallo.



| Totale | Interval | Comportamento                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Restituisce quando il buffer viene riempito completamente. I timeout non vengono usati.                                                                                                                    |
| T     | 0        | Restituisce quando il buffer viene riempito completamente o quando T millisecondi sono trascorsi dall'inizio dell'operazione.                                                                   |
| 0     | S        | Restituisce quando il buffer viene riempito completamente o quando sono trascorsi Y millisecondi tra la ricezione di due caratteri. L'intervallo di tempo non inizia fino a quando non viene ricevuto il primo carattere. |
| T     | S        | Restituisce quando il buffer viene riempito completamente o quando si verifica uno dei due tipi di timeout.                                                                                                     |



 

> [!Note]  
> Tuttavia, tale tempistica è relativa al sistema che controlla il dispositivo fisico. Per un dispositivo remoto, ad esempio un modem, la tempistica è relativa al sistema server a cui è collegato il modem. Eventuali ritardi di propagazione della rete non vengono calcolati in. Ad esempio, un'applicazione client può specificare un timeout totale calcolato per essere 500 millisecondi. Quando sono trascorsi 500 millisecondi sul server, al client viene restituito un errore di timeout. Se si verifica un ritardo di propagazione della rete di 50 millisecondi, il client non riceverà alcuna notifica del timeout fino a circa 50 millisecondi dopo il timeout effettivo.

 

> [!Note]  
> I parametri di timeout influiscono sul comportamento delle operazioni di lettura e scrittura sovrapposte in un dispositivo di comunicazione. Con I/O sovrapposti, la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) può restituire prima del completamento dell'operazione. I parametri di timeout possono determinare il momento in cui l'operazione è stata completata.

 

 

 
