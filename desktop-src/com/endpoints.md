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
# <a name="endpoints"></a><span data-ttu-id="f27ad-104">Endpoint</span><span class="sxs-lookup"><span data-stu-id="f27ad-104">Endpoints</span></span>

<span data-ttu-id="f27ad-105">Configura un'applicazione COM per l'utilizzo di un numero di porta TCP specificato per le comunicazioni DCOM.</span><span class="sxs-lookup"><span data-stu-id="f27ad-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f27ad-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f27ad-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="f27ad-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f27ad-107">Remarks</span></span>

<span data-ttu-id="f27ad-108">Si tratta di un valore **reg \_ \_ multisz** .</span><span class="sxs-lookup"><span data-stu-id="f27ad-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="f27ad-109">Il valore della *porta* è un numero compreso tra 1024 e 65535 che specifica il numero di porta TCP che verrà utilizzato dall'applicazione com per le comunicazioni DCOM.</span><span class="sxs-lookup"><span data-stu-id="f27ad-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="f27ad-110">Se non si specifica questa chiave del registro di sistema, i numeri di porta per le comunicazioni DCOM vengono assegnati dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="f27ad-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="f27ad-111">Nella maggior parte degli scenari può essere preferibile lasciare invariata la chiave del registro di sistema e consentire a DCOM di assegnare dinamicamente i numeri di porta.</span><span class="sxs-lookup"><span data-stu-id="f27ad-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




