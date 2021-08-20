---
title: TB_SETBUTTONSIZE messaggio (Commctrl.h)
description: Imposta le dimensioni dei pulsanti su una barra degli strumenti.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- TB_SETBUTTONSIZE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b0b957ad6328515da7aee2f978870662801aa6aba81133e9e4bc22ee7d9c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167734"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ SETBUTTONSIZE message

Imposta le dimensioni dei pulsanti su una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza, in pixel, dei pulsanti. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'altezza, in pixel, dei pulsanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

**TB \_ È in genere consigliabile chiamare SETBUTTONSIZE** dopo l'aggiunta di pulsanti.

Usare [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) per impostare le larghezze massime e minime consentite per i pulsanti prima che siano aggiunti. Usare **TB \_ SETBUTTONSIZE** per impostare le dimensioni effettive dei pulsanti.

## <a name="examples"></a>Esempio

Il codice di esempio seguente imposta la larghezza dei pulsanti su 80 pixel e l'altezza su 30 pixel.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

