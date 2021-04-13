---
title: IAgentCharacter SetIdleOn
description: IAgentCharacter SetIdleOn
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396975"
---
# <a name="iagentcharactersetidleon"></a><span data-ttu-id="da4d0-103">IAgentCharacter::SetIdleOn</span><span class="sxs-lookup"><span data-stu-id="da4d0-103">IAgentCharacter::SetIdleOn</span></span>

<span data-ttu-id="da4d0-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da4d0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

<span data-ttu-id="da4d0-105">Imposta l'elaborazione inattiva automatica per un carattere.</span><span class="sxs-lookup"><span data-stu-id="da4d0-105">Sets automatic idle processing for a character.</span></span>

-   <span data-ttu-id="da4d0-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="da4d0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="da4d0-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span><span class="sxs-lookup"><span data-stu-id="da4d0-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="da4d0-108">Flag di elaborazione inattiva.</span><span class="sxs-lookup"><span data-stu-id="da4d0-108">Idle processing flag.</span></span> <span data-ttu-id="da4d0-109">Se questo parametro è impostato su **true**, l'agente Microsoft riproduce automaticamente le animazioni di stato al **minimo** .</span><span class="sxs-lookup"><span data-stu-id="da4d0-109">If this parameter is **True**, the Microsoft Agent automatically plays **Idling** state animations.</span></span>

</dd> </dl>

<span data-ttu-id="da4d0-110">Il server imposta automaticamente un timeout dopo l'ultima animazione riprodotta per un carattere.</span><span class="sxs-lookup"><span data-stu-id="da4d0-110">The server automatically sets a time out after the last animation played for a character.</span></span> <span data-ttu-id="da4d0-111">Quando l'intervallo di questo timer è completo, il server inizia gli Stati di **minimo** per un carattere, eseguendo le animazioni al **minimo** associate a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="da4d0-111">When this timer's interval is complete, the server begins the **Idling** states for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="da4d0-112">Se si desidera gestire manualmente le animazioni **dello stato di** inattivo, impostare la proprietà su **false**.</span><span class="sxs-lookup"><span data-stu-id="da4d0-112">If you want to manage the **Idling** state animations yourself, set the property to **False**.</span></span> <span data-ttu-id="da4d0-113">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="da4d0-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="da4d0-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="da4d0-114">See Also</span></span>

[<span data-ttu-id="da4d0-115">**IAgentCharacter::GetIdleOn**</span><span class="sxs-lookup"><span data-stu-id="da4d0-115">**IAgentCharacter::GetIdleOn**</span></span>](iagentcharacter--getidleon.md)


 

 




