---
title: LegacySecureReferences
description: Determina se le chiamate AddRef/Release sono protette per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valore del Registro di sistema LegacySecureReferences COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef3a4ab964d73fa4b194c734f28c23ff068239370088c090051464129b6caf14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736548"
---
# <a name="legacysecurereferences"></a>LegacySecureReferences

Determina se le chiamate di versione **AddRef** /  sono protette per le applicazioni che non chiamano [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG SZ.** Il valore "Y" o "y" indica che **AddRef** e **Release** sono protetti. Se questo valore del Registro di sistema non è presente o è impostato su un valore diverso da 'Y' o 'y', **AddRef** e **Release** non sono protetti. L'abilitazione dei riferimenti sicuri rallenta le chiamate remote.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




