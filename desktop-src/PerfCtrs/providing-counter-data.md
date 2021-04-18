---
description: In Windows Vista, i contatori delle prestazioni implementavano una nuova architettura (versione 2,0) per fornire i dati dei contatori.
ms.assetid: c17eda2f-3cf8-40d6-8be6-c1ce190d1a26
title: Fornire dati del contatore
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: ed5aa4cc505baab9e15d3f69c3fb466712eddbfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312092"
---
# <a name="providing-counter-data"></a><span data-ttu-id="338a8-103">Fornire dati del contatore</span><span class="sxs-lookup"><span data-stu-id="338a8-103">Providing Counter Data</span></span>

<span data-ttu-id="338a8-104">I componenti software che pubblicano i dati tramite i contatori delle prestazioni di Windows sono detti provider di dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="338a8-104">Software components that publish data via Windows Performance Counters are called performance data providers.</span></span>

<span data-ttu-id="338a8-105">Windows supporta due tipi di provider di dati sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="338a8-105">Windows supports two kinds of performance data providers.</span></span> <span data-ttu-id="338a8-106">I provider di dati delle prestazioni legacy (**V1 provider**) vengono implementati mediante un. File INI e DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="338a8-106">Legacy performance data providers (**V1 providers**) are implemented using an .INI file and a performance DLL.</span></span> <span data-ttu-id="338a8-107">I provider di dati delle prestazioni moderni (**provider v2**) usano un. MAN (manifesto XML) e API del provider del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="338a8-107">Modern performance data providers (**V2 providers**) use a .MAN (XML manifest) and the performance counter provider APIs.</span></span>

## <a name="manifests"></a><span data-ttu-id="338a8-108">Manifesti</span><span class="sxs-lookup"><span data-stu-id="338a8-108">Manifests</span></span>

<span data-ttu-id="338a8-109">I provider di dati delle prestazioni moderni usano un. MAN (manifesto XML) per definire i dati del contatore e utilizzare le API del provider del contatore delle prestazioni per gestire i dati all'interno del contesto del provider.</span><span class="sxs-lookup"><span data-stu-id="338a8-109">Modern performance data providers use a .MAN (XML manifest) to define the counter data and use performance counter provider APIs to manage data within the context of the provider.</span></span>

<span data-ttu-id="338a8-110">I provider implementati utilizzando un manifesto e le API del provider del contatore delle prestazioni vengono spesso chiamati **provider v2**.</span><span class="sxs-lookup"><span data-stu-id="338a8-110">Providers implemented using a manifest and performance counter provider APIs are often called **V2 providers**.</span></span>

<span data-ttu-id="338a8-111">Windows supporta i provider v2 in modalità utente in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="338a8-111">Windows supports user-mode V2 providers on Windows Vista or later.</span></span> <span data-ttu-id="338a8-112">Per informazioni dettagliate sulla modalità utente, vedere la pagina relativa alla [fornitura di dati del contatore con la versione 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="338a8-112">For user-mode details, see [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>

<span data-ttu-id="338a8-113">Windows supporta i provider v2 in modalità kernel in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="338a8-113">Windows supports kernel-mode V2 providers on Windows 7 or later.</span></span> <span data-ttu-id="338a8-114">Per informazioni dettagliate sulla modalità kernel, vedere [monitoraggio delle prestazioni in modalità kernel](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span><span class="sxs-lookup"><span data-stu-id="338a8-114">For kernel-mode details, see [Kernel Mode Performance Monitoring](/windows-hardware/drivers/devtest/kernel-mode-performance-monitoring).</span></span>

## <a name="performance-dll-deprecated"></a><span data-ttu-id="338a8-115">DLL prestazioni (deprecata)</span><span class="sxs-lookup"><span data-stu-id="338a8-115">Performance DLL (deprecated)</span></span>

<span data-ttu-id="338a8-116">Nell'architettura del contatore delle prestazioni legacy, i provider implementavano una DLL di prestazioni in che veniva eseguita nel processo del consumer per raccogliere e fornire i dati del contatore quando un consumer lo ha richiesto.</span><span class="sxs-lookup"><span data-stu-id="338a8-116">In the legacy performance counter architecture, providers implemented a performance DLL to that ran in the consumer's process to collect and provide the counter data when a consumer requested it.</span></span> <span data-ttu-id="338a8-117">Il provider ha utilizzato un'inizializzazione (. INI) e le voci del registro di sistema per definire i contatori e configurare la DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="338a8-117">The provider used an initialization (.INI) file and registry entries to define the counters and to configure the performance DLL.</span></span>

<span data-ttu-id="338a8-118">Provider implementati utilizzando un oggetto. Il file INI e una DLL di prestazioni sono spesso denominati **provider v1**.</span><span class="sxs-lookup"><span data-stu-id="338a8-118">Providers implemented using an .INI file and a performance DLL are often called **V1 providers**.</span></span>

> [!CAUTION]
> <span data-ttu-id="338a8-119">Sebbene sia comunque possibile utilizzare una DLL di prestazioni per fornire i dati dei contatori, questa architettura è deprecata a causa di limitazioni significative in merito a prestazioni e affidabilità.</span><span class="sxs-lookup"><span data-stu-id="338a8-119">Although you can still use a performance DLL to provide counter data, this architecture is deprecated due to significant performance and reliability limitations.</span></span> <span data-ttu-id="338a8-120">Inoltre, i provider v1 sono spesso più difficili da implementare perché richiedono la distribuzione di una DLL separata che deve essere eseguita nel processo del consumer.</span><span class="sxs-lookup"><span data-stu-id="338a8-120">In addition, V1 providers are often harder to implement since they require shipping a separate DLL that must run in the consumer's process.</span></span>

<span data-ttu-id="338a8-121">Per informazioni dettagliate, vedere [fornire dati del contatore tramite una DLL di prestazioni](providing-counter-data-using-a-performance-dll.md).</span><span class="sxs-lookup"><span data-stu-id="338a8-121">For details, see [Providing Counter Data Using a Performance DLL](providing-counter-data-using-a-performance-dll.md).</span></span>
