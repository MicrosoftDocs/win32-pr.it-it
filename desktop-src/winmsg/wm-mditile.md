---
description: Un'applicazione invia il messaggio MDITILE WM a una finestra client dell'interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un \_ formato di riquadro.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: WM_MDITILE messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379394d413c0c9d15b9f63297934b97da6aff65b4ae5d803627cb0107493c4e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436218"
---
# <a name="wm_mditile-message"></a>Messaggio \_ WM MDITILE

Un'applicazione invia il messaggio **\_ MDITILE WM** a una finestra client dell'interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un formato di riquadro.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Opzione di affiancamento. Questo parametro può essere uno dei valori seguenti, facoltativamente combinati con **MDITILE \_ SKIPDISABLED** per impedire che le finestre figlio MDI disabilitate vengano affiancate.



| Valore                                                                                                                                                                                                                                    | Significato                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_ HORIZONTAL**</dt> <dt>0x0001</dt> </dl> | Affianca le finestre orizzontalmente.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_ Vertical**</dt> <dt>0x0000</dt> </dl>       | Affianca verticalmente le finestre.<br/>   |



 

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

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDIICONARRANGE**](wm-mdiiconarrange.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




