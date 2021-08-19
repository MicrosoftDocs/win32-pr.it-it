---
title: CB_GETTOPINDEX messaggio (Winuser.h)
description: Un'applicazione invia il messaggio CB GETTOPINDEX per recuperare l'indice in base zero del primo elemento visibile nella parte casella di riepilogo \_ di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- CB_GETTOPINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2360b07c86d6d5bcbb8296d705e8ef65b3a81481a8fc647a362aedc729f38b42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089111"
---
# <a name="cb_gettopindex-message"></a>Messaggio \_ GETTOPINDEX CB

Un'applicazione invia il **messaggio \_ CB GETTOPINDEX** per recuperare l'indice in base zero del primo elemento visibile nella parte casella di riepilogo di una casella combinata. Inizialmente, l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se il contenuto della casella di riepilogo è stato scorrendo, un altro elemento potrebbe essere nella parte superiore.

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

Se il messaggio ha esito positivo, il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo della casella combinata.

Se il messaggio ha esito negativo, il valore restituito è CB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





