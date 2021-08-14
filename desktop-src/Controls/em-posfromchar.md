---
title: EM_POSFROMCHAR messaggio (Winuser.h)
description: Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1d9d2dccb6ccf1bd80b44b2221f8628f13e595ee514074956e7869447d513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437881"
---
# <a name="em_posfromchar-message"></a>Messaggio \_ EM POSFROMCHAR

Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica. È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 1.0 e 3.0:** Puntatore a una [**struttura POINTL**](/previous-versions//dd162807(v=vs.85)) che riceve le coordinate dell'area client del carattere. Le coordinate sono in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.

**Controlli di modifica e Rich Edit 2.0:** Indice in base zero del carattere.

</dd> <dt>

*lParam* 
</dt> <dd>

**Rich Edit 1.0 e 3.0:** Indice in base zero del carattere.

**Controlli di modifica e Rich Edit 2.0:** Questo parametro non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Rich Edit 1.0 e 3.0:** Il valore restituito non viene utilizzato.

**Controlli di modifica e Rich Edit 2.0:** Il valore restituito contiene le coordinate dell'area client del carattere. LOWORD [**contiene**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) la coordinata orizzontale e [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordinata verticale.

## <a name="remarks"></a>Commenti

Una coordinata restituita può essere un valore negativo se il carattere specificato non viene visualizzato nell'area client del controllo di modifica. Le coordinate vengono troncate a valori interi.

Se il carattere è un delimitatore di riga, le coordinate restituite indicano un punto oltre l'ultimo carattere visibile nella riga. Se l'indice specificato è maggiore dell'indice dell'ultimo carattere nel controllo, il controllo restituisce -1.

**Rich Edit 3.0 e versioni successive:** Per compatibilità con le versioni precedenti, Microsoft Rich Edit 3.0 supporta la sintassi usata da Microsoft Rich Edit 2.0. Se Microsoft Rich Edit 3.0 rileva che *wParam* non è un puntatore [**POINTL**](/previous-versions//dd162807(v=vs.85)) valido, presuppone che il messaggio sia stato inviato usando la sintassi di Microsoft Rich Edit 2.0. In questo caso, usa il valore restituito per restituire le coordinate.

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

[**EM \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

