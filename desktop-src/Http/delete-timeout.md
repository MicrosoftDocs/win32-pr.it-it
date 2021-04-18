---
title: delete timeout
description: Elimina un timeout globale e fa in modo che il servizio di HTTP.sys ripristini i valori predefiniti.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- Elimina timeout HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299273"
---
# <a name="delete-timeout"></a>delete timeout

Elimina un timeout globale e fa in modo che il servizio di HTTP.sys ripristini i valori predefiniti.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {IdleConnectionTimeout \| HeaderWaitTimeout}**
</dt> <dd>

Specifica il tipo di impostazione di timeout.

</dd> </dl>

## <a name="examples"></a>Esempio

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




