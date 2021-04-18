---
description: Se l'origine dati è un file di log, è possibile specificare un intervallo di tempo per la query.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Impostazione di un intervallo di tempo per una query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312086"
---
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="88b9e-103">Impostazione di un intervallo di tempo per una query</span><span class="sxs-lookup"><span data-stu-id="88b9e-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="88b9e-104">Se l'origine dati è un file di log, è possibile specificare un intervallo di tempo per la query.</span><span class="sxs-lookup"><span data-stu-id="88b9e-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="88b9e-105">La query recupera i dati del contatore dal file di log raccolto durante l'intervallo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="88b9e-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="88b9e-106">Per impostare l'intervallo di tempo, chiamare la funzione [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) .</span><span class="sxs-lookup"><span data-stu-id="88b9e-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="88b9e-107">**PdhSetQueryTimeRange** non viene utilizzato per eseguire query sui dati sulle prestazioni da origini dati in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="88b9e-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="88b9e-108">Per creare un valore di ora, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="88b9e-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="88b9e-109">Allocare una struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inizializzare i campi con il valore di ora desiderato.</span><span class="sxs-lookup"><span data-stu-id="88b9e-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="88b9e-110">Chiamare [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) per convertire il valore dell'ora della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) in un'ora di struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="88b9e-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="88b9e-111">Eseguire il cast della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) come variabile LONGLONG, tenendo presente le convenzioni di riempimento dei membri della struttura della piattaforma e del compilatore.</span><span class="sxs-lookup"><span data-stu-id="88b9e-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="88b9e-112">Copiare il valore LONGLONG nel campo appropriato nella struttura [**PDH \_ time \_ info**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .</span><span class="sxs-lookup"><span data-stu-id="88b9e-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="88b9e-113">Per recuperare l'intervallo di tempo di tutti i dati sulle prestazioni contenuti in un file di log, chiamare la funzione [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .</span><span class="sxs-lookup"><span data-stu-id="88b9e-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
