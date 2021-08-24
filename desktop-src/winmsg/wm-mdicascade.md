---
description: Un'applicazione invia il messaggio WM MDICASCADE a una finestra client dell'interfaccia a documenti multipli per disporre tutte le finestre figlio in un \_ formato a cascata.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: WM_MDICASCADE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59977b86a63c62d69571a6e5c631dd9044fb57f072adf04b0882e16af4f65e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119448731"
---
# <a name="wm_mdicascade-message"></a>Messaggio DI WM \_ MDICASCADE

Un'applicazione invia il **\_ messaggio WM MDICASCADE** a una finestra client dell'interfaccia a documenti multipli per disporre tutte le finestre figlio in un formato a cascata.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Comportamento di propagazione. Questo parametro può essere uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_ SkipDISABLED**</dt> <dt>0x0002</dt> </dl> | Impedisce la propagazione a catena delle finestre figlio MDI disabilitate. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_ Ordine ZORDER**</dt> <dt>0x0004</dt> </dl>                   | Dispone le finestre in ordine Z.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **BOOL**

Se il messaggio ha esito positivo, il valore restituito è **TRUE.**

Se il messaggio ha esito negativo, il valore restituito è **FALSE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




