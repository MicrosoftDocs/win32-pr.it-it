---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398863"
---
# <a name="iagentcommandsetconfidencetext"></a><span data-ttu-id="3a053-103">IAgentCommand::SetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="3a053-103">IAgentCommand::SetConfidenceText</span></span>

<span data-ttu-id="3a053-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3a053-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

<span data-ttu-id="3a053-105">Imposta il valore del testo del suggerimento di ascolto per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="3a053-105">Sets the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="3a053-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3a053-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3a053-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span><span class="sxs-lookup"><span data-stu-id="3a053-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="3a053-108">BSTR che specifica il testo per la proprietà [**ConfidenceText**](confidencetext-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="3a053-108">A BSTR that specifies the text for the [**ConfidenceText**](confidencetext-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="3a053-109">Se il valore di confidenza restituito della corrispondenza migliore restituita nell'evento del [**comando**](/windows/desktop/lwef/the-command-object) non supera il valore impostato per la proprietà [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , il testo fornito in *bszTipText* viene visualizzato nel suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="3a053-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in *bszTipText* is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a053-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3a053-110">See Also</span></span>

<span data-ttu-id="3a053-111">[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="3a053-111">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 