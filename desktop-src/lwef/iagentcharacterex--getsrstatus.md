---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4396e325f5afba161046f2a001cebb29033d709b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044528"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Recupera lo stato della condizione necessaria per supportare l'input vocale.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:



| Valore                                                                               | Descrizione                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const unsigned long** **Listen \_ status \_ CANLISTEN = 0;**<br/>               | Le condizioni supportano l'input vocale.                                                                                                                                                                                                          |
| **const unsigned long** **Listen \_ status \_ noaudio = 1;**<br/>                 | Nessun dispositivo di input audio disponibile nel sistema. Si noti che questo non rileva se un microfono è installato; può solo rilevare se l'utente dispone di una scheda audio abilitata per l'input correttamente installata con un driver funzionante. |
| stato di ascolto **lungo senza segno const** **\_ \_ NOTTOPMOST = 2;**<br/>              | Un altro client è il client attivo di questo carattere oppure il carattere corrente non è in primo piano.                                                                                                                                           |
| **const unsigned long** **Listen \_ status \_ CANTOPENAUDIO = 3;**<br/>           | Il canale di input o di output audio è attualmente occupato, altre applicazioni usano l'audio.                                                                                                                                               |
| **const unsigned long** **Listen \_ status \_ COULDNTINITIALIZESPEECH = 4;**<br/> | Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale. Ciò include la possibilità che non sia disponibile un motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.                          |
| **const unsigned long** **Listen \_ status \_ SPEECHDISABLED = 5;**<br/>          | L'utente ha disabilitato l'input vocale nella finestra Opzioni carattere avanzate.                                                                                                                                                              |
| errore di stato di ascolto **Long senza segno const** **\_ \_ = 6;**<br/>                   | Si è verificato un errore durante il controllo dello stato dell'audio, ma la cause dell'errore non è stata restituita dal sistema.                                                                                                                                |



 

</dd> </dl>

Questa funzione consente di eseguire una query se le condizioni correnti supportano l'input di riconoscimento vocale, incluso lo stato del dispositivo audio. Se l'applicazione usa il metodo [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) , è possibile usare questa funzione per assicurarsi che la chiamata venga eseguita correttamente. La chiamata a questo metodo carica anche il motore vocale se non è già caricato. Tuttavia, non attiva la modalità di ascolto.

Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'esecuzione di query sullo stato caricherà il motore associato (se non è già caricato) e avvierà servizi vocali. Ovvero, la chiave di ascolto è disponibile e il suggerimento di ascolto è visualizzabile. (Il tasto di attesa e il suggerimento di ascolto sono abilitati solo se sono abilitati anche nelle opzioni dei caratteri avanzati). Tuttavia, se si esegue una query sulla proprietà quando la voce Speech è disabilitata, il server non avvia i servizi di riconoscimento vocale.

Questa funzione restituisce solo l'impostazione per l'uso del carattere da parte dell'applicazione client. l'impostazione non riflette altri client del carattere o di altri caratteri dell'applicazione client.

 

 





