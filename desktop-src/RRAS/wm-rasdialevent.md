---
title: WM_RASDIALEVENT messaggio (Ras.h)
description: Il sistema operativo invia un messaggio WM RASDIALEVENT a una routine della finestra quando si verifica un evento di modifica dello stato \_ durante un processo di connessione RAS.
ms.assetid: 4526da20-04e7-47b2-b576-8dc36c08b053
keywords:
- WM_RASDIALEVENT messaggio RAS
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
ms.openlocfilehash: 093591ffe07ecbe662ca85306b74c34c670e1adbe51e2605b1f21faa20696c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024771"
---
# <a name="wm_rasdialevent-message"></a>Messaggio \_ DI WM RASDIALEVENT

Il sistema operativo invia un **messaggio WM \_ RASDIALEVENT** a una routine finestra quando si verifica un evento di modifica dello stato durante un processo di connessione RAS. Ciò si verifica quando è stata specificata una finestra per gestire le notifiche di tali eventi usando il *parametro notifier* di [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala).

I due parametri del messaggio sono equivalenti ai parametri con gli stessi nomi usati con le funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)


```C++
WM_RASDIALEVENT 
rasconnstate = (RASCONNSTATE) wParam; 
dwError = (DWORD) lParam;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rasconnstate* 
</dt> <dd>

Valore di *wParam*. Equivale al *parametro rasconnstate* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Specifica un [**valore dell'enumeratore RASCONNSTATE**](/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)) che indica lo stato che sta per essere immesso dal processo di connessione di accesso remoto RasDial.

</dd> <dt>

*dwError* 
</dt> <dd>

Valore di *lParam*. Equivale al *parametro dwError* delle funzioni di callback [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) e [**RasDialFunc1.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) Un valore diverso da zero indica l'errore che si è verificato oppure zero se non si è verificato alcun errore.

[**RasDial invia**](/windows/desktop/api/Ras/nf-ras-rasdiala) questo messaggio con *dwError* impostato su zero al momento dell'immissione a ogni stato di connessione. Se si verifica un errore all'interno di uno stato, il messaggio viene inviato nuovamente per lo stato, questa volta con un valore *dwError* diverso da zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se un'applicazione elabora questo messaggio, deve restituire **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Ras.h</dt> </dl> |



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

 

