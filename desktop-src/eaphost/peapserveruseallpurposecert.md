---
title: PeapServerUseAllPurposeCert
description: La chiave del registro di sistema PeapServerUseAllPurposeCert determina se vengono utilizzati certificati tutti gli scopi per l'autenticazione PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104335740"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La chiave del registro di sistema PeapServerUseAllPurposeCert determina se vengono utilizzati certificati tutti gli scopi per l'autenticazione PEAP.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore        | Descrizione                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | Per l'autenticazione PEAP sono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.     |
| Altri valori | I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP. |



 

Se il valore del registro di sistema non è presente, per l'autenticazione PEAP vengono selezionati i certificati per tutti gli scopi nell'archivio certificati del client o del server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




