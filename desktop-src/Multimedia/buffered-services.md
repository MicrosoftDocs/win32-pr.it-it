---
title: Servizi memorizzati nel buffer
description: Servizi memorizzati nel buffer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- I/O di file multimediali, servizi memorizzati nel buffer
- I/O di file, servizi memorizzati nel buffer
- input e output (I/O),servizi memorizzati nel buffer
- I/O (input e output),servizi memorizzati nel buffer
- I/O memorizzato nel buffer
- Funzione mmioOpen
- buffer I/O interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f8e7c11dbc90f7090bc8fcee114ebfac79f9bd54d834203f4b8e7bf893f591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989379"
---
# <a name="buffered-services"></a>Servizi memorizzati nel buffer

La maggior parte del sovraccarico nell'I/O dei file si verifica quando si accede al dispositivo multimediale. Se si stanno leggendo o scrivendo molti piccoli blocchi di informazioni, il dispositivo può dedicare molto tempo al passaggio alla posizione fisica sul supporto per ogni operazione di lettura o scrittura. In questo caso, è possibile ottenere prestazioni migliori usando i servizi di I/O di file memorizzati nel buffer. Con l'I/O memorizzato nel buffer, gestione I/O dei file mantiene un buffer intermedio più grande dei blocchi di informazioni che si stanno leggendo o scrivendo. Accede al dispositivo solo quando il buffer deve essere riempito o scritto sul disco.

Prima di impostare e usare l'I/O di file memorizzato nel buffer, è necessario decidere se si vuole che il buffer venga allocato da Gestione I/O del file o dall'applicazione. È più semplice consentire al gestore di I/O di file di allocare il buffer. Tuttavia, è possibile consentire all'applicazione di allocare il buffer se si vuole accedere direttamente al buffer o aprire un file di memoria. Per altre informazioni sull'uso dei file di memoria, vedere [Esecuzione di I/O di file di memoria.](performing-memory-file-i-o.md) Per un esempio di accesso diretto a un buffer di I/O, vedere Accesso a un buffer [di I/O di file](accessing-a-file-i-o-buffer.md)

Un buffer allocato dal gestore di I/O dei file viene chiamato buffer di I/O interno. Per aprire un file per l'I/O memorizzato nel buffer usando un buffer interno, specificare il flag MMIO ALLOCBUF quando si apre il file con la funzione \_ [**mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Nella figura seguente viene illustrato lo stato iniziale del buffer di I/O del file dopo l'apertura di un file per un'operazione di lettura memorizzata nel buffer. La memorizzazione nel buffer è trasparente. Le operazioni di lettura e ricerca vengono lette e ricercate come se si usa un I/O senza buffer. La **funzione mmioOpen** ha impostato pchNext e *pchEndRead* in modo che puntino all'inizio del buffer di I/O del file.

