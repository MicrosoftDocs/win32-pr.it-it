---
description: Inviato alla funzione CPlApplet di un'applicazione Pannello di controllo richiesta di eseguire l'inizializzazione globale, in particolare l'allocazione di memoria.
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: CPL_INIT messaggio (Cpl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456371"
---
# <a name="cpl_init-message"></a>Messaggio \_ INIT CPL

Inviato alla funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) di un'applicazione Pannello di controllo richiesta di eseguire l'inizializzazione globale, in particolare l'allocazione di memoria.


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'inizializzazione ha esito positivo, la [**funzione CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve restituire un valore diverso da zero. In caso contrario, deve restituire zero.

Se [**CPlApplet restituisce**](/windows/win32/api/cpl/nc-cpl-applet_proc) zero, l'applicazione di controllo termina la comunicazione e rilascia la DLL contenente l Pannello di controllo applicazione.

## <a name="remarks"></a>Commenti

Poiché questo è l'unico modo in cui un'Pannello di controllo può segnalare una condizione di errore, l'applicazione deve allocare memoria in risposta a questo messaggio.

Questo messaggio viene inviato immediatamente dopo il caricamento della DLL contenente l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                      |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Cpl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Freelibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
