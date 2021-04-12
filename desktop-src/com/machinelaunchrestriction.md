---
title: MachineLaunchRestriction
description: Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione dei componenti.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valore MachineLaunchRestriction del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221934"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione dei componenti.

> [!Caution]  
> La modifica di questo valore influirà su tutte le applicazioni server COM e potrebbe impedire il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno restrittive rispetto a quelle a livello di computer, la riduzione delle restrizioni a livello di computer può esporre tali applicazioni a accessi non desiderati. Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** .

Le entità non concesse in questo caso non possono ottenerle anche se le autorizzazioni vengono concesse dal valore del registro di sistema [DefaultAccessPermission](defaultaccesspermission.md) o dalla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Per impostazione predefinita, gli amministratori possono ottenere le autorizzazioni di avvio e attivazione locali e remote e i membri del gruppo Everyone possono ottenere le autorizzazioni di attivazione e avvio locali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




