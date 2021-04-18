---
title: StopAll IAgentCharacter
description: StopAll IAgentCharacter
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298644"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter:: StopAll

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Arresta tutte le animazioni (richieste) e le rimuove dalla coda di animazione del carattere.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Oggetto bit che indica i tipi di richieste da arrestare (e rimuovere dalla coda del carattere), costituite da quanto segue:



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| tipo Stop **Long senza segno const** **\_ \_ All = 0xFFFFFFFF;**<br/>              | Arresta tutte le richieste di animazione, incluse le richieste di [**preparazione**](iagentcharacter--prepare.md) non in coda. |
| tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000001;**<br/>             | Arresta tutte le richieste di riproduzione.                                                                                 |
| spostamento del tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000002;**<br/>             | Arresta tutte le richieste di [**spostamento**](https://www.bing.com/search?q=**Move**) .                                               |
| tipo di arresto **lungo senza segno const** **\_ \_ = 0x00000004;**<br/>            | Arresta tutte le richieste di [**pronuncia**](iagentcharacter--speak.md) .                                              |
| tipo di arresto **lungo senza segno const** **\_ \_ Prepare = 0x00000008;**<br/>          | Arresta tutte le richieste di [**preparazione**](iagentcharacter--prepare.md) in coda.                                   |
| tipo di arresto **lungo senza segno const** **\_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Arresta tutte le richieste di [**preparazione**](iagentcharacter--prepare.md) non in coda.                               |
| tipo di arresto **lungo senza segno const** **\_ \_ visibile = 0x00000020;**<br/>          | Arresta tutte le richieste [**Nascondi**](iagentcharacter--hide.md) o [**Mostra**](iagentcharacter--show.md) .       |



 

</dd> </dl>

## <a name="see-also"></a>Vedere anche

[**IAgentCharacter:: Stop**](iagentcharacter--stop.md)


 

 





