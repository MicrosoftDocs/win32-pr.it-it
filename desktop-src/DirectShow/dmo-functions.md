---
description: DMO (funzioni)
ms.assetid: 0a380dc0-23f0-4ef0-898a-3b5afddf5eaa
title: DMO (funzioni)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f41750f5e442d93d3cacb2499bf2986a53cda6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480669"
---
# <a name="dmo-functions"></a><span data-ttu-id="55815-103">DMO (funzioni)</span><span class="sxs-lookup"><span data-stu-id="55815-103">DMO Functions</span></span>

<span data-ttu-id="55815-104">In questa sezione vengono descritte le funzioni DMO (Microsoft DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="55815-104">This section describes the Microsoft DirectX Media Object (DMO) functions.</span></span>



| <span data-ttu-id="55815-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="55815-105">Function</span></span>                                             | <span data-ttu-id="55815-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55815-106">Description</span></span>                                                   |
|------------------------------------------------------|---------------------------------------------------------------|
| [<span data-ttu-id="55815-107">**DMOEnum**</span><span class="sxs-lookup"><span data-stu-id="55815-107">**DMOEnum**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum)                           | <span data-ttu-id="55815-108">Enumera DMOs elencati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="55815-108">Enumerates DMOs listed in the registry.</span></span>                       |
| [<span data-ttu-id="55815-109">**DMOGetName**</span><span class="sxs-lookup"><span data-stu-id="55815-109">**DMOGetName**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogetname)                     | <span data-ttu-id="55815-110">Recupera il nome di un DMO dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="55815-110">Retrieves the name of a DMO from the registry.</span></span>                |
| [<span data-ttu-id="55815-111">**DMOGetTypes**</span><span class="sxs-lookup"><span data-stu-id="55815-111">**DMOGetTypes**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmogettypes)                   | <span data-ttu-id="55815-112">Recupera i tipi di supporto registrati per un DMO.</span><span class="sxs-lookup"><span data-stu-id="55815-112">Retrieves the media types registered for a DMO.</span></span>               |
| [<span data-ttu-id="55815-113">**DMORegister**</span><span class="sxs-lookup"><span data-stu-id="55815-113">**DMORegister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister)                   | <span data-ttu-id="55815-114">Registra un DMO.</span><span class="sxs-lookup"><span data-stu-id="55815-114">Registers a DMO.</span></span>                                              |
| [<span data-ttu-id="55815-115">**DMOUnregister**</span><span class="sxs-lookup"><span data-stu-id="55815-115">**DMOUnregister**</span></span>](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmounregister)               | <span data-ttu-id="55815-116">Annulla la registrazione di un DMO.</span><span class="sxs-lookup"><span data-stu-id="55815-116">Unregisters a DMO.</span></span>                                            |
| [<span data-ttu-id="55815-117">**MoCopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-117">**MoCopyMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocopymediatype)           | <span data-ttu-id="55815-118">Copia una struttura del tipo di supporto in un'altra.</span><span class="sxs-lookup"><span data-stu-id="55815-118">Copies one media type structure to another.</span></span>                   |
| [<span data-ttu-id="55815-119">**MoCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-119">**MoCreateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mocreatemediatype)       | <span data-ttu-id="55815-120">Alloca una nuova struttura del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="55815-120">Allocates a new media type structure.</span></span>                         |
| [<span data-ttu-id="55815-121">**MoDeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-121">**MoDeleteMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-modeletemediatype)       | <span data-ttu-id="55815-122">Elimina una struttura del tipo di supporto allocata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="55815-122">Deletes a media type structure that was previously allocated.</span></span> |
| [<span data-ttu-id="55815-123">**MoDuplicateMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-123">**MoDuplicateMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moduplicatemediatype) | <span data-ttu-id="55815-124">Duplica una struttura del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="55815-124">Duplicates a media type structure.</span></span>                            |
| [<span data-ttu-id="55815-125">**MoFreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-125">**MoFreeMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-mofreemediatype)           | <span data-ttu-id="55815-126">Libera i membri allocati di una struttura del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="55815-126">Frees the allocated members of a media type structure.</span></span>        |
| [<span data-ttu-id="55815-127">**MoInitMediaType**</span><span class="sxs-lookup"><span data-stu-id="55815-127">**MoInitMediaType**</span></span>](/previous-versions/windows/desktop/api/Dmort/nf-dmort-moinitmediatype)           | <span data-ttu-id="55815-128">Inizializza una struttura del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="55815-128">Initializes a media type structure.</span></span>                           |



 

## <a name="related-topics"></a><span data-ttu-id="55815-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55815-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55815-130">Guida di riferimento a DMO</span><span class="sxs-lookup"><span data-stu-id="55815-130">DMO Reference</span></span>](dmo-reference.md)
</dt> </dl>

 

 



