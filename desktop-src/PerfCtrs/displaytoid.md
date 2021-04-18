---
description: La tabella DisplayToID correla la stringa descrittiva visualizzata da monitoraggio di sistema al GUID archiviato nelle altre tabelle.
ms.assetid: 414d16f1-ab6f-45f0-9287-154810543a6d
title: DisplayToID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b71ae8c4ebaafc80d98580a13a83e3cc7cff815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312171"
---
# <a name="displaytoid"></a><span data-ttu-id="2d974-103">DisplayToID</span><span class="sxs-lookup"><span data-stu-id="2d974-103">DisplayToID</span></span>

<span data-ttu-id="2d974-104">La tabella **DisplayToID** correla la stringa descrittiva visualizzata da monitoraggio di sistema al GUID archiviato nelle altre tabelle.</span><span class="sxs-lookup"><span data-stu-id="2d974-104">The **DisplayToID** table relates the user-friendly string displayed by the System Monitor to the GUID stored in the other tables.</span></span>

<span data-ttu-id="2d974-105">La tabella **DisplayToID** definisce i campi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d974-105">The **DisplayToID** table defines the following fields:</span></span>

-   <span data-ttu-id="2d974-106">**GUID:** Identificatore univoco generato per un log.</span><span class="sxs-lookup"><span data-stu-id="2d974-106">**GUID:** Unique identifier generated for a log.</span></span> <span data-ttu-id="2d974-107">Questo campo è la chiave primaria della tabella.</span><span class="sxs-lookup"><span data-stu-id="2d974-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="2d974-108">**RunId:** Riservato per uso interno.</span><span class="sxs-lookup"><span data-stu-id="2d974-108">**RunID:** Reserved for internal use.</span></span>
-   <span data-ttu-id="2d974-109">**DisplayString:** Nome del file di log visualizzato in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="2d974-109">**DisplayString:** Name of the log file as displayed in the System Monitor.</span></span>
-   <span data-ttu-id="2d974-110">**LogStartTime:** Ora di inizio del processo di registrazione nel formato aaaa-mm-gg hh: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="2d974-110">**LogStartTime:** Time the logging process started in yyyy-mm-dd hh:mm:ss:nnn format.</span></span>
-   <span data-ttu-id="2d974-111">**LogStopTime:** Ora di arresto del processo di registrazione nel formato aaaa-mm-gg hh: mm: SS: nnn.</span><span class="sxs-lookup"><span data-stu-id="2d974-111">**LogStopTime:** Time the logging process stopped in yyyy-mm-dd hh:mm:ss:nnn format.</span></span> <span data-ttu-id="2d974-112">È possibile differenziare più file di log con lo stesso valore **displayString** usando il valore in questo e i campi **LogStartTime** .</span><span class="sxs-lookup"><span data-stu-id="2d974-112">Multiple log files with the same **DisplayString** value can be differentiated by using the value in this and the **LogStartTime** fields.</span></span> <span data-ttu-id="2d974-113">I valori nei campi **LogStartTime** e **LogStopTime** consentono inoltre di accedere rapidamente al tempo totale di raccolta.</span><span class="sxs-lookup"><span data-stu-id="2d974-113">The values in the **LogStartTime** and **LogStopTime** fields also allows the total collection time to be accessed quickly.</span></span>
-   <span data-ttu-id="2d974-114">**NumberOfRecords:** Numero di campioni archiviati nella tabella per ogni raccolta di log.</span><span class="sxs-lookup"><span data-stu-id="2d974-114">**NumberOfRecords:** Number of samples stored in the table for each log collection.</span></span>
-   <span data-ttu-id="2d974-115">**MinutesToUTC:** Valore utilizzato per convertire i dati della riga archiviati nell'ora UTC nell'ora locale.</span><span class="sxs-lookup"><span data-stu-id="2d974-115">**MinutesToUTC:** Value used to convert the row data stored in UTC time to local time.</span></span>
-   <span data-ttu-id="2d974-116">**TimeZoneName:** Nome del fuso orario in cui sono stati raccolti i dati.</span><span class="sxs-lookup"><span data-stu-id="2d974-116">**TimeZoneName:** Name of the time zone where the data was collected.</span></span> <span data-ttu-id="2d974-117">Se si raccolgono o si riregistrano dati da un file raccolto nei sistemi nel proprio fuso orario, questo campo dimostrerà il percorso.</span><span class="sxs-lookup"><span data-stu-id="2d974-117">If you are collecting or have relogged data from a file collected on systems in your own time zone, this field will state the location.</span></span>

<span data-ttu-id="2d974-118">**Nota**  Prima di Windows Vista, gli insiemi agenti di raccolta dati venivano archiviati nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2d974-118">**Note**  Prior to Windows Vista, the data collector sets were stored in the registry at</span></span>

<span data-ttu-id="2d974-119">**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Services \\ SysmonLog \\ log queries**</span><span class="sxs-lookup"><span data-stu-id="2d974-119">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\SysmonLog\\Log Queries**</span></span>

<span data-ttu-id="2d974-120">.</span><span class="sxs-lookup"><span data-stu-id="2d974-120">.</span></span> <span data-ttu-id="2d974-121">I campi elencati sopra non corrispondono ai valori nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2d974-121">The fields listed above do not correspond to the values in registry.</span></span> <span data-ttu-id="2d974-122">Per Windows Vista, gli insiemi agenti di raccolta dati non vengono archiviati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="2d974-122">For Windows Vista, the data collector sets are not stored in the registry.</span></span>

 

 



