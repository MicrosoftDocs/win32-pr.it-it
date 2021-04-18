---
title: Messaggio TB_SETBUTTONSIZE (COMmctrl. h)
description: Imposta la dimensione dei pulsanti in una barra degli strumenti.
ms.assetid: ef6beed7-a3d6-4379-b9c1-c64a5e33ce78
keywords:
- Controlli di Windows Message TB_SETBUTTONSIZE
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
ms.openlocfilehash: 5db17b943c8a7cc8e71735d08718ece02a8c2582
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301669"
---
# <a name="tb_setbuttonsize-message"></a>TB \_ SETBUTTONSIZE messaggio

Imposta la dimensione dei pulsanti in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza, in pixel, dei pulsanti. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'altezza, in pixel, dei pulsanti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

**TB \_ SETBUTTONSIZE** deve essere in genere chiamato dopo l'aggiunta di pulsanti.

Usare [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) per impostare le larghezze massime e minime consentite per i pulsanti prima di aggiungerli. Usare **TB \_ SETBUTTONSIZE** per impostare le dimensioni effettive dei pulsanti.

## <a name="examples"></a>Esempio

Il codice di esempio seguente imposta la larghezza dei pulsanti su 80 pixel e l'altezza su 30 pixel.


```C++
// hWndToolbar is a handle to the toolbar window.
SendMessage(hWndToolbar, TB_SETBUTTONSIZE, 0, MAKELPARAM(80, 30);
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

