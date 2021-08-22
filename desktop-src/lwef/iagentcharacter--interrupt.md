---
title: IAgentCharacter Interrupt
description: IAgentCharacter Interrupt
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ea2529d4da78607d3ad22bf688857c8917e3317df17ae9a5eb99d0b184878e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750906"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter::Interrupt

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrompe l'animazione specificata (richiesta) di un altro carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene restituita, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

ID della richiesta da interrompere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID **richiesta interrupt.**

</dd> </dl>

Se si caricano più caratteri, è possibile usare questo metodo per sincronizzare l'animazione tra i caratteri. Ad esempio, se un altro carattere è in un'animazione a ciclo continuo, questo metodo arresta l'animazione a ciclo continuo e avvia l'animazione successiva nella coda del carattere.

**Interrupt** arresta l'animazione esistente, ma non scarica la coda di animazione del carattere. Avvia l'animazione successiva nella coda del carattere. Per arrestare e scaricare la coda di un carattere, usare il [**metodo Stop.**](/windows/desktop/lwef/iagentcharacter--stop)

Non è possibile usare questo metodo per fare in modo che un carattere interrompa se stesso perché il server Microsoft Agent accoda il **metodo Interrupt** nella coda di animazione del carattere. Pertanto, è possibile usare **Interrupt solo per** arrestare l'animazione di un altro carattere caricato.

 

 