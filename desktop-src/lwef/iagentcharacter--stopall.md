---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120914"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Arresta tutte le animazioni (richieste) e le rimuove dalla coda di animazione del carattere.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Campo di bit che indica i tipi di richieste da arrestare (e rimuovere dalla coda del carattere), costituite dalle seguenti:



| Valore                                                                                  |  Descrizione                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**<br/>              | Arresta tutte le richieste di animazione, incluse le richieste [**di preparazione**](iagentcharacter--prepare.md) non in coda. |
| **const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**<br/>             | Arresta tutte le richieste di riproduzione.                                                                                 |
| **const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**<br/>             | Arresta tutte [**le richieste Move.**](https://www.bing.com/search?q=**Move**)                                               |
| **const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**<br/>            | Arresta tutte [**le richieste Speak.**](iagentcharacter--speak.md)                                              |
| **const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**<br/>          | Arresta tutte le richieste [**Prepare in**](iagentcharacter--prepare.md) coda.                                   |
| **const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Arresta tutte le richieste [**di preparazione**](iagentcharacter--prepare.md) non in coda.                               |
| **const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**<br/>          | Arresta [**tutte le richieste Nascondi**](iagentcharacter--hide.md) [**o**](iagentcharacter--show.md) Mostra.       |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Stop**](iagentcharacter--stop.md)


 

 





