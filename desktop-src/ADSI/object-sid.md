---
title: SID oggetto (provider WinNT)
description: L'ID di sicurezza (SID) utente può essere recuperato utilizzando l'attributo objectSID. ObjectSID viene restituito come matrice VARIANT di caratteri che formano la stringa SID.
ms.assetid: 15845e6d-ea30-4d6c-9f35-b2abc1a564ba
ms.tgt_platform: multiple
keywords:
- ADSI del provider WinNT, esempi di gestione degli utenti, SID oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5d47e939770b9584a85e4e628c5c168901fc1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044062"
---
# <a name="object-sid-winnt-provider"></a>SID oggetto (provider WinNT)

L'ID di sicurezza (SID) utente può essere recuperato utilizzando l'attributo **objectSID** . **ObjectSID** viene restituito come matrice **Variant** di caratteri che formano la stringa SID.

## <a name="example-code"></a>Codice di esempio


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




