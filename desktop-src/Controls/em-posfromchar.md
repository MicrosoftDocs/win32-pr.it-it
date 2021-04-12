---
title: Messaggio EM_POSFROMCHAR (winuser. h)
description: Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Controlli di Windows Message EM_POSFROMCHAR
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
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517980"
---
# <a name="em_posfromchar-message"></a>\_Messaggio POSFROMCHAR em

Recupera le coordinate dell'area client di un carattere specificato in un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 1,0 e 3,0:** Puntatore a una struttura [**POINTL**](/previous-versions//dd162807(v=vs.85)) che riceve le coordinate dell'area client del carattere. Le coordinate sono espresse in unità dello schermo e sono relative all'angolo superiore sinistro dell'area client del controllo.

**Modificare i controlli e rich edit 2,0:** Indice in base zero del carattere.

</dd> <dt>

*lParam* 
</dt> <dd>

**Rich Edit 1,0 e 3,0:** Indice in base zero del carattere.

**Modificare i controlli e rich edit 2,0:** Questo parametro non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**Rich Edit 1,0 e 3,0:** Il valore restituito non viene utilizzato.

**Modificare i controlli e rich edit 2,0:** Il valore restituito contiene le coordinate dell'area client del carattere. [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene la coordinata orizzontale e il [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contiene la coordinata verticale.

## <a name="remarks"></a>Commenti

Una coordinata restituita può essere un valore negativo se il carattere specificato non viene visualizzato nell'area client del controllo di modifica. Le coordinate vengono troncate in base ai valori integer.

Se il carattere è un delimitatore di riga, le coordinate restituite indicano un punto appena oltre l'ultimo carattere visibile nella riga. Se l'indice specificato è maggiore dell'indice dell'ultimo carattere del controllo, il controllo restituisce-1.

**Rich Edit 3,0 e versioni successive:** Per compatibilità con le versioni precedenti, Microsoft Rich Edit 3,0 supporta la sintassi utilizzata da Microsoft Rich Edit 2,0. Se Microsoft Rich Edit 3,0 rileva che *wParam* non è un puntatore [**punto**](/previous-versions//dd162807(v=vs.85)) valido, presuppone che il messaggio sia stato inviato utilizzando la sintassi Microsoft Rich Edit 2,0. In questo caso, usa il valore restituito per restituire le coordinate.

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

[**\_CHARFROMPOS em**](em-charfrompos.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

