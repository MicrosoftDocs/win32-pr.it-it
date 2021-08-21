---
title: SRPActivateAsActivatorChecks
description: Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- SRPActivateAsActivatorChecks valore del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c88accfb436124f13fc25eea9a5ee3621c7784fb509de7d842765bf0a072c977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104272"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Determina se i livelli di attendibilità dei criteri di restrizione software vengono usati durante le attivazioni ActivateAsActivator.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.**

I valori stringa {N, n, NO, No, no} indicano che l'oggetto server viene eseguito con il livello di attendibilità SRP dell'oggetto client, indipendentemente dal livello di attendibilità SRP con cui è stato configurato. Se questo valore del Registro di sistema è impostato su qualsiasi altro valore o non esiste, il livello di attendibilità SRP configurato per l'oggetto server viene confrontato con il livello di attendibilità SRP dell'oggetto client e il livello di attendibilità più stringente viene usato per eseguire l'oggetto server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




