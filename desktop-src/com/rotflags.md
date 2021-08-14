---
title: ROTFlags
description: Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Valore del Registro di sistema ROTFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1695a601cfc6aa2bf39f8be4ed72afb0336279d631d01aeef0625855d83b8837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104403"
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

Si tratta di **un valore \_ DWORD REG.**



| Valore flag | Costante                        |
|------------|---------------------------------|
| 0x1        | **ROTREGFLAGS \_ ALLOWANYCLIENT** |



 

### <a name="rotregflags_allowanyclient-description"></a>Descrizione di ROTREGFLAGS \_ ALLOWANYCLIENT

Se un server COM vuole registrarsi nella ROT e consentire a qualsiasi client di accedere alla registrazione, deve usare il flag **ROTFLAGS \_ ALLOWANYCLIENT.** Un server COM "Attiva come attivatore" non può specificare **ROTFLAGS \_ ALLOWANYCLIENT** perché DCOM Service Control Manager (DCOMSCM) applica un controllo di spoofing a questo flag. Pertanto, in Windows Vista e versioni successive, COM aggiunge il supporto per la voce del Registro di sistema **ROTFlags** che consente al server di stabilire che le registrazioni ROT siano rese disponibili per qualsiasi client.

La voce deve esistere nell'hive **HKEY \_ LOCAL \_ MACHINE.** Questa voce fornisce un server "Attiva come attivatore" con le stesse funzionalità fornite da **ROTFLAGS \_ ALLOWANYCLIENT** per un server RunAs.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiave AppID](appid-key.md)
</dt> <dt>

[Registrazione di server COM](registering-com-servers.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




