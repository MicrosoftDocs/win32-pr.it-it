---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723814"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Recupera l'ID modalità del motore di riconoscimento vocale impostato per il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Indirizzo di un BSTR che riceve l'impostazione dell'ID modalità del motore di riconoscimento vocale per il carattere.

</dd> </dl>

Questa impostazione restituisce il motore impostato per l'input vocale di un carattere. L'ID modalità per un motore di riconoscimento vocale è una rappresentazione in forma di stringa del GUID (formattato con parentesi graffe e trattini) dal fornitore di sintesi vocale che identifica in modo univoco il motore. Per ulteriori informazioni, vedere la [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx).

Se non si imposta un ID modalità del motore di riconoscimento vocale per il carattere, il server restituisce un motore che corrisponde all'impostazione della lingua del carattere (usando le interfacce Speech API Microsoft). Se non è disponibile alcun motore di riconoscimento vocale corrispondente per il carattere, il server restituisce una stringa null (vuota).

Quando l'input vocale è abilitato (nella finestra Opzioni carattere avanzato), l'esecuzione di una query o l'impostazione di questa proprietà caricherà il motore associato (se non è già caricato) e avvierà servizi vocali. Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile. (Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia servizi vocali e restituisce una stringa null (stringa vuota).

Questa funzione restituisce solo l'impostazione per l'uso del carattere da parte dell'applicazione client. l'impostazione non riflette altri client del carattere o di altri caratteri dell'applicazione client.

Questa funzione non ha esito negativo se [**IAgentSpeechInputProperties:: GetEnabled**](iagentspeechinputproperties--getenabled.md) restituisce **false**.

I requisiti del motore vocale di Microsoft Agent sono basati sulla Speech API Microsoft. I motori che supportano i requisiti di SAPI di Microsoft Agent possono essere installati e usati con Agent.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




