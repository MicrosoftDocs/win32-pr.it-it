---
title: Messaggio EM_CHARFROMPOS (winuser. h)
description: Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Controlli di Windows Message EM_CHARFROMPOS
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477608"
---
# <a name="em_charfrompos-message"></a>\_Messaggio CHARFROMPOS em

Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordinate di un punto nell'area client del controllo. Le coordinate sono espresse in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.

**Controlli Rich Edit:** Puntatore a una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) che contiene le coordinate orizzontali e verticali.

**Controlli di modifica:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordinata orizzontale. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordinata verticale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Controlli Rich Edit:** Il valore restituito specifica l'indice dei caratteri in base zero del carattere più vicino al punto specificato. Il valore restituito indica l'ultimo carattere del controllo di modifica se il punto specificato è oltre l'ultimo carattere nel controllo.

**Controlli di modifica:** [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del carattere più vicino al punto specificato. Questo indice è relativo all'inizio del controllo, non all'inizio della riga. Se il punto specificato è oltre l'ultimo carattere del controllo di modifica, il valore restituito indica l'ultimo carattere del controllo. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice in base zero della riga che contiene il carattere. Per i controlli di modifica a riga singola, questo valore è zero. L'indice indica il delimitatore di riga se il punto specificato è oltre l'ultimo carattere visibile in una riga.

## <a name="remarks"></a>Commenti

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

Se un punto viene passato al **\_ CHARFROMPOS em** come *lParam* e il punto si trova all'esterno dei limiti del controllo di modifica, *LRESULT* è (65535, 65535).

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

[**\_POSFROMCHAR em**](em-posfromchar.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

