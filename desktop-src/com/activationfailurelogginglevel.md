---
title: ActivationFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi sulle richieste non riuscite per l'avvio e l'attivazione dei componenti.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valore ActivationFailureLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396870"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Imposta il livello di dettaglio delle voci del registro eventi sulle richieste non riuscite per l'avvio e l'attivazione dei componenti.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore | Descrizione                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Usare la registrazione discrezionale. Per impostazione predefinita, gli errori di log, ma i client possono eseguire l'override di questo comportamento specificando CLSCTX \_ nessun \_ log degli errori \_ in [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Rappresenta il valore predefinito. |
| 1     | Registrare sempre tutti gli errori indipendentemente dal client specificato.                                                                                                                                                      |
| 2     | Non registrare mai eventuali errori indipendentemente dal client specificato.                                                                                                                                                       |



 

Se è necessaria un'applicazione per controllare la registrazione degli eventi, è consigliabile impostare questo valore su 0 e scrivere il codice client per eseguirne l'override quando necessario. Si consiglia vivamente di non impostare il valore su 2. Se la registrazione degli eventi è disabilitata, è più difficile diagnosticare i problemi. Per gli errori di autorizzazione per le restrizioni del computer, in cui COM non dispone dei bit CLSCTX, COM considererà un valore pari a 0 come 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




