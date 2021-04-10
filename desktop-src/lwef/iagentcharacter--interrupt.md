---
title: IAgentCharacter interrupt
description: IAgentCharacter interrupt
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956360"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter:: interrupt

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrompe l'animazione (richiesta) specificata di un altro carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da interrompere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di **interrupt** .

</dd> </dl>

Se si caricano più caratteri, è possibile usare questo metodo per sincronizzare l'animazione tra i caratteri. Se, ad esempio, un altro carattere si trova in un'animazione di ciclo, questo metodo arresterà l'animazione di ciclo e avvierà l'animazione successiva nella coda del carattere.

**Interrupt interrompe** l'animazione esistente, ma non Scarica la coda di animazione del carattere. Viene avviata l'animazione successiva nella coda del carattere. Per arrestare e scaricare la coda di un carattere, usare il metodo [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .

Non è possibile usare questo metodo per avere un interrupt di tipo carattere, perché il server Microsoft Agent Accoda il metodo **interrupt** nella coda di animazione del carattere. Pertanto, è possibile utilizzare solo **interrupt** per arrestare l'animazione di un altro carattere caricato.

 

 