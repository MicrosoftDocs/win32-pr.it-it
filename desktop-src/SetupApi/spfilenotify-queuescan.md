---
description: La notifica SPFILENOTIFY QUEUESCAN viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia \_ della coda di file. Questo errore si verifica solo se è stata chiamata la funzione SetupScanFileQueue specificando il flag SPQ \_ SCAN \_ USE \_ CALLBACK.
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: SPFILENOTIFY_QUEUESCAN messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab9c680ff2aaa3056ab74db741a34bb9f0379ec7123821b1de4c20200997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664851"
---
# <a name="spfilenotify_queuescan-message"></a>SPFILENOTIFY \_ QUEUESCAN message

La **notifica SPFILENOTIFY \_ QUEUESCAN** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ SCAN USE \_ \_ CALLBACK.


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Stringa con terminazione Null che specifica le informazioni sul percorso di destinazione per il file accodato nel nodo corrente.

</dd> <dt>

*Param2* 
</dt> <dd>

Se il file nel nodo corrente della coda è in uso, *Param2* accetta il valore SPQ \_ DELAYED \_ COPY. Se il file non è in uso, il valore è zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Se la routine di callback restituisce NO \_ ERROR, l'analisi della coda continua. Se la routine restituisce qualsiasi altro codice di errore, l'analisi della coda viene interrotta [**e SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce **FALSE.**

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

 

