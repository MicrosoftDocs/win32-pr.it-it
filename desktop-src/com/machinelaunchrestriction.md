---
title: MachineLaunchRestriction
description: Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione del componente.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valore del Registro di sistema MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048059"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Imposta i criteri di restrizione a livello di computer per l'avvio e l'attivazione del componente.

> [!Caution]  
> La modifica di questo valore influirà su tutte le applicazioni server COM e potrebbe impedirne il corretto funzionamento. Se sono presenti applicazioni server COM con restrizioni meno stringenti rispetto alle restrizioni a livello di computer, la riduzione delle restrizioni a livello di computer può esporre queste applicazioni ad accesso indesiderato. Al contrario, se si aumentano le restrizioni a livello di computer, alcune applicazioni server COM potrebbero non essere più accessibili chiamando le applicazioni.

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore REG \_ BINARY.**

Le entità a cui non sono state concesse autorizzazioni in questo caso non possono ottenerle anche se le autorizzazioni vengono concesse dal valore del Registro di sistema [DefaultAccessPermission](defaultaccesspermission.md) o dalla [**funzione CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

Per impostazione predefinita, gli amministratori possono ottenere le autorizzazioni di avvio e attivazione locali e remote e i membri del gruppo Everyone possono ottenere le autorizzazioni di attivazione e avvio locali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza per le applicazioni COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




