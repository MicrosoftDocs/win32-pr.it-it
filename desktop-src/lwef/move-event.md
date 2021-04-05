---
title: Sposta evento
description: Sposta evento
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856209"
---
# <a name="move-event"></a><span data-ttu-id="a945d-103">Sposta evento</span><span class="sxs-lookup"><span data-stu-id="a945d-103">Move Event</span></span>

<span data-ttu-id="a945d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a945d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a945d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="a945d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a945d-106">Si verifica quando viene spostato un carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-106">Occurs when a character is moved.</span></span>

</dd> <dt>

<span data-ttu-id="a945d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="a945d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a945d-108">Spostamento dell'agente **secondario**  \_ **(ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="a945d-108">**Sub** *agent*\_**Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="a945d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="a945d-109">Part</span></span>          | <span data-ttu-id="a945d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a945d-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a945d-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="a945d-111">*CharacterID*</span></span> | <span data-ttu-id="a945d-112">Restituisce l'ID del carattere spostato.</span><span class="sxs-lookup"><span data-stu-id="a945d-112">Returns the ID of the character that moved.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a945d-113">*X*</span><span class="sxs-lookup"><span data-stu-id="a945d-113">*X*</span></span>           | <span data-ttu-id="a945d-114">Restituisce la coordinata x (in pixel) del bordo superiore della nuova posizione del frame di caratteri come valore integer.</span><span class="sxs-lookup"><span data-stu-id="a945d-114">Returns the x-coordinate (in pixels) of the top edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="a945d-115">*S*</span><span class="sxs-lookup"><span data-stu-id="a945d-115">*Y*</span></span>           | <span data-ttu-id="a945d-116">Restituisce la coordinata y (in pixel) del bordo sinistro della nuova posizione del frame di caratteri come valore integer.</span><span class="sxs-lookup"><span data-stu-id="a945d-116">Returns the y-coordinate (in pixels) of the left edge of character frame's new location as an integer.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="a945d-117">*Causa*</span><span class="sxs-lookup"><span data-stu-id="a945d-117">*Cause*</span></span>       | <span data-ttu-id="a945d-118">Restituisce un valore che indica la causa dello spostamento del carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-118">Returns a value that indicates what caused the character to move.</span></span> <span data-ttu-id="a945d-119">1 l'utente ha trascinato il carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-119">1 The user dragged the character.</span></span><br/> <span data-ttu-id="a945d-120">2 l'applicazione client ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-120">2 Your client application moved the character.</span></span><br/> <span data-ttu-id="a945d-121">3 un'altra applicazione client ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-121">3 Another client application moved the character.</span></span><br/> <span data-ttu-id="a945d-122">4 il server agente ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a945d-122">4 The Agent server moved the character to keep it onscreen after a screen resolution change.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="a945d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="a945d-123">Remarks</span></span>

<span data-ttu-id="a945d-124">Questo evento si verifica quando l'utente o un'applicazione modifica la posizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-124">This event occurs when the user or an application changes the character's position.</span></span> <span data-ttu-id="a945d-125">Le coordinate sono rilevanti per l'angolo superiore sinistro dello schermo.</span><span class="sxs-lookup"><span data-stu-id="a945d-125">Coordinates are relevant to the upper left corner of the screen.</span></span> <span data-ttu-id="a945d-126">Questo evento viene inviato solo ai client del carattere, ovvero le applicazioni che hanno caricato il carattere.</span><span class="sxs-lookup"><span data-stu-id="a945d-126">This event is sent only to the clients of the character (applications that have loaded the character).</span></span>

<span data-ttu-id="a945d-127">**Vedere anche**</span><span class="sxs-lookup"><span data-stu-id="a945d-127">**See Also**</span></span>

<span data-ttu-id="a945d-128">[**Proprietà MoveCause**](movecause-property.md), [ **evento size**](size-event.md)</span><span class="sxs-lookup"><span data-stu-id="a945d-128">[**MoveCause property**](movecause-property.md), [**Size event**](size-event.md)</span></span>

 

 





