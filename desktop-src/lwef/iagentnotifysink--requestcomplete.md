---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331999"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Notifica a un'applicazione client il completamento di una richiesta.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificatore della richiesta avviata.

</dd> <dt>

<span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*
</dt> <dd>

Codice di stato. Questo parametro restituisce il codice di stato per la richiesta.

</dd> </dl>

Questo evento consente di tenere traccia del momento in cui un metodo in coda viene completato utilizzando il relativo ID richiesta.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink:: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveto**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentCharacter:: Show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)


 

 




