---
title: ROTFlags
description: Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valore ROTFlags del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298035"
---
# <a name="rotflags"></a>ROTFlags

Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore flag | Costante                        |
|------------|---------------------------------|
| 0x1        | **\_ALLOWANYCLIENT ROTREGFLAGS** |



 

### <a name="rotregflags_allowanyclient-description"></a>Descrizione di ROTREGFLAGS \_ ALLOWANYCLIENT

Se un server COM vuole eseguire la registrazione nella tabella ROT e consentire a qualsiasi client di accedere alla registrazione, deve usare il flag **ROTFLAGS \_ ALLOWANYCLIENT** . Un server COM "Activate As Activator" non è in grado di specificare **ROTFLAGS \_ ALLOWANYCLIENT** perché la gestione controllo servizi DCOM (Dcomscm) impone un controllo di spoofing rispetto a questo flag. Pertanto, in Windows Vista e versioni successive COM aggiunge il supporto per la voce del registro di sistema **ROTFlags** che consente al server di stabilire che le registrazioni Rot saranno rese disponibili per qualsiasi client.

La voce deve esistere nell'hive **del \_ \_ computer locale HKEY** . Questa voce fornisce un server "Activate As Activator" con la stessa funzionalità fornita da **ROTFLAGS \_ ALLOWANYCLIENT** per un server RunAs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiave AppID](appid-key.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




