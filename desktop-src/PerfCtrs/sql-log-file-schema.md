---
description: Le applicazioni possono utilizzare PDH per estrarre i contatori delle prestazioni dai log SQL oppure possono estrarre i contatori formattati o non elaborati direttamente dal database tramite query SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Schema del file di log SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312079"
---
# <a name="sql-log-file-schema"></a><span data-ttu-id="0f3a1-103">Schema del file di log SQL</span><span class="sxs-lookup"><span data-stu-id="0f3a1-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f3a1-104">Il supporto di PDH per i database SQL ODBC può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="0f3a1-105">Le applicazioni possono utilizzare le API PDH per leggere e scrivere i dati dei contatori delle prestazioni in database SQL ODBC compatibili, quindi eseguire ulteriori elaborazioni tramite query SQL.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="0f3a1-106">In questa sezione viene descritto lo schema SQL utilizzato per archiviare i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="0f3a1-107">È possibile utilizzare queste informazioni per creare visualizzazioni e report personalizzati.</span><span class="sxs-lookup"><span data-stu-id="0f3a1-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="0f3a1-108">Lo schema è costituito dalle tre tabelle seguenti:</span><span class="sxs-lookup"><span data-stu-id="0f3a1-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="0f3a1-109">**CounterData**</span><span class="sxs-lookup"><span data-stu-id="0f3a1-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="0f3a1-110">**CounterDetails**</span><span class="sxs-lookup"><span data-stu-id="0f3a1-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="0f3a1-111">**DisplayToID**</span><span class="sxs-lookup"><span data-stu-id="0f3a1-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="0f3a1-112">Il supporto di PDH per i database SQL ODBC funziona solo con i driver SQL ODBC che supportano le estensioni per la [copia bulk (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span><span class="sxs-lookup"><span data-stu-id="0f3a1-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
