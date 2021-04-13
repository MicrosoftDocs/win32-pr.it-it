---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396991"
---
# <a name="iagentcharactergetmovecause"></a><span data-ttu-id="012e4-103">IAgentCharacter::GetMoveCause</span><span class="sxs-lookup"><span data-stu-id="012e4-103">IAgentCharacter::GetMoveCause</span></span>

<span data-ttu-id="012e4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="012e4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

<span data-ttu-id="012e4-105">Recupera la motivo dell'ultima spostamento del carattere.</span><span class="sxs-lookup"><span data-stu-id="012e4-105">Retrieves the cause of the character's last move.</span></span>

-   <span data-ttu-id="012e4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="012e4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="012e4-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="012e4-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="012e4-108">Indirizzo di una variabile che riceve la motivo dell'ultimo spostamento del carattere e sarà uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="012e4-108">Address of a variable that receives the cause of the character's last move and will be one of the following:</span></span>



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="012e4-109">**const unsigned short** **NeverMoved = 0;**</span><span class="sxs-lookup"><span data-stu-id="012e4-109">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="012e4-110">Il carattere non è stato spostato.</span><span class="sxs-lookup"><span data-stu-id="012e4-110">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="012e4-111">**const unsigned short** **UserMoved = 1;**</span><span class="sxs-lookup"><span data-stu-id="012e4-111">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="012e4-112">Il carattere è stato trascinato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="012e4-112">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="012e4-113">ProgramMoved **short const senza segno** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="012e4-113">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="012e4-114">L'applicazione ha spostato il carattere.</span><span class="sxs-lookup"><span data-stu-id="012e4-114">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="012e4-115">**const unsigned short** **OtherProgramMoved = 3;**</span><span class="sxs-lookup"><span data-stu-id="012e4-115">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="012e4-116">Il carattere è stato spostato da un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="012e4-116">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="012e4-117">SystemMoved **short const senza segno** **= 4**</span><span class="sxs-lookup"><span data-stu-id="012e4-117">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="012e4-118">Il server ha spostato il carattere per mantenerlo sullo schermo dopo una modifica della risoluzione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="012e4-118">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="012e4-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="012e4-119">See Also</span></span>

[<span data-ttu-id="012e4-120">**IAgentNotifySink:: Move**</span><span class="sxs-lookup"><span data-stu-id="012e4-120">**IAgentNotifySink::Move**</span></span>](iagentnotifysink--move.md)


 

 





