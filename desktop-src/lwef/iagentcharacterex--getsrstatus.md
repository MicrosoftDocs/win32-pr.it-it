---
title: IAgentCharacterEx GetSRStatus
description: IAgentCharacterEx GetSRStatus
ms.assetid: ccb34108-8078-421a-a883-731b51fae179
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f9f888fcea9069ff31ccef6b2c1ef5a0148fbb34ba21d03ee881c52056f10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105539"
---
# <a name="iagentcharacterexgetsrstatus"></a>IAgentCharacterEx::GetSRStatus

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetSRStatus(
   long * plStatus  // address of the speech input status
);
```

Recupera lo stato della condizione necessaria per supportare l'input vocale.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:



| Valore                                                                               | Descrizione                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const unsigned long** **LISTEN STATUS \_ \_ CANLISTEN = 0;**<br/>               | Le condizioni supportano l'input vocale.                                                                                                                                                                                                          |
| **const unsigned long** **LISTEN STATUS \_ \_ NOAUDIO = 1;**<br/>                 | In questo sistema non è disponibile alcun dispositivo di input audio. Si noti che non viene rilevato se è installato un microfono, ma solo se l'utente dispone di una scheda audio abilitata per l'input installata correttamente con un driver funzionante. |
| **const unsigned long** **LISTEN STATUS \_ \_ NOTTOPMOST = 2;**<br/>              | Un altro client è il client attivo di questo carattere o il carattere corrente non è in primo piano.                                                                                                                                           |
| **const unsigned long** **LISTEN STATUS \_ \_ CANTOPENAUDIO = 3;**<br/>           | Il canale di input o output audio è attualmente occupato, un'altra applicazione usa l'audio.                                                                                                                                               |
| **const unsigned long** **LISTEN STATUS \_ \_ COULDNTINITIALIZESPEECH = 4;**<br/> | Si è verificato un errore non specificato durante il processo di inizializzazione del sottosistema di riconoscimento vocale. Ciò include la possibilità che non sia disponibile alcun motore di riconoscimento vocale corrispondente all'impostazione della lingua del carattere.                          |
| **const unsigned long** **LISTEN STATUS \_ \_ SPEECHDISABLED = 5;**<br/>          | L'utente ha disabilitato l'input vocale nella finestra Opzioni carattere avanzate.                                                                                                                                                              |
| **const unsigned long** **LISTEN STATUS ERROR = \_ \_ 6;**<br/>                   | Si è verificato un errore durante il controllo dello stato audio, ma la causa dell'errore non è stata restituita dal sistema.                                                                                                                                |



 

</dd> </dl>

Questa funzione consente di verificare se le condizioni correnti supportano l'input di riconoscimento vocale, incluso lo stato del dispositivo audio. Se l'applicazione usa il [**metodo IAgentCharacterEx::Listen,**](iagentcharacterex--listen.md) è possibile usare questa funzione per garantire che la chiamata avrà esito positivo. La chiamata a questo metodo carica anche il motore di riconoscimento vocale se non è già caricato. Tuttavia, non attiva la modalità di ascolto.

Quando l'input vocale è abilitato nella finestra delle proprietà dell'agente (Opzioni carattere avanzate), l'esecuzione di query sullo stato carica il motore associato (se non è già stato caricato) e avvia i servizi voce. Ciò significa che la chiave di ascolto è disponibile e il suggerimento per l'ascolto è visualizzabile. La chiave di ascolto e il suggerimento di ascolto sono abilitati solo se sono abilitati anche in Opzioni carattere avanzate. Tuttavia, se si esegue una query sulla proprietà quando la voce è disabilitata, il server non avvia i servizi voce.

Questa funzione restituisce solo l'impostazione per l'uso del carattere da parte dell'applicazione client. l'impostazione non riflette altri client del carattere o di altri caratteri dell'applicazione client.

 

 





