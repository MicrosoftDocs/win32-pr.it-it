---
title: show servicestate
description: Mostra uno snapshot del servizio HTTP.
ms.assetid: a50a3ef5-5e62-412e-a443-11d453778f70
keywords:
- Mostra HTTP ServiceState
topic_type:
- apiref
api_name:
- show servicestate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f79bfdb946d286c31ce284efa09e75ad93c34438
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299271"
---
# <a name="show-servicestate"></a><span data-ttu-id="9db47-104">show servicestate</span><span class="sxs-lookup"><span data-stu-id="9db47-104">show servicestate</span></span>

<span data-ttu-id="9db47-105">Mostra uno snapshot del servizio HTTP.</span><span class="sxs-lookup"><span data-stu-id="9db47-105">Shows a snapshot of the HTTP service.</span></span>

``` syntax
show servicestate [[view=]{session|requestq}] [[verbose=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="9db47-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9db47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db47-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[visualizzazione = \] {Session \| requestq}\]**</span><span class="sxs-lookup"><span data-stu-id="9db47-107"><span id="__view___session_requestq__"></span><span id="__VIEW___SESSION_REQUESTQ__"></span>**\[\[view=\]{session\|requestq}\]**</span></span>
</dt> <dd>

<span data-ttu-id="9db47-108">Visualizzazione dello stato del servizio HTTP in base alla sessione del server o alle code di richieste.</span><span class="sxs-lookup"><span data-stu-id="9db47-108">View snapshot of HTTP service state based on server session or request queues.</span></span>

</dd> <dt>

<span data-ttu-id="9db47-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose = \] {Yes \| No}\]**</span><span class="sxs-lookup"><span data-stu-id="9db47-109"><span id="__verbose___yes_no__"></span><span id="__VERBOSE___YES_NO__"></span>**\[\[verbose=\]{yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="9db47-110">Visualizzare le informazioni dettagliate che mostrano anche le informazioni sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="9db47-110">View verbose information showing property information too.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9db47-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="9db47-111">Examples</span></span>

<span data-ttu-id="9db47-112">**Mostra visualizzazione ServiceState = sessione**</span><span class="sxs-lookup"><span data-stu-id="9db47-112">**show servicestate view=session**</span></span>

<span data-ttu-id="9db47-113">**Mostra visualizzazione ServiceState = requestq verbose = Sì**</span><span class="sxs-lookup"><span data-stu-id="9db47-113">**show servicestate view=requestq verbose=yes**</span></span>

 

 




