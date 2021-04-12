---
description: La \_ notifica SPFILENOTIFY NEEDNEWCABINET viene inviata da SetupIterateCabinet per indicare che il file corrente continua in un altro file CAB.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Messaggio SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233679"
---
# <a name="spfilenotify_neednewcabinet-message"></a>\_Messaggio SPFILENOTIFY NEEDNEWCABINET

La notifica **SPFILENOTIFY \_ NEEDNEWCABINET** viene inviata da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per indicare che il file corrente continua in un altro file CAB. La routine di callback può quindi chiamare [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)o creare la propria finestra di dialogo per richiedere all'utente di inserire il disco successivo.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura di [**\_ informazioni sul cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) che contiene informazioni sul file CAB e il file da estrarre.

</dd> <dt>

*Param2* 
</dt> <dd>

Se il callback non restituisce alcun \_ errore, questo parametro è un puntatore a una stringa con terminazione null. Se la stringa non è vuota, specifica un nuovo percorso per il file CAB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine deve restituire uno dei valori seguenti.



| Codice restituito                                                                                 | Descrizione                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Nessun \_ errore**</dt> </dl>    | Non è stato rilevato alcun errore, continuare l'elaborazione del file CAB.<br/>                                                                                                                                                                        |
| <dl> <dt>**Errore \_* XXX * * *</dt> </dl> | Si è verificato un errore del tipo specificato. La funzione [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) restituirà **false** e il codice di errore specificato verrà restituito da una chiamata a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).<br/> |



 

> [!Note]  
> Non esiste alcuna routine di callback predefinita del cabinet. Pertanto, è necessario fornire una routine di callback per gestire le notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="remarks"></a>Commenti

Se la routine di callback non restituisce alcun \_ errore, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) controlla il buffer a cui punta *param2*. Se il buffer non è vuoto, contiene un nuovo percorso di origine. Se il buffer è vuoto, si presuppone che il percorso di origine sia invariato.

La funzione di callback deve garantire che il file CAB sia accessibile prima che venga restituito, chiamando la funzione [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , se è necessario inserire nuovi supporti.

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

[**informazioni sul CABINET \_**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

