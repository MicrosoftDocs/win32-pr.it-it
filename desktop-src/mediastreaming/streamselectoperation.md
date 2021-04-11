---
title: Classe StreamSelectOperation
description: Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetMuteAsync e fornisce un metodo che restituisce i risultati dell'operazione. | Classe StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API di streaming multimediale della classe StreamSelectOperation
- API di streaming multimediale della classe StreamSelectOperation, descritta
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234791"
---
# <a name="streamselectoperation-class"></a><span data-ttu-id="e463a-106">Classe StreamSelectOperation</span><span class="sxs-lookup"><span data-stu-id="e463a-106">StreamSelectOperation class</span></span>

<span data-ttu-id="e463a-107">Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) e fornisce un metodo che restituisce i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="e463a-107">Registers an event handler that is invoked when the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) completes, and provides a method that returns the results of the operation.</span></span>

<span data-ttu-id="e463a-108">**StreamSelectOperation** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e463a-108">**StreamSelectOperation** has these types of members:</span></span>

-   [<span data-ttu-id="e463a-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="e463a-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e463a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e463a-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e463a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="e463a-111">Methods</span></span>

<span data-ttu-id="e463a-112">La classe **StreamSelectOperation** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e463a-112">The **StreamSelectOperation** class has these methods.</span></span>



| <span data-ttu-id="e463a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="e463a-113">Method</span></span>                                                 | <span data-ttu-id="e463a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e463a-114">Description</span></span>                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e463a-115">**GetResults**</span><span class="sxs-lookup"><span data-stu-id="e463a-115">**GetResults**</span></span>](streamselectoperation-getresults.md) | <span data-ttu-id="e463a-116">Restituisce i risultati dell'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e463a-116">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="e463a-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e463a-117">Properties</span></span>

<span data-ttu-id="e463a-118">La classe **StreamSelectOperation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e463a-118">The **StreamSelectOperation** class has these properties.</span></span>



| <span data-ttu-id="e463a-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e463a-119">Property</span></span>                                                        | <span data-ttu-id="e463a-120">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="e463a-120">Access type</span></span>           | <span data-ttu-id="e463a-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e463a-121">Description</span></span>                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e463a-122">**Completi**</span><span class="sxs-lookup"><span data-stu-id="e463a-122">**Completed**</span></span>](streamselectoperation-completed.md)<br/> | <span data-ttu-id="e463a-123">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="e463a-123">Read/write</span></span><br/> | <span data-ttu-id="e463a-124">Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e463a-124">Gets or sets an event handler that is invoked when the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) is completed.</span></span><br/> |



 

 

