---
title: OverrideEAPCertificateSelection
description: La chiave del registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito per la selezione del certificato della smart card e fornirà all'utente più certificati tra cui scegliere.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857854"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

La chiave del registro di sistema OverrideEAPCertificateSelection determina se il client eseguirà l'override del comportamento predefinito per la selezione del certificato della smart card e fornirà all'utente più certificati tra cui scegliere.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **\_ binario REG** .



| Valore | Descrizione                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Non eseguire l'override del comportamento predefinito.                                                                                                                                                                |
| 0x001 | Scegliere l'ultimo certificato collegato dalla smart card.                                                                                                                                            |
| 0x010 | Mostra tutti i certificati nell'interfaccia utente di selezione dei certificati dalla smart card.                                                                                                                          |
| 0x100 | Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema.                                                                                                                            |
| 0x101 | Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema e l'ultimo certificato collegato dalla smart card. Mostra l'ultimo certificato collegato dalla smart card selezionato. |
| 0x110 | Mostra tutti i certificati nell'interfaccia utente di selezione del certificato dal registro di sistema e dalla smart card.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




