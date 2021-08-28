---
title: BypassNegotiation
description: La chiave del Registro di sistema BypassNegotiation determina se si verifica la negoziazione delle funzionalità tra il server e il client o se vengono usate impostazioni preconfigurata.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ba914b9c1ec1d5e3caef6b86ddbda49d021268e456c877ff4f67db86efd2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978251"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

La chiave del Registro di sistema BypassNegotiation determina se si verifica la negoziazione delle funzionalità tra il server e il client o se vengono usate impostazioni preconfigurata.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore   | Descrizione                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Server e client negoziano le funzionalità EAP.                                                                                                                                                        |
| diverso da zero | Il server e il client non negoziano le funzionalità EAP. Server e client usano il valore della chiave del Registro di sistema [AssumePhase2Fragmentation](assumephase2fragmentation.md) per trovare le funzionalità dell'altra parte. |



 

Se questo valore del Registro di sistema non è presente, il server e il client negoziano le funzionalità EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




