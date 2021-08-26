---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a24195fd177abbde3c6423f966df67ba0faeaf315038d7f8cb0b4ca136f16c3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114721"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Imposta l'ID modalità del set di motori TTS per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

Impostazione dell'ID modalità del motore TTS per il carattere.

> [!Note]  
> **IAgentCharacterEx:SetTTSModeID** può non riuscire se Speech.dll non è installato e il motore specificato non corrisponde all'impostazione della modalità TTS compilata del carattere.

 

</dd> </dl>

Questa impostazione determina la modalità del motore preferita per l'output TTS parlato di un carattere. L'ID modalità per un motore TTS (sintesi vocale) è il GUID definito dal fornitore di riconoscimento vocale che identifica in modo univoco la modalità del motore (formattata con parentesi graffe e trattini). Per altre informazioni, vedere la [documentazione di Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx)

Se si imposta un ID modalità TTS, il server esegue l'override del tentativo di corrispondenza con un motore di riconoscimento vocale in base all'ID della modalità TTS compilato del carattere, all'ID della lingua di sistema corrente e all'ID lingua corrente del carattere. Tuttavia, se si tenta di impostare un ID modalità quando l'utente ha disabilitato l'output vocale nella finestra delle proprietà di Microsoft Agent o quando il motore associato non è installato, questa chiamata avrà esito negativo.

Se non si imposta un ID modalità motore TTS per il carattere, il server imposta un motore che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft). L'impostazione di questa proprietà carica il motore associato se non è già caricato.

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore di riconoscimento vocale di Microsoft Agent sono basati su Microsoft Speech API. I motori che supportano i requisiti SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




