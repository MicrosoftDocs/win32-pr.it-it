---
title: SRPRunningObjectChecks
description: Determina se i tentativi di connessione agli oggetti in esecuzione vengono selezionati per i livelli di attendibilità dei criteri di restrizione software (SRP) compatibili.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valore SRPRunningObjectChecks del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709430"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Determina se i tentativi di connessione agli oggetti in esecuzione vengono selezionati per i livelli di attendibilità dei criteri di restrizione software (SRP) compatibili.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** .

I valori stringa di {N, N, NO, no, no} indicano che i tentativi di connessione agli oggetti in esecuzione non vengono selezionati per i livelli di attendibilità SRP compatibili. Se questo valore del registro di sistema è impostato su qualsiasi altro valore o non esiste, l'oggetto in esecuzione non può disporre di un livello di attendibilità del rollup meno rigoroso rispetto all'oggetto client. L'oggetto in esecuzione, ad esempio, non può avere un livello di attendibilità non consentito se l'oggetto client ha un livello di attendibilità senza restrizioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




