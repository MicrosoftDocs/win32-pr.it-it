---
description: I tipi di contatori dell'algoritmo timer di precisione ottengono letture più accurate rispetto ai timer di sistema.
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: Tipi di contatori dell'algoritmo timer di precisione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a8864587fedc915678dfa4a9e578ca051e1262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759770"
---
# <a name="precision-timer-algorithm-counter-types"></a><span data-ttu-id="7a6bb-103">Tipi di contatori dell'algoritmo timer di precisione</span><span class="sxs-lookup"><span data-stu-id="7a6bb-103">Precision Timer Algorithm Counter Types</span></span>

<span data-ttu-id="7a6bb-104">I tipi di contatori dell'algoritmo timer di precisione ottengono letture più accurate rispetto ai timer di sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bb-104">The precision timer algorithm counter types obtain more accurate readings than system timers.</span></span> <span data-ttu-id="7a6bb-105">Il servizio che fornisce i dati fornisce anche un timestamp, che elimina gli errori che possono verificarsi a causa del tempo ridotto e variabile che trascorre tra l'acquisizione del timestamp di sistema e la raccolta dei dati dalla DLL di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7a6bb-105">The service that provides the data also provides a timestamp, which eliminates the errors that can occur because of the small and variable time that elapses between capture of the system timestamp and collection of the data from the performance DLL.</span></span> <span data-ttu-id="7a6bb-106">Questo timestamp di base per i timer di precisione è una \_ \_ proprietà timestamp precisione prestazioni, che deve seguire immediatamente la \_ \_ Proprietà Timer precisione prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7a6bb-106">This base timestamp for precision timers is a PERF\_PRECISION\_TIMESTAMP property, which must immediately follow the PERF\_PRECISION\_TIMER property.</span></span>



| <span data-ttu-id="7a6bb-107">Costante CounterType</span><span class="sxs-lookup"><span data-stu-id="7a6bb-107">CounterType Constant</span></span>                                                                                         | <span data-ttu-id="7a6bb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a6bb-108">Description</span></span>                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a6bb-109">[Prestazioni \_ \_ \_ Timer di sistema precisione](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 541525248</span><span class="sxs-lookup"><span data-stu-id="7a6bb-109">[PERF\_PRECISION\_SYSTEM\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248</span></span><br/> | <span data-ttu-id="7a6bb-110">Simile al \_ \_ timer del contatore delle prestazioni, con la differenza che usa una base temporale definita dal contatore anziché il timestamp di sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bb-110">Similar to PERF\_COUNTER\_TIMER except that it uses a counter defined time base instead of the system timestamp.</span></span>             |
| <span data-ttu-id="7a6bb-111">[Prestazioni \_ PRECISIONE \_ 100 NS \_ timer](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimale 542573824</span><span class="sxs-lookup"><span data-stu-id="7a6bb-111">[PERF\_PRECISION\_100NS\_TIMER](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 542573824</span></span><br/>  | <span data-ttu-id="7a6bb-112">Simile al \_ timer perf 100NSEC \_ , ad eccezione del fatto che usa una base di tempo definita per il contatore 100 ns anziché il timestamp del 100 NS di sistema.</span><span class="sxs-lookup"><span data-stu-id="7a6bb-112">Similar to PERF\_100NSEC\_TIMER except that it uses a 100ns counter defined time base instead of the system 100ns timestamp.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7a6bb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a6bb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a6bb-114">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="7a6bb-114">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> </dl>

 

