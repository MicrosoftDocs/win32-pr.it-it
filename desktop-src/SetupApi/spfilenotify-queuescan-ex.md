---
description: La notifica SPFILENOTIFY QUEUESCAN EX viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia \_ \_ della coda di file.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: SPFILENOTIFY_QUEUESCAN_EX messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992591"
---
# <a name="spfilenotify_queuescan_ex-message"></a>SPFILENOTIFY \_ QUEUESCAN \_ EX message

La **notifica SPFILENOTIFY \_ QUEUESCAN \_ EX** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ SCAN USE \_ \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura FILEPATHS.**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) Il **membro Target** è il nome del file di destinazione nel sistema. Il **membro Source** è il percorso previsto del file di origine. Il **membro Win32Error** è l'errore di firma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Se la routine di callback restituisce NO \_ ERROR, l'analisi della coda continua. Se la routine restituisce qualsiasi altro codice di errore, l'analisi della coda viene interrotta [**e SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce FALSE.

> [!Note]  
> Questa notifica non viene gestita dalla [**funzione SetupDefaultQueueCallback.**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

