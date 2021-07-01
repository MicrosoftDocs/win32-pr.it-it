---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119685"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="f3a7d-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="f3a7d-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="f3a7d-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3a7d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="f3a7d-105">Recupera la causa dell'ultimo spostamento del carattere.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="f3a7d-106">Restituisce S \_ OK per indicare che l'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3a7d-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="f3a7d-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="f3a7d-108">Indirizzo di una variabile che riceve la causa dell'ultimo spostamento del carattere e sarà uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3a7d-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



| <span data-ttu-id="f3a7d-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f3a7d-109">Value</span></span>                                                               | <span data-ttu-id="f3a7d-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3a7d-110">Description</span></span>                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a7d-111">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-111">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="f3a7d-112">Il carattere non è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-112">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="f3a7d-113">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-113">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="f3a7d-114">L'utente ha trascinato il carattere.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-114">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="f3a7d-115">**const unsigned short** **ProgramMoved = 2;**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-115">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="f3a7d-116">L'applicazione ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-116">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="f3a7d-117">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-117">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="f3a7d-118">Un'altra applicazione ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-118">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="f3a7d-119">**const unsigned short** **SystemMoved = 4**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-119">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="f3a7d-120">Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="f3a7d-120">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f3a7d-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f3a7d-121">See Also</span></span>

[<span data-ttu-id="f3a7d-122">**IAgentNotifySink::Move**</span><span class="sxs-lookup"><span data-stu-id="f3a7d-122">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





