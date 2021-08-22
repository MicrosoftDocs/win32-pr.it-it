---
title: Generazione dell'UUID
description: Il primo passaggio per definire l'interfaccia consiste nell'usare l'utilità uuidgen per generare un identificatore univoco universale (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Chiamata di procedura remota RPC, attività, generazione dell'UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c1fbb257a4ce41a4fc0159f703a01705b4dd5926356d7850ec4ce1e0d2e002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929528"
---
# <a name="generating-the-uuid"></a>Generazione dell'UUID

Il primo passaggio per definire l'interfaccia consiste nell'usare l'utilità **uuidgen** per generare un identificatore univoco universale (UUID). Un UUID consente alle applicazioni client e server di identificarsi a vicenda. **L'utilità uuidgen** (Uuidgen.exe) viene installata automaticamente quando si installa Platform Software Development Kit (SDK).

Il comando seguente genera un UUID e crea un file modello denominato Hello.idl.

**uuidgen /i /ohello.idl**

Il modello hello.idl sarà simile al seguente (con un UUID diverso, naturalmente).

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




