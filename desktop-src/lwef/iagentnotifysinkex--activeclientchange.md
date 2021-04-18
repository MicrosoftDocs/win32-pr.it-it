---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298331"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Notifica a un'applicazione client se il client attivo non è più il client attivo di un carattere.

-   Nessun valore restituito.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificatore del carattere per il quale lo stato del client attivo è stato modificato.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Modifica dello stato attivo del client, che può essere una combinazione dei valori seguenti:



| Valore                                                              | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **Activate \_ notacty = 0;**<br/>   | Il client non è il client attivo del carattere.                |
| **const unsigned short** **Activate \_ attivo = 1;**<br/>      | Il client è il client attivo del carattere.                    |
| **const unsigned short** **Activate \_ INPUTACTIVE = 2;**<br/> | Il client è di input-attivo (client attivo del carattere superiore). |



 

</dd> </dl>

Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse (ad esempio, gli eventi di clic o di trascinamento del controllo agente Microsoft). Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere superiore (noto anche come client di input-attivo) riceve gli eventi [**IAgentNotifySink:: Command**](iagentnotifysink--command.md) .

Quando viene modificato il client attivo di un carattere, questo evento restituisce l'ID di tale carattere e **true** se l'applicazione è diventata il client attivo del carattere o **false** se non è più il client attivo del carattere.

Un'applicazione client può ricevere questo evento quando l'utente seleziona la voce di un'altra applicazione client nel menu popup del carattere o tramite il comando vocale, l'applicazione client ne modifica lo stato attivo oppure un'altra applicazione client chiude la connessione a Microsoft Agent. Agent invia questo evento solo alle applicazioni client interessate direttamente, ovvero quelle che diventano il client attivo o smettono di essere il client attivo.

È possibile usare il metodo [**Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per rendere l'applicazione il client di input-attivo (che rende anche il carattere in primo piano).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx:: getActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





