---
title: Evento IdleStart
description: Evento IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298218"
---
# <a name="idlestart-event"></a><span data-ttu-id="90a65-103">Evento IdleStart</span><span class="sxs-lookup"><span data-stu-id="90a65-103">IdleStart Event</span></span>

<span data-ttu-id="90a65-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="90a65-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="90a65-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="90a65-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="90a65-106">Si verifica quando il server imposta un carattere sullo **stato di** inattivo.</span><span class="sxs-lookup"><span data-stu-id="90a65-106">Occurs when the server sets a character to the **Idling** state.</span></span>

</dd> <dt>

<span data-ttu-id="90a65-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="90a65-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="90a65-108">Agente **secondario** \*\* \* \* \_ IdleStart\* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="90a65-108">**Sub** *agent\*\*\*\_IdleStart*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="90a65-109">Parte</span><span class="sxs-lookup"><span data-stu-id="90a65-109">Part</span></span>          | <span data-ttu-id="90a65-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90a65-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="90a65-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="90a65-111">*CharacterID*</span></span> | <span data-ttu-id="90a65-112">Restituisce l'ID del carattere minimo sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="90a65-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="90a65-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="90a65-113">Remarks</span></span>

<span data-ttu-id="90a65-114">Il server invia questo evento a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="90a65-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="90a65-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="90a65-115">See Also</span></span>

[<span data-ttu-id="90a65-116">**Evento IdleComplete**</span><span class="sxs-lookup"><span data-stu-id="90a65-116">**IdleComplete event**</span></span>](idlecomplete-event.md)


 

 




