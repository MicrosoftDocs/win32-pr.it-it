---
title: Architettura WFP
description: In questa sezione viene fornita una breve panoramica dell'architettura di piattaforma filtro Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223849"
---
# <a name="wfp-architecture"></a><span data-ttu-id="3befb-103">Architettura WFP</span><span class="sxs-lookup"><span data-stu-id="3befb-103">WFP Architecture</span></span>

<span data-ttu-id="3befb-104">Nella figura seguente viene illustrata l'architettura di base di Windows Filtering Platform (PAM).</span><span class="sxs-lookup"><span data-stu-id="3befb-104">The following figure shows the basic architecture of the Windows Filtering Platform (WFP).</span></span>

![architettura di base del diagramma della piattaforma filtro Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a><span data-ttu-id="3befb-106">Motore di filtro</span><span class="sxs-lookup"><span data-stu-id="3befb-106">Filter Engine</span></span>

<span data-ttu-id="3befb-107">Il motore di filtro contiene un componente in modalità utente e un componente in modalità kernel, che insieme eseguono tutte le operazioni di filtro sui dati di rete.</span><span class="sxs-lookup"><span data-stu-id="3befb-107">The filter engine contains a user-mode component and a kernel-mode component, which together perform all of the filtering operations on network data.</span></span> <span data-ttu-id="3befb-108">Il motore di filtro contiene più livelli di filtro che vengono mappati in modo libero ai livelli dello stack di rete del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3befb-108">The filter engine contains multiple filtering layers that map loosely to the operating system's networking stack layers.</span></span> <span data-ttu-id="3befb-109">I livelli del motore di filtro sono divisi in livelli in modalità utente e livelli in modalità kernel basati sul componente del motore di filtro che li possiede.</span><span class="sxs-lookup"><span data-stu-id="3befb-109">The filter engine layers are divided into user-mode layers and kernel-mode layers based on the filter engine component that owns them.</span></span>

<span data-ttu-id="3befb-110">Il componente in modalità utente esegue il filtro RPC e IPsec.</span><span class="sxs-lookup"><span data-stu-id="3befb-110">The user-mode component performs RPC and IPsec filtering.</span></span> <span data-ttu-id="3befb-111">Il motore di filtro contiene circa 10 livelli di filtro in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="3befb-111">The filter engine contains approximately 10 user-mode filtering layers.</span></span>

<span data-ttu-id="3befb-112">Il componente in modalità kernel esegue il filtro ai livelli di rete e trasporto dello stack TC/IP.</span><span class="sxs-lookup"><span data-stu-id="3befb-112">The kernel-mode component performs filtering at the network and transport layers of the TC/IP stack.</span></span> <span data-ttu-id="3befb-113">Questo componente chiama anche le funzioni di callout disponibili durante il processo di [classificazione](basic-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="3befb-113">This component also calls the available callout functions during the [classification](basic-operation.md) process.</span></span> <span data-ttu-id="3befb-114">Il motore di filtro contiene circa 50 livelli di filtro in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="3befb-114">The filter engine contains approximately 50 kernel-mode filtering layers.</span></span>

<span data-ttu-id="3befb-115">Vedere [**filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md) per una descrizione di ognuno dei livelli del motore di filtro.</span><span class="sxs-lookup"><span data-stu-id="3befb-115">See [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md) for a description of each of the filter engine layers.</span></span>

## <a name="base-filtering-engine"></a><span data-ttu-id="3befb-116">Base Filtering Engine</span><span class="sxs-lookup"><span data-stu-id="3befb-116">Base Filtering Engine</span></span>

<span data-ttu-id="3befb-117">Il motore di filtro di base (BFE) è un servizio in modalità utente (bfe.dll in esecuzione in un processo di svchost.exe) che coordina i componenti Pam.</span><span class="sxs-lookup"><span data-stu-id="3befb-117">The Base Filtering Engine (BFE) is a user-mode service (bfe.dll running in a svchost.exe process) that coordinates the WFP components.</span></span> <span data-ttu-id="3befb-118">Le attività principali eseguite da BFE sono l'aggiunta e la rimozione di filtri dal sistema, l'archiviazione della configurazione del filtro e l'applicazione della sicurezza della configurazione di Pam.</span><span class="sxs-lookup"><span data-stu-id="3befb-118">The principal tasks performed by BFE are adding and removing filters from the system, storing filter configuration, and enforcing WFP configuration security.</span></span> <span data-ttu-id="3befb-119">Le applicazioni comunicano con BFE tramite le [funzioni di gestione del PAM](fwp-mgmt-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3befb-119">Applications communicate with BFE through the [WFP management functions](fwp-mgmt-functions.md).</span></span>

## <a name="callout-drivers"></a><span data-ttu-id="3befb-120">Driver di callout</span><span class="sxs-lookup"><span data-stu-id="3befb-120">Callout Drivers</span></span>

<span data-ttu-id="3befb-121">I driver di callout forniscono funzionalità di filtro aggiuntive aggiungendo funzioni di callout personalizzate al motore di filtro in uno o più livelli di filtro in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="3befb-121">Callout drivers provide additional filtering functionality by adding custom callout functions to the filter engine at one or more of the kernel-mode filtering layers.</span></span> <span data-ttu-id="3befb-122">I callout supportano l'ispezione approfondita e il pacchetto, nonché la modifica dei flussi.</span><span class="sxs-lookup"><span data-stu-id="3befb-122">Callouts support deep inspection and packet as well as stream modification.</span></span> <span data-ttu-id="3befb-123">Dopo che un driver di callout ha aggiunto le funzioni di callout al motore di filtro, è possibile aggiungere filtri che specificano la funzione di callout di un determinato driver al processo di filtraggio.</span><span class="sxs-lookup"><span data-stu-id="3befb-123">After a callout driver has added its callout functions to the filter engine, filters that specify a given driver's callout function can be added to the filtering process.</span></span> <span data-ttu-id="3befb-124">Tali filtri possono essere aggiunti da un'applicazione di gestione in modalità utente o dal driver di callout.</span><span class="sxs-lookup"><span data-stu-id="3befb-124">Such filters can be added by either a user-mode management application or by the callout driver itself.</span></span> <span data-ttu-id="3befb-125">L'interfaccia in modalità kernel, fornita in Windows Development Kit, deve essere utilizzata solo se necessario e non come sostituto per l'API in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="3befb-125">The kernel-mode interface, delivered in the Windows Development Kit, should only be used where needed and not as a substitute for the user-mode API.</span></span>

> [!Note]  
> <span data-ttu-id="3befb-126">Per ulteriori informazioni sui driver di callout, vedere la sezione Windows Filtering Platform di [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span><span class="sxs-lookup"><span data-stu-id="3befb-126">For more information on callout drivers, see the Windows Filtering Platform section of the [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).</span></span>

 

<span data-ttu-id="3befb-127">La piattaforma filtro Windows include una serie di funzioni di callout predefinite che possono essere utilizzate per la comunicazione dati protetta IPsec, le impostazioni di filtro con stato e il filtro in modalità stealth.</span><span class="sxs-lookup"><span data-stu-id="3befb-127">The Windows Filtering Platform includes a number of built-in callout functions that can be used for IPsec secure data communication, stateful filtering settings, and stealth-mode filtering.</span></span> <span data-ttu-id="3befb-128">Per un elenco completo delle funzioni di callout predefinite, vedere [**identificatori di callout predefiniti**](built-in-callout-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="3befb-128">See [**Built-in Callout Identifiers**](built-in-callout-identifiers.md) for a complete list of built-in callout functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3befb-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3befb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3befb-130">Modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="3befb-130">Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="3befb-131">Operazione PAM</span><span class="sxs-lookup"><span data-stu-id="3befb-131">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="3befb-132">Driver di callout della piattaforma filtro Windows-Guida alla progettazione</span><span class="sxs-lookup"><span data-stu-id="3befb-132">Windows Filtering Platform Callout Drivers - Design Guide</span></span>](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[<span data-ttu-id="3befb-133">Driver di callout della piattaforma filtro Windows-informazioni di riferimento</span><span class="sxs-lookup"><span data-stu-id="3befb-133">Windows Filtering Platform Callout Drivers - Reference</span></span>](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 