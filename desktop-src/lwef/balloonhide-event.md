---
title: Evento BalloonHide
description: Evento BalloonHide
ms.assetid: dd1f3e83-f3d9-496e-9a54-b3a23b2403da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062a82afcabb3597ca8c254e039c231b52033657
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221955"
---
# <a name="balloonhide-event"></a><span data-ttu-id="bcdde-103">Evento BalloonHide</span><span class="sxs-lookup"><span data-stu-id="bcdde-103">BalloonHide Event</span></span>

<span data-ttu-id="bcdde-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bcdde-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="bcdde-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bcdde-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="bcdde-106">Si verifica quando il fumetto di parole di un carattere è nascosto.</span><span class="sxs-lookup"><span data-stu-id="bcdde-106">Occurs when a character's word balloon is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="bcdde-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="bcdde-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="bcdde-108">**Sub** *Agent* \_ **BalloonHide** **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="bcdde-108">**Sub** *agent*\_**BalloonHide** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="bcdde-109">Parte</span><span class="sxs-lookup"><span data-stu-id="bcdde-109">Part</span></span>          | <span data-ttu-id="bcdde-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcdde-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="bcdde-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="bcdde-111">*CharacterID*</span></span> | <span data-ttu-id="bcdde-112">Restituisce l'ID del carattere associato alla parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="bcdde-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="bcdde-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcdde-113">Remarks</span></span>

<span data-ttu-id="bcdde-114">Il server invia questo evento solo ai client del carattere (le applicazioni che hanno caricato il carattere) che utilizza la parola fumetto.</span><span class="sxs-lookup"><span data-stu-id="bcdde-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="bcdde-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bcdde-115">See Also</span></span>

[<span data-ttu-id="bcdde-116">**Evento BalloonShow**</span><span class="sxs-lookup"><span data-stu-id="bcdde-116">**BalloonShow event**</span></span>](balloonshow-event.md)


 

 




