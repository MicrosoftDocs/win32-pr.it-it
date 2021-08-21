---
title: PeapServerUseAllPurposeCert
description: La chiave del Registro di sistema PeapServerUseAllPurposeCert determina se vengono usati certificati per tutti gli scopi per l'autenticazione PEAP.
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042819"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

La chiave del Registro di sistema PeapServerUseAllPurposeCert determina se vengono usati certificati per tutti gli scopi per l'autenticazione PEAP.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore        | Descrizione                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | I certificati per tutti gli scopi nell'archivio certificati del client o del server vengono selezionati per l'autenticazione PEAP.     |
| Altri valori | I certificati per tutti gli scopi nell'archivio certificati del client o del server non sono selezionati per l'autenticazione PEAP. |



 

Se questo valore del Registro di sistema non è presente, i certificati per tutti gli scopi nell'archivio certificati del client o del server vengono selezionati per l'autenticazione PEAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




