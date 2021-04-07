---
description: Le prestazioni di WMI ad alte prestazioni formattate provider di dati calcolano i tipi di contatori statistici su un numero specificato di campioni di dati del contatore non elaborati.
ms.assetid: a7e32ef2-fad1-449c-beee-07db4b93e3fe
ms.tgt_platform: multiple
title: Tipi di contatori statistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb97224b06881cbc3c8b1375c04a4df5be1095f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057859"
---
# <a name="statistical-counter-types"></a><span data-ttu-id="b36e7-103">Tipi di contatori statistici</span><span class="sxs-lookup"><span data-stu-id="b36e7-103">Statistical Counter Types</span></span>

<span data-ttu-id="b36e7-104">Le prestazioni di WMI ad alte prestazioni [formattate provider di dati](formatted-performance-data-provider.md) calcolano i tipi di contatori statistici su un numero specificato di campioni di dati del contatore non elaborati.</span><span class="sxs-lookup"><span data-stu-id="b36e7-104">The WMI high-performance [Formatted Performance Data Provider](formatted-performance-data-provider.md) calculates the statistical counter types on a specified number of raw counter data samples.</span></span> <span data-ttu-id="b36e7-105">Gli algoritmi per i tipi di contatore non richiedono proprietà timestamp o Frequency ereditate, ad esempio **timestamp \_ PerfTime** o **Frequency \_ PerfTime**, che altri tipi di contatori richiedono.</span><span class="sxs-lookup"><span data-stu-id="b36e7-105">The algorithms for the counter types do not require inherited timestamp or frequency properties (such as **TimeStamp\_PerfTime** or **Frequency\_PerfTime**) that other counter types require.</span></span>

<span data-ttu-id="b36e7-106">I tipi di contatori statistici supportano invece un **qualificatore** che identifica il numero di campioni da usare.</span><span class="sxs-lookup"><span data-stu-id="b36e7-106">Instead, the statistical counter types support a **qualifier** that identifies how many samples to use.</span></span> <span data-ttu-id="b36e7-107">Un esempio viene raccolto quando viene chiamato il metodo [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) per l'oggetto prestazione.</span><span class="sxs-lookup"><span data-stu-id="b36e7-107">A sample is collected when the [**Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh) method is called for the performance object.</span></span> <span data-ttu-id="b36e7-108">Per gli script, usare il metodo [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="b36e7-108">For scripts use the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method.</span></span> <span data-ttu-id="b36e7-109">I dati calcolati contengono il risultato del calcolo eseguito sul numero di campioni **SampleWindow** dalla proprietà dati non elaborati.</span><span class="sxs-lookup"><span data-stu-id="b36e7-109">The calculated data contains the result of the calculation performed on the **SampleWindow** number of samples from the raw data property.</span></span> <span data-ttu-id="b36e7-110">I dati non elaborati per il calcolo risultano frm il nome della proprietà specificato nel qualificatore del **contatore** .</span><span class="sxs-lookup"><span data-stu-id="b36e7-110">The raw data for the calculation comes frm the property name specified in the **Counter** qualifier.</span></span>

<span data-ttu-id="b36e7-111">Per ulteriori informazioni, vedere [ottenere dati statistici sulle prestazioni](obtaining-statistical-performance-data.md) e [accedere alle classi di prestazioni preinstallate WMI](accessing-wmi-preinstalled-performance-classes.md).</span><span class="sxs-lookup"><span data-stu-id="b36e7-111">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Accessing WMI Preinstalled Performance Classes](accessing-wmi-preinstalled-performance-classes.md).</span></span>



| <span data-ttu-id="b36e7-112">Costante CounterType</span><span class="sxs-lookup"><span data-stu-id="b36e7-112">CounterType Constant</span></span>                    | <span data-ttu-id="b36e7-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b36e7-113">Description</span></span>                                                                                                                                                                                |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b36e7-114">media COOKer \_</span><span class="sxs-lookup"><span data-stu-id="b36e7-114">COOKER\_AVERAGE</span></span>](cooker-average.md)   | <span data-ttu-id="b36e7-115">Somma le osservazioni ripetute di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e divide la somma per il numero di osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b36e7-115">Sums repeated observations of one property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class and divides the sum by the number of observations.</span></span>                              |
| [<span data-ttu-id="b36e7-116">massimo COOKer \_</span><span class="sxs-lookup"><span data-stu-id="b36e7-116">COOKER\_MAX</span></span>](cooker-max.md)           | <span data-ttu-id="b36e7-117">Valore più grande da un set di osservazioni di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="b36e7-117">Largest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                    |
| [<span data-ttu-id="b36e7-118">MIN COOKer \_</span><span class="sxs-lookup"><span data-stu-id="b36e7-118">COOKER\_MIN</span></span>](cooker-min.md)           | <span data-ttu-id="b36e7-119">Valore più piccolo da un set di osservazioni di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="b36e7-119">Smallest value from a set of observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>                                                                   |
| [<span data-ttu-id="b36e7-120">intervallo di cottura \_</span><span class="sxs-lookup"><span data-stu-id="b36e7-120">COOKER\_RANGE</span></span>](cooker-range.md)       | <span data-ttu-id="b36e7-121">Differenza tra i valori [minimo](cooker-min.md) e [massimo](cooker-max.md) per un set di osservazioni non elaborate di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="b36e7-121">Difference between the [Min](cooker-min.md) and [Max](cooker-max.md) values for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span> |
| [<span data-ttu-id="b36e7-122">varianza del COOKer \_</span><span class="sxs-lookup"><span data-stu-id="b36e7-122">COOKER\_VARIANCE</span></span>](cooker-variance.md) | <span data-ttu-id="b36e7-123">Misura della variabilità che può essere usata per caratterizzare la dispersione per un set di osservazioni non elaborate di una proprietà in una classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="b36e7-123">Measure of variability that can be used to characterize dispersion for a set of raw observations of a property in a [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="b36e7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b36e7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36e7-125">Tipi di contatori delle prestazioni WMI</span><span class="sxs-lookup"><span data-stu-id="b36e7-125">WMI Performance Counter Types</span></span>](wmi-performance-counter-types.md)
</dt> <dt>

[<span data-ttu-id="b36e7-126">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="b36e7-126">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="b36e7-127">Aggiornamento dei dati WMI negli script</span><span class="sxs-lookup"><span data-stu-id="b36e7-127">Refreshing WMI Data in Scripts</span></span>](refreshing-wmi-data-in-scripts.md)
</dt> <dt>

[<span data-ttu-id="b36e7-128">Accesso ai dati sulle prestazioni nello script</span><span class="sxs-lookup"><span data-stu-id="b36e7-128">Accessing Performance Data in Script</span></span>](accessing-performance-data-in-script.md)
</dt> <dt>

[<span data-ttu-id="b36e7-129">Accesso ai dati sulle prestazioni in C++</span><span class="sxs-lookup"><span data-stu-id="b36e7-129">Accessing Performance Data in C++</span></span>](accessing-performance-data-in-c--.md)
</dt> </dl>

 

 
