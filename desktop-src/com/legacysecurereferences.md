---
title: LegacySecureReferences
description: Determina se le chiamate AddRef/release sono protette per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valore LegacySecureReferences del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298368"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina se  / le chiamate di **rilascio** AddRef sono protette per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ SZ** . Il valore ' Y ' o ' y ' indica che **AddRef** e **Release** sono protette. Se il valore del registro di sistema non è presente o è impostato su un valore diverso da' Y ' o ' y ', **AddRef** e **Release** non sono protetti. L'abilitazione di riferimenti protetti rallenta le chiamate remote.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




