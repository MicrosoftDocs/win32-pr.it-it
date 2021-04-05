---
title: Mostra evento
description: Mostra evento
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6964164e14c759a971e5ceeda542a5c27131663
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855770"
---
# <a name="show-event"></a><span data-ttu-id="def04-103">Mostra evento</span><span class="sxs-lookup"><span data-stu-id="def04-103">Show Event</span></span>

<span data-ttu-id="def04-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="def04-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="def04-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="def04-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="def04-106">Si verifica quando viene visualizzato un carattere.</span><span class="sxs-lookup"><span data-stu-id="def04-106">Occurs when a character is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="def04-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="def04-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="def04-108">**Sub** *Agent \* \* \* \_ Show (ByVal* \*  *CharacterID*, **ByVal** *causare \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="def04-108">**Sub** *agent\*\*\*\_Show (ByVal*\* *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="def04-109">Parte</span><span class="sxs-lookup"><span data-stu-id="def04-109">Part</span></span>          | <span data-ttu-id="def04-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="def04-110">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def04-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="def04-111">*CharacterID*</span></span> | <span data-ttu-id="def04-112">Restituisce l'ID del carattere visualizzato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="def04-112">Returns the ID of the character shown as a string.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="def04-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="def04-113">*Cause*</span></span>       | <span data-ttu-id="def04-114">Restituisce un valore che indica ciò che ha causato la visualizzazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="def04-114">Returns a value that indicates what caused the character to display.</span></span> <span data-ttu-id="def04-115">2 l'utente ha visualizzato il carattere (usando il comando menu o Voice).</span><span class="sxs-lookup"><span data-stu-id="def04-115">2 The user showed the character (using the menu or voice command).</span></span><br/> <span data-ttu-id="def04-116">4 l'applicazione client ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="def04-116">4 Your client application showed the character.</span></span><br/> <span data-ttu-id="def04-117">6 un'altra applicazione client ha mostrato il carattere.</span><span class="sxs-lookup"><span data-stu-id="def04-117">6 Another client application showed the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="def04-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="def04-118">Remarks</span></span>

<span data-ttu-id="def04-119">Il server invia questo evento a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="def04-119">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="def04-120">Per eseguire una query sullo stato corrente del carattere, utilizzare la proprietà [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="def04-120">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="def04-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="def04-121">See Also</span></span>

<span data-ttu-id="def04-122">[**Nascondi evento**](hide-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="def04-122">[**Hide event**](hide-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





