---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1d5894a04eeb09289e98db42362acbc43d587e5ac680b98276260ba9c323b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961931"
---
# <a name="iagentcommandgetconfidencetext"></a>IAgentCommand::GetConfidenceText

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Recupera il testo del suggerimento di ascolto impostato in precedenza per un [**oggetto Command.**](/windows/desktop/lwef/the-command-object)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*
</dt> <dd>

Indirizzo di un BSTR che riceve il valore del [](/windows/desktop/lwef/the-command-object)testo della descrizione comando.

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCommand::SetConfidenceThreshold,**](iagentcommand--setconfidencethreshold.md) [**IAgentCommand::GetConfidenceThreshold,**](iagentcommand--getconfidencethreshold.md) [**IAgentCommand::SetConfidenceText,**](iagentcommand--setconfidencetext.md) [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 