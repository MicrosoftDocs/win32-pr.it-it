---
title: CB_GETEXTENDEDUI messaggio (Winuser.h)
description: Determina se una casella combinata ha l'interfaccia utente predefinita o l'interfaccia utente estesa.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- CB_GETEXTENDEDUI di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05201b0986b114e97523716edacc6fe391908d3ed2841d36bf7578a6455f42a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089221"
---
# <a name="cb_getextendedui-message"></a>CB \_ GETEXTENDEDUI message

Determina se una casella combinata ha l'interfaccia utente predefinita o l'interfaccia utente estesa.

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

Se la casella combinata ha l'interfaccia utente estesa, il valore restituito è **TRUE**. in caso contrario, è **FALSE.**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il tasto F4 apre o chiude l'elenco e la freccia GIÙ modifica la selezione corrente. In una casella combinata con l'interfaccia utente estesa, il tasto F4 è disabilitato e premendo freccia GIÙ viene aperto l'elenco a discesa.

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

[**CB \_ SETEXTENDEDUI**](cb-setextendedui.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Funzionalità della casella combinata](combo-box-features.md)
</dt> </dl>

 

 





