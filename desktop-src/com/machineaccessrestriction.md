---
title: MachineAccessRestriction
description: Imposta i criteri di restrizione a livello di computer per l'accesso al componente.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valore MachineAccessRestriction del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298633"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Imposta i criteri di restrizione a livello di computer per l'accesso al componente.

> [!Caution]  
> La modifica di questo valore influirà su tutte le applicazioni server COM e potrebbe impedire il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno restrittive rispetto a quelle a livello di computer, la riduzione delle restrizioni a livello di computer può esporre tali applicazioni a accessi non desiderati. Viceversa, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** .

Le entità non concesse in questo caso non possono ottenerle anche se le autorizzazioni vengono concesse dal valore del registro di sistema [DefaultAccessPermission](defaultaccesspermission.md) o dalla funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Per impostazione predefinita, i membri del gruppo Everyone possono ottenere le autorizzazioni di accesso locale e remoto, mentre gli utenti anonimi possono ottenere le autorizzazioni di accesso locale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




