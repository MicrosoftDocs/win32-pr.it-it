---
title: Evento BalloonShow
description: Evento BalloonShow
ms.assetid: 8a73e883-c003-480b-8a0a-e699caffe54c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de67318b02775619332fe60ea47fb27edb893c8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396511"
---
# <a name="balloonshow-event"></a><span data-ttu-id="fd74e-103">Evento BalloonShow</span><span class="sxs-lookup"><span data-stu-id="fd74e-103">BalloonShow Event</span></span>

<span data-ttu-id="fd74e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fd74e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fd74e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="fd74e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fd74e-106">Si verifica quando viene visualizzato il fumetto di parole di un carattere.</span><span class="sxs-lookup"><span data-stu-id="fd74e-106">Occurs when a character's word balloon is shown.</span></span>

</dd> <dt>

<span data-ttu-id="fd74e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="fd74e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fd74e-108">**Sub** *Agent* \_ **BalloonShow** **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="fd74e-108">**Sub** *agent*\_**BalloonShow** **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="fd74e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fd74e-109">Part</span></span>          | <span data-ttu-id="fd74e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd74e-110">Description</span></span>                                                       |
|---------------|-------------------------------------------------------------------|
| <span data-ttu-id="fd74e-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="fd74e-111">*CharacterID*</span></span> | <span data-ttu-id="fd74e-112">Restituisce l'ID del carattere associato alla parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="fd74e-112">Returns the ID of the character associated with the word balloon.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="fd74e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd74e-113">Remarks</span></span>

<span data-ttu-id="fd74e-114">Il server invia questo evento solo ai client del carattere (le applicazioni che hanno caricato il carattere) che utilizza la parola fumetto.</span><span class="sxs-lookup"><span data-stu-id="fd74e-114">The server sends this event only to the clients of the character (applications that have loaded the character) that uses the word balloon.</span></span>

### <a name="see-also"></a><span data-ttu-id="fd74e-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fd74e-115">See Also</span></span>

[<span data-ttu-id="fd74e-116">**Evento BalloonHide**</span><span class="sxs-lookup"><span data-stu-id="fd74e-116">**BalloonHide event**</span></span>](balloonhide-event.md)


 

 




