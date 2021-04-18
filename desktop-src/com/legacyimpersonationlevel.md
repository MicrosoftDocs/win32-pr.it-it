---
title: LegacyImpersonationLevel
description: Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valore LegacyImpersonationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298367"
---
# <a name="legacyimpersonationlevel"></a>LegacyImpersonationLevel

Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

> [!Caution]  
> Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento. Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).

 

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ Word** equivalente alle costanti a livello di RPC \_ C \_ \_ .



| Valore | Costante                        |
|-------|---------------------------------|
| 1     | \_ \_ livello IMP C \_ RPC \_ Anonimo   |
| 2     | \_ \_ \_ Identificazione livello IMP C \_ RPC    |
| 3     | RAPPRESENTAZIONE a livello di RPC \_ C \_ Imp \_ \_ |
| 4     | \_ \_ \_ delegato livello IMP C \_ RPC    |



 

Se il valore del registro di sistema non è presente, il livello di rappresentazione predefinito stabilito dal sistema è 2 ( \_ Identificazione del livello di RPC C \_ \_ \_ ).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




