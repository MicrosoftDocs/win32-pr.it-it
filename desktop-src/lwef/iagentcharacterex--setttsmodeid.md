---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398682"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Imposta l'ID modalità del set di motori TTS per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

Impostazione dell'ID modalità del motore TTS per il carattere.

> [!Note]  
> **IAgentCharacterEx: SetTTSModeID** può avere esito negativo se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.

 

</dd> </dl>

Questa impostazione determina la modalità del motore preferenziale per l'output TTS vocale di un carattere. L'ID modalità per un motore di sintesi vocale è il GUID definito dal fornitore di riconoscimento vocale che identifica in modo univoco la modalità del motore (formattato con parentesi graffe e trattini). Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).

Se si imposta un ID modalità TTS, viene eseguito l'override del tentativo del server di trovare la corrispondenza con un motore di riconoscimento vocale basato sull'ID della modalità TTS compilata del carattere, sull'ID lingua del sistema corrente e sull'ID lingua corrente del carattere. Tuttavia, se si tenta di impostare un ID modalità quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà dell'agente Microsoft o quando il motore associato non è installato, la chiamata avrà esito negativo.

Se non si imposta un ID modalità motore di TTS per il carattere, il server imposta un motore che corrisponde all'impostazione della lingua del carattere (mediante interfacce Speech API Microsoft). Se si imposta questa proprietà, il motore associato verrà caricato se non è già caricato.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




