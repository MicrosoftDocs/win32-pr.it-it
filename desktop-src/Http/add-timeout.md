---
title: add timeout
description: Aggiunge un timeout globale al servizio HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Aggiungi timeout HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2637cb5db663ea36b15eb382a16b02b166e98f88
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104398097"
---
# <a name="add-timeout"></a>add timeout

Aggiunge un timeout globale al servizio HTTP.sys.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {IdleConnectionTimeout \| HeaderWaitTimeout}**
</dt> <dd>

Specifica il tipo di timeout per l'impostazione.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[valore = \] * * * u-Short*
</dt> <dd>

Specifica il valore del timeout (in secondi). Se il valore è esadecimale, aggiungere il prefisso 0x.

</dd> </dl>

## <a name="examples"></a>Esempio

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




