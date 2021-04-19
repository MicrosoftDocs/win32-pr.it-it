---
description: La \_ notifica SPFILENOTIFY QUEUESCAN viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione SetupScanFileQueue specificando il flag SPQ \_ Scan \_ use \_ callback.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Messaggio SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66202a398f7e3f4e1121782f9469d2d6f299452c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316077"
---
# <a name="spfilenotify_queuescan-message"></a>\_Messaggio SPFILENOTIFY QUEUESCAN

La notifica **SPFILENOTIFY \_ QUEUESCAN** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ callback.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Stringa con terminazione null che specifica le informazioni sul percorso di destinazione per il file in coda nel nodo corrente.

</dd> <dt>

*Param2* 
</dt> <dd>

Se il file nel nodo corrente della coda è in uso, *param2* acquisisce il valore SPQ \_ Retarded \_ Copy. Se il file non è in uso, il valore è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua. Se la routine restituisce un altro codice di errore, l'analisi della coda viene interrotta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce **false**.

> [!Note]  
> Questa notifica non viene gestita dalla funzione [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

