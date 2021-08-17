---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcefb523bd2e9f477991bf6fa8352382f75b6bc76d93aab2e7f5c9e8cc1358dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117693003"
---
# <a name="iagentcharactershow"></a>IAgentCharacter::Show

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Visualizza un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene restituita, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*Colazione*
</dt> <dd>

Visualizzazione del flag di animazione dello stato. Se questo parametro è **True,** **l'animazione Dello** stato di visualizzazione viene riprodotta dopo aver rendere visibile il carattere. se **False**, l'animazione non viene riprodotta.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**richiesta Show.**](/windows/desktop/lwef/iagentcharacter--show)

</dd> </dl>

Evitare di impostare *il parametro bFast* su **True** senza riprodurre un'animazione in anticipo. In caso contrario, il fotogramma carattere potrebbe essere visualizzato, ma non avere alcuna immagine da visualizzare. In particolare, si noti che se si chiama [**MoveTo**](iagentcharacter--moveto.md) quando il carattere non è visibile, non viene riprodotta alcuna animazione. Pertanto, se si chiama il **metodo Show** con *bFast impostato* su **True,** non verrà visualizzata alcuna immagine. Analogamente, se si chiama [**Nascondi**](/windows/desktop/lwef/iagentcharacter--hide), quindi **Mostra** con *bFast* impostato su **True**, non verrà visualizzata alcuna immagine visibile.

Quando si usa il protocollo HTTP per accedere ai dati di animazione e carattere, usare il [**metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità dell'animazione dello stato **Showing** prima di chiamare questo metodo.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Hide**](iagentcharacter--hide.md)


 

 