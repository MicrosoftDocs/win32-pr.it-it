---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961501"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Identificatore del carattere per il quale è stato modificato lo stato del client attivo.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Modifica dello stato attivo del client, che può essere una combinazione di uno dei valori seguenti:



| Valore                                                              | Descrizione                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Il client non è il client attivo del carattere.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Il client è il client attivo del carattere.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Il client è attivo di input (client attivo del carattere in primo piano). |



 

</dd> </dl>

Quando più applicazioni client condividono lo stesso carattere, il client attivo del carattere riceve l'input del mouse, ad esempio eventi di clic o trascinamento del controllo di Microsoft Agent. Analogamente, quando vengono visualizzati più caratteri, il client attivo del carattere in primo piano (noto anche come client attivo di input) riceve gli eventi [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Quando il client attivo di un carattere cambia, questo evento restituisce l'ID del carattere e **True** se l'applicazione è diventata il client attivo del carattere oppure **False** se non è più il client attivo del carattere.

Un'applicazione client può ricevere questo evento quando l'utente seleziona la voce di un'altra applicazione client nel menu a comparsa del carattere o tramite comando vocale, l'applicazione client modifica lo stato attivo o un'altra applicazione client chiude la connessione a Microsoft Agent. Agent invia questo evento solo alle applicazioni client interessate direttamente, quelle che diventano il client attivo o smettino di essere il client attivo.

È possibile usare il [**metodo Activate**](iagentcharacter--activate.md) per impostare se l'applicazione è il client attivo del carattere o per impostare l'applicazione come client attivo per l'input (che rende anche il carattere in primo piano).

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive**](iagentcharacterex--getactive.md), [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





