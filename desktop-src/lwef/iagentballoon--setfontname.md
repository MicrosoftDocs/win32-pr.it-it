---
title: IAgentBalloon sefontname
description: IAgentBalloon sefontname
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045299"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="d9b3d-103">IAgentBalloon:: sefontname</span><span class="sxs-lookup"><span data-stu-id="d9b3d-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="d9b3d-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9b3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="d9b3d-105">Imposta il tipo di carattere visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="d9b3d-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d9b3d-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="d9b3d-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="d9b3d-108">BSTR che imposta il tipo di carattere visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="d9b3d-109">Il tipo di carattere predefinito utilizzato nella parola Balloon di un carattere viene definito nell'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="d9b3d-110">È possibile modificarlo con **IAgentBalloon:: Sefontname**.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="d9b3d-111">Tuttavia, l'utente può eseguire l'override dell'impostazione del tipo di carattere per tutti i caratteri utilizzando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d9b3d-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9b3d-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d9b3d-112">See Also</span></span>

[<span data-ttu-id="d9b3d-113">**IAgentBalloon:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="d9b3d-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




