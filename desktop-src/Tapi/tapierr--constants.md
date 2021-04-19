---
description: Le \_ costanti TAPIERR forniscono informazioni sugli errori di esecuzione della funzione.
ms.assetid: 6d1cf18b-efeb-4703-9b8e-fce59b61b63f
title: Costanti TAPIERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e8a60e2a625ff456a4a8aa2730b80000e92ff54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326237"
---
# <a name="tapierr_-constants"></a>\_Costanti TAPIERR

Le **\_ costanti TAPIERR** forniscono informazioni sugli errori di esecuzione della funzione.

<dl> <dt>

<span id="TAPIERR_CONNECTED"></span><span id="tapierr_connected"></span>**TAPIERR \_ connesso**
</dt> <dd> <dl> <dt>



Non è possibile eseguire l'operazione mentre lo stato della chiamata è connected.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTBUSY"></span><span id="tapierr_destbusy"></span>**\_DESTBUSY TAPIERR**
</dt> <dd> <dl> <dt>



La destinazione della chiamata è occupata.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTNOANSWER"></span><span id="tapierr_destnoanswer"></span>**\_DESTNOANSWER TAPIERR**
</dt> <dd> <dl> <dt>



La destinazione della chiamata non ha risposto.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DESTUNAVAIL"></span><span id="tapierr_destunavail"></span>**\_DESTUNAVAIL TAPIERR**
</dt> <dd> <dl> <dt>



La destinazione della chiamata non è disponibile.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICECLASSUNAVAIL"></span><span id="tapierr_deviceclassunavail"></span>**\_DEVICECLASSUNAVAIL TAPIERR**
</dt> <dd> <dl> <dt>



La classe del dispositivo necessaria non è disponibile.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEIDUNAVAIL"></span><span id="tapierr_deviceidunavail"></span>**\_DEVICEIDUNAVAIL TAPIERR**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo necessario non è disponibile.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DEVICEINUSE"></span><span id="tapierr_deviceinuse"></span>**\_DEVICEINUSE TAPIERR**
</dt> <dd> <dl> <dt>



Il dispositivo necessario è in uso.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_DROPPED"></span><span id="tapierr_dropped"></span>**TAPIERR \_ eliminato**
</dt> <dd> <dl> <dt>



La chiamata è stata eliminata.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDESTADDRESS"></span><span id="tapierr_invaldestaddress"></span>**\_INVALDESTADDRESS TAPIERR**
</dt> <dd> <dl> <dt>



Il puntatore all'indirizzo di destinazione non è valido, è **null** o la stringa dell'indirizzo di destinazione è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICECLASS"></span><span id="tapierr_invaldeviceclass"></span>**\_INVALDEVICECLASS TAPIERR**
</dt> <dd> <dl> <dt>



La classe del dispositivo richiesta non è valida.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALDEVICEID"></span><span id="tapierr_invaldeviceid"></span>**\_INVALDEVICEID TAPIERR**
</dt> <dd> <dl> <dt>



L'identificatore di classe del dispositivo richiesto non è valido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALPOINTER"></span><span id="tapierr_invalpointer"></span>**\_INVALPOINTER TAPIERR**
</dt> <dd> <dl> <dt>



Il puntatore non fa riferimento a una posizione di memoria valida. Uno o più puntatori *lpszDestAddress*, *lpszAppName*, *lpszCalledParty* o *lpszComment* sono stati specificati ma non sono validi.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_INVALWINDOWHANDLE"></span><span id="tapierr_invalwindowhandle"></span>**\_INVALWINDOWHANDLE TAPIERR**
</dt> <dd> <dl> <dt>



Handle di finestra non valido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOREQUESTRECIPIENT"></span><span id="tapierr_norequestrecipient"></span>**\_NOREQUESTRECIPIENT TAPIERR**
</dt> <dd> <dl> <dt>



Nessuna applicazione destinatario disponibile per gestire la richiesta. L'utente deve avviare l'applicazione del destinatario e riprovare.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_NOTADMIN"></span><span id="tapierr_notadmin"></span>**\_NOTADMIN TAPIERR**
</dt> <dd> <dl> <dt>



L'operazione richiesta richiede privilegi amministrativi.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTCANCELLED"></span><span id="tapierr_requestcancelled"></span>**\_REQUESTCANCELLED TAPIERR**
</dt> <dd> <dl> <dt>



La richiesta di telefonia assistita è stata annullata.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTFAILED"></span><span id="tapierr_requestfailed"></span>**\_REQUESTFAILED TAPIERR**
</dt> <dd> <dl> <dt>



La richiesta non è riuscita per motivi non specificati.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_REQUESTQUEUEFULL"></span><span id="tapierr_requestqueuefull"></span>**\_REQUESTQUEUEFULL TAPIERR**
</dt> <dd> <dl> <dt>



Un'applicazione destinatario è attiva, ma la coda di richieste è piena o la memoria è insufficiente per espandere la coda. L'applicazione può riprovare più tardi.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNREQUESTID"></span><span id="tapierr_unknownrequestid"></span>**\_UNKNOWNREQUESTID TAPIERR**
</dt> <dd> <dl> <dt>



L'identificatore della richiesta a cui si fa riferimento non è valido.


</dt> </dl> </dd> <dt>

<span id="TAPIERR_UNKNOWNWINHANDLE"></span><span id="tapierr_unknownwinhandle"></span>**\_UNKNOWNWINHANDLE TAPIERR**
</dt> <dd> <dl> <dt>



È stato fatto riferimento a un handle di finestra sconosciuto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Qualsiasi altro \_ valore TAPIERR è obsoleto e non deve essere utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




