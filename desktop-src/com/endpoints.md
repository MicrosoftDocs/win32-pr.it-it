---
title: Endpoint
description: Configura un'applicazione COM per l'utilizzo di un numero di porta TCP specificato per le comunicazioni DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valore del registro di sistema endpoint COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395670"
---
# <a name="endpoints"></a>Endpoint

Configura un'applicazione COM per l'utilizzo di un numero di porta TCP specificato per le comunicazioni DCOM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ \_ multisz** .

Il valore della *porta* è un numero compreso tra 1024 e 65535 che specifica il numero di porta TCP che verrà utilizzato dall'applicazione com per le comunicazioni DCOM. Se non si specifica questa chiave del registro di sistema, i numeri di porta per le comunicazioni DCOM vengono assegnati dinamicamente. Nella maggior parte degli scenari può essere preferibile lasciare invariata la chiave del registro di sistema e consentire a DCOM di assegnare dinamicamente i numeri di porta.

 

 




