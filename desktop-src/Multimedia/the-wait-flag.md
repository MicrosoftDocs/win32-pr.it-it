---
title: Flag di attesa
description: Flag di attesa
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- Flag di MCI_WAIT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045372"
---
# <a name="the-wait-flag"></a><span data-ttu-id="4969a-104">Flag di attesa</span><span class="sxs-lookup"><span data-stu-id="4969a-104">The Wait Flag</span></span>

<span data-ttu-id="4969a-105">I comandi MCI in genere restituiscono immediatamente l'utente, anche se sono necessari alcuni minuti per completare l'azione iniziata dal comando.</span><span class="sxs-lookup"><span data-stu-id="4969a-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="4969a-106">È possibile usare il flag di attesa (MCI \_ Wait) per indirizzare il dispositivo in modo che attenda che l'azione richiesta venga completata prima di restituire il controllo all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4969a-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="4969a-107">Ad esempio, il comando [**Play**](play.md) seguente non restituirà il controllo all'applicazione fino a quando non viene completata la riproduzione:</span><span class="sxs-lookup"><span data-stu-id="4969a-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="4969a-108">L'utente può annullare un'operazione di attesa premendo un tasto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="4969a-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="4969a-109">Per impostazione predefinita, questa chiave è CTRL + INTERr.</span><span class="sxs-lookup"><span data-stu-id="4969a-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="4969a-110">Le applicazioni possono ridefinire questa chiave utilizzando il comando [**break**](break.md) ([**MCI \_ break**](mci-break.md)).</span><span class="sxs-lookup"><span data-stu-id="4969a-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="4969a-111">(**L' \_ interruzioni MCI** utilizza la struttura [**\_ \_ parametri di MCI break**](mci-break-parms.md) ). Quando viene annullata un'operazione di attesa, MCI tenta di restituire il controllo all'applicazione senza interrompere il comando associato al flag "Wait".</span><span class="sxs-lookup"><span data-stu-id="4969a-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




