---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472259"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Imposta l'ID modalità del motore di riconoscimento vocale impostato per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

bszModeID

Impostazione dell'ID modalità del motore di riconoscimento vocale per il carattere.

Questa impostazione imposta il motore per l'input vocale di un carattere. L'ID modalità per un motore di riconoscimento vocale è il GUID definito dal fornitore vocale che identifica in modo univoco la modalità del motore (formattato con parentesi graffe e trattini). Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).

Se si specifica un ID modalità che non corrisponde all'impostazione della lingua del carattere, se l'utente ha disabilitato il riconoscimento vocale (nella finestra delle proprietà di Microsoft Agent) o se il motore non è installato, la chiamata avrà esito negativo. Se non si imposta un ID modalità del motore di riconoscimento vocale per il carattere, il server ne imposta uno che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft).

Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali. Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile. (Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.

Questa proprietà si applica solo al client del carattere; l'impostazione non riflette l'impostazione per altri client del carattere o di altri caratteri del client.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




