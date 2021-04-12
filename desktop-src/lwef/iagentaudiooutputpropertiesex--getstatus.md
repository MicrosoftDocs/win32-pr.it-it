---
title: IAgentAudioOutputPropertiesEx GetStatus
description: IAgentAudioOutputPropertiesEx GetStatus
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd89f4b3d8101ff15b868551626775e6f2e341f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396310"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx:: GetStatus

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Recupera lo stato del canale audio.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Stato del canale di output audio, che può corrispondere a uno dei valori seguenti:



| Valore                                                                         | Descrizione                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| stato dell'audio **short senza segno const** **\_ \_ disponibile = 0;**<br/>         | Il canale di output audio è disponibile (non occupato).                                                              |
| stato audio **breve senza segno const** **\_ \_ = 1;**<br/>           | Non è disponibile alcun supporto per l'output audio. ad esempio, perché non è presente alcuna scheda audio.                             |
| stato dell'audio **breve senza segno const** **\_ \_ CANTOPENAUDIO = 2;**<br/>     | Non è possibile aprire il canale di output audio (è occupato); ad esempio, perché un'altra applicazione sta riproducendo audio. |
| stato dell'audio **breve senza segno const** **\_ \_ USERSPEAKING = 3;**<br/>      | Il canale di output audio è occupato perché il server sta elaborando l'input vocale dell'utente                            |
| stato dell'audio **breve senza segno const** **\_ \_ CHARACTERSPEAKING = 4;**<br/> | Il canale di output audio è occupato perché è in corso un carattere.                                    |
| stato dell'audio **breve senza segno const** **\_ \_ SROVERRIDEABLE = 5;**<br/>    | Il canale di output audio non è occupato, ma è in attesa dell'input vocale dell'utente.                                 |
| errore di stato dell'audio **breve const senza segno** **\_ \_ = 6;**<br/>             | Si è verificato un altro problema (sconosciuto) durante il tentativo di accedere al canale di output audio.                       |



 

</dd> </dl>

Questa impostazione consente all'applicazione client di eseguire query sullo stato del canale di output audio. È possibile usare questo valore per determinare se il carattere deve parlare o provare ad attivare la modalità di ascolto (usando [**IAgentCharacterEx:: Listen**](lwef.iagentcharacterex::listen_method)).

 

 





