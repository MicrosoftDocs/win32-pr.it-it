---
title: Evento IdleComplete
description: Evento IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043975"
---
# <a name="idlecomplete-event"></a><span data-ttu-id="084db-103">Evento IdleComplete</span><span class="sxs-lookup"><span data-stu-id="084db-103">IdleComplete Event</span></span>

<span data-ttu-id="084db-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="084db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="084db-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="084db-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="084db-106">Si verifica quando il server termina **lo stato di** inattivo di un carattere.</span><span class="sxs-lookup"><span data-stu-id="084db-106">Occurs when the server ends the **Idling** state of a character.</span></span>

</dd> <dt>

<span data-ttu-id="084db-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="084db-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="084db-108">Agente **secondario** \*\* \* \* \_ IdleComplete\* \*  **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="084db-108">**Sub** *agent\*\*\*\_IdleComplete*\* **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="084db-109">Parte</span><span class="sxs-lookup"><span data-stu-id="084db-109">Part</span></span>          | <span data-ttu-id="084db-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="084db-110">Description</span></span>                                         |
|---------------|-----------------------------------------------------|
| <span data-ttu-id="084db-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="084db-111">*CharacterID*</span></span> | <span data-ttu-id="084db-112">Restituisce l'ID del carattere minimo sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="084db-112">Returns the ID of the idling character as a string.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="084db-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="084db-113">Remarks</span></span>

<span data-ttu-id="084db-114">Il server invia questo evento a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="084db-114">The server sends this event to all clients of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="084db-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="084db-115">See Also</span></span>

[<span data-ttu-id="084db-116">**Evento IdleStart**</span><span class="sxs-lookup"><span data-stu-id="084db-116">**IdleStart event**</span></span>](idlestart-event.md)


 

 




