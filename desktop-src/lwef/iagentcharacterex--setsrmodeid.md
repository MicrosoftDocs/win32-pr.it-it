---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7fcfbf4aff25c1af0fbdb1f40471f6b54c4731f22fb2c736da42fe462eb390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750418"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Imposta l'ID modalità del motore di riconoscimento vocale impostato per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

bszModeID

Impostazione dell'ID modalità del motore di riconoscimento vocale per il carattere.

Questa impostazione imposta il motore per l'input vocale di un carattere. L'ID modalità per un motore di riconoscimento vocale è il GUID definito dal fornitore del riconoscimento vocale che identifica in modo univoco la modalità del motore (formattata con parentesi graffe e trattini). Per altre informazioni, vedere la [documentazione di Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx)

Se si specifica un ID modalità che non corrisponde all'impostazione della lingua del carattere, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o il motore non è installato, questa chiamata avrà esito negativo. Se non si imposta un ID modalità motore di riconoscimento vocale per il carattere, il server ne imposta uno che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft).

Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'impostazione di questa proprietà carica il motore associato (se non è già stato caricato) e avvia i servizi voce. In altri, la chiave listening è disponibile e il suggerimento di ascolto è visualizzabile. La chiave di ascolto e il suggerimento di ascolto sono abilitati solo se sono abilitati anche in Opzioni carattere avanzate. Tuttavia, se si esegue una query sulla proprietà quando la voce è disabilitata, il server non avvia i servizi voce.

Questa proprietà si applica solo al client del carattere. l'impostazione non riflette l'impostazione per altri client del carattere o di altri caratteri del client.

I requisiti del motore di riconoscimento vocale di Microsoft Agent sono basati su Microsoft Speech API. I motori che supportano i requisiti SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




