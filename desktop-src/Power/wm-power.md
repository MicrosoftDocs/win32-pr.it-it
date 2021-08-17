---
description: Notifica alle applicazioni che il sistema, in genere un dispositivo alimentato a personal computer, sta per entrare in modalità sospesa.
ms.assetid: ceaa5ca4-799e-4801-96cd-aeea3dfd7d52
title: WM_POWER messaggio (WinUser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd525b4bf229fdb04dac4c1d1492a52dad44317344f58a2f0807ba9afbdc962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143184"
---
# <a name="wm_power-message"></a>Messaggio \_ DI WM POWER

Notifica alle applicazioni che il sistema, in genere un dispositivo alimentato a personal computer, sta per entrare in modalità sospesa.

> [!Note]  
> Il **messaggio WM \_ POWER** è obsoleto. Viene fornito solo per la compatibilità con applicazioni Windows a 16 bit. Le applicazioni devono usare [**il messaggio WM \_ POWERBROADCAST.**](wm-powerbroadcast.md)

 

Una finestra riceve questo messaggio tramite la **relativa funzione WindowProc.**


```C++
LRESULT CALLBACK WindowProc
  HWND   hwnd,    // handle to window
  UINT   uMsg,    // WM_POWER
  WPARAM wParam,  // power-event notification
  LPARAM lParam   // not used
); 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Identificatore **del messaggio WM \_ POWER.**

</dd> <dt>

*wParam* 
</dt> <dd>

Notifica dell'evento di alimentazione. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                        | Significato                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PWR_CRITICALRESUME"></span><span id="pwr_criticalresume"></span><dl> <dt>**PWR \_ CRITICALRESUME**</dt> </dl> | Indica che il sistema sta riprendendo l'operazione dopo l'accesso alla modalità sospesa senza prima trasmettere all'applicazione un messaggio di notifica **PWR \_ SUSPENDREQUEST.** Un'applicazione deve eseguire le azioni di ripristino necessarie.<br/>                                                   |
| <span id="PWR_SUSPENDREQUEST"></span><span id="pwr_suspendrequest"></span><dl> <dt>**PWR \_ SUSPENDREQUEST**</dt> </dl> | Indica che il sistema sta per entrare in modalità sospesa.<br/>                                                                                                                                                                                                                                 |
| <span id="PWR_SUSPENDRESUME"></span><span id="pwr_suspendresume"></span><dl> <dt>**PWR \_ SUSPENDRESUME**</dt> </dl>    | Indica che il sistema sta riprendendo l'operazione dopo essere passato normalmente alla modalità di sospensione, ad esempio il sistema ha trasmesso un messaggio di notifica **PWR \_ SUSPENDREQUEST** all'applicazione prima della sospensione del sistema. Un'applicazione deve eseguire le azioni di ripristino necessarie.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito da un'applicazione dipende dal valore del *parametro wParam.* Se *wParam* è **PWR \_ SUSPENDREQUEST**, il valore restituito è **PWR \_ FAIL** per impedire al sistema di entrare nello stato sospeso; in caso contrario, **è PWR \_ OK**. Se *wParam* è **PWR \_ SUSPENDRESUME** o **PWR \_ CRITICALRESUME**, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Questo messaggio viene trasmesso solo a un'applicazione in esecuzione in un sistema conforme alla specifica DEL BIOS (Basic Input/Output System) di Advanced Power Management (APM). Il messaggio viene trasmesso dal driver di risparmio energia a ogni finestra restituita dalla **funzione EnumWindows.**

La modalità sospesa è lo stato in cui si verifica la maggiore quantità di risparmio energia, ma tutti i dati operativi e i parametri vengono mantenuti. Il contenuto della memoria ad accesso casuale (RAM) viene mantenuto, ma è probabile che molti dispositivi siano spenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>WinUser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)
</dt> </dl>

 

 




