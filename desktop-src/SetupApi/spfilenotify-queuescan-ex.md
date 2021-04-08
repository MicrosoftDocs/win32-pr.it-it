---
description: La \_ notifica SPFILENOTIFY QUEUESCAN \_ ex viene inviata a una routine di callback da SetupScanFileQueue per ogni nodo nella coda secondaria di copia della coda di file.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Messaggio SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e18cf1cdb1cd007dcf46793d2d018dedd80037
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880834"
---
# <a name="spfilenotify_queuescan_ex-message"></a>\_Messaggio SPFILENOTIFY QUEUESCAN \_ ex

La notifica **SPFILENOTIFY \_ QUEUESCAN \_ ex** viene inviata a una routine di callback da [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) per ogni nodo nella coda secondaria di copia della coda di file. Questo errore si verifica solo se è stata chiamata la funzione **SetupScanFileQueue** specificando il flag SPQ \_ Scan \_ use \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Il membro di **destinazione** è il nome del file di destinazione nel sistema. Il membro di **origine** è il percorso previsto del file di origine. Il membro **Win32Error** è l'errore di firma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes).

Se la routine di callback non restituisce alcun \_ errore, l'analisi della coda continua. Se la routine restituisce un altro codice di errore, l'analisi della coda viene interrotta e [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) restituisce false.

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

 

