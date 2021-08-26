---
title: EM_GETSEL messaggio (Winuser.h)
description: Ottiene le posizioni dei caratteri iniziale e finale (in TCHAR) della selezione corrente in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- EM_GETSEL dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dca5f3cf1fdaa3c40dd1bb25ebbabb672474e76ae621a05cf52247c216adca17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048801"
---
# <a name="em_getsel-message"></a>Messaggio \_ GETSEL EM

Ottiene le posizioni dei caratteri iniziale e finale (in **TCHAR** s) della selezione corrente in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a un **valore DWORD** che riceve la posizione iniziale della selezione. Questo parametro può essere **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a **un valore DWORD** che riceve la posizione del primo carattere non selezionato dopo la fine della selezione. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore in base zero con la posizione iniziale della selezione in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la posizione del primo **TCHAR** dopo l'ultimo **TCHAR** selezionato in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se uno di questi valori supera 65.535, il valore restituito è -1.

È meglio usare i valori restituiti in *wParam* e *lParam* perché sono valori completi a 32 bit.

## <a name="remarks"></a>Commenti

Se non è presente alcuna selezione, i valori iniziale e finale sono entrambi la posizione del cursore.

**Controlli Rich Edit:** È anche possibile usare [**il messaggio EM \_ EXGETSEL**](em-exgetsel.md) per recuperare le stesse informazioni. **EM \_ EXGETSEL restituisce** anche le posizioni dei caratteri iniziale e finale come valori a 32 bit.

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ EXGETSEL**](em-exgetsel.md)
</dt> <dt>

[**EM \_ SETSEL**](em-setsel.md)
</dt> </dl>

 

