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
# <a name="event-log-file-format"></a><span data-ttu-id="1305f-103">Formato file registro eventi</span><span class="sxs-lookup"><span data-stu-id="1305f-103">Event Log File Format</span></span>

<span data-ttu-id="1305f-104">Ogni registro eventi contiene un'intestazione, rappresentata dalla struttura dell' [**\_ \_ intestazione del file di log Elf**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) , che ha una dimensione fissa, seguita da un numero variabile di record di eventi, rappresentati da strutture [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) , e da un record di fine del file (rappresentato dalla struttura dei [**\_ \_ record Elf EOF**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) ).</span><span class="sxs-lookup"><span data-stu-id="1305f-104">Each event log contains a header (represented by the [**ELF\_LOGFILE\_HEADER**](/previous-versions/windows/desktop/legacy/bb309024(v=vs.85)) structure) that has a fixed size, followed by a variable number of event records (represented by [**EVENTLOGRECORD**](/windows/desktop/api/winnt/ns-winnt-eventlogrecord) structures), and an end-of-file record (represented by the [**ELF\_EOF\_RECORD**](/previous-versions/windows/desktop/legacy/bb309022(v=vs.85)) structure).</span></span>

<span data-ttu-id="1305f-105">La struttura dell' **\_ \_ intestazione Logfile di Elf** e la struttura dei **\_ \_ record Elf EOF** vengono scritte nel registro eventi quando il registro eventi viene creato e vengono aggiornati ogni volta che un evento viene scritto nel log.</span><span class="sxs-lookup"><span data-stu-id="1305f-105">The **ELF\_LOGFILE\_HEADER** structure and the **ELF\_EOF\_RECORD** structure are written in the event log when the event log is created and are updated each time an event is written to the log.</span></span>

<span data-ttu-id="1305f-106">Quando un'applicazione chiama la funzione [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) per scrivere una voce nel registro eventi, il sistema passa i parametri al servizio di registrazione eventi.</span><span class="sxs-lookup"><span data-stu-id="1305f-106">When an application calls the [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) function to write an entry to the event log, the system passes the parameters to the event-logging service.</span></span> <span data-ttu-id="1305f-107">Il servizio di registrazione eventi utilizza le informazioni per scrivere una struttura **EVENTLOGRECORD** nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="1305f-107">The event-logging service uses the information to write an **EVENTLOGRECORD** structure to the event log.</span></span> <span data-ttu-id="1305f-108">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="1305f-108">The following diagram illustrates this process.</span></span>

![scrittura di un file di log](images/evreport.png)

<span data-ttu-id="1305f-110">I record degli eventi sono organizzati in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1305f-110">The event records are organized in one of the following ways:</span></span>

-   <span data-ttu-id="1305f-111">Non wrapping.</span><span class="sxs-lookup"><span data-stu-id="1305f-111">Non-wrapping.</span></span> <span data-ttu-id="1305f-112">Il record meno recente si trova subito dopo l'intestazione del log eventi e i nuovi record vengono aggiunti dopo l'ultimo record aggiunto (prima del **\_ \_ record Elf EOF**).</span><span class="sxs-lookup"><span data-stu-id="1305f-112">The oldest record is immediately after the event log header and new records are added after the last record that was added (before the **ELF\_EOF\_RECORD**).</span></span> <span data-ttu-id="1305f-113">Nell'esempio seguente viene illustrato il metodo di non wrapping:</span><span class="sxs-lookup"><span data-stu-id="1305f-113">The following example shows the non-wrapping method:</span></span>

    ``` syntax
    HEADER                   (ELF_LOGFILE_HEADER)
    EVENT RECORD 1           (EVENTLOGRECORD)
    EVENT RECORD 2           (EVENTLOGRECORD)
    EOF RECORD               (ELF_EOF_RECORD)
    ```

    <span data-ttu-id="1305f-114">Il mancato ritorno a capo può verificarsi quando viene creato il log eventi o quando viene cancellato il registro eventi.</span><span class="sxs-lookup"><span data-stu-id="1305f-114">Non-wrapping can occur when the event log is created or when the event log is cleared.</span></span> <span data-ttu-id="1305f-115">Il registro eventi continua a non essere incapsulato fino a quando non viene raggiunto il limite di dimensioni del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="1305f-115">The event log continues to be non-wrapping until the event log size limit is reached.</span></span> <span data-ttu-id="1305f-116">Le dimensioni del registro eventi sono limitate dal valore di configurazione **MaxSize** o dalla quantità di risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="1305f-116">The event log size is limited by either the **MaxSize** configuration value or the amount of system resources.</span></span>

    <span data-ttu-id="1305f-117">Quando viene raggiunto il limite di dimensioni del registro eventi, potrebbe iniziare a eseguire il wrapping.</span><span class="sxs-lookup"><span data-stu-id="1305f-117">When the event log size limit is reached, it might start wrapping.</span></span> <span data-ttu-id="1305f-118">Il wrapping è controllato dal valore di configurazione di **conservazione** .</span><span class="sxs-lookup"><span data-stu-id="1305f-118">Wrapping is controlled by the **Retention** configuration value.</span></span> <span data-ttu-id="1305f-119">Per ulteriori informazioni sui valori di configurazione del registro eventi, vedere [EventLog Key](eventlog-key.md).</span><span class="sxs-lookup"><span data-stu-id="1305f-119">For more information about the event log configuration values, see [Eventlog Key](eventlog-key.md).</span></span>

