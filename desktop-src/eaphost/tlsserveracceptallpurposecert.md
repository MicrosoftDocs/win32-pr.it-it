---
title: TlsServerAcceptAllPurposeCert
description: La chiave del registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per l'autenticazione EAP-TLS sono accettati per tutti gli scopi.
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299297"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

La chiave del registro di sistema TlsServerAcceptAllPurposeCert determina se i certificati per l'autenticazione EAP-TLS sono accettati per tutti gli scopi.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore        | Descrizione                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server e client accettano i certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.       |
| Altri valori | Server e client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS |



 

Se il valore del registro di sistema non è presente, il server e il client accettano i certificati tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




