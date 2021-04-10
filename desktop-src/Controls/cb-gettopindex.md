---
title: Messaggio CB_GETTOPINDEX (winuser. h)
description: Un'applicazione invia il \_ messaggio CB GETTOPINDEX per recuperare l'indice in base zero del primo elemento visibile nella parte della casella di riepilogo di una casella combinata.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Controlli di Windows Message CB_GETTOPINDEX
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
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964204"
---
# <a name="cb_gettopindex-message"></a>\_Messaggio GETTOPINDEX CB

Un'applicazione invia il messaggio **CB \_ GETTOPINDEX** per recuperare l'indice in base zero del primo elemento visibile nella parte della casella di riepilogo di una casella combinata. Inizialmente, l'elemento con indice 0 si trova nella parte superiore della casella di riepilogo, ma se il contenuto della casella di riepilogo è stato spostato, un altro elemento potrebbe trovarsi nella parte superiore.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è l'indice del primo elemento visibile nella casella di riepilogo della casella combinata.

Se il messaggio ha esito negativo, il valore restituito è CB \_ Err.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ SETTOPINDEX**](cb-settopindex.md)
</dt> </dl>

 

 





