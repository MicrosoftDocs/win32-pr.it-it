---
title: TlsServerAcceptAllPurposeCert
description: La chiave del Registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione EAP-TLS.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804185773a948299aed3d8b8e2f581d8d8355d112720b66e860bd1f00b7fc3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085753"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

La chiave del Registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per tutti gli scopi vengono accettati per l'autenticazione EAP-TLS.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore        | Descrizione                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Il server e il client accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.       |
| Altri valori | Il server e il client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS |



 

Se questo valore del Registro di sistema non è presente, il server e il client accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro di sistema EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




