---
description: I provider di pacchetti di rete (centrali) forniscono interfacce COM chiamate da applicazioni NPP e Network Monitor.
ms.assetid: 101ce722-3101-4f50-b492-dad8b68a7aaf
title: Interfacce NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3146d34798c57aea0bbd0f4bfec0037ed2ac879c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308161"
---
# <a name="npp-interfaces"></a><span data-ttu-id="cd288-103">Interfacce NPP</span><span class="sxs-lookup"><span data-stu-id="cd288-103">NPP Interfaces</span></span>

<span data-ttu-id="cd288-104">I provider di pacchetti di rete (centrali) forniscono interfacce COM chiamate da applicazioni NPP e Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="cd288-104">Network packet providers (NPPs) provide COM interfaces that are called by NPP applications, and Network Monitor.</span></span> <span data-ttu-id="cd288-105">Quando si chiama [CreateNPPInterface](createnppinterface.md), tenere presente che ogni npp è rappresentato come un singolo oggetto com in-process.</span><span class="sxs-lookup"><span data-stu-id="cd288-105">When you call [CreateNPPInterface](createnppinterface.md), remember that each NPP is represented as a single in-process COM object.</span></span> <span data-ttu-id="cd288-106">Le applicazioni possono creare un'istanza di un numero qualsiasi di oggetti NPP.</span><span class="sxs-lookup"><span data-stu-id="cd288-106">Applications can instantiate any number of NPP objects.</span></span> <span data-ttu-id="cd288-107">Tuttavia, ogni oggetto di cui è stata creata un'istanza deve utilizzarne uno, e solo uno, delle cinque interfacce NPP.</span><span class="sxs-lookup"><span data-stu-id="cd288-107">However, each instantiated object must use one—and only one—of the five NPP interfaces.</span></span>

<span data-ttu-id="cd288-108">Si noti inoltre che diverse interfacce NPP forniscono dati di rete in vari formati.</span><span class="sxs-lookup"><span data-stu-id="cd288-108">Note also that different NPP interfaces provide network data in various forms.</span></span> <span data-ttu-id="cd288-109">Ad esempio, Network Monitor usa l'interfaccia **IDelaydC** per acquisire il traffico di rete e salvarlo in un file di acquisizione. mentre i monitoraggi usano l'interfaccia **IRTC** per acquisire il traffico di rete in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="cd288-109">For example, Network Monitor uses the **IDelaydC** interface to capture network traffic and save it to a capture file; while monitors use the **IRTC** interface to capture real time network traffic.</span></span> <span data-ttu-id="cd288-110">Nella tabella seguente vengono descritte Network Monitor le interfacce NPP.</span><span class="sxs-lookup"><span data-stu-id="cd288-110">The following table describes Network Monitor NPP interfaces.</span></span>



| <span data-ttu-id="cd288-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="cd288-111">Interface</span></span>                | <span data-ttu-id="cd288-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd288-112">Description</span></span>                                                                                                                                                         |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd288-113">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="cd288-113">IDelaydC</span></span>](idelaydc.md) | <span data-ttu-id="cd288-114">Acquisisce il traffico di rete archiviato in un file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="cd288-114">Captures network traffic that is stored in a capture file.</span></span> <span data-ttu-id="cd288-115">Questa interfaccia viene utilizzata dalle applicazioni Network Monitor e NPP.</span><span class="sxs-lookup"><span data-stu-id="cd288-115">This interface is used by Network Monitor and NPP applications.</span></span>                                          |
| [<span data-ttu-id="cd288-116">IESP</span><span class="sxs-lookup"><span data-stu-id="cd288-116">IESP</span></span>](iesp.md)         | <span data-ttu-id="cd288-117">Acquisisce il traffico di rete archiviato in un file di acquisizione e fornisce statistiche avanzate in un formato di file ESP speciale.</span><span class="sxs-lookup"><span data-stu-id="cd288-117">Captures network traffic that is stored in a capture file and provides enhanced statistics in a special ESP file format.</span></span> <span data-ttu-id="cd288-118">Questa interfaccia viene utilizzata dalle applicazioni NPP</span><span class="sxs-lookup"><span data-stu-id="cd288-118">This interface is used by NPP applications</span></span> |
| [<span data-ttu-id="cd288-119">IRTC</span><span class="sxs-lookup"><span data-stu-id="cd288-119">IRTC</span></span>](irtc.md)         | <span data-ttu-id="cd288-120">Acquisisce il traffico di rete in tempo reale e attiva gli eventi quando si verificano.</span><span class="sxs-lookup"><span data-stu-id="cd288-120">Captures real time network traffic and triggers events when they occur.</span></span> <span data-ttu-id="cd288-121">Questa interfaccia viene utilizzata dai [*monitoraggi*](m.md) e dalle applicazioni NPP.</span><span class="sxs-lookup"><span data-stu-id="cd288-121">This interface is used by [*monitors*](m.md) and NPP applications.</span></span>     |
| [<span data-ttu-id="cd288-122">IStats</span><span class="sxs-lookup"><span data-stu-id="cd288-122">IStats</span></span>](istats.md)     | <span data-ttu-id="cd288-123">Recupera le statistiche come dati non elaborati anziché come frame.</span><span class="sxs-lookup"><span data-stu-id="cd288-123">Retrieves statistics as raw data rather than frames.</span></span> <span data-ttu-id="cd288-124">Questa interfaccia viene utilizzata dalle applicazioni NPP come [*PerfMon*](p.md).</span><span class="sxs-lookup"><span data-stu-id="cd288-124">This interface is used by NPP applications such as [*Perfmon*](p.md).</span></span>                     |



 

 

 



