---
title: TlsServerUseAllPurposeCert
description: La chiave del Registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati per tutti gli scopi per l'autenticazione EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af2f9d47b4e80409c27c71fe3655a1d3266571e0f8a8dd757e5334b0ef9fec40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085696"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La chiave del Registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati per tutti gli scopi per l'autenticazione EAP-TLS.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore        | Descrizione                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | I certificati per tutti gli scopi nell'archivio certificati del client o del server vengono selezionati per l'autenticazione PEAP.     |
| Altri valori | I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP. |



 

Se questo valore del Registro di sistema non è presente, i certificati per tutti gli scopi nell'archivio certificati del client o del server vengono selezionati per l'autenticazione EAP-TLS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




