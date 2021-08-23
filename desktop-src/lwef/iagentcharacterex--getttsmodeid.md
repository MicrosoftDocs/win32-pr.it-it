---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e6bc029a6fce1da3d6f920a25ccc86c49619751a6bd43f865154bd7a235696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105489"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera l'ID modalità del set di motori TTS per il carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Indirizzo di un BSTR che riceve l'impostazione dell'ID modalità del motore TTS per il carattere.

</dd> </dl>

Questa impostazione restituisce l'ID della modalità motore TTS (sintesi vocale) per l'output parlato di un carattere. L'ID modalità per un motore TTS è una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) definito dal fornitore di riconoscimento vocale che identifica in modo univoco il motore. Per altre informazioni, vedere la [documentazione di Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx) L'esecuzione di query su questa proprietà carica il motore associato se non è già caricato.

Se non si imposta un ID modalità motore TTS per il carattere, il server tenta di restituire un motore che corrisponde (usando le interfacce di Microsoft Speech API) all'impostazione TTS compilata del carattere e all'impostazione della lingua corrente del carattere. Se sono diverse, l'impostazione della lingua del carattere sostituisce l'impostazione della modalità di creazione. Se non è stata impostata l'impostazione della lingua del carattere, la lingua del carattere è l'ID della lingua predefinita dell'utente e il server tenta la corrispondenza in base a tale ID lingua.

Questa funzione non ha esito negativo se [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) restituisce **False.**

Questa proprietà si applica solo all'uso del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore di riconoscimento vocale di Microsoft Agent sono basati su Microsoft Speech API. I motori che supportano i requisiti SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




