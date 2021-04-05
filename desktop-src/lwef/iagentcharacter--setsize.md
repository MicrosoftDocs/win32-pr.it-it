---
title: IAgentCharacter dimensioni
description: IAgentCharacter dimensioni
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713186"
---
# <a name="iagentcharactersetsize"></a><span data-ttu-id="f3d7e-103">IAgentCharacter:: sesize</span><span class="sxs-lookup"><span data-stu-id="f3d7e-103">IAgentCharacter::SetSize</span></span>

<span data-ttu-id="f3d7e-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3d7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

<span data-ttu-id="f3d7e-105">Imposta la dimensione del frame di animazione del carattere.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-105">Sets the size of the character's animation frame.</span></span>

-   <span data-ttu-id="f3d7e-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3d7e-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="f3d7e-107"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="f3d7e-108">Larghezza del fotogramma di animazione del carattere in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-108">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="f3d7e-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="f3d7e-109"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="f3d7e-110">Altezza del frame di animazione del carattere in pixel.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-110">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="f3d7e-111">Se si modifica la dimensione del fotogramma del carattere, il carattere viene ridimensionato in modo da impostare le dimensioni con questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-111">Changing the character's frame size scales the character to the size set with this method.</span></span> <span data-ttu-id="f3d7e-112">L'impostazione di questa proprietà si applica a tutti i client del carattere.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-112">This property's setting applies to all clients of the character.</span></span>

<span data-ttu-id="f3d7e-113">Anche se il carattere viene visualizzato in una finestra dell'area a forma irregolare, la posizione del carattere è basata sul relativo frame di animazione rettangolare.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-113">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3d7e-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f3d7e-114">See Also</span></span>

[<span data-ttu-id="f3d7e-115">**IAgentCharacter:: GetSize**</span><span class="sxs-lookup"><span data-stu-id="f3d7e-115">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




