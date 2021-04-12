---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331847"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="856a2-103">IAgentBalloonEx::SetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="856a2-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="856a2-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="856a2-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="856a2-105">Imposta il numero di caratteri per riga che è possibile visualizzare nel fumetto di parola del carattere.</span><span class="sxs-lookup"><span data-stu-id="856a2-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="856a2-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="856a2-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="856a2-107">Restituisce E \_ INVALIDARG se il parametro è minore di otto.</span><span class="sxs-lookup"><span data-stu-id="856a2-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="856a2-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="856a2-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="856a2-109">Numero di righe da visualizzare nel fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="856a2-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="856a2-110">L'impostazione minima è 8 e il valore massimo è 255.</span><span class="sxs-lookup"><span data-stu-id="856a2-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="856a2-111">Se il testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) supera le dimensioni del fumetto corrente, Agent scorre automaticamente il testo nel fumetto.</span><span class="sxs-lookup"><span data-stu-id="856a2-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="856a2-112">L'impostazione predefinita è basata sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="856a2-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="856a2-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="856a2-113">See Also</span></span>

[<span data-ttu-id="856a2-114">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="856a2-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




