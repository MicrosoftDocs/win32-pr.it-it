---
description: Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: WM_GETFONT messaggio (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d3dbd4a34557459fa0f31f6e2a96eba9d0cab36d54cf2bddaa353343a18b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200472"
---
# <a name="wm_getfont-message"></a>Messaggio WM \_ GETFONT

Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HFONT**

Il valore restituito è un handle per il tipo di carattere utilizzato dal controllo oppure **NULL** se il controllo usa il tipo di carattere di sistema.

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

[**WM \_ SETFONT**](wm-setfont.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




