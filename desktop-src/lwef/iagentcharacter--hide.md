---
title: Nascondi IAgentCharacter
description: Nascondi IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046667"
---
# <a name="iagentcharacterhide"></a>IAgentCharacter:: Hide

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Nasconde il carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Flag animazione stato **nascosto** . Se questo parametro è **true**, l'animazione **nascosta** non viene riprodotto prima che il frame di caratteri sia nascosto; Se **false**, l'animazione viene riprodotta.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID richiesta **Hide** .

</dd> </dl>

Il server accoda l'animazione associata al metodo **Hide** nella coda del carattere. In questo modo è possibile usarlo per nascondere il carattere dopo una sequenza di altre animazioni. È possibile riprodurre l'azione immediatamente usando il metodo [**Stop**](iagentcharacter--stop.md) prima di chiamare il metodo **Hide** .

Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità dell'animazione dello stato di **occultamento** prima di chiamare questo metodo.

Nascondere un carattere può anche causare l'attivazione dell'evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) di un altro carattere visibile.

I caratteri nascosti non possono accedere al canale audio. Il server restituirà uno stato di errore nell'evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) se si genera una richiesta di animazione e il carattere è nascosto.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Show**](iagentcharacter--show.md)


 

 