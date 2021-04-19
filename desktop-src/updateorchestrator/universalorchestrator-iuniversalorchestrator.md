---
title: Interfaccia IUniversalOrchestrator
description: Interfaccia COM che fornisce metodi per consentire a un client di comunicare con l'agente di orchestrazione universale.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/21/2021
ms.locfileid: "106320073"
---
# <a name="iuniversalorchestrator-interface"></a><span data-ttu-id="25e6d-103">Interfaccia IUniversalOrchestrator</span><span class="sxs-lookup"><span data-stu-id="25e6d-103">IUniversalOrchestrator interface</span></span>

> [!NOTE] 
> <span data-ttu-id="25e6d-104">Questa API appartiene all'API dell'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="25e6d-104">This API belongs to the Universal Orchestrator API.</span></span>

<span data-ttu-id="25e6d-105">**IUniversalOrchestrator** è un'interfaccia com che fornisce i metodi seguenti per consentire a un client di comunicare con l'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="25e6d-105">**IUniversalOrchestrator** is a COM interface that provides the following methods to allow a client to communicate with the Universal Orchestrator.</span></span>

## <a name="methods"></a><span data-ttu-id="25e6d-106">Metodi</span><span class="sxs-lookup"><span data-stu-id="25e6d-106">Methods</span></span>

|<span data-ttu-id="25e6d-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="25e6d-107">Method</span></span> | <span data-ttu-id="25e6d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25e6d-108">Description</span></span> |
|---|---|
|[<span data-ttu-id="25e6d-109">:: Pianificazioni</span><span class="sxs-lookup"><span data-stu-id="25e6d-109">::ScheduleWork</span></span>](universalorchestrator-schedulework.md) | <span data-ttu-id="25e6d-110">Registra il lavoro in sospeso con l'agente di orchestrazione universale.</span><span class="sxs-lookup"><span data-stu-id="25e6d-110">Registers pending work with the Universal Orchestrator.</span></span> |
|[<span data-ttu-id="25e6d-111">::WorkCompleted</span><span class="sxs-lookup"><span data-stu-id="25e6d-111">::WorkCompleted</span></span>](universalorchestrator-workcompleted.md) | <span data-ttu-id="25e6d-112">Informa l'agente di orchestrazione universale che tutto il lavoro è completo.</span><span class="sxs-lookup"><span data-stu-id="25e6d-112">Informs the Universal Orchestrator that all work is complete.</span></span> |
|[<span data-ttu-id="25e6d-113">::HasMoratoriumPassed</span><span class="sxs-lookup"><span data-stu-id="25e6d-113">::HasMoratoriumPassed</span></span>](universalorchestrator-hasmoratoriumpassed.md) | <span data-ttu-id="25e6d-114">Esegue una query sull'agente di orchestrazione universale per determinare se funziona immediatamente dopo la nuova esperienza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e6d-114">Queries Universal Orchestrator to determine if it is operating immediately after the new device Out of Box Experience.</span></span> |


## <a name="requirements"></a><span data-ttu-id="25e6d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25e6d-115">Requirements</span></span>

| <span data-ttu-id="25e6d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e6d-116">Requirement</span></span> | <span data-ttu-id="25e6d-117">Versione</span><span class="sxs-lookup"><span data-stu-id="25e6d-117">Version</span></span> |
|---|---|
| <span data-ttu-id="25e6d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25e6d-118">Minimum supported client</span></span> | <span data-ttu-id="25e6d-119">Windows 10 1903</span><span class="sxs-lookup"><span data-stu-id="25e6d-119">Windows 10 1903</span></span> |
|   |   |