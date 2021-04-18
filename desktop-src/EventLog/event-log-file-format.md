---
description: Ogni registro eventi contiene un'intestazione, rappresentata dalla struttura dell'intestazione del file di log ELF, \_ \_ che ha una dimensione fissa, seguita da un numero variabile di record di eventi, rappresentati da strutture EVENTLOGRECORD, e da un record di fine del file (rappresentato dalla \_ struttura dei record Elf EOF \_ ).
ms.assetid: 2b62b807-4ffd-4a8f-afe4-34e109d01856
title: Formato file registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4ba5c8bc0114e319107272e706801544e3effa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528752"
---
# <a name="event-log-file-format"></a>Formato file registro eventi

Ogni registro eventi contiene un'intestazione, rappresentata dalla struttura dell' [**\_ \_ intestazione del file di log Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) , che ha una dimensione fissa, seguita da un numero variabile di record di eventi, rappresentati da strutture [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) , e da un record di fine del file (rappresentato dalla struttura dei [**\_ \_ record Elf EOF**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).

La struttura dell' **\_ \_ intestazione Logfile di Elf** e la struttura dei **\_ \_ record Elf EOF** vengono scritte nel registro eventi quando il registro eventi viene creato e vengono aggiornati ogni volta che un evento viene scritto nel log.

Quando un'applicazione chiama la funzione [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) per scrivere una voce nel registro eventi, il sistema passa i parametri al servizio di registrazione eventi. Il servizio di registrazione eventi utilizza le informazioni per scrivere una struttura **EVENTLOGRECORD** nel registro eventi. La figura seguente illustra questo processo.

![scrittura di un file di log](images/evreport.png)

I record degli eventi sono organizzati in uno dei modi seguenti:

-   Non wrapping. Il record meno recente si trova subito dopo l'intestazione del log eventi e i nuovi record vengono aggiunti dopo l'ultimo record aggiunto (prima del **\_ \_ record Elf EOF**). Nell'esempio seguente viene illustrato il metodo di non wrapping:

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    Il mancato ritorno a capo può verificarsi quando viene creato il log eventi o quando viene cancellato il registro eventi. Il registro eventi continua a non essere incapsulato fino a quando non viene raggiunto il limite di dimensioni del registro eventi. Le dimensioni del registro eventi sono limitate dal valore di configurazione **MaxSize** o dalla quantità di risorse di sistema.

    Quando viene raggiunto il limite di dimensioni del registro eventi, potrebbe iniziare a eseguire il wrapping. Il wrapping è controllato dal valore di configurazione di **conservazione** . Per ulteriori informazioni sui valori di configurazione del registro eventi, vedere [EventLog Key](eventlog-key.md).

-   Avvolgimento. I record sono organizzati come buffer circolare. Quando vengono aggiunti nuovi record, i record meno recenti vengono sostituiti. La posizione dei record meno recenti e più recenti può variare. Nell'esempio seguente viene illustrato il metodo di wrapping.

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

    Esiste uno spazio tra il **record Elf \_ EOF \_** e il record meno recente, perché il sistema cancellerà un numero integrale di record per liberare spazio per il record più recente. Se, ad esempio, il record più recente è di 100 byte e i due record meno recenti sono di 75 byte, i due record meno recenti verranno rimossi dal sistema. I 50 byte aggiuntivi verranno utilizzati in un secondo momento, quando verranno scritti nuovi record.

    Un file di registro eventi ha una dimensione fissa e quando i record nel file sono a capo, il record alla fine del file viene in genere suddiviso in due record. Se, ad esempio, la posizione per la scrittura successiva è 100 byte alla fine del file e la dimensione del record è 300 byte, i primi 100 byte verranno scritti alla fine del file e i successivi 200 byte verranno scritti all'inizio del file immediatamente dopo l' **\_ \_ intestazione di logfile Elf**. Se lo spazio disponibile alla fine del file è inferiore alla parte fissa di **EVENTLOGRECORD** (0x38 bytes), tutto il nuovo record verrà scritto all'inizio del file immediatamente dopo l' **\_ \_ intestazione di logfile Elf**. I byte non utilizzati alla fine del file verranno riempiti con il modello 0x00000027.

Per ulteriori informazioni e un esempio di codice, vedere [segnalazione di un evento](reporting-an-event.md).

 

 
