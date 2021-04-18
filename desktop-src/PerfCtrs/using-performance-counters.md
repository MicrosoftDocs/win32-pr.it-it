---
description: Per utilizzare i dati del contatore, vedere Utilizzo dei dati del contatore.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Utilizzo dei contatori delle prestazioni
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312075"
---
# <a name="using-performance-counters"></a><span data-ttu-id="82fb5-103">Utilizzo dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="82fb5-103">Using Performance Counters</span></span>

<span data-ttu-id="82fb5-104">**I consumer** del contatore delle prestazioni sono componenti software che raccolgono e usano i dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="82fb5-104">Performance counter **consumers** are software components that collect and make use of performance counter data.</span></span> <span data-ttu-id="82fb5-105">I consumer di esempio forniti da Microsoft includono Performance Monitor (perfmon.exe), Monitoraggio risorse (resmon.exe), gestione log (logman.exe) e typeperf.exe.</span><span class="sxs-lookup"><span data-stu-id="82fb5-105">Example consumers provided by Microsoft include Performance Monitor (perfmon.exe), Resource Monitor (resmon.exe), Log Manager (logman.exe) and typeperf.exe.</span></span> <span data-ttu-id="82fb5-106">I componenti software di terze parti possono inoltre raccogliere dati sulle prestazioni tramite le API di raccolta prestazioni o tramite le classi del contatore delle prestazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="82fb5-106">Third-party software components may also collect performance data via performance collection APIs or via WMI performance counter classes.</span></span>

<span data-ttu-id="82fb5-107">I **provider** di contatori delle prestazioni sono componenti software che pubblicano i dati dei contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="82fb5-107">Performance counter **providers** are software components that publish performance counter data.</span></span> <span data-ttu-id="82fb5-108">I contatori delle prestazioni possono essere forniti da componenti del sistema operativo, driver di dispositivo e servizi.</span><span class="sxs-lookup"><span data-stu-id="82fb5-108">Performance counters can be provided by operating system components, device drivers, and services.</span></span> <span data-ttu-id="82fb5-109">Molti contatori delle prestazioni vengono forniti come parte del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="82fb5-109">Many performance counters are provided as part of the Windows operating system.</span></span> <span data-ttu-id="82fb5-110">I contatori aggiuntivi possono essere forniti da componenti software di terze parti tramite le API del provider del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="82fb5-110">Additional counters may be provided by third-party software components via the performance counter provider APIs.</span></span>

- <span data-ttu-id="82fb5-111">Utilizzare [gli strumenti del contatore delle prestazioni](performance-counters-tools.md) quando si desidera raccogliere o visualizzare i dati dei contatori da un sistema.</span><span class="sxs-lookup"><span data-stu-id="82fb5-111">Use [Performance Counter Tools](performance-counters-tools.md) when you want to collect or view the counter data from a system.</span></span>
- <span data-ttu-id="82fb5-112">Utilizzare le [API di consumer del contatore delle prestazioni](consuming-counter-data.md) quando si desidera scrivere un programma che raccoglie i dati dei contatori dal sistema locale.</span><span class="sxs-lookup"><span data-stu-id="82fb5-112">Use [Performance Counter Consumer APIs](consuming-counter-data.md) when you want to write a program that collects counter data from the local system.</span></span>
- <span data-ttu-id="82fb5-113">Utilizzare [le classi del contatore delle prestazioni WMI](/windows/desktop/WmiSdk/monitoring-performance-data) quando si desidera raccogliere i dati dei contatori da un sistema locale o remoto utilizzando WMI.</span><span class="sxs-lookup"><span data-stu-id="82fb5-113">Use [WMI Performance Counter Classes](/windows/desktop/WmiSdk/monitoring-performance-data) when you want to collect counter data from a local or remote system using WMI.</span></span>
- <span data-ttu-id="82fb5-114">Utilizzare le [API del provider del contatore delle prestazioni](providing-counter-data.md) quando si desidera pubblicare i dati dei contatori delle prestazioni dal componente software.</span><span class="sxs-lookup"><span data-stu-id="82fb5-114">Use [Performance Counter Provider APIs](providing-counter-data.md) when you want to publish performance counter data from your software component.</span></span>

## <a name="see-also"></a><span data-ttu-id="82fb5-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82fb5-115">See also</span></span>

[<span data-ttu-id="82fb5-116">Informazioni sui contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="82fb5-116">About Performance Counters</span></span>](about-performance-counters.md)

[<span data-ttu-id="82fb5-117">Riferimento ai contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="82fb5-117">Performance Counters Reference</span></span>](performance-counters-reference.md)
