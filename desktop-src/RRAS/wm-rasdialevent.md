---
title: Messaggio di WM_RASDIALEVENT (RAS. h)
description: Il sistema operativo invia un \_ messaggio WM RASDIALEVENT a una routine della finestra quando si verifica una modifica dell'evento di stato durante un processo di connessione RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- RAS del messaggio WM_RASDIALEVENT
topic_type:
- apiref
api_name:
- WM_RASDIALEVENT
api_location:
- Ras.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470fe3915c9f672c4663971159386e529ea60db4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301002"
---
# <a name="wm_rasdialevent-message"></a>\_Messaggio RASDIALEVENT WM

Il sistema operativo invia un messaggio **WM \_ RASDIALEVENT** a una routine della finestra quando si verifica una modifica dell'evento di stato durante un processo di connessione RAS. Questo errore si verifica quando viene specificata una finestra per gestire le notifiche di tali eventi utilizzando il parametro *Notifier* di [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

I due parametri del messaggio sono equivalenti ai parametri degli stessi nomi utilizzati con le funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) .


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valore di *wParam*. Equivale al parametro *rasconnstate* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Specifica un valore di enumeratore [**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) che indica lo stato in cui il processo di connessione di accesso remoto RasDial sta per essere inserito.

</dd> <dt>

*dwError* 
</dt> <dd>

Valore di *lParam*. Equivale al parametro *dwError* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) . Un valore diverso da zero indica l'errore che si è verificato o zero se non si è verificato alcun errore.

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) Invia questo messaggio con *dwError* impostato su zero alla voce per ogni stato della connessione. Se si verifica un errore all'interno di uno stato, il messaggio viene inviato di nuovo per lo stato, questa volta con un valore *dwError* diverso da zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora il messaggio, deve restituire **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>RAS. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Messaggi del servizio di accesso remoto](remote-access-service-messages.md)
</dt> <dt>

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)
</dt> <dt>

[**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)
</dt> <dt>

[**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)
</dt> <dt>

[**RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85))
</dt> </dl>

 

