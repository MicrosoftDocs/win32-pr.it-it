---
description: Quando si usa la direttiva RegisterDlls INF per registrare autonomamente le dll, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione.
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: Messaggio SPFILENOTIFY_ENDREGISTRATION (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8992d318d605110d74521efdb8a9c911aeeb9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318618"
---
# <a name="spfilenotify_endregistration-message"></a>\_Messaggio SPFILENOTIFY ENDREGISTRATION

Quando si usa la direttiva **RegisterDlls** inf per registrare autonomamente le dll, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione. Per inviare una **notifica \_ ENDREGISTRATION di SPFILENOTIFY** a una routine di callback una volta dopo la registrazione o l'annullamento della registrazione di un file, includere \_ il REGISTERCALLBACKAWARE più spinoso \_ regsvr nel parametro *Flags* di **SetupInstallFromInfSection**. Per inviare la notifica di annullamento della registrazione, includere \_ REGISTERCALLBACKAWARE più spin \_ UNREGSVR nel parametro *Flags* .

La routine di callback specificata dal parametro *MsgHandler* di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve corrispondere al [ \_ \_ callback dei file](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a)di tipo PSP. Impostare il parametro di *contesto* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**. Impostare il parametro *Notification* su **SPFILENOTIFY \_ ENDREGISTRATION**.


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura di [**\_ stato del \_ controllo \_ del registro SP**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente le informazioni sul file di cui è in corso la registrazione o l'annullamento della registrazione. Il membro **cbSize** deve essere impostato sulla dimensione della struttura. **Filename** deve essere impostato sul percorso completo del file registrato. **Win32Error** deve essere impostato su un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) che indica un codice di errore esteso. **FailureCode** deve essere impostato su uno dei codici di errore validi che indicano il risultato della registrazione. Per i codici di errore validi, vedere [**SP \_ Register \_ Control \_ status**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).

</dd> <dt>

*Param2* 
</dt> <dd>

Se il file viene registrato, *param2* deve essere impostato su un puntatore a un valore diverso da zero. Se è in corso l'annullamento della registrazione del file, *param2* deve essere impostato su un puntatore a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dopo la ricezione della notifica, la funzione di callback può restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_interruzione FILEOP**</dt> </dl> | Interrompere l'elaborazione della sezione INF.<br/>     |
| <dl> <dt>**\_doit FILEOP**</dt> </dl>  | Continuare l'elaborazione della sezione INF.<br/> |
| <dl> <dt>**\_Ignora file**</dt> </dl>    | Continua l'elaborazione della sezione INF<br/>  |



 

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

[**\_STARTREGISTRATION SPFILENOTIFY**](spfilenotify-startregistration.md)
</dt> </dl>

 

