---
description: Le funzioni correlate al tempo restituiscono il tempo in uno dei diversi formati. È possibile usare le funzioni temporali per eseguire la conversione tra alcuni formati di tempo per semplificare il confronto e la visualizzazione. Nella tabella seguente vengono riepilogati i formati di ora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Informazioni sul tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050134"
---
# <a name="about-time"></a><span data-ttu-id="cf774-105">Informazioni sul tempo</span><span class="sxs-lookup"><span data-stu-id="cf774-105">About Time</span></span>

<span data-ttu-id="cf774-106">Le funzioni correlate al tempo restituiscono il tempo in uno dei diversi formati.</span><span class="sxs-lookup"><span data-stu-id="cf774-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="cf774-107">È possibile usare le funzioni temporali per eseguire la conversione tra alcuni formati di tempo per semplificare il confronto e la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cf774-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="cf774-108">Nella tabella seguente vengono riepilogati i formati di ora.</span><span class="sxs-lookup"><span data-stu-id="cf774-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="cf774-109">Formato</span><span class="sxs-lookup"><span data-stu-id="cf774-109">Format</span></span>          | <span data-ttu-id="cf774-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf774-110">Type</span></span>                                                                     | <span data-ttu-id="cf774-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf774-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf774-112">Sistema</span><span class="sxs-lookup"><span data-stu-id="cf774-112">System</span></span>          | [<span data-ttu-id="cf774-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="cf774-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="cf774-114">Anno, mese, giorno, ora, secondo e millisecondo, tratto dal clock hardware interno.</span><span class="sxs-lookup"><span data-stu-id="cf774-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="cf774-115">Locale</span><span class="sxs-lookup"><span data-stu-id="cf774-115">Local</span></span>           | <span data-ttu-id="cf774-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="cf774-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="cf774-117">Ora di sistema o di file convertito nel fuso orario locale del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf774-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="cf774-118">File</span><span class="sxs-lookup"><span data-stu-id="cf774-118">File</span></span>            | [<span data-ttu-id="cf774-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="cf774-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="cf774-120">Numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="cf774-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="cf774-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="cf774-121">MS-DOS</span></span>          | <span data-ttu-id="cf774-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="cf774-122">**WORD**</span></span>                                                                 | <span data-ttu-id="cf774-123">Una parola compressa per la data, un'altra per l'ora.</span><span class="sxs-lookup"><span data-stu-id="cf774-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="cf774-124">Windows</span><span class="sxs-lookup"><span data-stu-id="cf774-124">Windows</span></span>         | <span data-ttu-id="cf774-125">**DWORD** o **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="cf774-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="cf774-126">Numero di millisecondi trascorsi dall'ultimo avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf774-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="cf774-127">Quando viene recuperato come valore DWORD, l'ora di Windows viene ciclica ogni 49,7 giorni.</span><span class="sxs-lookup"><span data-stu-id="cf774-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="cf774-128">Numero di interrupt</span><span class="sxs-lookup"><span data-stu-id="cf774-128">Interrupt Count</span></span> | <span data-ttu-id="cf774-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="cf774-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="cf774-130">Numero di intervalli di 100-nanosecondi dall'ultimo avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="cf774-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="cf774-131">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="cf774-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cf774-132">Ora di sistema</span><span class="sxs-lookup"><span data-stu-id="cf774-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="cf774-133">Ora locale</span><span class="sxs-lookup"><span data-stu-id="cf774-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="cf774-134">Orari file</span><span class="sxs-lookup"><span data-stu-id="cf774-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="cf774-135">Data e ora di MS-DOS</span><span class="sxs-lookup"><span data-stu-id="cf774-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="cf774-136">Ora di Windows</span><span class="sxs-lookup"><span data-stu-id="cf774-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="cf774-137">Tempo di interrupt</span><span class="sxs-lookup"><span data-stu-id="cf774-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
