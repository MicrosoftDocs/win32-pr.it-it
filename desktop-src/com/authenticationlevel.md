---
title: AuthenticationLevel
description: Imposta il livello di autenticazione per le applicazioni che non chiamano CoInitializeSecurity o per le applicazioni che chiamano CoInitializeSecurity e specificano un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valore del Registro di sistema AuthenticationLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120531"
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

Si tratta di **un \_ valore DWORD REG** equivalente alle costanti RPC C \_ \_ AUTHN \_ LEVEL.



| Valore | Costante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | CHIAMATA A LIVELLO DI AUTENTICAZIONE \_ RPC C \_ \_ \_           |
| 4     | PKT \_ DI LIVELLO RPC C \_ AUTHN \_ \_            |
| 5     | INTEGRITÀ \_ \_ PKT A \_ LIVELLO DI \_ AUTENTICAZIONE \_ RPC C |
| 6     | PRIVACY PKT DI LIVELLO \_ RPC C \_ AUTHN \_ \_ \_   |



 

Il **valore AuthenticationLevel** è simile al [**valore LegacyAuthenticationLevel.**](legacyauthenticationlevel.md) Se il **valore AuthenticationLevel** è presente, viene usato al posto del **valore LegacyAuthenticationLevel** per l'AppID.

Se il **valore AuthenticationLevel** è di tipo errato o non è compreso nell'intervallo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ha esito negativo, causando l'esito negativo del marshalling dell'interfaccia. In questo modo l'applicazione non effettua alcuna chiamata (cross-apartment, cross-thread, cross-process o cross-computer).

I **valori AuthenticationLevel** e [**AccessPermission**](accesspermission.md) sono indipendenti. Se non ne è presente uno, viene usato il valore predefinito. Le regole seguenti elencano l'interazione tra **il valore AuthenticationLevel** e il **valore AccessPermission:**

-   Se **AuthenticationLevel è** NONE, i [**valori AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per l'applicazione).
-   Se **AuthenticationLevel non** è presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) è NONE, i [**valori AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per l'applicazione).

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

 

 




