---
title: add timeout
description: Aggiunge un timeout globale al HTTP.sys servizio.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- aggiungere il timeout HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66a136acf65022ccc3ba8b05d070e4855a64f7abdf9b0519f7c1628d292aa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047601"
---
# <a name="add-timeout"></a>add timeout

Aggiunge un timeout globale al HTTP.sys servizio.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype= \] {idleconnectiontimeout \| headerwaittimeout}**
</dt> <dd>

Specifica il tipo di timeout per l'impostazione.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[ value= \]**_u-short_
</dt> <dd>

Specifica il valore del timeout (in secondi). Se value è esadecimale, aggiungere il prefisso 0x.

</dd> </dl>

## <a name="examples"></a>Esempio

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




