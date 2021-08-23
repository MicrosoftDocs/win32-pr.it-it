---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff1811e7b7ee323ef57e21dbeea4e6ea9d33dc8bc735327ec9ba5afc2ce299b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609780"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Arresta tutte le animazioni (richieste) e le rimuove dalla coda di animazione del carattere.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Campo di bit che indica i tipi di richieste da arrestare (e rimuovere dalla coda del carattere), costituito dagli elementi seguenti:



| Valore                                                                                  |  Descrizione                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**<br/>              | Arresta tutte le richieste di animazione, incluse le richieste [**di preparazione**](iagentcharacter--prepare.md) non in coda. |
| **const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**<br/>             | Arresta tutte le richieste di riproduzione.                                                                                 |
| **const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**<br/>             | Arresta tutte [**le richieste di**](https://www.bing.com/search?q=**Move**) spostamento.                                               |
| **const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**<br/>            | Arresta tutte [**le richieste Speak.**](iagentcharacter--speak.md)                                              |
| **const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**<br/>          | Arresta tutte le richieste [**Prepare in**](iagentcharacter--prepare.md) coda.                                   |
| **const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Arresta tutte le richieste Prepare non [**in**](iagentcharacter--prepare.md) coda.                               |
| **const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**<br/>          | Arresta [**tutte le richieste Nascondi**](iagentcharacter--hide.md) [**o**](iagentcharacter--show.md) Mostra.       |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter::Stop**](iagentcharacter--stop.md)


 

 





