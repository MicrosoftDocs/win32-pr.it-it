---
title: IAgentCharacterEx getActive
description: IAgentCharacterEx getActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856657"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx:: getActive

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera un valore che indica se l'applicazione client è il client attivo del carattere e se il carattere è in primo piano.

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Indirizzo di una variabile che riceve uno dei valori seguenti per l'impostazione dello stato:



| Valore                                                              | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **Activate \_ notacty = 0;**<br/>   | Il client non è il client attivo del carattere.                |
| **const unsigned short** **Activate \_ attivo = 1;**<br/>      | Il client è il client attivo del carattere.                    |
| **const unsigned short** **Activate \_ INPUTACTIVE = 2;**<br/> | Il client è di input-attivo (client attivo del carattere superiore). |



 

</dd> </dl>

Questa impostazione consente di sapere se si è il client attivo del carattere o se il carattere è il carattere attivo di input. Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft). Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client di input-attivo) riceve gli eventi [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

Usare il metodo [**Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client attivo di input (che rende anche il carattere in primo piano).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





