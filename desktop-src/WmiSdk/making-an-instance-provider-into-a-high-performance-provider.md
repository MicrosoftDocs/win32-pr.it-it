---
description: Non è consigliabile scrivere un provider WMI a prestazioni elevate per creare contatori delle prestazioni.
ms.assetid: 6a22d6f7-d9e2-45fa-876d-921a4bc4f574
ms.tgt_platform: multiple
title: Creazione di un provider di istanze in un provider di High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10744b110463a3207f76bb55d48a8045ec22783d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312692"
---
# <a name="making-an-instance-provider-into-a-high-performance-provider"></a><span data-ttu-id="8d69f-103">Creazione di un provider di istanze in un provider di High-Performance</span><span class="sxs-lookup"><span data-stu-id="8d69f-103">Making an Instance Provider into a High-Performance Provider</span></span>

<span data-ttu-id="8d69f-104">Non è consigliabile scrivere un provider WMI a prestazioni elevate per creare contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8d69f-104">Writing a WMI high-performance provider to create performance counters is not recommended.</span></span> <span data-ttu-id="8d69f-105">A partire da Windows Vista, le [classi del contatore delle prestazioni](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI non vengono più migrate nelle librerie delle prestazioni di Windows tramite l'adattatore inverso AutoDiscovery/AutoPurge (ADAP).</span><span class="sxs-lookup"><span data-stu-id="8d69f-105">Starting with Windows Vista, the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes) are no longer migrated into the Windows performance libraries by the AutoDiscovery/AutoPurge (ADAP) reverse adapter.</span></span> <span data-ttu-id="8d69f-106">Per creare un provider del contatore delle prestazioni, utilizzare i [contatori delle prestazioni versione 2,0](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="8d69f-106">To create a performance counter provider, use [Performance Counters Version 2.0](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span> <span data-ttu-id="8d69f-107">Dopo aver creato gli oggetti della libreria di prestazioni, il [provider WMIPerfClass](wmiperfclass-provider.md) analizza gli oggetti e crea o aggiorna una classe WMI derivata da [**\_ Perf Win32**](/windows/desktop/CIMWin32Prov/win32-perf) per ogni oggetto prestazione.</span><span class="sxs-lookup"><span data-stu-id="8d69f-107">After performance library objects are created, the [WMIPerfClass Provider](wmiperfclass-provider.md) parses the objects and creates or refreshes a WMI class derived from [**Win32\_Perf**](/windows/desktop/CIMWin32Prov/win32-perf) for each performance object.</span></span> <span data-ttu-id="8d69f-108">Il [provider WMIPerfInst](wmiperfinst-provider.md) fornisce quindi dinamicamente i dati dei contatori delle prestazioni non elaborati e formattati alle classi di prestazioni WMI.</span><span class="sxs-lookup"><span data-stu-id="8d69f-108">The [WMIPerfInst Provider](wmiperfinst-provider.md) then dynamically provides raw and formatted performance counter data to the WMI performance classes.</span></span>

<span data-ttu-id="8d69f-109">Nella procedura di alto livello riportata di seguito vengono illustrati i passaggi necessari per creare un provider a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="8d69f-109">The following high-level procedure provides the steps required to create a high-performance provider.</span></span>

<span data-ttu-id="8d69f-110">**Per creare un provider a prestazioni elevate**</span><span class="sxs-lookup"><span data-stu-id="8d69f-110">**To create a high-performance provider**</span></span>

1.  <span data-ttu-id="8d69f-111">Registrare il provider con WMI.</span><span class="sxs-lookup"><span data-stu-id="8d69f-111">Register your provider with WMI.</span></span> <span data-ttu-id="8d69f-112">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un provider di High-Performance](registering-a-high-performance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8d69f-112">For more information, see [Registering a High-Performance Provider](registering-a-high-performance-provider.md).</span></span>
2.  <span data-ttu-id="8d69f-113">Implementare il provider.</span><span class="sxs-lookup"><span data-stu-id="8d69f-113">Implement your provider.</span></span> <span data-ttu-id="8d69f-114">Per ulteriori informazioni, vedere [scrittura di un provider di istanze](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8d69f-114">For more information, see [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>
3.  <span data-ttu-id="8d69f-115">Implementare l'interfaccia a prestazioni elevate.</span><span class="sxs-lookup"><span data-stu-id="8d69f-115">Implement the high-performance interface.</span></span> <span data-ttu-id="8d69f-116">Per ulteriori informazioni, vedere [implementazione dell'interfaccia High-Performance](implementing-the-high-performance-interface.md).</span><span class="sxs-lookup"><span data-stu-id="8d69f-116">For more information, see [Implementing the High-Performance Interface](implementing-the-high-performance-interface.md).</span></span>
4.  <span data-ttu-id="8d69f-117">Derivare e scrivere lo schema di Managed Object Format (MOF) per ottenere i dati sulle prestazioni non elaborati.</span><span class="sxs-lookup"><span data-stu-id="8d69f-117">Derive and write your Managed Object Format (MOF) schema to obtain raw performance data.</span></span> <span data-ttu-id="8d69f-118">Per ulteriori informazioni, vedere [supporto della \_ classe Win32 PerfRawData](supporting-the-win32-perfrawdata-class.md).</span><span class="sxs-lookup"><span data-stu-id="8d69f-118">For more information, see [Supporting the Win32\_PerfRawData Class](supporting-the-win32-perfrawdata-class.md).</span></span>
5.  <span data-ttu-id="8d69f-119">Derivare e scrivere lo schema MOF per ottenere i dati precalcolati.</span><span class="sxs-lookup"><span data-stu-id="8d69f-119">Derive and write your MOF schema to obtain precalculated data.</span></span> <span data-ttu-id="8d69f-120">Grazie al supporto di questa classe, il provider non è necessario per eseguire i calcoli.</span><span class="sxs-lookup"><span data-stu-id="8d69f-120">By supporting this class, the provider is not required to perform the calculations.</span></span> <span data-ttu-id="8d69f-121">Questi dati saranno gli stessi visualizzati in monitoraggio di sistema in Perfmon.</span><span class="sxs-lookup"><span data-stu-id="8d69f-121">This data will be the same that appears in the System Monitor in Perfmon.</span></span> <span data-ttu-id="8d69f-122">Per ulteriori informazioni, vedere [supporto della \_ classe Win32 PerfFormattedData](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="8d69f-122">For more information, see [Supporting the Win32\_PerfFormattedData Class](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d69f-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d69f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d69f-124">Sviluppo di un provider WMI</span><span class="sxs-lookup"><span data-stu-id="8d69f-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="8d69f-125">Librerie di prestazioni e WMI</span><span class="sxs-lookup"><span data-stu-id="8d69f-125">Performance Libraries and WMI</span></span>](performance-libraries-and-wmi.md)
</dt> </dl>

 

 
