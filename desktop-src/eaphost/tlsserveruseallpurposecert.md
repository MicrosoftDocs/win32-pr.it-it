---
title: TlsServerUseAllPurposeCert
description: La chiave del registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati tutti gli scopi per l'autenticazione EAP-TLS.
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335711"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

La chiave del registro di sistema TlsServerUseAllPurposeCert determina se vengono usati certificati tutti gli scopi per l'autenticazione EAP-TLS.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore        | Descrizione                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Per l'autenticazione PEAP sono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.     |
| Altri valori | I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP. |



 

Se il valore del registro di sistema non è presente, per l'autenticazione EAP-TLS vengono selezionati i certificati tutti gli scopi nell'archivio certificati del client o del server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




