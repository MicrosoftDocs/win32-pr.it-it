---
description: Il messaggio TAPI LINE \_ APPNEWCALLHUB viene inviato per informare un'applicazione quando è stato creato un nuovo hub chiamate.
ms.assetid: cf693d95-9abb-4999-81b6-7d2aa06d0f58
title: LINE_APPNEWCALLHUB messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bf413f16270ba54fd7447cc0c41c040759edd699c995eac79314b9961486ce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905905"
---
# <a name="line_appnewcallhub-message"></a>LINE \_ APPNEWCALLHUB MESSAGE

Il messaggio TAPI **LINE \_ APPNEWCALLHUB** viene inviato per informare un'applicazione quando è stato creato un nuovo hub chiamate.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per la chiamata.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga della chiamata.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Livello di rilevamento nel nuovo hub, come definito da una delle costanti [**LINECALLHUBTRACKING \_**](linecallhubtracking--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questo messaggio ha origine con TAPI anziché con un provider di servizi, quindi non esiste alcun messaggio TSPI corrispondente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




