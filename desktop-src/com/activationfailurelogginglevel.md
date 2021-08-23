---
title: ActivationFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del log eventi relative alle richieste non riuscite per l'avvio e l'attivazione del componente.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Valore com del Registro di sistema ActivationFailureLoggingLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51d0f92dbf1b54d572de44e750fba20ca39954ced57b6276ecdc4b8c4e07960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855101"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Imposta il livello di dettaglio delle voci del log eventi relative alle richieste non riuscite per l'avvio e l'attivazione del componente.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore | Descrizione                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Usare la registrazione discrezionale. Gli errori del log per impostazione predefinita, ma i client possono eseguire l'override di questo comportamento specificando CLSCTX \_ NO FAILURE LOG in \_ \_ [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex). Rappresenta il valore predefinito. |
| 1     | Registrare sempre tutti gli errori indipendentemente dal client specificato.                                                                                                                                                      |
| 2     | Non registrare mai gli errori indipendentemente dal client specificato.                                                                                                                                                       |



 

Se è necessaria un'applicazione per controllare la registrazione degli eventi, è consigliabile impostare questo valore su 0 e scrivere il codice client per eseguirne l'override quando necessario. È consigliabile non impostare il valore su 2. Se la registrazione degli eventi è disabilitata, è più difficile diagnosticare i problemi. Per gli errori di autorizzazione delle restrizioni del computer, in cui COM non ha i bit CLSCTX, COM considera il valore 0 come 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