-   <span data-ttu-id="1305f-120">Avvolgimento.</span><span class="sxs-lookup"><span data-stu-id="1305f-120">Wrapping.</span></span> <span data-ttu-id="1305f-121">I record sono organizzati come buffer circolare.</span><span class="sxs-lookup"><span data-stu-id="1305f-121">The records are organized as a circular buffer.</span></span> <span data-ttu-id="1305f-122">Quando vengono aggiunti nuovi record, i record meno recenti vengono sostituiti.</span><span class="sxs-lookup"><span data-stu-id="1305f-122">As new records are added, the oldest records are replaced.</span></span> <span data-ttu-id="1305f-123">La posizione dei record meno recenti e più recenti può variare.</span><span class="sxs-lookup"><span data-stu-id="1305f-123">The location of the oldest and newest records will vary.</span></span> <span data-ttu-id="1305f-124">Nell'esempio seguente viene illustrato il metodo di wrapping.</span><span class="sxs-lookup"><span data-stu-id="1305f-124">The following example shows the wrapping method.</span></span>

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

    <span data-ttu-id="1305f-125">Nell'esempio il record meno recente non è più 1, ma è 102 perché lo spazio per i record da 1 a 101 è stato sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="1305f-125">In the example the oldest record is no longer 1, but is 102 because the space for records 1 to 101 was overwritten.</span></span>

    <span data-ttu-id="1305f-126">Esiste uno spazio tra il **record Elf \_ EOF \_** e il record meno recente, perché il sistema cancellerà un numero integrale di record per liberare spazio per il record più recente.</span><span class="sxs-lookup"><span data-stu-id="1305f-126">There is some space between the **ELF\_EOF\_RECORD** and the oldest record because the system will erase an integral number of records to free space for the newest record.</span></span> <span data-ttu-id="1305f-127">Se, ad esempio, il record più recente è di 100 byte e i due record meno recenti sono di 75 byte, i due record meno recenti verranno rimossi dal sistema.</span><span class="sxs-lookup"><span data-stu-id="1305f-127">For example, if the newest record is 100 bytes long and the two oldest records are 75 bytes long, then the system will remove the two oldest records.</span></span> <span data-ttu-id="1305f-128">I 50 byte aggiuntivi verranno utilizzati in un secondo momento, quando verranno scritti nuovi record.</span><span class="sxs-lookup"><span data-stu-id="1305f-128">The extra 50 bytes will be used later when new records are written.</span></span>

    <span data-ttu-id="1305f-129">Un file di registro eventi ha una dimensione fissa e quando i record nel file sono a capo, il record alla fine del file viene in genere suddiviso in due record.</span><span class="sxs-lookup"><span data-stu-id="1305f-129">An event log file has a fixed size and when the records in the file wrap, the record at the end of the file will typically be split into two records.</span></span> <span data-ttu-id="1305f-130">Se, ad esempio, la posizione per la scrittura successiva è 100 byte alla fine del file e la dimensione del record è 300 byte, i primi 100 byte verranno scritti alla fine del file e i successivi 200 byte verranno scritti all'inizio del file immediatamente dopo l' **\_ \_ intestazione di logfile Elf**.</span><span class="sxs-lookup"><span data-stu-id="1305f-130">For example, if the position for the next write is 100 bytes from the end of the file and the size of the record is 300 bytes, the first 100 bytes will be written at the end of the file and the next 200 bytes will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="1305f-131">Se lo spazio disponibile alla fine del file è inferiore alla parte fissa di **EVENTLOGRECORD** (0x38 bytes), tutto il nuovo record verrà scritto all'inizio del file immediatamente dopo l' **\_ \_ intestazione di logfile Elf**.</span><span class="sxs-lookup"><span data-stu-id="1305f-131">If the available space at the end of the file is less than the fixed portion of the **EVENTLOGRECORD** (0x38 bytes), all of the new record will be written at the beginning of the file immediately after the **ELF\_LOGFILE\_HEADER**.</span></span> <span data-ttu-id="1305f-132">I byte non utilizzati alla fine del file verranno riempiti con il modello 0x00000027.</span><span class="sxs-lookup"><span data-stu-id="1305f-132">The unused bytes at the end of the file will be filled with the pattern 0x00000027.</span></span>

<span data-ttu-id="1305f-133">Per ulteriori informazioni e un esempio di codice, vedere [segnalazione di un evento](reporting-an-event.md).</span><span class="sxs-lookup"><span data-stu-id="1305f-133">For more information and a code example, see [Reporting an Event](reporting-an-event.md).</span></span>

 

 
