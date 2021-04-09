---
title: Servizi memorizzati nel buffer
description: Servizi memorizzati nel buffer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- I/O di file multimediali, servizi memorizzati nel buffer
- I/O di file, servizi memorizzati nel buffer
- input e output (I/O), servizi memorizzati nel buffer
- I/O (input e output), servizi memorizzati nel buffer
- I/O memorizzato nel buffer
- mmioOpen (funzione)
- buffer I/O interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103968799"
---
# <a name="buffered-services"></a>Servizi memorizzati nel buffer

La maggior parte del sovraccarico nell'I/O dei file si verifica quando si accede al dispositivo multimediale. Se si stanno leggendo o scrivendo molti piccoli blocchi di informazioni, il dispositivo può dedicare molto tempo al passaggio alla posizione fisica sui supporti per ogni operazione di lettura o scrittura. In questo caso, è possibile ottenere prestazioni migliori usando I servizi di I/O dei file memorizzati nel buffer. Con l'I/O memorizzato nel buffer, il gestore di I/O dei file mantiene un buffer intermedio maggiore dei blocchi di informazioni che vengono letti o scritti. Accede al dispositivo solo quando il buffer deve essere compilato o scritto sul disco.

Prima di configurare e utilizzare l'I/O dei file memorizzati nel buffer, è necessario decidere se si desidera che l'applicazione o l'allocazione del buffer da parte di gestione i/O file. È più semplice consentire al gestore di I/O dei file di allocare il buffer. Tuttavia, è possibile consentire all'applicazione di allocare il buffer se si desidera accedere direttamente al buffer o aprire un file di memoria. Per ulteriori informazioni sull'utilizzo dei file di memoria, vedere [esecuzione di operazioni di i/O su file di memoria](performing-memory-file-i-o.md). Per un esempio di accesso diretto a un buffer di I/O, vedere [accesso a un buffer di i/o di file](accessing-a-file-i-o-buffer.md)

Un buffer allocato dal gestore di I/O dei file è denominato buffer di I/O interno. Per aprire un file per l'I/O memorizzato nel buffer usando un buffer interno, specificare il \_ flag MMIO ALLOCBUF quando si apre il file con la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Nella figura seguente viene illustrato lo stato iniziale del buffer di I/O dei file dopo l'apertura di un file per un'operazione di lettura memorizzata nel buffer. Il buffering è trasparente: è possibile leggere e cercare come se si stesse usando l'I/O non memorizzato nel buffer. La funzione **mmioOpen** ha impostato PchNext e *pchEndRead* in modo che punti all'inizio del buffer di i/O del file.

![Screenshot che mostra "pchEndRead" e "pchNext" che punta all'inizio del buffer di I/O del file.](images/mmio7.gif)

Nella figura seguente viene illustrato lo stato iniziale del buffer di I/O dei file dopo l'apertura di un file per un'operazione di scrittura nel buffer. La funzione **mmioOpen** ha impostato **pchNext** in modo che punti all'inizio del buffer di i/O dei file e **pchEndWrite** per puntare alla fine del buffer.

![Screenshot che mostra ' pchNext ' all'inizio del buffer di I/O dei file è pchEndWrite ' alla fine.](images/mmio11.gif)

Le dimensioni predefinite del buffer di I/O interno sono pari a 8 KB. Se questa dimensione non è adeguata, è possibile usare la funzione [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) per modificare la dimensione del buffer. È anche possibile usare questa funzione per abilitare il buffering su un file aperto per I/O senza buffer o per fornire un buffer personalizzato da usare come file di memoria.

È possibile forzare la scrittura su disco del contenuto di un buffer di I/O tramite la funzione [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) . Tuttavia, quando si chiude un file usando la funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , non è necessario chiamare **mmioFlush** per scaricare un buffer di I/O, la funzione **mmioClose** lo scarica automaticamente. Se lo spazio su disco è esaurito, **mmioFlush** potrebbe avere esito negativo, anche se le chiamate precedenti alla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) sono state completate. Analogamente, **mmioClose** potrebbe non riuscire a eseguire lo scaricamento del buffer di i/O.

