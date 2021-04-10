---
title: AuthenticationLevel
description: Imposta il livello di autenticazione per le applicazioni che non chiamano CoInitializeSecurity o per le applicazioni che chiamano CoInitializeSecurity e specificano un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valore AuthenticationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332636"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

Imposta il livello di autenticazione per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o per le applicazioni che chiamano **CoInitializeSecurity** e specificano un AppID.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** equivalente alle \_ costanti del \_ livello auth C RPC \_ .



| Valore | Costante                             |
|-------|--------------------------------------|
| 1     | \_ \_ livello auth C \_ RPC \_           |
| 2     | \_connessione a \_ livello auth \_ C \_ RPC        |
| 3     | \_chiamata al \_ livello auth \_ C \_ RPC           |
| 4     | \_ \_ \_ PKT livello auth C RPC \_            |
| 5     | \_ \_ \_ integrità PKT del livello auth \_ C \_ RPC |
| 6     | \_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_   |



 

Il valore di **AuthenticationLevel** è simile al valore di [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) . Se il valore **AuthenticationLevel** è presente, viene usato al posto del valore **LegacyAuthenticationLevel** per tale AppID.

Se il valore **AuthenticationLevel** è di tipo errato o non è compreso nell'intervallo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ha esito negativo, causando l'esito negativo del marshalling dell'interfaccia. In questo modo si impedisce all'applicazione di effettuare tutte le chiamate (Cross-Apartment, cross-thread, tra processi o tra computer).

I valori **AuthenticationLevel** e [**AccessPermission**](accesspermission.md) sono indipendenti. Se non è presente, viene usato il valore predefinito. Le regole seguenti elencano l'interazione tra il valore di **AuthenticationLevel** e il valore di **AccessPermission** :

-   Se **AuthenticationLevel** è None, i valori [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per tale applicazione).
-   Se **AuthenticationLevel** non è presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) è None, i valori [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per tale applicazione).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti del livello di autenticazione](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




