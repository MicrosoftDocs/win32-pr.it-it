---
title: PreferredServerBitness
description: Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valore del Registro di sistema PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b003fd4bdd861cbfd82e249123831e4e017eaeef1ad76b95121244fd415ae0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309986"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un \_ valore DWORD REG** disponibile solo nelle versioni a 64 bit di Windows.



| Valore | Descrizione                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Associare l'architettura del server all'architettura client. Ad esempio, se il client è a 32 bit, usare una versione a 32 bit del server, se disponibile. In caso contrario, la richiesta di attivazione del client avrà esito negativo. |
| 2     | Usare una versione a 32 bit del server. Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.                                                                                                      |
| 3     | Usare una versione a 64 bit del server. Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.                                                                                                      |



 

Se questo valore non è presente, eseguire le seguenti operazione:

-   Se il computer che ospita il server esegue Windows XP o Windows Server 2003 senza SP1 o versione successiva installata, COM preferirà una versione a 64 bit del server, se disponibile; in caso contrario, verrà attivata una versione a 32 bit del server.
-   Se il computer che ospita il server esegue Windows Server 2003 con SP1 o versione successiva installata, COM tenterà di associare l'architettura del server all'architettura client. In altre parole, per un client a 32 bit, COM attiverà un server a 32 bit, se disponibile; in caso contrario, verrà attivata una versione a 64 bit del server. Per un client a 64 bit, COM attiverà un server a 64 bit, se disponibile. in caso contrario, attiverà un server a 32 bit.

Il client può anche specificare le proprie preferenze di architettura tramite i flag CLSCTX \_ ACTIVATE \_ 32 BIT SERVER e \_ \_ CLSCTX \_ ACTIVATE 64 BIT SERVER \_ e \_ \_ questi eseguiranno l'override delle preferenze del server. Per altre informazioni e un grafico delle possibili interazioni tra le preferenze dell'architettura client e server, vedere [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 