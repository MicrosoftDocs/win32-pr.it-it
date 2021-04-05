---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046385"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera l'ID modalità del set di motori TTS per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Indirizzo di un BSTR che riceve l'impostazione dell'ID modalità del motore TTS per il carattere.

</dd> </dl>

Questa impostazione restituisce l'ID della modalità del motore TTS (sintesi vocale) per l'output parlato di un carattere. L'ID modalità per un motore TTS è una rappresentazione di stringa del GUID (formattato con parentesi graffe e trattini) definita dal fornitore di riconoscimento vocale che identifica in modo univoco il motore. Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx). Se si esegue una query su questa proprietà, il motore associato verrà caricato se non è già caricato.

Se non si imposta un ID modalità motore di TTS per il carattere, il server tenta di restituire un motore che corrisponde a (usando le interfacce di Microsoft Speech API) l'impostazione TTS compilata del carattere e l'impostazione della lingua corrente del carattere. Se sono diversi, l'impostazione della lingua del carattere sostituisce la relativa impostazione della modalità di creazione. Se l'impostazione della lingua del carattere non è stata impostata, la lingua del carattere è l'ID della lingua predefinita dell'utente e il server tenta la corrispondenza in base a tale ID lingua.

Questa funzione non ha esito negativo se [**IAgentAudioObjectProperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) restituisce **false**.

Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




