---
title: PeapServerAcceptAllPurposeCert
description: La chiave del Registro di sistema PeapServerAcceptAllPurposeCert determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione PEAP.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784683"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La chiave del Registro di sistema PeapServerAcceptAllPurposeCert determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione PEAP.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore        | Descrizione                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Il server e il client accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.       |
| Altri valori | Il server e il client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS |



 

Se questo valore del Registro di sistema non è presente, il server e il client accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione PEAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro di sistema EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




