---
description: Un'applicazione invia il \_ messaggio WM MDITILE a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un formato di riquadro.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Messaggio WM_MDITILE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226038"
---
# <a name="wm_mditile-message"></a>\_Messaggio MDITILE WM

Un'applicazione invia il messaggio **WM \_ MDITILE** a una finestra del client di interfaccia a documenti multipli (MDI) per disporre tutte le finestre figlio MDI in un formato di riquadro.


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Opzione di affiancamento. Questo parametro può essere uno dei valori seguenti, combinati facoltativamente con **MDITILE \_ SKIPDISABLED** per impedire che vengano affiancate le finestre figlio MDI disabilitate.



| Valore                                                                                                                                                                                                                                    | Significato                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0001</dt> orizzontale </dl> | Affianca le finestre orizzontalmente.<br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <dt>**MDITILE \_**</dt> <dt>0x0000</dt> verticali </dl>       | Affianca le finestre verticalmente.<br/>   |



 

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

[**\_MDICASCADE WM**](wm-mdicascade.md)
</dt> <dt>

[**\_MDIICONARRANGE WM**](wm-mdiiconarrange.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Interfaccia a documenti multipli](multiple-document-interface.md)
</dt> </dl>

 

 




