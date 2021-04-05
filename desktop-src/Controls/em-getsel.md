---
title: Messaggio EM_GETSEL (winuser. h)
description: Ottiene le posizioni dei caratteri iniziali e finali (in TCHARs) della selezione corrente in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Controlli di Windows Message EM_GETSEL
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
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048304"
---
# <a name="em_getsel-message"></a>\_Messaggio GETSEL em

Ottiene le posizioni dei caratteri iniziali e finali (in **TCHAR** s) della selezione corrente in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a un valore **DWORD** che riceve la posizione iniziale della selezione. Questo parametro può essere **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un valore **DWORD** che riceve la posizione del primo carattere non selezionato dopo la fine della selezione. Questo parametro può essere **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un valore in base zero con la posizione iniziale della selezione in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e la posizione del primo **TCHAR** dopo l'ultimo **TCHAR** selezionato in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Se uno di questi valori supera 65.535, il valore restituito è-1.

È preferibile usare i valori restituiti in *wParam* e *lParam* perché sono valori a 32 bit completi.

## <a name="remarks"></a>Commenti

Se non è presente alcuna selezione, i valori iniziale e finale sono entrambi la posizione del punto di inserimento.

**Controlli Rich Edit:** È anche possibile usare il [**messaggio \_ EXGETSEL em**](em-exgetsel.md) per recuperare le stesse informazioni. **Em \_ EXGETSEL** restituisce anche le posizioni dei caratteri iniziale e finale come valori a 32 bit.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_EXGETSEL em**](em-exgetsel.md)
</dt> <dt>

[**\_SETSEL em**](em-setsel.md)
</dt> </dl>

 

