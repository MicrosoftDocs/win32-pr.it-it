---
description: Un'applicazione invia il \_ messaggio WM MDICASCADE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio in un formato Cascade.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: Messaggio WM_MDICASCADE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343201"
---
# <a name="wm_mdicascade-message"></a>\_Messaggio MDICASCADE WM

Un'applicazione invia il messaggio **WM \_ MDICASCADE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio in un formato Cascade.


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Comportamento di propagazione. Il parametro può essere costituito da uno o più dei valori seguenti.



| Valore                                                                                                                                                                                                                                          | Significato                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0002</dt> SKIPDISABLED </dl> | Impedisce la propagazione delle finestre figlio MDI disabilitate. <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0004</dt> ZOrder </dl>                   | Dispone le finestre in z order.<br/>                          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **bool**

Se il messaggio ha esito positivo, il valore restituito è **true**.

Se il messaggio ha esito negativo, il valore restituito è **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md)
</dt> <dt>

[**\_MDITILE WM**](wm-mditile.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




