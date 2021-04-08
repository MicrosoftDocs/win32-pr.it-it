---
description: Le informazioni relative a ogni evento vengono archiviate nel registro eventi in un record del registro eventi. Il record del registro eventi include informazioni su tempo, tipo e categoria. Per ulteriori informazioni, vedere la struttura EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Record del registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880893"
---
# <a name="event-log-records"></a><span data-ttu-id="287ef-105">Record del registro eventi</span><span class="sxs-lookup"><span data-stu-id="287ef-105">Event Log Records</span></span>

<span data-ttu-id="287ef-106">Le informazioni relative a ogni evento vengono archiviate nel registro eventi in un *record del registro eventi*.</span><span class="sxs-lookup"><span data-stu-id="287ef-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="287ef-107">Il record del registro eventi include informazioni su tempo, tipo e categoria.</span><span class="sxs-lookup"><span data-stu-id="287ef-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="287ef-108">Per ulteriori informazioni, vedere la struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="287ef-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="287ef-109">Il membro **RecordNumber** di [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contiene il numero di record per il record del log eventi.</span><span class="sxs-lookup"><span data-stu-id="287ef-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="287ef-110">Il primo record scritto in un log eventi è il numero di record 1 e gli altri record sono numerati in sequenza.</span><span class="sxs-lookup"><span data-stu-id="287ef-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="287ef-111">Se il numero di record raggiunge ULONG \_ Max, il numero di record successivo sarà 0, non 1, ma si userà zero per cercare il record.</span><span class="sxs-lookup"><span data-stu-id="287ef-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="287ef-112">Se il valore del registro di sistema [conservazione](eventlog-key.md) è impostato su zero, i record degli eventi vengono sovrascritti quando viene raggiunta la dimensione massima del log.</span><span class="sxs-lookup"><span data-stu-id="287ef-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="287ef-113">Il record meno recente in un log eventi, quindi, non può essere un record numero 1.</span><span class="sxs-lookup"><span data-stu-id="287ef-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="287ef-114">Per identificare il record meno recente nel log, chiamare la funzione [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="287ef-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="287ef-115">È quindi possibile chiamare la funzione [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) e aggiungere il valore restituito al numero di record meno recente per determinare il record più recente.</span><span class="sxs-lookup"><span data-stu-id="287ef-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="287ef-116">È possibile leggere singoli record dal registro eventi usando la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) .</span><span class="sxs-lookup"><span data-stu-id="287ef-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="287ef-117">Per ulteriori informazioni, vedere [esecuzione di query per informazioni sull'evento](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="287ef-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



