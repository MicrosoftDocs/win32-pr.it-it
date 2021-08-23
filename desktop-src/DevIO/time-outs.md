---
description: A un handle per una risorsa di comunicazione è associato un set di parametri di timeout che influiscono sul comportamento delle operazioni di lettura e scrittura.
ms.assetid: 271d4c68-1f6d-4483-a9a1-703220de761f
title: Timeout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6226e8a2d13020bd4dc90a416e7ef359fbd919cf54e886c5e691e5fca2cdea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956790"
---
# <a name="time-outs"></a>Timeout

A un handle per una risorsa di comunicazione è associato un set di parametri di timeout che influiscono sul comportamento delle operazioni di lettura e scrittura. I timeout possono causare la conclusione di un'operazione [**ReadFile,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**ReadFileEx,**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) quando è trascorso un intervallo di timeout, anche se il numero specificato di caratteri non è stato letto o scritto. Non viene considerato un errore quando si verifica un timeout durante un'operazione di lettura o scrittura, ovvero il valore restituito della funzione di lettura o scrittura indica l'esito positivo. Il numero di byte effettivamente letti o scritti viene segnalato da **ReadFile** o **WriteFile** (o dalla [**funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**FileIOCompletionRoutine,**](/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine) se l'I/O è stato eseguito come operazione sovrapposta).

Quando un'applicazione apre una risorsa di comunicazione, il sistema imposta i valori di timeout della risorsa sui valori effettivi quando la risorsa è stata usata per l'ultima volta. Se la risorsa di comunicazione non è mai stata aperta, il sistema imposta i valori di timeout su un valore predefinito. In entrambi i casi, un'applicazione deve sempre determinare i valori di timeout correnti dopo l'apertura della risorsa e quindi impostarli in modo esplicito in modo che soddisfino i requisiti. Per determinare i valori di timeout correnti di una risorsa di comunicazione, usare la [**funzione GetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) Per modificare i valori di timeout, usare la [**funzione SetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)

Due tipi di timeout sono abilitati dai parametri di timeout. Un timeout di intervallo si verifica quando il tempo tra la ricezione di due caratteri qualsiasi supera un numero specificato di millisecondi. L'intervallo inizia quando viene ricevuto il primo carattere e viene riavviato quando viene ricevuto ogni nuovo carattere. Un timeout totale si verifica quando la quantità totale di tempo utilizzata da un'operazione di lettura supera un numero calcolato di millisecondi. La temporizzazione inizia immediatamente all'inizio dell'operazione di I/O. Le operazioni di scrittura supportano solo i timeout totali. Le operazioni di lettura supportano sia intervalli che timeout totali, che possono essere usati separatamente o combinati.

Il tempo, in millisecondi, del periodo di timeout totale per un'operazione di lettura o scrittura viene calcolato usando il moltiplicatore e i valori costanti della struttura [**COMMTIMEOUTS**](/windows/desktop/api/Winbase/ns-winbase-commtimeouts) specificata nella [**funzione GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts) o [**SetCommTimeouts.**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts) Viene usata la formula seguente:


```C++
Timeout = (MULTIPLIER * number_of_bytes) + CONSTANT
```



L'uso di un moltiplicatore e di una costante consente di variare il periodo di timeout totale, a seconda della quantità di dati richiesti. Un'applicazione può usare solo la costante impostando il moltiplicatore su zero oppure solo il moltiplicatore impostando la costante su zero. Se la costante e il moltiplicatore sono pari a zero, il timeout totale non viene usato.

Se tutti i parametri di timeout di lettura sono pari a zero, i timeout di lettura non vengono usati e un'operazione di lettura non viene completata fino a quando non viene letto il numero richiesto di byte o non si verifica un errore. Analogamente, se tutti i parametri di timeout di scrittura sono pari a zero, un'operazione di scrittura non viene completata fino a quando non viene scritto il numero richiesto di byte o non si verifica un errore.

Se il parametro di timeout dell'intervallo di lettura è il valore **MAXDWORD** ed entrambi i parametri di timeout totali di lettura sono pari a zero, un'operazione di lettura viene completata immediatamente dopo la lettura dei caratteri disponibili nel buffer di input, anche se è vuoto.

L'intervallo di tempo forza la restituzione di un'operazione di lettura in caso di interruzione della ricezione. Un processo che usa timeout di intervallo può impostare un parametro di intervallo piuttosto breve, in modo che possa rispondere rapidamente a piccoli burst isolati di uno o pochi caratteri, ma può comunque raccogliere grandi buffer di caratteri con una singola chiamata quando i dati vengono ricevuti in un flusso costante.

I timeout per un'operazione di scrittura possono essere utili quando la trasmissione è bloccata da un tipo di controllo di flusso o quando la [**funzione SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) è stata chiamata per sospendere la trasmissione dei caratteri.

Nella tabella seguente viene riepilogato il comportamento delle operazioni di lettura in base ai valori specificati per i timeout totali e di intervallo.



| Totale | Intervallo | Comportamento                                                                                                                                                                                 |
|-------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | 0        | Restituisce quando il buffer è completamente pieno. I timeout non vengono usati.                                                                                                                    |
| T     | 0        | Restituisce quando il buffer è completamente pieno o quando sono trascorsi millisecondi T dall'inizio dell'operazione.                                                                   |
| 0     | S        | Restituisce quando il buffer è completamente riempito o quando sono trascorsi millisecondi Y tra la ricezione di due caratteri qualsiasi. L'intervallo non inizia fino a quando non viene ricevuto il primo carattere. |
| T     | S        | Restituisce quando il buffer è completamente pieno o quando si verifica uno dei due tipi di timeout.                                                                                                     |



 

> [!Note]  
> Tale intervallo è tuttavia relativo al sistema che controlla il dispositivo fisico. Per un dispositivo remoto, ad esempio un modem, l'intervallo è relativo al sistema server a cui è collegato il modem. Non viene fattoriato alcun ritardo di propagazione della rete. Ad esempio, un'applicazione client potrebbe specificare un timeout totale che calcola un valore di 500 millisecondi. Quando sono trascorsi 500 millisecondi nel server, al client viene restituito un errore di timeout. Se si verifica un ritardo di propagazione della rete di 50 millisecondi, il client non riceverà una notifica del timeout fino a circa 50 millisecondi dopo il timeout effettivamente verificatosi.

 

> [!Note]  
> I parametri di timeout influiscono sul comportamento delle operazioni di lettura e scrittura sovrapposte in un dispositivo di comunicazione. Con l'I/O sovrapposto, la funzione [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)o [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) può restituire prima del completamento dell'operazione. I parametri di timeout possono determinare quando l'operazione è stata completata.

 

 

 
