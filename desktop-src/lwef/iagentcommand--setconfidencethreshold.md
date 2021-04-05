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
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Imposta il valore della proprietà [**confidenza**](confidence-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

Valore per la proprietà [**confidenza**](confidence-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se il valore di confidenza restituito della corrispondenza migliore restituita nell'evento del [**comando**](/windows/desktop/lwef/the-command-object) non supera il valore impostato per la proprietà [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , il testo fornito in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) viene visualizzato nel suggerimento di ascolto.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 