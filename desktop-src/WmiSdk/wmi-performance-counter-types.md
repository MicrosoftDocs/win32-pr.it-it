---
description: Il tipo di contatore delle prestazioni designa una formula necessaria per ottenere i contatori delle prestazioni calcolati. Si tratta degli stessi tipi di contatori utilizzati dal monitoraggio delle prestazioni di Windows.
ms.assetid: d4a9feca-80a2-4ce5-b4d7-4e83ef951c08
ms.tgt_platform: multiple
title: Tipi di contatori delle prestazioni WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b12ac0d2c8afb1499fec44c983364b5e3278b864
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131147"
---
# <a name="wmi-performance-counter-types"></a><span data-ttu-id="d9c41-104">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="d9c41-104">WMI Performance Counter Types</span></span>

<span data-ttu-id="d9c41-105">Il [tipo di contatore](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) delle prestazioni designa una formula necessaria per ottenere i contatori delle prestazioni calcolati.</span><span class="sxs-lookup"><span data-stu-id="d9c41-105">The performance [counter type](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)) designates a formula required to obtain calculated performance counters.</span></span> <span data-ttu-id="d9c41-106">Si tratta degli stessi tipi di contatori utilizzati dal [monitoraggio delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal)di Windows.</span><span class="sxs-lookup"><span data-stu-id="d9c41-106">These are the same counter types used by Windows [Performance Monitoring](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="d9c41-107">Nelle classi di prestazioni WMI, i dati non elaborati per la formula del tipo di contatore provengono da una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e il risultato calcolato viene trovato nella stessa proprietà denominata di una classe [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d9c41-107">In WMI performance classes, the raw data for the counter type formula comes from a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and the calculated result is found in the same-named property of a corresponding [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) class.</span></span>

<span data-ttu-id="d9c41-108">I tipi di contatore vengono visualizzati come qualificatore **CounterType** per le proprietà nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e come qualificatore **CookingType** per le proprietà nelle classi [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="d9c41-108">Counter types appear as the **CounterType** qualifier for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes, and as the **CookingType** qualifier for properties in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="d9c41-109">Ad esempio, la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfRawData \_ perfdisk \_ disco logico**](./retrieving-raw-and-formatted-performance-data.md) è l'origine dati non elaborata per la proprietà **AvgDiskBytesPerRead** nella classe [**Win32 \_ PerfFormattedData \_ perfdisk \_**](./retrieving-raw-and-formatted-performance-data.md)disco logico, che contiene gli stessi dati mostrati in Monitor di sistema.</span><span class="sxs-lookup"><span data-stu-id="d9c41-109">For example, the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class is the raw data source for the **AvgDiskBytesPerRead** property in the class [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), which contains the same data as shown in System Monitor.</span></span>

<span data-ttu-id="d9c41-110">Nell'elenco seguente vengono organizzate le descrizioni dei tipi di contatore per tipo funzionale:</span><span class="sxs-lookup"><span data-stu-id="d9c41-110">The following list organizes counter type descriptions by functional type:</span></span>

-   [<span data-ttu-id="d9c41-111">Tipi di contatori di base</span><span class="sxs-lookup"><span data-stu-id="d9c41-111">Base Counter Types</span></span>](base-counter-types.md)
-   [<span data-ttu-id="d9c41-112">Tipi di contatori di algoritmi di base</span><span class="sxs-lookup"><span data-stu-id="d9c41-112">Basic Algorithm Counter Types</span></span>](basic-algorithm-counter-types.md)
-   [<span data-ttu-id="d9c41-113">Tipi di contatori dell'algoritmo contatore</span><span class="sxs-lookup"><span data-stu-id="d9c41-113">Counter Algorithm Counter Types</span></span>](counter-algorithm-counter-types.md)
-   [<span data-ttu-id="d9c41-114">Tipi di contatori non computazionali</span><span class="sxs-lookup"><span data-stu-id="d9c41-114">Noncomputational Counter Types</span></span>](noncomputational-counter-types.md)
-   [<span data-ttu-id="d9c41-115">Tipi di contatori dell'algoritmo timer di precisione</span><span class="sxs-lookup"><span data-stu-id="d9c41-115">Precision Timer Algorithm Counter Types</span></span>](precision-timer-algorithm-counter-types.md)
-   [<span data-ttu-id="d9c41-116">Tipi di contatori degli algoritmi a lunghezza coda</span><span class="sxs-lookup"><span data-stu-id="d9c41-116">Queue-length Algorithm Counter Types</span></span>](queue-length-algorithm-counter-types.md)
-   [<span data-ttu-id="d9c41-117">Tipi di contatori statistici</span><span class="sxs-lookup"><span data-stu-id="d9c41-117">Statistical Counter Types</span></span>](statistical-counter-types.md)
-   [<span data-ttu-id="d9c41-118">Tipi di contatori degli algoritmi timer</span><span class="sxs-lookup"><span data-stu-id="d9c41-118">Timer Algorithm Counter Types</span></span>](timer-algorithm-counter-types.md)

 

 
