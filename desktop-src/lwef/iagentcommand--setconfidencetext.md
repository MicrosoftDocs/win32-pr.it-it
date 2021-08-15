---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8889c8c8c52f392a368c38a91510e112adbeeca42c611cdc0adcadad94f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976341"
---
# <a name="iagentcommandsetconfidencetext"></a>IAgentCommand::SetConfidenceText

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Imposta il valore del testo [](/windows/desktop/lwef/the-command-object)della descrizione comando.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*
</dt> <dd>

Oggetto BSTR che specifica il testo per la [**proprietà ConfidenceText**](confidencetext-property.md) di un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Se il valore di attendibilità restituito dalla corrispondenza migliore restituita nell'evento [**Command**](/windows/desktop/lwef/the-command-object) non supera il valore impostato per la [**proprietà ConfidenceThreshold,**](/windows/desktop/lwef/confidence-property) il testo fornito in *bszTipText* viene visualizzato nel suggerimento di ascolto.

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::SetConfidenceThreshold,**](iagentcommand--setconfidencethreshold.md) [**IAgentCommand::GetConfidenceThreshold,**](iagentcommand--getconfidencethreshold.md) [**IAgentCommand::GetConfidenceText,**](iagentcommand--getconfidencetext.md) [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 