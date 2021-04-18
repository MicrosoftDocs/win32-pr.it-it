---
title: Novità di monitoraggio di sistema
description: Nella tabella seguente sono riportate le novità per ogni versione di monitoraggio di sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2020
ms.locfileid: "104398689"
---
# <a name="whats-new-in-system-monitor"></a><span data-ttu-id="a95be-103">Novità di monitoraggio di sistema</span><span class="sxs-lookup"><span data-stu-id="a95be-103">What's New in System Monitor</span></span>

<span data-ttu-id="a95be-104">Nella tabella seguente sono riportate le novità per ogni versione di monitoraggio di sistema (SYSMON).</span><span class="sxs-lookup"><span data-stu-id="a95be-104">The following table identifies what is new for each release of System Monitor (SYSMON).</span></span>



| <span data-ttu-id="a95be-105">Versione</span><span class="sxs-lookup"><span data-stu-id="a95be-105">Version</span></span>     | <span data-ttu-id="a95be-106">Descrizione delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="a95be-106">Description of features</span></span>                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a95be-107">Versione 3,7</span><span class="sxs-lookup"><span data-stu-id="a95be-107">Version 3.7</span></span> | <span data-ttu-id="a95be-108">Questa versione aggiunge nuovi tipi di grafico, la possibilità di selezionare più contatori, di recuperare i valori dei contatori da un punto nel grafico, di salvare i valori dei contatori con grafici in un file di log e l'opzione per fare in modo che un grafico a linee scorra continuamente nella finestra del grafico anziché eseguire il wrapping su se stesso. Incluso in Windows Server 2008 e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a95be-108">This version adds new graph types, the ability to select multiple counters, retrieve counter values from a point on the graph, save graphed counter values to a log file, and the option to have a line graph continuously scroll in the graph window instead of wrap-around on itself.Included in Windows Server 2008 and Windows Vista.</span></span><br/> |



 

## <a name="version-37"></a><span data-ttu-id="a95be-109">Versione 3,7</span><span class="sxs-lookup"><span data-stu-id="a95be-109">Version 3.7</span></span>

<span data-ttu-id="a95be-110">Nuovi metodi e proprietà aggiunti a [**CounterItem**](counteritem.md).</span><span class="sxs-lookup"><span data-stu-id="a95be-110">New properties and methods that were added to [**CounterItem**](counteritem.md).</span></span>

-   [<span data-ttu-id="a95be-111">**GetDataAt**</span><span class="sxs-lookup"><span data-stu-id="a95be-111">**GetDataAt**</span></span>](counteritem-getdataat.md)
-   [<span data-ttu-id="a95be-112">**Selezionato**</span><span class="sxs-lookup"><span data-stu-id="a95be-112">**Selected**</span></span>](counteritem-selected.md)
-   [<span data-ttu-id="a95be-113">**Visible**</span><span class="sxs-lookup"><span data-stu-id="a95be-113">**Visible**</span></span>](counteritem-visible.md)
-   <span data-ttu-id="a95be-114">Intervallo di valori validi modificato per [ **CounterItem. Width**](counteritem-width.md)</span><span class="sxs-lookup"><span data-stu-id="a95be-114">Range of valid values changed for [**CounterItem.Width**](counteritem-width.md)</span></span>

<span data-ttu-id="a95be-115">Nuovi metodi e proprietà aggiunti a [**SystemMonitor**](systemmonitor.md).</span><span class="sxs-lookup"><span data-stu-id="a95be-115">New properties and methods that were added to [**SystemMonitor**](systemmonitor.md).</span></span>

-   [<span data-ttu-id="a95be-116">**BatchingLock**</span><span class="sxs-lookup"><span data-stu-id="a95be-116">**BatchingLock**</span></span>](systemmonitor-batchinglock.md)
-   [<span data-ttu-id="a95be-117">**ChartScroll**</span><span class="sxs-lookup"><span data-stu-id="a95be-117">**ChartScroll**</span></span>](systemmonitor-chartscroll.md)
-   [<span data-ttu-id="a95be-118">**ClearData**</span><span class="sxs-lookup"><span data-stu-id="a95be-118">**ClearData**</span></span>](systemmonitor-cleardata.md)
-   [<span data-ttu-id="a95be-119">**DataPointCount**</span><span class="sxs-lookup"><span data-stu-id="a95be-119">**DataPointCount**</span></span>](systemmonitor-datapointcount.md)
-   [<span data-ttu-id="a95be-120">**EnableDigitGrouping**</span><span class="sxs-lookup"><span data-stu-id="a95be-120">**EnableDigitGrouping**</span></span>](systemmonitor-enabledigitgrouping.md)
-   [<span data-ttu-id="a95be-121">**EnableToolTips**</span><span class="sxs-lookup"><span data-stu-id="a95be-121">**EnableToolTips**</span></span>](systemmonitor-enabletooltips.md)
-   [<span data-ttu-id="a95be-122">**GetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="a95be-122">**GetLogViewRange**</span></span>](systemmonitor-getlogviewrange.md)
-   [<span data-ttu-id="a95be-123">**LoadSettings**</span><span class="sxs-lookup"><span data-stu-id="a95be-123">**LoadSettings**</span></span>](systemmonitor-loadsettings.md)
-   [<span data-ttu-id="a95be-124">**LogSourceStartTime**</span><span class="sxs-lookup"><span data-stu-id="a95be-124">**LogSourceStartTime**</span></span>](systemmonitor-logsourcestarttime.md)
-   [<span data-ttu-id="a95be-125">**LogSourceStopTime**</span><span class="sxs-lookup"><span data-stu-id="a95be-125">**LogSourceStopTime**</span></span>](systemmonitor-logsourcestoptime.md)
-   [<span data-ttu-id="a95be-126">**Relog**</span><span class="sxs-lookup"><span data-stu-id="a95be-126">**Relog**</span></span>](systemmonitor-relog.md)
-   [<span data-ttu-id="a95be-127">**SaveAs**</span><span class="sxs-lookup"><span data-stu-id="a95be-127">**SaveAs**</span></span>](systemmonitor-saveas.md)
-   [<span data-ttu-id="a95be-128">**ScaleToFit**</span><span class="sxs-lookup"><span data-stu-id="a95be-128">**ScaleToFit**</span></span>](systemmonitor-scaletofit.md)
-   [<span data-ttu-id="a95be-129">**SetLogViewRange**</span><span class="sxs-lookup"><span data-stu-id="a95be-129">**SetLogViewRange**</span></span>](systemmonitor-setlogviewrange.md)
-   [<span data-ttu-id="a95be-130">**ShowTimeAxisLables**</span><span class="sxs-lookup"><span data-stu-id="a95be-130">**ShowTimeAxisLables**</span></span>](systemmonitor-showtimeaxislabels.md)

<span data-ttu-id="a95be-131">Nuove enumerazioni aggiunte.</span><span class="sxs-lookup"><span data-stu-id="a95be-131">New enumerations that were added.</span></span>

-   [<span data-ttu-id="a95be-132">**SysmonDataType**</span><span class="sxs-lookup"><span data-stu-id="a95be-132">**SysmonDataType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [<span data-ttu-id="a95be-133">**SysmonFileType**</span><span class="sxs-lookup"><span data-stu-id="a95be-133">**SysmonFileType**</span></span>](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   <span data-ttu-id="a95be-134">Sono stati aggiunti nuovi valori del tipo di visualizzazione a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span><span class="sxs-lookup"><span data-stu-id="a95be-134">New display type values were added to [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)</span></span>

 

 





