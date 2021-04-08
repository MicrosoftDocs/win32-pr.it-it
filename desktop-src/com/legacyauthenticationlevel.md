---
title: LegacyAuthenticationLevel
description: Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valore LegacyAuthenticationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045364"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ Word** equivalente alle \_ costanti del \_ livello auth C RPC \_ .



| Valore | Costante                             |
|-------|--------------------------------------|
| 1     | \_ \_ livello auth C \_ RPC \_           |
| 2     | \_connessione a \_ livello auth \_ C \_ RPC        |
| 3     | \_chiamata al \_ livello auth \_ C \_ RPC           |
| 4     | \_ \_ \_ PKT livello auth C RPC \_            |
| 5     | \_ \_ \_ integrità PKT del livello auth \_ C \_ RPC |
| 6     | \_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_   |



 

Se il valore del registro di sistema non è presente, il livello di autenticazione predefinito stabilito dal sistema è 2 ( \_ \_ connessione auth C RPC \_ ).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




