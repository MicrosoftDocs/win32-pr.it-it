---
title: OverrideEAPCertificateSelection
description: La chiave del Registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito smart card selezione del certificato e fornirà all'utente più certificati tra cui scegliere.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93efec6968fb27b0d27d88c696101815f0b48c36c100f78092d5b559d4c0f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085915"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

La chiave del Registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito smart card selezione del certificato e fornirà all'utente più certificati tra cui scegliere.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore REG \_ BINARY.**



| Valore | Descrizione                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Non eseguire l'override del comportamento predefinito.                                                                                                                                                                |
| 0x001 | Scegliere l'ultimo certificato collegato dal smart card.                                                                                                                                            |
| 0x010 | Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati smart card.                                                                                                                          |
| 0x100 | Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati dal Registro di sistema.                                                                                                                            |
| 0x101 | Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati dal Registro di sistema e l'ultimo certificato collegato dal smart card. Mostra l'ultimo certificato collegato dall'smart card come selezionato. |
| 0x110 | Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati dal Registro di sistema e dal smart card.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




