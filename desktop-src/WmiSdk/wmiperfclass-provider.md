---
description: A partire da Windows Vista, questo provider crea le classi del contatore delle prestazioni WMI.
ms.assetid: 5bb3d5e0-cdeb-4fea-a8ca-cf934e056206
ms.tgt_platform: multiple
title: Provider WmiPerfClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941422211ac9892406181ac0271e0d50239eef1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050118"
---
# <a name="wmiperfclass-provider"></a><span data-ttu-id="11637-103">Provider WmiPerfClass</span><span class="sxs-lookup"><span data-stu-id="11637-103">WmiPerfClass Provider</span></span>

<span data-ttu-id="11637-104">A partire da Windows Vista, questo provider crea le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="11637-104">Starting with Windows Vista, this provider creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="11637-105">I dati vengono forniti dinamicamente a queste classi di prestazioni WMI dal provider [wmiperfinst](wmiperfinst-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="11637-105">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst](wmiperfinst-provider.md) provider.</span></span> <span data-ttu-id="11637-106">Il processo di individuazione automatica/AutoPurge (ADAP) non trasferisce più gli oggetti contatore delle prestazioni in classi di prestazioni WMI nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="11637-106">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="11637-107">Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="11637-107">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="11637-108">Per ulteriori informazioni, vedere [librerie di prestazioni e WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="11637-108">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

<span data-ttu-id="11637-109">Sebbene non sia consigliabile sviluppare nuovi oggetti prestazione creando un provider WMI a prestazioni elevate e dipendono dal processo di [*adattamento dell'adattatore ADAP*](gloss-r.md) per trasferire i dati alle librerie di prestazioni, l'eccezione riguarda lo sviluppo di un driver Windows Driver Model che fornisce dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="11637-109">While it is not recommended that you develop new performance objects by creating a WMI high-performance provider and depend on the [*ADAP reverse adapter*](gloss-r.md) process to transfer the data to the performance libraries, the exception is development of a Windows Driver Model driver that supplies performance data.</span></span> <span data-ttu-id="11637-110">Mentre il processo dell'adattatore inverso continua a funzionare per la compatibilità con le versioni precedenti, il metodo consigliato prevede l'uso dei [contatori delle prestazioni versione 6,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="11637-110">While the reverse adapter process continues to work for backward compatibility, the recommended method is to use [Performance Counters Version 6.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

<span data-ttu-id="11637-111">Il nome dell'istanza di [**\_ \_ Win32Provider**](--win32provider.md) di questo provider è "wmiperfclass".</span><span class="sxs-lookup"><span data-stu-id="11637-111">The [**\_\_Win32Provider**](--win32provider.md) instance name of this provider is "WmiPerfClass".</span></span>

## <a name="related-topics"></a><span data-ttu-id="11637-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11637-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11637-113">Provider WMI</span><span class="sxs-lookup"><span data-stu-id="11637-113">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="11637-114">Librerie di prestazioni e WMI</span><span class="sxs-lookup"><span data-stu-id="11637-114">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="11637-115">Monitoraggio dei dati sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="11637-115">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

 
