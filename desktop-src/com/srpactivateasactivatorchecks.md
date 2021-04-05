---
title: SRPActivateAsActivatorChecks
description: Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni di ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valore SRPActivateAsActivatorChecks del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709433"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni di ActivateAsActivator.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** .

I valori stringa di {N, N, NO, no, no} indicano che l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è stato configurato. Se questo valore del registro di sistema è impostato su qualsiasi altro valore o non esiste, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più rigoroso viene utilizzato per eseguire l'oggetto server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




