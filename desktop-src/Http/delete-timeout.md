---
title: delete timeout
description: Elimina un timeout globale e fa in modo che il HTTP.sys ripristino dei valori predefiniti.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- delete timeout HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95571f3cfb0ff1b77b6da0106cb734af342dcb68689f15dbfdc35f6cb5e7339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014879"
---
# <a name="delete-timeout"></a>delete timeout

Elimina un timeout globale e fa in modo che il HTTP.sys ripristino dei valori predefiniti.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype= \] {idleconnectiontimeout \| headerwaittimeout}**
</dt> <dd>

Specifica il tipo di impostazione di timeout.

</dd> </dl>

## <a name="examples"></a>Esempio

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




