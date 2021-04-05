---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713621"
---
# <a name="iagentnotifysinkrequeststart"></a>IAgentNotifySink::RequestStart

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

Notifica a un'applicazione client l'inizio di una richiesta.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*
</dt> <dd>

Identificatore della richiesta avviata.

</dd> </dl>

Questo evento consente di tenere traccia del momento in cui una richiesta accodata inizia a usare il relativo ID richiesta.

## <a name="see-also"></a>Vedere anche

[**IAgentNotifySink:: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter:: moveto**](iagentcharacter--moveto.md), [**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentCharacter:: Show**](iagentcharacter--show.md), [**IAgentCharacter:: Speak**](iagentcharacter--speak.md), [**IAgentCharacter:: wait**](iagentcharacter--wait.md)


 

 




