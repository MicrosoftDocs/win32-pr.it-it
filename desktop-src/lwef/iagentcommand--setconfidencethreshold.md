---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976301"
---
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Imposta il valore della proprietà [**Confidence**](confidence-property.md) per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

Valore della proprietà [**Confidence di**](confidence-property.md) un oggetto [**Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se il valore di attendibilità restituito dalla corrispondenza migliore restituita nell'evento [**Command**](/windows/desktop/lwef/the-command-object) non supera il valore impostato per la [**proprietà ConfidenceThreshold,**](/windows/desktop/lwef/confidence-property) il testo fornito in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) viene visualizzato nel suggerimento per l'ascolto.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 