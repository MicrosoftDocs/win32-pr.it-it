---
description: Quando si usa la direttiva RegisterDlls INF per registrare autonomamente le dll, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Messaggio SPFILENOTIFY_STARTREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316074"
---
# <a name="spfilenotify_startregistration-message"></a>\_Messaggio SPFILENOTIFY STARTREGISTRATION

Quando si usa la direttiva **RegisterDlls** inf per registrare autonomamente le dll, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione. Per inviare una notifica **SPFILENOTIFY \_ STARTREGISTRATION** alla routine di callback una volta prima di registrare un file, includere \_ REGISTERCALLBACKAWARE più spin \_ regsvr nel parametro *Flags* di **SetupInstallFromInfSection**. Per inviare la notifica di annullamento della registrazione, includere \_ REGISTERCALLBACKAWARE più spin \_ UNREGSVR nel parametro *Flags* .

La routine di callback specificata dal parametro *MsgHandler* di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve corrispondere al [ \_ \_ callback dei file](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)di tipo PSP. Impostare il parametro di *contesto* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**. Impostare il parametro *Notification* su **SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura di [**\_ stato del \_ controllo \_ del registro SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente le informazioni sul file di cui è in corso la registrazione o l'annullamento della registrazione. Il membro **cbSize** deve essere impostato sulla dimensione della struttura. Il membro **filename** deve essere impostato sul percorso completo del file registrato. **Win32Error** non viene utilizzato e deve essere impostato su nessun \_ errore. **FailureCode** non viene usato e deve essere impostato su SPREG \_ Success.

</dd> <dt>

*Param2* 
</dt> <dd>

Se il file viene registrato, *param2* deve essere impostato su un puntatore a un valore diverso da zero. Se è in corso l'annullamento della registrazione del file, *param2* deve essere impostato su un puntatore a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dopo la ricezione della notifica, la funzione di callback può restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl> | Non registrare o annullare la registrazione del file e arrestare l'elaborazione della sezione INF.<br/>             |
| <dl> <dt>**\_doit FILEOP**</dt> </dl>  | Registrare o annullare la registrazione del file e continuare l'elaborazione della sezione INF.<br/>                |
| <dl> <dt>**\_Ignora file**</dt> </dl>    | Ignora la registrazione o l'annullamento della registrazione del file ma continua l'elaborazione della sezione INF<br/> |



 

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

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**\_ENDREGISTRATION SPFILENOTIFY**](spfilenotify-endregistration.md)
</dt> </dl>

 

