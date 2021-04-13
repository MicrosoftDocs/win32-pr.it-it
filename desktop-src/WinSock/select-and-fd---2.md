---
description: Poiché i socket non sono rappresentati dall'intero di tipo UNIX, piccolo e non negativo, l'implementazione della funzione Select è stata modificata in Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macro Select, FD_SET e FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528627"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="69410-103">Macro Select, FD \_ set e FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="69410-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="69410-104">Poiché i socket non sono rappresentati dall'intero di tipo UNIX, piccolo e non negativo, l'implementazione della funzione [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) è stata modificata in Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="69410-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="69410-105">Ogni set di socket è ancora rappresentato dalla struttura **del \_ set FD** , ma anziché essere archiviato come maschera di maschera, il set viene implementato come una matrice di socket.</span><span class="sxs-lookup"><span data-stu-id="69410-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="69410-106">Per evitare potenziali problemi, le applicazioni devono essere conformi all'uso delle \_ macro fd xxx per impostare, inizializzare, cancellare e controllare le strutture del [**\_ set FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .</span><span class="sxs-lookup"><span data-stu-id="69410-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69410-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69410-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69410-108">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="69410-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="69410-109">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="69410-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



