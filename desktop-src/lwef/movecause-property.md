---
title: Proprietà MoveCause
description: Proprietà MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856210"
---
# <a name="movecause-property"></a><span data-ttu-id="b580d-103">Proprietà MoveCause</span><span class="sxs-lookup"><span data-stu-id="b580d-103">MoveCause Property</span></span>

<span data-ttu-id="b580d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b580d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b580d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b580d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b580d-106">Restituisce un valore intero che specifica la causa dell'ultima spostamento del carattere.</span><span class="sxs-lookup"><span data-stu-id="b580d-106">Returns an integer value that specifies what caused the character's last move.</span></span>

</dd> <dt>

<span data-ttu-id="b580d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b580d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b580d-108">*agente*. **Caratteri ("***CharacterID***"). MoveCause**</span><span class="sxs-lookup"><span data-stu-id="b580d-108">*agent*.**Characters("***CharacterID***").MoveCause**</span></span>



| <span data-ttu-id="b580d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b580d-109">Value</span></span> | <span data-ttu-id="b580d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b580d-110">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b580d-111">0</span><span class="sxs-lookup"><span data-stu-id="b580d-111">0</span></span>     | <span data-ttu-id="b580d-112">Il carattere non è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="b580d-112">The character has not been moved.</span></span>                                                          |
| <span data-ttu-id="b580d-113">1</span><span class="sxs-lookup"><span data-stu-id="b580d-113">1</span></span>     | <span data-ttu-id="b580d-114">L'utente ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="b580d-114">The user moved the character.</span></span>                                                              |
| <span data-ttu-id="b580d-115">2</span><span class="sxs-lookup"><span data-stu-id="b580d-115">2</span></span>     | <span data-ttu-id="b580d-116">L'applicazione ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="b580d-116">Your application moved the character.</span></span>                                                      |
| <span data-ttu-id="b580d-117">3</span><span class="sxs-lookup"><span data-stu-id="b580d-117">3</span></span>     | <span data-ttu-id="b580d-118">Un'altra applicazione client ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="b580d-118">Another client application moved the character.</span></span>                                            |
| <span data-ttu-id="b580d-119">4</span><span class="sxs-lookup"><span data-stu-id="b580d-119">4</span></span>     | <span data-ttu-id="b580d-120">Il Server Agent ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b580d-120">The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b580d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b580d-121">Remarks</span></span>

<span data-ttu-id="b580d-122">È possibile usare questa proprietà per determinare la causa dello spostamento del carattere, quando più di un'applicazione condivide (ha caricato) lo stesso carattere.</span><span class="sxs-lookup"><span data-stu-id="b580d-122">You can use this property to determine what caused the character to move, when more than one application is sharing (has loaded) the same character.</span></span> <span data-ttu-id="b580d-123">Questi valori corrispondono a quelli restituiti dall'evento [**Move**](move-event.md) .</span><span class="sxs-lookup"><span data-stu-id="b580d-123">These values are the same as those returned by the [**Move**](move-event.md) event.</span></span>

## <a name="see-also"></a><span data-ttu-id="b580d-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b580d-124">See Also</span></span>

<span data-ttu-id="b580d-125">[**Evento Move**](move-event.md), [ **metodo MoveTo**](moveto-method.md)</span><span class="sxs-lookup"><span data-stu-id="b580d-125">[**Move event**](move-event.md), [**MoveTo method**](moveto-method.md)</span></span>


 

 




