---
title: PeapServerAcceptAllPurposeCert
description: La chiave del registro di sistema PeapServerAcceptAllPurposeCert determina se per l'autenticazione PEAP sono accettati certificati tutti gli scopi.
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299313"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

La chiave del registro di sistema PeapServerAcceptAllPurposeCert determina se per l'autenticazione PEAP sono accettati certificati tutti gli scopi.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore        | Descrizione                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | Server e client accettano i certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS.       |
| Altri valori | Server e client non accettano certificati per tutti gli scopi inviati dall'altra parte per l'autenticazione EAP-TLS |



 

Se il valore del registro di sistema non è presente, il server e il client accettano i certificati tutti gli scopi inviati dall'altra parte per l'autenticazione PEAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