![Screenshot che mostra 'pchEndRead' e 'pchNext' che puntano all'inizio del buffer di I/O file.](images/mmio7.gif)

Nella figura seguente viene illustrato lo stato iniziale del buffer di I/O del file dopo l'apertura di un file per un'operazione di scrittura memorizzata nel buffer. La **funzione mmioOpen** ha impostato **pchNext** in modo che punti all'inizio del buffer di I/O del file e **pchEndWrite** in modo che punti alla fine del buffer.

![Screenshot che mostra "pchNext" all'inizio del buffer di I/O file e "pchEndWrite" alla fine.](images/mmio11.gif)

La dimensione predefinita del buffer di I/O interno è 8K. Se queste dimensioni non sono adeguate, è possibile usare la funzione [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) per modificare le dimensioni del buffer. È anche possibile usare questa funzione per abilitare il buffering in un file aperto per I/O senza buffer o per fornire un buffer personalizzato da usare come file di memoria.

È possibile forzare la scrittura su disco del contenuto di un buffer di I/O usando la [**funzione mmioFlush.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) Tuttavia, quando si chiude un file usando la funzione [**mmioClose,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) non è necessario chiamare **mmioFlush** per scaricare un buffer di I/O. La funzione **mmioClose** lo scarica automaticamente. Se lo spazio su disco è insufficiente, **mmioFlush** potrebbe non riuscire, anche se le chiamate precedenti alla funzione [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) hanno avuto esito positivo. Analogamente, **mmioClose potrebbe** non riuscire quando scarica il buffer di I/O.

Le applicazioni sensibili alle prestazioni, ad esempio quelle che tras streaming dei dati in tempo reale da un CD-ROM, possono ottimizzare le prestazioni di I/O dei file accedendo direttamente al buffer di I/O. È necessario prestare attenzione se si sceglie di eseguire questa operazione, perché si ignorano alcune misure di sicurezza e il controllo degli errori forniti da Gestione I/O dei file.

Gestione I/O dei file multimediali usa la [**struttura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) per gestire le informazioni sullo stato di un file aperto. In questa struttura si usano tre membri per leggere e scrivere il buffer di I/O: **pchNext**, **pchEndRead** e **pchEndWrite**. Il **membro pchNext** punta alla posizione successiva nel buffer da leggere o scrivere. È necessario incrementare questo membro durante la lettura e la scrittura del buffer. Il **membro pchEndRead** identifica l'ultimo carattere valido che è possibile leggere dal buffer. Analogamente, questo membro identifica l'ultima posizione nel buffer che è possibile scrivere. Più precisamente, **pchEndRead** e **pchEndWrite** puntano alla posizione di memoria che segue gli ultimi dati validi nel buffer. Usare le [**funzioni mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) e [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) per recuperare e impostare le informazioni sullo stato relative al buffer di I/O del file. Nella figura seguente viene illustrato lo stato del buffer di I/O dopo che l'applicazione ha chiamato **mmioAdvance durante** un'operazione di lettura. La **funzione mmioAdvance** riempie il buffer e imposta il puntatore **pchEndRead** alla fine del buffer.

![Screenshot che mostra "pchNext" all'inizio del buffer di I/O file e "pchEndRead" alla fine.](images/mmio8.gif)

Nella figura seguente l'applicazione legge dal buffer di I/O nella posizione specificata da **pchNext** e fa avanzare il puntatore.

![Screenshot che mostra "pchNext" al centro del buffer di I/O dei file e "pchEndRead" alla fine.](images/mmio9.gif)

Analogamente, per un'operazione di scrittura, l'applicazione scrive nel buffer di I/O e fa avanzare il puntatore **pchNext,** come illustrato nella figura seguente.

![Screenshot che mostra "pchNext" al centro del buffer di I/O dei file e "pchEndWrite" alla fine.](images/mmio12.gif)

Dopo che l'applicazione ha riempito il buffer, chiama **mmioAdvance** per scaricare il buffer su disco. La **funzione mmioAdvance** reimposta **pchNext** in modo che punti all'inizio del buffer, come illustrato nella figura seguente.

![Screenshot che mostra "pchNext" all'inizio del buffer di I/O file, il buffer al centro di E O F e "pchEndWrite" alla fine del buffer.](images/mmio13.gif)

Quando si raggiunge la fine del buffer di I/O, è necessario far avanzare il buffer per riempirlo dal disco, se si sta leggendo, o scaricarlo sul disco, se si sta scrivendo. Usare la [**funzione mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) per far avanzare un buffer di I/O. Per riempire un buffer di I/O dal disco, **usare mmioAdvance** con il flag MMIO \_ READ. Se il file non contiene dati sufficienti per riempire il buffer, il membro **pchEndRead** della struttura **MMIOINFO** punta alla posizione dopo l'ultimo byte valido nel buffer. Per scaricare un buffer su disco, impostare il flag MMIO DIRTY nel membro \_ **dwFlags** della **struttura MMIOINFO** e quindi chiamare **mmioAdvance** con il flag MMIO \_ WRITE.

Ad esempio, durante un'operazione di lettura, la funzione **mmioAdvance** imposta **pchEndRead** in modo che punti alla fine dei dati validi nel buffer, come illustrato nella figura seguente.

![Screenshot che mostra "pchNext" all'inizio del buffer di I/O file, il buffer alla fine di E O F e "pchEndRead" alla fine del buffer.](images/mmio10.gif)

Analogamente, durante un'operazione di scrittura, l'applicazione chiama **mmioAdvance** per scaricare il buffer e far avanzare **pchNext** alla fine dei dati validi nel buffer, come illustrato nella figura seguente.

![immagine del buffer di i/o file](images/mmio14.gif)

 

 