---
description: Le interfacce CRM sono necessarie per fornire supporto per i ruoli di lavoro CRM e i compensatori CRM sviluppati con Visual Basic e Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfacce COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749007"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="108bd-103">Interfacce COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="108bd-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="108bd-104">Le interfacce CRM sono necessarie per fornire supporto per i ruoli di lavoro CRM e i compensatori CRM sviluppati con Visual Basic e Visual C++.</span><span class="sxs-lookup"><span data-stu-id="108bd-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="108bd-105">È possibile utilizzare il Gestione risorse di compensazione COM+ (CRM) per integrare in modo rapido e semplice le risorse dell'applicazione con le transazioni Microsoft Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="108bd-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="108bd-106">È più facile per i componenti scritti con Visual Basic per creare un record di log come una raccolta di varianti.</span><span class="sxs-lookup"><span data-stu-id="108bd-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="108bd-107">Inoltre, i componenti Visual Basic sono con threading Apartment, il che significa che deve essere possibile effettuare il marshalling delle interfacce dall'Apartment multithread a un Apartment a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="108bd-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="108bd-108">I componenti CRM sviluppati con Visual C++ possono anche usare il modello di threading dell'Apartment, sebbene sia consigliabile usare invece il modello di Threading.</span><span class="sxs-lookup"><span data-stu-id="108bd-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="108bd-109">Le interfacce descritte nella tabella seguente forniscono informazioni di riferimento dettagliate per gli sviluppatori di COM+ dispongono.</span><span class="sxs-lookup"><span data-stu-id="108bd-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="108bd-110">Interfacce CRM</span><span class="sxs-lookup"><span data-stu-id="108bd-110">CRM interfaces</span></span>                                             | <span data-ttu-id="108bd-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="108bd-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="108bd-112">**ICrmCompensator**</span><span class="sxs-lookup"><span data-stu-id="108bd-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="108bd-113">Questa interfaccia recapita i record di log non strutturati in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="108bd-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="108bd-114">**ICrmCompensatorVariants**</span><span class="sxs-lookup"><span data-stu-id="108bd-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="108bd-115">Questa interfaccia recapita i record di log strutturati al compensatore CRM quando si usa Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="108bd-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="108bd-116">**ICrmFormatLogRecords**</span><span class="sxs-lookup"><span data-stu-id="108bd-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="108bd-117">Questa interfaccia converte i record del log in formato visualizzabile in modo che possano essere presentati utilizzando uno strumento di monitoraggio generico.</span><span class="sxs-lookup"><span data-stu-id="108bd-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="108bd-118">**ICrmLogControl**</span><span class="sxs-lookup"><span data-stu-id="108bd-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="108bd-119">Questa interfaccia viene usata dal processo di lavoro CRM e dal compensatore CRM per scrivere record nel log e renderli durevoli.</span><span class="sxs-lookup"><span data-stu-id="108bd-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="108bd-120">**ICrmMonitor**</span><span class="sxs-lookup"><span data-stu-id="108bd-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="108bd-121">Questa interfaccia acquisisce uno snapshot dello stato corrente di un CRM e possiede un clerk CRM specifico.</span><span class="sxs-lookup"><span data-stu-id="108bd-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="108bd-122">**ICrmMonitorClerks**</span><span class="sxs-lookup"><span data-stu-id="108bd-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="108bd-123">Questa interfaccia ottiene informazioni sullo stato dei Clerk.</span><span class="sxs-lookup"><span data-stu-id="108bd-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="108bd-124">**ICrmMonitorLogRecords**</span><span class="sxs-lookup"><span data-stu-id="108bd-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="108bd-125">Questa interfaccia monitora i singoli record di log gestiti da uno specifico Clerk CRM per una determinata transazione.</span><span class="sxs-lookup"><span data-stu-id="108bd-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="108bd-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="108bd-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="108bd-127">Concetti Gestione risorse di compensazione COM+</span><span class="sxs-lookup"><span data-stu-id="108bd-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



