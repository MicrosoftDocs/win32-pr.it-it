---
description: Ogni log eventi contiene un'intestazione (rappresentata dalla struttura ELF LOGFILE HEADER) con dimensioni fisse, seguite da un numero variabile di record di eventi (rappresentati dalle strutture EVENTLOGRECORD) e un record di fine file (rappresentato dalla struttura \_ \_ \_ ELF EOF \_ RECORD).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato del file di log eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ed6df35ac1fcd641a9a895b2c32eb34d6a4c1cb472ab03f16417f55900c767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117814294"
---
# <a name="event-log-file-format"></a>Formato del file di log eventi

Ogni log eventi contiene un'intestazione (rappresentata dalla struttura [**ELF \_ LOGFILE \_ HEADER)**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) con dimensioni fisse, seguite da un numero variabile di record di eventi (rappresentati dalle [**strutture EVENTLOGRECORD)**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) e un record di fine file (rappresentato dalla struttura [**\_ ELF EOF \_ RECORD).**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85))

La **struttura ELF \_ LOGFILE \_ HEADER** e la struttura **\_ ELF EOF \_ RECORD** vengono scritte nel registro eventi quando il registro eventi viene creato e aggiornato ogni volta che viene scritto un evento nel log.

Quando un'applicazione chiama la [**funzione ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) per scrivere una voce nel log eventi, il sistema passa i parametri al servizio di registrazione eventi. Il servizio di registrazione eventi usa le informazioni per scrivere **una struttura EVENTLOGRECORD** nel registro eventi. La figura seguente illustra questo processo.

![scrittura di un file di log](images/evreport.png)

I record degli eventi sono organizzati in uno dei modi seguenti:

-   Senza ritorno a capo. Il record meno recente si trova immediatamente dopo l'intestazione del log eventi e vengono aggiunti nuovi record dopo l'ultimo record aggiunto (prima di **\_ ELF EOF \_ RECORD**). Nell'esempio seguente viene illustrato il metodo senza ritorno a capo:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    Il wrapping può verificarsi quando viene creato il registro eventi o quando il registro eventi viene cancellato. Il registro eventi continua a non eseguire il wrapping finché non viene raggiunto il limite di dimensioni del registro eventi. Le dimensioni del registro eventi sono limitate dal valore **di configurazione MaxSize** o dalla quantità di risorse di sistema.

    Quando viene raggiunto il limite di dimensioni del registro eventi, potrebbe iniziare a eseguire il wrapping. Il wrapping è controllato dal **valore di configurazione Retention.** Per altre informazioni sui valori di configurazione del registro eventi, vedere [Eventlog Key](eventlog-key.md).

-   Avvolgimento. I record sono organizzati come buffer circolare. Quando vengono aggiunti nuovi record, i record meno recenti vengono sostituiti. La posizione dei record meno recenti e meno recenti varia. Nell'esempio seguente viene illustrato il metodo di wrapping.

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    EVENT RECORD 301         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 400         (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    Wasted space
    EVENT RECORD 102         (EVENTLOGRECORD)
    EVENT RECORD 103         (EVENTLOGRECORD)
    .
    .
    .
    EVENT RECORD 299         (EVENTLOGRECORD)
    Part of EVENT RECORD 300 (EVENTLOGRECORD)
    ```

    Nell'esempio il record meno recente non è più 1, ma è 102 perché lo spazio per i record da 1 a 101 è stato sovrascritto.

    C'è spazio tra **il \_ record ELF EOF \_ e** il record meno recente perché il sistema cancellerà un numero integrale di record per liberare spazio per il record più recente. Ad esempio, se il record più recente è lungo 100 byte e i due record meno recenti hanno una lunghezza di 75 byte, il sistema rimuoverà i due record meno recenti. I 50 byte aggiuntivi verranno usati in un secondo momento quando vengono scritti nuovi record.

    Un file di log eventi ha dimensioni fisse e quando i record nel file vengono a capo, il record alla fine del file verrà in genere suddiviso in due record. Ad esempio, se la posizione per la scrittura successiva è a 100 byte dalla fine del file e le dimensioni del record sono 300 byte, i primi 100 byte verranno scritti alla fine del file e i successivi 200 byte verranno scritti all'inizio del file immediatamente dopo **l'intestazione LOGFILE ELF \_ \_**. Se lo spazio disponibile alla fine del file è minore della parte fissa di **EVENTLOGRECORD** (0x38 byte), tutti i nuovi record verranno scritti all'inizio del file immediatamente dopo **eLF \_ LOGFILE \_ HEADER**. I byte inutilizzati alla fine del file verranno riempiti con il modello 0x00000027.

Per altre informazioni e un esempio di codice, vedere [Creazione di report su un evento](reporting-an-event.md).

 

 
