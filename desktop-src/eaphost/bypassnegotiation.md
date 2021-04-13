---
title: BypassNegotiation
description: La chiave del registro di sistema BypassNegotiation determina se la negoziazione delle funzionalità tra il server e il client si verifica o se vengono utilizzate impostazioni preconfigurate.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398358"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

La chiave del registro di sistema BypassNegotiation determina se la negoziazione delle funzionalità tra il server e il client si verifica o se vengono utilizzate impostazioni preconfigurate.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore   | Descrizione                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | Server e client negoziano le funzionalità EAP.                                                                                                                                                        |
| diverso da zero | Server e client non negoziano le funzionalità EAP. Server e client utilizzano il valore della chiave del registro di sistema [AssumePhase2Fragmentation](assumephase2fragmentation.md) per trovare le funzionalità dell'altra parte. |



 

Se il valore del registro di sistema non è presente, il server e il client negoziano le funzionalità EAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




