---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851c8fc73e9f427bd725d7ef647b84a68be13e4
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380745"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx::GetStatus

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Recupera lo stato del canale audio.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Stato del canale di output audio, che può essere uno dei valori seguenti:



| Valore                                                                         | Descrizione                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| **const unsigned short** **AUDIO STATUS AVAILABLE = \_ \_ 0;**<br/>         | Il canale di output audio è disponibile (non occupato).                                                              |
| **const unsigned short** **AUDIO STATUS \_ \_ NOAUDIO = 1;**<br/>           | Non è disponibile alcun supporto per l'output audio. ad esempio, poiché non è presente alcuna scheda audio.                             |
| **const unsigned short** **AUDIO STATUS \_ \_ CANTOPENAUDIO = 2;**<br/>     | Il canale di output audio non può essere aperto (è occupato). ad esempio perché un'altra applicazione sta riproducendo l'audio. |
| **const unsigned short** **AUDIO STATUS \_ \_ USERSPEAKING = 3;**<br/>      | Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente                            |
| **const unsigned short** **AUDIO STATUS \_ \_ CHARACTERSPEAKING = 4;**<br/> | Il canale di output audio è occupato perché un carattere sta parlando.                                    |
| **const unsigned short** **AUDIO STATUS \_ \_ SROVERRIDEABLE = 5;**<br/>    | Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.                                 |
| **const unsigned short** **AUDIO STATUS ERROR = \_ \_ 6;**<br/>             | Si è verificato un altro problema (sconosciuto) durante il tentativo di accesso al canale di output audio.                       |



 

</dd> </dl>

Questa impostazione consente all'applicazione client di eseguire query sullo stato del canale di output audio. È possibile usarlo per determinare se il tuo carattere deve parlare o se provare ad attivare la modalità di ascolto **(usando IAgentCharacterEx::Listen).**

 

 





