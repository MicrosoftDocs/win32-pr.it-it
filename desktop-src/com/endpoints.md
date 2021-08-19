---
title: Endpoint
description: Configura un'applicazione COM per l'utilizzo di un numero di porta TCP specificato per le comunicazioni DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valore com del Registro di sistema degli endpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ee2444be55aaf32c028792100e3e6f0ed6989509b7c0af02c5d83bd739fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048319"
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

Si tratta di **un valore REG MULTI \_ \_ SZ.**

Il *valore* della porta è un numero compreso tra 1024 e 65535 che specifica il numero di porta TCP che verrà utilizzato dall'applicazione COM per le comunicazioni DCOM. Se non si specifica questa chiave del Registro di sistema, i numeri di porta per le comunicazioni DCOM vengono assegnati dinamicamente. Nella maggior parte degli scenari è preferibile lasciare indefinita questa chiave del Registro di sistema e consentire a DCOM di assegnare in modo dinamico i numeri di porta.

 

 




