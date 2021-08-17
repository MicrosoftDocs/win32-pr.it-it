---
title: SRPRunningObjectChecks
description: Determina se i tentativi di connessione agli oggetti in esecuzione vengono schermati per i livelli di attendibilità SRP (Software Restriction Policy) compatibili.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- SRPRunningObjectChecks valore del Registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c416b5f430540282873e37c5e74ef2cccc1c564f4a5b27842ba2a49e99cc8769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129793"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina se i tentativi di connessione agli oggetti in esecuzione vengono schermati per i livelli di attendibilità SRP (Software Restriction Policy) compatibili.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.**

I valori stringa {N, n, NO, No, no} indicano che i tentativi di connessione agli oggetti in esecuzione non vengono cercati per i livelli di attendibilità SRP compatibili. Se questo valore del Registro di sistema è impostato su qualsiasi altro valore o non esiste, l'oggetto in esecuzione non può avere un livello di attendibilità SRP meno stringente rispetto all'oggetto client. Ad esempio, l'oggetto in esecuzione non può avere un livello di attendibilità Non consentito se l'oggetto client ha un livello di attendibilità Senza restrizioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




