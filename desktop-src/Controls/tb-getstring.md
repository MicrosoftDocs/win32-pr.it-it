---
title: Messaggio TB_GETSTRING (COMmctrl. h)
description: Recupera una stringa dal pool di stringhe di una barra degli strumenti.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Controlli di Windows Message TB_GETSTRING
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048121"
---
# <a name="tb_getstring-message"></a>TB- \_ messaggio GETstring

Recupera una stringa dal pool di stringhe di una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la lunghezza, in byte, del buffer *lParam* . [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice della stringa.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer utilizzato per restituire la stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce la lunghezza della stringa in caso di esito positivo; in caso contrario,-1.

## <a name="remarks"></a>Commenti

Questo messaggio restituisce la stringa specificata dal pool di stringhe della barra degli strumenti. Non corrisponde necessariamente alla stringa di testo attualmente visualizzata da un pulsante. Per recuperare la stringa di testo corrente di un pulsante, inviare la barra degli strumenti di un messaggio [**\_ GETBUTTONTEXT TB**](tb-getbuttontext.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TB \_ GETSTRINGW** (Unicode) e **TB \_ getstringa** (ANSI)<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TB \_ ADDSTRING**](tb-addstring.md)
</dt> <dt>

[**TB \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TB \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

