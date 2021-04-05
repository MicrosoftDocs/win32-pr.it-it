---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117726"
---
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="199fa-103">IAgentCommand::SetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="199fa-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="199fa-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="199fa-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="199fa-105">Imposta il valore della proprietà [**confidenza**](confidence-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="199fa-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="199fa-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="199fa-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="199fa-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span><span class="sxs-lookup"><span data-stu-id="199fa-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="199fa-108">Valore per la proprietà [**confidenza**](confidence-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="199fa-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="199fa-109">Se il valore di confidenza restituito della corrispondenza migliore restituita nell'evento del [**comando**](/windows/desktop/lwef/the-command-object) non supera il valore impostato per la proprietà [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , il testo fornito in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) viene visualizzato nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="199fa-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="199fa-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="199fa-110">See Also</span></span>

<span data-ttu-id="199fa-111">[**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="199fa-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 