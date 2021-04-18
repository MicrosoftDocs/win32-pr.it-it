---
description: Rappresenta le differenze tra i campioni nel tempo e spesso usa un valore di base per il calcolo.
ms.assetid: 613268ab-386b-421d-a5b5-aab6a065999c
ms.tgt_platform: multiple
title: Tipi di contatori di algoritmi di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70514c10b2695aa940d48341752ef647dcca9719
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316575"
---
# <a name="basic-algorithm-counter-types"></a><span data-ttu-id="688df-103">Tipi di contatori di algoritmi di base</span><span class="sxs-lookup"><span data-stu-id="688df-103">Basic Algorithm Counter Types</span></span>

<span data-ttu-id="688df-104">I tipi di contatori di base dell'algoritmo rappresentano in genere le differenze tra i campioni nel tempo e spesso utilizzano un valore di base per il calcolo.</span><span class="sxs-lookup"><span data-stu-id="688df-104">Basic algorithm counter types generally represent differences between samples over time, and often use a base value for the calculation.</span></span> <span data-ttu-id="688df-105">Ad esempio, la proprietà **PercentFreeSpace** della classe [**Win32 \_ PerfFormattedData \_ perfdisk \_ PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) rappresenta il rapporto tra lo spazio libero disponibile nell'unità disco fisico e lo spazio totale utilizzabile fornito dall'unità disco fisica selezionata.</span><span class="sxs-lookup"><span data-stu-id="688df-105">For example, the **PercentFreeSpace** property of the [**Win32\_PerfFormattedData\_PerfDisk\_PhysicalDisk**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) class represents the ratio of the free space available on the physical disk unit to the total usable space provided by the selected physical disk drive.</span></span> <span data-ttu-id="688df-106">Questa classe contiene anche il valore di base, **PercentFreeSpace \_ base**.</span><span class="sxs-lookup"><span data-stu-id="688df-106">This class also contains the base value, **PercentFreeSpace\_Base**.</span></span> <span data-ttu-id="688df-107">La percentuale di spazio libero su disco si ottiene dividendo **PercentFreeSpace** per **PercentFreeSpace \_ base** e moltiplicando per il 100%.</span><span class="sxs-lookup"><span data-stu-id="688df-107">The percentage of free disk space is obtained by dividing **PercentFreeSpace** by **PercentFreeSpace\_Base** and multiplying by 100%.</span></span>

<span data-ttu-id="688df-108">Sono disponibili gli algoritmi di base nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="688df-108">The basic algorithms in the following table are provided.</span></span>



| <span data-ttu-id="688df-109">Costante CounterType</span><span class="sxs-lookup"><span data-stu-id="688df-109">CounterType Constant</span></span>                                                                                    | <span data-ttu-id="688df-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="688df-110">Description</span></span>                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688df-111">[Prestazioni \_ Decimale \_ frazione non elaborata](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))537003008</span><span class="sxs-lookup"><span data-stu-id="688df-111">[PERF\_RAW\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 537003008</span></span><br/>       | <span data-ttu-id="688df-112">Rapporto tra un subset e il relativo set come percentuale.</span><span class="sxs-lookup"><span data-stu-id="688df-112">Ratio of a subset to its set as a percentage.</span></span> <span data-ttu-id="688df-113">Questo tipo di contatore visualizza solo la percentuale corrente, non una media nel tempo.</span><span class="sxs-lookup"><span data-stu-id="688df-113">This counter type displays the current percentage only, not an average over time.</span></span>                                    |
| <span data-ttu-id="688df-114">[Prestazioni \_ \_Frazione di esempio](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 549585920</span><span class="sxs-lookup"><span data-stu-id="688df-114">[PERF\_SAMPLE\_FRACTION](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 549585920</span></span><br/>    | <span data-ttu-id="688df-115">Rapporto medio tra gli accessi e tutte le operazioni durante gli ultimi due intervalli di campionamento.</span><span class="sxs-lookup"><span data-stu-id="688df-115">Average ratio of hits to all operations during the last two sample intervals.</span></span> <span data-ttu-id="688df-116">Questo tipo di contatore richiede una proprietà di base con il tipo di contatore di base di esempio delle prestazioni \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="688df-116">This counter type requires a base property with the PERF\_SAMPLE\_BASE counter type.</span></span> |
| <span data-ttu-id="688df-117">[Prestazioni \_ CONTATORE \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 4195328</span><span class="sxs-lookup"><span data-stu-id="688df-117">[PERF\_COUNTER\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195328</span></span><br/>        | <span data-ttu-id="688df-118">Questo tipo di contatore mostra la variazione dell'attributo misurato tra i due intervalli di campionamento più recenti.</span><span class="sxs-lookup"><span data-stu-id="688df-118">This counter type shows the change in the measured attribute between the two most recent sample intervals.</span></span>                                                         |
| <span data-ttu-id="688df-119">[Prestazioni \_ CONTATORE \_ \_ Delta](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale grande 4195584</span><span class="sxs-lookup"><span data-stu-id="688df-119">[PERF\_COUNTER\_LARGE\_DELTA](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 4195584</span></span><br/> | <span data-ttu-id="688df-120">Uguale al \_ contatore \_ delle prestazioni Delta, ma una rappresentazione a 64 bit per valori più grandi.</span><span class="sxs-lookup"><span data-stu-id="688df-120">Same as PERF\_COUNTER\_DELTA but a 64-bit representation for larger values.</span></span>                                                                                        |
| <span data-ttu-id="688df-121">[Prestazioni \_ \_Tempo](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale trascorso 807666944</span><span class="sxs-lookup"><span data-stu-id="688df-121">[PERF\_ELAPSED\_TIME](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 807666944</span></span><br/>       | <span data-ttu-id="688df-122">Tempo totale tra il momento in cui il processo è stato avviato e l'ora in cui questo valore viene calcolato.</span><span class="sxs-lookup"><span data-stu-id="688df-122">Total time between when the process started and the time when this value is calculated.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="688df-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="688df-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="688df-124">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="688df-124">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

