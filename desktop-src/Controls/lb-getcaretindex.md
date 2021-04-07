---
title: Messaggio LB_GETCARETINDEX (winuser. h)
description: Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Controlli di Windows Message LB_GETCARETINDEX
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048710"
---
# <a name="lb_getcaretindex-message"></a>\_Messaggio GETCARETINDEX lb

Recupera l'indice dell'elemento con lo stato attivo in una casella di riepilogo a selezione multipla. L'elemento può essere selezionato o meno.

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

Il valore restituito è l'indice in base zero dell'elemento della casella di riepilogo con stato attivo oppure 0 se nessun elemento ha lo stato attivo.

## <a name="remarks"></a>Commenti

Questo messaggio può essere usato anche per ottenere l'indice dell'elemento attualmente selezionato in una casella di riepilogo a selezione singola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETCARETINDEX lb**](lb-setcaretindex.md)
</dt> </dl>

 

 





