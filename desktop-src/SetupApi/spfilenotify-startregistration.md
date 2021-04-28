---
description: "SPFILENOTIFY_STARTREGISTRATION messaggio: quando si usa la direttiva REGISTERDlls INF per registrare automaticamente le DLL, i chiamanti di SetupInstallFromInfSection possono ricevere notifiche su ogni file durante la registrazione o l'annullamento della registrazione."
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094499"
---
# <a name="spfilenotify_startregistration-message"></a>Messaggio SPFILENOTIFY \_ STARTREGISTRATION

Quando si usa la direttiva **REGISTERDlls** INF per registrare automaticamente le DLL, i chiamanti di [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) possono ricevere notifiche in ogni file durante la registrazione o l'annullamento della registrazione. Per inviare una notifica **SPFILENOTIFY \_ STARTREGISTRATION** alla routine di callback una volta prima di registrare un file, includere SPINST \_ REGISTERCALLBACKAWARE e SPINST REGSVR nel parametro Flags di \_  **SetupInstallFromInfSection**. Per inviare una notifica di annullamento della registrazione, includere SPINST \_ REGISTERCALLBACKAWARE e SPINST \_ UNREGSVR nel *parametro Flags.*

La routine di callback specificata dal *parametro MsgHandler* [**di SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) deve essere di tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a). Impostare il *parametro Context* sullo stesso *contesto* specificato in **SetupInstallFromInfSection**. Impostare il *parametro Notification* su **SPFILENOTIFY \_ STARTREGISTRATION**.


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una [**struttura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) contenente informazioni sul file da registrare o annullare la registrazione. Il membro **cbsize** deve essere impostato sulla dimensione della struttura . Il **membro FileName** deve essere impostato sul percorso completo del file registrato. **Win32Error** non viene usato e deve essere impostato su NO \_ ERROR. **FailureCode** non viene usato e deve essere impostato su SPREG \_ SUCCESS.

</dd> <dt>

*Param2* 
</dt> <dd>

Se il file viene registrato, *Param2* deve essere impostato su un puntatore a un valore diverso da zero. Se viene annullata la registrazione del file, *Param2* deve essere impostato su un puntatore a zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Dopo aver ricevuto la notifica, la funzione di callback può restituire uno dei valori seguenti.



| Codice restituito                                                                                  | Descrizione                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**INTERRUZIONE \_ FILEOP**</dt> </dl> | Non registrare o annullare la registrazione del file e arrestare l'elaborazione della sezione INF.<br/>             |
| <dl> <dt>**FILEOP \_ DOIT**</dt> </dl>  | Registrare o annullare la registrazione del file e continuare l'elaborazione della sezione INF.<br/>                |
| <dl> <dt>**FILE \_ SKIP**</dt> </dl>    | Ignorare la registrazione o annullare la registrazione del file, ma continuare l'elaborazione della sezione INF<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                           |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[**SPFILENOTIFY \_ ENDREGISTRATION**](spfilenotify-endregistration.md)
</dt> </dl>

 

