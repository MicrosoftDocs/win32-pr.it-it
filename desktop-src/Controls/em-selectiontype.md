---
title: EM_SELECTIONTYPE messaggio (Richedit.h)
description: Determina il tipo di selezione per un controllo Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b79cb36759c857cea280b1c4beb5a476fa27a794f1f9985e1d259c345a9dc4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437841"
---
# <a name="em_selectiontype-message"></a>Messaggio EM \_ SELECTIONTYPE

Determina il tipo di selezione per un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la selezione è vuota, il valore restituito è SEL \_ EMPTY.

Se la selezione non è vuota, il valore restituito è un set di flag contenente uno o più dei valori seguenti.



| Codice restituito                                                                                     | Descrizione                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**SEL \_ TEXT**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**OGGETTO \_ SEL**</dt> </dl>      | Almeno un oggetto COM.<br/>         |
| <dl> <dt>**SEL \_ MULTICHAR**</dt> </dl>   | Più di un carattere di testo.<br/> |
| <dl> <dt>**SEL \_ MULTIOBJECT**</dt> </dl> | Più oggetti COM.<br/>        |



 

## <a name="remarks"></a>Commenti

Questo messaggio è utile durante [**\_ l'elaborazione di WM SIZE**](/windows/desktop/winmsg/wm-size) per l'elemento padre di un controllo Rich Edit senza fine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

