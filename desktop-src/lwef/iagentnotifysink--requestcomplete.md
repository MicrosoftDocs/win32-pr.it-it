---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c797232ca968261c5857bec8953c6c76375bafc849b17ebe21bc8f353698f02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976171"
---
# <a name="iagentnotifysinkrequestcomplete"></a>IAgentNotifySink::RequestComplete

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

Notifica a un'applicazione client quando viene completata una richiesta.

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

Questo evento consente di tenere traccia del completamento di un metodo in coda usando il relativo ID richiesta.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [](iagentcharacter--wait.md) [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [](iagentcharacter--show.md) [**IAgentCharacter:::P Wait**](iagentcharacter--play.md) [](iagentcharacter--speak.md)


 

 




