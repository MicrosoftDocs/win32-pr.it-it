---
title: LaunchPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe. Questo valore può essere aggiunto in qualsiasi chiave AppID per limitare l'attivazione da parte di client remoti di classi specifiche.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valore del Registro di sistema LaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5967ee63288b11edca017820b9a367dd4e6c017e993330616e633e7448a098b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756101"
---
# <a name="launchpermission"></a>LaunchPermission

Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe. Questo valore può essere aggiunto in qualsiasi [**chiave AppID**](appid-key.md) per limitare l'attivazione da parte di client remoti di classi specifiche.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore REG \_ BINARY.** Quando si riceve una richiesta locale o remota per avviare il server di questa classe, l'ACL descritto da questo valore viene controllato durante la rappresentazione del client e il relativo esito positivo consente o non consente l'avvio del server. Se questo valore non esiste, il [**valore DefaultLaunchPermission**](defaultlaunchpermission.md) viene controllato nello stesso modo per determinare se il codice della classe può essere avviato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Coinitializesecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




