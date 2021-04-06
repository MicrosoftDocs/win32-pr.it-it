---
title: LaunchPermission
description: Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe. Questo valore può essere aggiunto con qualsiasi chiave AppID per limitare l'attivazione da parte di client remoti di classi specifiche.
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- Valore LaunchPermission del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045365"
---
# <a name="launchpermission"></a>LaunchPermission

Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe. Questo valore può essere aggiunto con qualsiasi chiave [**AppID**](appid-key.md) per limitare l'attivazione da parte di client remoti di classi specifiche.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** . Quando riceve una richiesta locale o remota per avviare il server di questa classe, l'ACL descritto da questo valore viene verificato durante la rappresentazione del client e il suo esito positivo consente o impedisce l'avvio del server. Se questo valore non esiste, il valore [**DefaultLaunchPermission**](defaultlaunchpermission.md) viene controllato nello stesso modo per determinare se il codice della classe può essere avviato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> </dl>

 

 




