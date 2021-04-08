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
# <a name="object-sid-winnt-provider"></a><span data-ttu-id="9ed02-105">SID oggetto (provider WinNT)</span><span class="sxs-lookup"><span data-stu-id="9ed02-105">Object SID (WinNT Provider)</span></span>

<span data-ttu-id="9ed02-106">L'ID di sicurezza (SID) utente può essere recuperato utilizzando l'attributo **objectSID** .</span><span class="sxs-lookup"><span data-stu-id="9ed02-106">The user security identifier (SID) can be retrieved using the **objectSID** attribute.</span></span> <span data-ttu-id="9ed02-107">**ObjectSID** viene restituito come matrice **Variant** di caratteri che formano la stringa SID.</span><span class="sxs-lookup"><span data-stu-id="9ed02-107">The **objectSID** is returned as a **VARIANT** array of characters that form the SID string.</span></span>

## <a name="example-code"></a><span data-ttu-id="9ed02-108">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="9ed02-108">Example Code</span></span>


```VB
sid = usr.Get("objectSID")
For i = LBound(sid) To UBound(sid)
    Debug.Print sid(i)
Next
```



 

 




