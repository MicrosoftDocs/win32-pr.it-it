---
description: Un'applicazione Visualizzatore eventi utilizza la funzione OpenEventLog per aprire il registro eventi per un'origine evento.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lettura dal registro eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049854"
---
# <a name="reading-from-the-event-log"></a><span data-ttu-id="f32f2-103">Lettura dal registro eventi</span><span class="sxs-lookup"><span data-stu-id="f32f2-103">Reading from the Event Log</span></span>

<span data-ttu-id="f32f2-104">Un'applicazione Visualizzatore eventi utilizza la funzione [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) per aprire il registro eventi per un'origine evento.</span><span class="sxs-lookup"><span data-stu-id="f32f2-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="f32f2-105">Il Visualizzatore eventi può quindi utilizzare la funzione [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) per leggere i record di eventi dal log.</span><span class="sxs-lookup"><span data-stu-id="f32f2-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="f32f2-106">**ReadEventLog** restituisce un buffer contenente una struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e informazioni aggiuntive che descrivono un evento registrato.</span><span class="sxs-lookup"><span data-stu-id="f32f2-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="f32f2-107">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="f32f2-107">The following diagram illustrates this process.</span></span>

![lettura dal registro eventi](images/readlog.png)

<span data-ttu-id="f32f2-109">Per un esempio di codice, vedere [esecuzione di query per informazioni sull'evento](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="f32f2-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



