---
title: EM_CHARFROMPOS messaggio (Winuser.h)
description: Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- EM_CHARFROMPOS di controllo Windows messaggio
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
ms.openlocfilehash: 3a133907b29857abdc1663d3283bc4b4164878f3fa0976769e6d42daef2c4cb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915961"
---
# <a name="em_charfrompos-message"></a>Messaggio \_ EM CHARFROMPOS

Ottiene informazioni sul carattere più vicino a un punto specificato nell'area client di un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*lParam* 
</dt> <dd>

Coordinate di un punto nell'area client del controllo. Le coordinate sono in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.

**Controlli Rich Edit:** Puntatore a una [**struttura POINTL**](/previous-versions//dd162807(v=vs.85)) che contiene le coordinate orizzontale e verticale.

**Controlli di modifica:** La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordinata orizzontale. HiWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) la coordinata verticale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Controlli Rich Edit:** Il valore restituito specifica l'indice dei caratteri in base zero del carattere più vicino al punto specificato. Il valore restituito indica l'ultimo carattere nel controllo di modifica se il punto specificato è oltre l'ultimo carattere nel controllo.

**Controlli di modifica:** La [**parola chiave LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero del carattere più vicino al punto specificato. Questo indice è relativo all'inizio del controllo, non all'inizio della riga. Se il punto specificato è oltre l'ultimo carattere nel controllo di modifica, il valore restituito indica l'ultimo carattere nel controllo. La [**parola chiave HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice in base zero della riga che contiene il carattere. Per i controlli di modifica a riga singola, questo valore è zero. L'indice indica il delimitatore di riga se il punto specificato è oltre l'ultimo carattere visibile in una riga.

## <a name="remarks"></a>Commenti

**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive. Per informazioni sulla compatibilità delle versioni rich edit con le diverse versioni del sistema, vedere [Informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

Se un punto viene passato a **EM \_ CHARFROMPOS** come *lParam* e il punto è esterno ai limiti del controllo di modifica, *lResult* è (65535, 65535).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ POSFROMCHAR**](em-posfromchar.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MAKELPARAM**](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

