---
title: Commenti (menu e altre risorse)
description: RC supporta la sintassi di tipo C per i commenti a riga singola e per i commenti del blocco. I commenti a riga singola iniziano con due barre (//) e vengono eseguite fino alla fine della riga. Di seguito è riportato un esempio di istruzione di risorsa seguita da un commento a riga singola.
ms.assetid: 045268fb-2d6e-446c-8b95-90e42baeb282
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fda05690df9b7e7fff6974d75d8275a2842b68
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739626"
---
# <a name="comments-menus-and-other-resources"></a><span data-ttu-id="54ddc-105">Commenti (menu e altre risorse)</span><span class="sxs-lookup"><span data-stu-id="54ddc-105">Comments (Menus and Other Resources)</span></span>

<span data-ttu-id="54ddc-106">RC supporta la sintassi di tipo C per i commenti a riga singola e per i commenti del blocco.</span><span class="sxs-lookup"><span data-stu-id="54ddc-106">RC supports C-style syntax for both single-line comments and block comments.</span></span> <span data-ttu-id="54ddc-107">I commenti a riga singola iniziano con due barre (//) e vengono eseguite fino alla fine della riga.</span><span class="sxs-lookup"><span data-stu-id="54ddc-107">Single-line comments begin with two forward slashes (//) and run to the end of the line.</span></span> <span data-ttu-id="54ddc-108">Di seguito è riportato un esempio di istruzione di risorsa seguita da un commento a riga singola.</span><span class="sxs-lookup"><span data-stu-id="54ddc-108">The following is an example of a resource statement followed by a single-line comment.</span></span>

``` syntax
NewCursor  CURSOR  NEW.CUR  // a new cursor for the application.
```

<span data-ttu-id="54ddc-109">I commenti dei blocchi iniziano con un delimitatore di apertura (/ \* ) ed eseguono fino a un delimitatore di chiusura ( \* /).</span><span class="sxs-lookup"><span data-stu-id="54ddc-109">Block comments begin with an opening delimiter (/\*) and run to a closing delimiter (\*/).</span></span> <span data-ttu-id="54ddc-110">I commenti non vengono annidati.</span><span class="sxs-lookup"><span data-stu-id="54ddc-110">Comments do not nest.</span></span> <span data-ttu-id="54ddc-111">Di seguito è riportato un esempio di un commento di blocco all'inizio di un file RC.</span><span class="sxs-lookup"><span data-stu-id="54ddc-111">The following is an example of a block comment at the beginning of a .rc file.</span></span>

``` syntax
/* 
    Resources.Rc

    Contains the resource definitions for the application.
    Control identifiers are defined in Resources.h.
*/

#include "resources.h"
//...
```

 

 




