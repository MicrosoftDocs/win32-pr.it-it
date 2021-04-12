---
title: Proprietà VisibilityCause
description: Proprietà VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a6e21e2cda201f8d04837d2b10efc757b93f824
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396055"
---
# <a name="visibilitycause-property"></a><span data-ttu-id="2344c-103">Proprietà VisibilityCause</span><span class="sxs-lookup"><span data-stu-id="2344c-103">VisibilityCause Property</span></span>

<span data-ttu-id="2344c-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2344c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="2344c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2344c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="2344c-106">Restituisce un valore intero che specifica ciò che ha causato lo stato visibile del carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-106">Returns an integer value that specifies what caused the character's visible state.</span></span>

</dd> <dt>

<span data-ttu-id="2344c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="2344c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="2344c-108">*agente*. **Caratteri ("***CharacterID***"). VisibilityCause**</span><span class="sxs-lookup"><span data-stu-id="2344c-108">*agent*.**Characters("***CharacterID***").VisibilityCause**</span></span>



| <span data-ttu-id="2344c-109">Valore</span><span class="sxs-lookup"><span data-stu-id="2344c-109">Value</span></span> | <span data-ttu-id="2344c-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2344c-110">Description</span></span>                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2344c-111">0</span><span class="sxs-lookup"><span data-stu-id="2344c-111">0</span></span>     | <span data-ttu-id="2344c-112">Il carattere non è stato visualizzato.</span><span class="sxs-lookup"><span data-stu-id="2344c-112">The character has not been shown.</span></span>                                                                            |
| <span data-ttu-id="2344c-113">1</span><span class="sxs-lookup"><span data-stu-id="2344c-113">1</span></span>     | <span data-ttu-id="2344c-114">L'utente ha nascosto il carattere usando il comando nel menu di scelta rapida dell'icona della barra delle applicazioni del carattere o usando l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="2344c-114">User hid the character using the command on the character's taskbar icon pop-up menu or using speech input..</span></span> |
| <span data-ttu-id="2344c-115">2</span><span class="sxs-lookup"><span data-stu-id="2344c-115">2</span></span>     | <span data-ttu-id="2344c-116">L'utente ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-116">The user showed the character.</span></span>                                                                               |
| <span data-ttu-id="2344c-117">3</span><span class="sxs-lookup"><span data-stu-id="2344c-117">3</span></span>     | <span data-ttu-id="2344c-118">L'applicazione ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-118">Your application hid the character.</span></span>                                                                          |
| <span data-ttu-id="2344c-119">4</span><span class="sxs-lookup"><span data-stu-id="2344c-119">4</span></span>     | <span data-ttu-id="2344c-120">L'applicazione ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-120">Your application showed the character.</span></span>                                                                       |
| <span data-ttu-id="2344c-121">5</span><span class="sxs-lookup"><span data-stu-id="2344c-121">5</span></span>     | <span data-ttu-id="2344c-122">Un'altra applicazione client ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-122">Another client application hid the character.</span></span>                                                                |
| <span data-ttu-id="2344c-123">6</span><span class="sxs-lookup"><span data-stu-id="2344c-123">6</span></span>     | <span data-ttu-id="2344c-124">Un'altra applicazione client ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-124">Another client application showed the character.</span></span>                                                             |
| <span data-ttu-id="2344c-125">7</span><span class="sxs-lookup"><span data-stu-id="2344c-125">7</span></span>     | <span data-ttu-id="2344c-126">L'utente ha nascosto il carattere usando il comando nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-126">The user hid the character using the command on the character's pop-up menu.</span></span>                                 |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2344c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="2344c-127">Remarks</span></span>

<span data-ttu-id="2344c-128">È possibile usare questa proprietà per determinare cosa ha causato lo spostamento del carattere quando più di un'applicazione condivide (ha caricato) lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="2344c-128">You can use this property to determine what caused the character to move when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="2344c-129">Questi valori corrispondono a quelli restituiti dagli eventi [**show**](show-event.md) e [**Hide**](hide-event.md) .</span><span class="sxs-lookup"><span data-stu-id="2344c-129">These values are the same as those returned by the [**Show**](show-event.md) and [**Hide**](hide-event.md) events.</span></span>

## <a name="see-also"></a><span data-ttu-id="2344c-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2344c-130">See Also</span></span>

<span data-ttu-id="2344c-131">[**Nascondi evento**](hide-event.md), [**Mostra evento**](show-event.md), [**Nascondi metodo**](hide-method.md), [**Mostra metodo**](show-method.md)</span><span class="sxs-lookup"><span data-stu-id="2344c-131">[**Hide event**](hide-event.md), [**Show event**](show-event.md), [**Hide method**](hide-method.md), [**Show method**](show-method.md)</span></span>


 

 




