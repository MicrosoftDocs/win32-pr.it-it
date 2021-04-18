---
title: AssumePhase2Fragmentation
description: La chiave del registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398340"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

La chiave del registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** .



| Valore   | Descrizione                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Server e client presuppongono che l'altra parte non sia in grado di deframmentare la fase 2 durante l'autenticazione PEAP. |
| diverso da zero | Server e client presuppongono che l'altra parte sia in grado di deframmentare la fase 2 durante l'autenticazione PEAP.     |



 

Se il valore del registro di sistema non è presente, il server e il client presuppongono che l'altra parte sia in grado di la frammentazione della fase 2 durante l'autenticazione PEAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazioni del registro di sistema EAPHost](eaphost-registry-settings.md)
</dt> </dl>

 

 