Le applicazioni che sono sensibili alle prestazioni, ad esempio quelle che inviano dati in tempo reale da un CD-ROM, possono ottimizzare le prestazioni di I/O dei file accedendo direttamente al buffer di I/O. È necessario prestare attenzione se si sceglie di eseguire questa operazione, perché si ignorano alcune delle misure di sicurezza e il controllo degli errori forniti dal gestore di I/O file.

Il gestore di I/O dei file multimediali usa la struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) per mantenere le informazioni sullo stato di un file aperto. Si utilizzano tre membri in questa struttura per leggere e scrivere il buffer di I/O: **pchNext**, **pchEndRead** e **pchEndWrite**. Il membro **pchNext** punta alla posizione successiva nel buffer per la lettura o la scrittura. È necessario incrementare questo membro durante la lettura e la scrittura del buffer. Il membro **pchEndRead** identifica l'ultimo carattere valido che è possibile leggere dal buffer. Analogamente, questo membro identifica l'ultima posizione nel buffer che è possibile scrivere. Più precisamente, **pchEndRead** e **pchEndWrite** puntano alla posizione di memoria che segue gli ultimi dati validi nel buffer. Usare le funzioni [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) e [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) per recuperare e impostare le informazioni sullo stato relative al buffer di i/O dei file. Nella figura seguente viene illustrato lo stato del buffer di I/O dopo che l'applicazione chiama **mmioAdvance** durante un'operazione di lettura. La funzione **mmioAdvance** riempie il buffer e imposta il puntatore **pchEndRead** alla fine del buffer.

![Screenshot che mostra ' pchNext ' all'inizio del buffer di I/O dei file è pchEndRead ' alla fine.](images/mmio8.gif)

Nella figura seguente l'applicazione legge dal buffer di I/O nella posizione specificata da **pchNext** e fa avanzare il puntatore.

![Screenshot che mostra ' pchNext ' al centro del buffer di I/O dei file è pchEndRead ' alla fine.](images/mmio9.gif)

Analogamente, per un'operazione di scrittura, l'applicazione scrive nel buffer di I/O e sposta in avanti il puntatore **pchNext** , come illustrato nella figura seguente.

![Screenshot che mostra ' pchNext ' al centro del buffer di I/O dei file è pchEndWrite ' alla fine.](images/mmio12.gif)

Dopo che l'applicazione riempie il buffer, chiama **mmioAdvance** per svuotare il buffer su disco. La funzione **mmioAdvance** Reimposta **pchNext** in modo che punti all'inizio del buffer, come illustrato nella figura seguente.

![Screenshot che mostra ' pchNext ' all'inizio del buffer di I/O dei file, il buffer al centro di E O F è pchEndWrite ' alla fine del buffer.](images/mmio13.gif)

Quando si raggiunge la fine del buffer di I/O, è necessario far avanzare il buffer per riempirlo dal disco, se si sta leggendo o scaricarlo sul disco, se si sta scrivendo. Utilizzare la funzione [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) per avanzare un buffer di I/O. Per riempire un buffer di I/O dal disco, usare **mmioAdvance** con il \_ flag di lettura MMIO. Se il file non contiene dati sufficienti per riempire il buffer, il membro **pchEndRead** della struttura **MMIOINFO** punta alla posizione successiva all'ultimo byte valido nel buffer. Per svuotare un buffer su disco, impostare il \_ flag MMIO Dirty nel membro **dwFlags** della struttura **MMIOINFO** e quindi chiamare **mmioAdvance** con il flag MMIO \_ Write.

Durante un'operazione di lettura, ad esempio, la funzione **mmioAdvance** imposta **pchEndRead** in modo che punti alla fine dei dati validi nel buffer, come illustrato nella figura seguente.

![Screenshot che mostra ' pchNext ' all'inizio del buffer di I/O dei file, il buffer alla fine di E O F è pchEndRead ' alla fine del buffer.](images/mmio10.gif)

Analogamente, durante un'operazione di scrittura, l'applicazione chiama **mmioAdvance** per svuotare il buffer e avanzare **pchNext** alla fine dei dati validi nel buffer, come illustrato nella figura seguente.

![immagine del buffer di i/o dei file](images/mmio14.gif)

 

 