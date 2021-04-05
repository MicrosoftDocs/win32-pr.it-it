---
description: La formula del tipo di contatore della varianza del COOKer \_ fornisce la variabilità che consente di caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in un'istanza di Win32 \_ PerfRawData.
ms.assetid: 6b184a36-7d22-41ab-98e7-b185d1063bcb
ms.tgt_platform: multiple
title: COOKER_VARIANCE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f9de6c5241ccd486e4da76864139e3e54f5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049816"
---
# <a name="cooker_variance"></a><span data-ttu-id="84744-103">varianza del COOKer \_</span><span class="sxs-lookup"><span data-stu-id="84744-103">COOKER\_VARIANCE</span></span>

<span data-ttu-id="84744-104">La formula del tipo di contatore della varianza del COOKer \_ fornisce la variabilità che consente di caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in un'istanza di [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="84744-104">The COOKER\_VARIANCE counter type formula provides variability that use to characterize dispersion for a set of raw observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) instance.</span></span> <span data-ttu-id="84744-105">La varianza viene calcolata dividendo la somma del quadrato della deviazione dalla media di ogni contatore per il numero di contatori.</span><span class="sxs-lookup"><span data-stu-id="84744-105">The variance is calculated by dividing the sum of the square of the deviation from the mean of each counter by the number of counters.</span></span> <span data-ttu-id="84744-106">In altre parole, la varianza corrisponde alla media delle deviazioni al quadrato dalla media per ogni contatore.</span><span class="sxs-lookup"><span data-stu-id="84744-106">In other words, the variance is the average of the squared deviations from the mean for each counter.</span></span> <span data-ttu-id="84744-107">Questo tipo di contatore viene definito solo all'interno di WMI e non è disponibile per le tecnologie di monitoraggio delle prestazioni, ad esempio i [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="84744-107">This counter type is defined only within WMI, and it is not available to the performance monitoring technologies, such as [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="84744-108">Per ulteriori informazioni sulla formula del tipo di contatore, vedere [tipi di contatori](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="84744-108">For more information about the counter type formula, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>

<span data-ttu-id="84744-109">Per ulteriori informazioni sui provider a prestazioni elevate e sullo scripting, vedere [tipi di contatori delle prestazioni WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="84744-109">For more information about high-performance providers and scripting, see [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

## <a name="example-code"></a><span data-ttu-id="84744-110">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="84744-110">Example Code</span></span>

<span data-ttu-id="84744-111">Per esempi di codice, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="84744-111">For code examples, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84744-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="84744-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84744-113">Tipi di contatori statistici</span><span class="sxs-lookup"><span data-stu-id="84744-113">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> <dt>

[<span data-ttu-id="84744-114">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="84744-114">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
