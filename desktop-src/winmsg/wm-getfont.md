---
description: Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.
ms.assetid: a6d05ef5-9933-4d03-a677-a8328bf1cb7d
title: Messaggio WM_GETFONT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5254b701630f09cc7980470a9f5be68ad377bc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314864"
---
# <a name="wm_getfont-message"></a>\_Messaggio WM GETfont

Recupera il tipo di carattere con cui il controllo sta attualmente disegnando il testo.


```C++
#define WM_GETFONT                      0x0031
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene utilizzato e deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **Hfont**

Il valore restituito è un handle per il tipo di carattere utilizzato dal controllo o **null** se il controllo utilizza il tipo di carattere di sistema.

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

[**\_tipo di carattere WM**](wm-setfont.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 




