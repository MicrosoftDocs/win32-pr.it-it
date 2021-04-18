---
description: A partire da Windows Vista, il provider WmiPerfInst fornisce dati del contatore delle prestazioni non elaborati e formattati dinamicamente alle classi del contatore delle prestazioni WMI derivate da \_ Perf Win32.
ms.assetid: 780f2564-73f8-46a7-99fe-9ea78b00dedb
ms.tgt_platform: multiple
title: Provider WmiPerfInst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374568de0780b18b1e3036eb7fc6ce7247b46039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310321"
---
# <a name="wmiperfinst-provider"></a><span data-ttu-id="6dade-103">Provider WmiPerfInst</span><span class="sxs-lookup"><span data-stu-id="6dade-103">WmiPerfInst Provider</span></span>

<span data-ttu-id="6dade-104">A partire da Windows Vista, il provider WmiPerfInst fornisce dati del contatore delle prestazioni non elaborati e formattati dinamicamente alle [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI derivate da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf).</span><span class="sxs-lookup"><span data-stu-id="6dade-104">Starting with Windows Vista, the WmiPerfInst provider supplies raw and formatted performance counter data dynamically to WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf).</span></span> <span data-ttu-id="6dade-105">Questo provider sostituisce il [provider di dati delle prestazioni formattato](formatted-performance-data-provider.md), noto anche come "provider di contatori cotti" e il [provider del contatore delle prestazioni](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6dade-105">This provider replaces the [Formatted Performance Data Provider](formatted-performance-data-provider.md), also known as the "Cooked Counter Provider", and the [Performance Counter Provider](performance-counter-provider.md).</span></span>

<span data-ttu-id="6dade-106">Il provider WmiPerfInst fornisce dati alle classi WMI fornite dal provider [wmiperfclass](wmiperfclass-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="6dade-106">The WmiPerfInst provider supplies data to the WMI classes that are provided by the [WMIPerfClass](wmiperfclass-provider.md) provider.</span></span> <span data-ttu-id="6dade-107">Questo provider è un bridge tra le istanze di PDH (Performance Data Helper) e le classi di prestazioni WMI fornite dal provider WmiPerfClass.</span><span class="sxs-lookup"><span data-stu-id="6dade-107">This provider is a bridge between Performance Data Helper (PDH) instances and the WMI performance classes supplied by the WmiPerfClass Provider.</span></span> <span data-ttu-id="6dade-108">Quando WmiPerfInst riceve una query per i dati, carica la classe e usa i [qualificatori](qualifiers-specific-to-wmi-performance-classes.md) della classe e della proprietà per individuare le istanze di PDH.</span><span class="sxs-lookup"><span data-stu-id="6dade-108">When WmiPerfInst receives a query for data, it loads the class and uses the class and property [qualifiers](qualifiers-specific-to-wmi-performance-classes.md) to locate the PDH instances.</span></span> <span data-ttu-id="6dade-109">Per ulteriori informazioni, vedere [utilizzo delle funzioni PDH per utilizzare i dati del contatore](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span><span class="sxs-lookup"><span data-stu-id="6dade-109">For more information, see [Using the PDH Functions to Consume Counter Data](/windows/desktop/PerfCtrs/using-the-pdh-functions-to-consume-counter-data).</span></span>

<span data-ttu-id="6dade-110">Non è consigliabile sviluppare nuovi oggetti prestazione creando un provider WMI a prestazioni elevate e dipendono dal processo di [*adattamento dell'adattatore ADAP*](gloss-r.md) per trasferire i dati alle librerie delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6dade-110">It is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries.</span></span> <span data-ttu-id="6dade-111">L'eccezione si verifica quando si sviluppa un driver Windows Driver Model e si desidera fornire dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6dade-111">The exception is when you are developing a Windows Driver Model driver and want to supply performance data.</span></span> <span data-ttu-id="6dade-112">Mentre il processo dell'adattatore inverso continua a funzionare per la compatibilità con le versioni precedenti, il metodo consigliato prevede l'uso dei [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="6dade-112">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="6dade-113">Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) di questo provider è "WmiPerfInst".</span><span class="sxs-lookup"><span data-stu-id="6dade-113">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfInst".</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dade-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6dade-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dade-115">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="6dade-115">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="6dade-116">Librerie di prestazioni e WMI</span><span class="sxs-lookup"><span data-stu-id="6dade-116">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="6dade-117">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="6dade-117">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
