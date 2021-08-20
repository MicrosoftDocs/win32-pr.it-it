---
title: LegacyImpersonationLevel
description: Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valore com del Registro di sistema LegacyImpersonationLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd032e83290c18fc3a2588e382ade7730fa2ea39a7847e375b1e887cdbbb90f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048079"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano [**CoInitializeSecurity.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)

> [!Caution]  
> Non è consigliabile modificare questo valore, perché ciò influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbero impedirne il corretto funzionamento. Se si modifica questo valore per influire sulle impostazioni di sicurezza per una particolare applicazione COM, è invece necessario modificare le impostazioni di sicurezza a livello di processo per tale applicazione COM specifica. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [Impostazione della sicurezza a livello di processo.](setting-processwide-security.md)

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di **\_ un valore REG WORD** equivalente alle costanti IMP LEVEL RPC \_ \_ \_ C.



| Valore | Costante                        |
|-------|---------------------------------|
| 1     | RPC \_ C \_ IMP \_ LEVEL \_ ANONYMOUS   |
| 2     | RPC \_ C \_ IMP \_ LEVEL \_ IDENTIFY    |
| 3     | RPC \_ C \_ IMP \_ LEVEL \_ IMPERSONATE |
| 4     | DELEGATO \_ DEL LIVELLO IMP RPC C \_ \_ \_    |



 

Se questo valore del Registro di sistema non è presente, il livello di rappresentazione predefinito stabilito dal sistema è 2 (RPC \_ C \_ IMP LEVEL \_ \_ IDENTIFY).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




