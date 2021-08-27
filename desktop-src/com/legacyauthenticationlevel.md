---
title: LegacyAuthenticationLevel
description: Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valore com del Registro di sistema LegacyAuthenticationLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6be9f562a543e4750695ec2bf967b5a261209aae70d0bf91269bc2a074a9e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096951"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

> [!Caution]  
> Non è consigliabile modificare questo valore, perché ciò influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbero impedirne il corretto funzionamento. Se si modifica questo valore per influire sulle impostazioni di sicurezza per una determinata applicazione COM, è invece necessario modificare le impostazioni di sicurezza a livello di processo per tale applicazione COM specifica. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [Impostazione della sicurezza a livello di processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ REG WORD** equivalente alle costanti RPC C \_ \_ AUTHN \_ LEVEL.



| Valore | Costante                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ AUTHN \_ LEVEL \_ NONE           |
| 2     | RPC \_ C \_ AUTHN \_ LEVEL \_ CONNECT        |
| 3     | CHIAMATA A LIVELLO DI AUTENTICAZIONE \_ RPC C \_ \_ \_           |
| 4     | PKT \_ DI LIVELLO RPC C \_ AUTHN \_ \_            |
| 5     | INTEGRITÀ \_ \_ PKT A \_ LIVELLO DI \_ AUTENTICAZIONE \_ RPC C |
| 6     | PRIVACY \_ \_ PKT A \_ LIVELLO DI AUTENTICAZIONE \_ \_ RPC C   |



 

Se questo valore del Registro di sistema non è presente, il livello di autenticazione predefinito stabilito dal sistema è 2 (RPC \_ C \_ AUTHN \_ CONNECT).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




