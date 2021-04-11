---
description: Notifica di CBasePin delle modifiche allo stato del filtro
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: Notifica di CBasePin delle modifiche allo stato del filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341751"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="aba49-103">Notifica di CBasePin delle modifiche allo stato del filtro</span><span class="sxs-lookup"><span data-stu-id="aba49-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="aba49-104">La classe **CBasePin** riceve una notifica ogni volta che lo stato del filtro proprietario viene modificato.</span><span class="sxs-lookup"><span data-stu-id="aba49-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="aba49-105">Per ogni transizione di stato, il filtro chiama un metodo corrispondente sul pin, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="aba49-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="aba49-106">Nuovo stato filtro</span><span class="sxs-lookup"><span data-stu-id="aba49-106">New Filter State</span></span> | <span data-ttu-id="aba49-107">Metodo CBasePin</span><span class="sxs-lookup"><span data-stu-id="aba49-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="aba49-108">Arrestato</span><span class="sxs-lookup"><span data-stu-id="aba49-108">Stopped</span></span>          | [<span data-ttu-id="aba49-109">**CBasePin:: inactive**</span><span class="sxs-lookup"><span data-stu-id="aba49-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="aba49-110">Paused</span><span class="sxs-lookup"><span data-stu-id="aba49-110">Paused</span></span>           | [<span data-ttu-id="aba49-111">**CBasePin:: Active**</span><span class="sxs-lookup"><span data-stu-id="aba49-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="aba49-112">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="aba49-112">Running</span></span>          | [<span data-ttu-id="aba49-113">**CBasePin:: Run**</span><span class="sxs-lookup"><span data-stu-id="aba49-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="aba49-114">La classe derivata deve eseguire l'override di questi metodi per rispondere alla modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="aba49-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="aba49-115">A seconda del filtro, il PIN potrebbe avviare un thread di lavoro che fornisce esempi, eseguire il commit o il decommit dell'allocatore di memoria e così via.</span><span class="sxs-lookup"><span data-stu-id="aba49-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



