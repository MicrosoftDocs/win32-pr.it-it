---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471579"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="a8b71-103">IAgentBalloonEx::SetNumLines</span><span class="sxs-lookup"><span data-stu-id="a8b71-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="a8b71-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a8b71-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="a8b71-105">Imposta il numero di righe di output di testo che è possibile visualizzare nel fumetto di parola del carattere.</span><span class="sxs-lookup"><span data-stu-id="a8b71-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="a8b71-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a8b71-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="a8b71-107">Restituisce E \_ INVALIDARG se il parametro è zero.</span><span class="sxs-lookup"><span data-stu-id="a8b71-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="a8b71-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span><span class="sxs-lookup"><span data-stu-id="a8b71-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="a8b71-109">Numero di righe da visualizzare nel fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="a8b71-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="a8b71-110">L'impostazione minima è 1 e il valore massimo è 128.</span><span class="sxs-lookup"><span data-stu-id="a8b71-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="a8b71-111">Se il testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) supera le dimensioni del fumetto corrente, Agent scorre automaticamente il testo nel fumetto.</span><span class="sxs-lookup"><span data-stu-id="a8b71-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="a8b71-112">Questo metodo avrà esito negativo se è impostato il bit di stile del fumetto **SizeToText** .</span><span class="sxs-lookup"><span data-stu-id="a8b71-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="a8b71-113">L'impostazione predefinita è basata sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a8b71-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8b71-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a8b71-114">See Also</span></span>

<span data-ttu-id="a8b71-115">[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: Sestyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="a8b71-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




