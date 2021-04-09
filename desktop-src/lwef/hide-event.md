---
title: Nascondi evento
description: Nascondi evento
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d396fb0985cd4c3c2e9647dfe0e7c9126ad9c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856229"
---
# <a name="hide-event"></a><span data-ttu-id="af8cb-103">Nascondi evento</span><span class="sxs-lookup"><span data-stu-id="af8cb-103">Hide Event</span></span>

<span data-ttu-id="af8cb-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af8cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="af8cb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="af8cb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="af8cb-106">Si verifica quando un carattere è nascosto.</span><span class="sxs-lookup"><span data-stu-id="af8cb-106">Occurs when a character is hidden.</span></span>

</dd> <dt>

<span data-ttu-id="af8cb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="af8cb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="af8cb-108">**Sub** *Agent \* \* \* \_ Hide (* \*  **ByVal** *CharacterID*, **ByVal** *cause \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="af8cb-108">**Sub** *agent\*\*\*\_Hide(*\* **ByVal** *CharacterID*, **ByVal** *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="af8cb-109">Parte</span><span class="sxs-lookup"><span data-stu-id="af8cb-109">Part</span></span>          | <span data-ttu-id="af8cb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af8cb-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af8cb-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="af8cb-111">*CharacterID*</span></span> | <span data-ttu-id="af8cb-112">Restituisce l'ID del carattere nascosto sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="af8cb-112">Returns the ID of the hidden character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="af8cb-113">*Causa*</span><span class="sxs-lookup"><span data-stu-id="af8cb-113">*Cause*</span></span>       | <span data-ttu-id="af8cb-114">Restituisce un valore che indica la causa del carattere da nascondere.</span><span class="sxs-lookup"><span data-stu-id="af8cb-114">Returns a value that indicates what caused the character to hide.</span></span> <span data-ttu-id="af8cb-115">1 utente ha nascosto il carattere selezionando il comando nel menu a comparsa dell'icona della barra delle applicazioni del carattere o usando l'input vocale.</span><span class="sxs-lookup"><span data-stu-id="af8cb-115">1 User hid the character by selecting the command on the character's taskbar icon pop-up menu or using speech input.</span></span><br/> <span data-ttu-id="af8cb-116">3 l'applicazione client ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="af8cb-116">3 Your client application hid the character.</span></span><br/> <span data-ttu-id="af8cb-117">5 un'altra applicazione client ha nascosto il carattere.</span><span class="sxs-lookup"><span data-stu-id="af8cb-117">5 Another client application hid the character.</span></span><br/> <span data-ttu-id="af8cb-118">7 l'utente ha nascosto il carattere selezionando il comando nel menu a comparsa del carattere.</span><span class="sxs-lookup"><span data-stu-id="af8cb-118">7 User hid the character by selecting the command on the character's pop-up menu.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="af8cb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="af8cb-119">Remarks</span></span>

<span data-ttu-id="af8cb-120">Il server invia questo evento a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="af8cb-120">The server sends this event to all clients of the character.</span></span> <span data-ttu-id="af8cb-121">Per eseguire una query sullo stato corrente del carattere, utilizzare la proprietà [**Visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="af8cb-121">To query the current state of the character, use the [**Visible**](visible-property.md) property.</span></span>

### <a name="see-also"></a><span data-ttu-id="af8cb-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="af8cb-122">See Also</span></span>

<span data-ttu-id="af8cb-123">[**Mostra evento**](show-event.md), [ **VisibilityCause**](visibilitycause-property.md)</span><span class="sxs-lookup"><span data-stu-id="af8cb-123">[**Show event**](show-event.md), [**VisibilityCause**](visibilitycause-property.md)</span></span>


 

 





