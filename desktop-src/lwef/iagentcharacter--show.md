---
title: IAgentCharacter Show
description: IAgentCharacter Show
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046747"
---
# <a name="iagentcharactershow"></a>IAgentCharacter:: Show

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Visualizza un carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Visualizzazione del flag di animazione stato. Se questo parametro è **true**, l'animazione di stato che **Visualizza** viene riprodotta dopo aver reso visibile il carattere; Se **false**, l'animazione non viene riprodotto.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di [**visualizzazione**](/windows/desktop/lwef/iagentcharacter--show) .

</dd> </dl>

Evitare di impostare il parametro *bFast* su **true** senza prima riprodurre un'animazione. in caso contrario, è possibile che venga visualizzato il frame di caratteri, ma che non sia presente alcuna immagine da visualizzare. In particolare, si noti che se si chiama [**MoveTo**](iagentcharacter--moveto.md) quando il carattere non è visibile, non viene eseguita alcuna animazione. Se pertanto si chiama il metodo **show** con *Bfast* impostato su **true**, non verrà visualizzata alcuna immagine. In modo analogo, se si chiama [**Nascondi**](/windows/desktop/lwef/iagentcharacter--hide), quindi **Mostra** con *bFast* impostato su **true**, non sarà presente alcuna immagine visibile.

Quando si utilizza il protocollo HTTP per accedere ai dati di tipo carattere e animazione, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità dell'animazione **di visualizzazione dello stato prima** di chiamare questo metodo.

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Hide**](iagentcharacter--hide.md)


 

 