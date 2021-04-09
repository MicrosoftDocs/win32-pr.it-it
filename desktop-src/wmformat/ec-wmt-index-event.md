---
title: EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)
description: '\_evento di \_ indice \_ WMT EC'
ms.assetid: 46e6a011-7f25-470b-9e10-fa59f0ddbf22
keywords:
- Windows Media Format SDK, EC_WMT_INDEX_EVENT
- DirectShow, EC_WMT_INDEX_EVENT
- EC_WMT_INDEX_EVENT
- Formato Advanced Systems (ASF), EC_WMT_INDEX_EVENT
- ASF (formato avanzato dei sistemi), EC_WMT_INDEX_EVENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34bca14ed02ac78fcfc77d1b9b716f75115a24f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047691"
---
# <a name="ec_wmt_index_event-windows-media-format-11-sdk"></a><span data-ttu-id="e0179-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="e0179-108">EC_WMT_INDEX_EVENT (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e0179-109">Inviato da Windows Media Format SDK quando un'applicazione usa il writer ASF per indicizzare i file Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="e0179-109">Sent by the Windows Media Format SDK when an application uses the ASF Writer to index Windows Media Video files.</span></span>

<span data-ttu-id="e0179-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0179-110">Parameters</span></span>

<span data-ttu-id="e0179-111">*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e0179-111">*lParam1*</span></span>

<span data-ttu-id="e0179-112">Può essere uno qualsiasi dei seguenti messaggi **di \_ stato di WMT** .</span><span class="sxs-lookup"><span data-stu-id="e0179-112">Can be any one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="e0179-113">Message</span><span class="sxs-lookup"><span data-stu-id="e0179-113">Message</span></span>              | <span data-ttu-id="e0179-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0179-114">Description</span></span>                                     |
|----------------------|-------------------------------------------------|
| <span data-ttu-id="e0179-115">WMT \_ avviato</span><span class="sxs-lookup"><span data-stu-id="e0179-115">WMT\_STARTED</span></span>         | <span data-ttu-id="e0179-116">L'indicizzazione è iniziata.</span><span class="sxs-lookup"><span data-stu-id="e0179-116">Indexing has begun.</span></span> <span data-ttu-id="e0179-117">*lParam2* è zero.</span><span class="sxs-lookup"><span data-stu-id="e0179-117">*lParam2* is zero.</span></span>          |
| <span data-ttu-id="e0179-118">WMT \_ chiuso</span><span class="sxs-lookup"><span data-stu-id="e0179-118">WMT\_CLOSED</span></span>          | <span data-ttu-id="e0179-119">L'indicizzazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e0179-119">Indexing has been completed.</span></span> <span data-ttu-id="e0179-120">*lParam2* è zero.</span><span class="sxs-lookup"><span data-stu-id="e0179-120">*lParam2* is zero.</span></span> |
| <span data-ttu-id="e0179-121">\_stato dell'indice WMT \_</span><span class="sxs-lookup"><span data-stu-id="e0179-121">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="e0179-122">L'indicizzazione è in corso.</span><span class="sxs-lookup"><span data-stu-id="e0179-122">Indexing is in progress.</span></span>                        |



 

<span data-ttu-id="e0179-123">*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e0179-123">*lParam2*</span></span>

<span data-ttu-id="e0179-124">Se *lParam1* è WMT \_ Closed o WMT \_ Started, *lParam2* è zero.</span><span class="sxs-lookup"><span data-stu-id="e0179-124">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="e0179-125">Se *lParam1* è \_ lo stato di avanzamento dell'indice WMT \_ , *lParam2* è un **DWORD** che esprime la quantità di avanzamento come percentuale delle dimensioni totali del download.</span><span class="sxs-lookup"><span data-stu-id="e0179-125">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that expresses the amount of progress as a percentage of the total download size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0179-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0179-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0179-127">**Informazioni di riferimento su DirectShow QASF**</span><span class="sxs-lookup"><span data-stu-id="e0179-127">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 




