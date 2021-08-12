---
title: AssumePhase2Fragmentation
description: La chiave del Registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275838"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

La chiave del Registro di sistema AssumePhase2Fragmentation determina se il server e il client presuppongono la frammentazione della fase 2.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>Commenti

Si tratta di **un valore \_ DWORD REG.**



| Valore   | Descrizione                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | Il server e il client presuppongono che l'altra parte non sia in grado di frammentare la fase 2 durante l'autenticazione PEAP. |
| diverso da zero | Il server e il client presuppongono che l'altra parte sia in grado di frammentare la fase 2 durante l'autenticazione PEAP.     |



 

Se questo valore del Registro di sistema non è presente, il server e il client presuppongono che l'altra parte sia in grado di frammentare la fase 2 durante l'autenticazione PEAP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registro di sistema EAPHost Impostazioni](eaphost-registry-settings.md)
</dt> </dl>

 

 




