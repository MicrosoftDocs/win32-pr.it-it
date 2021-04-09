---
title: Messaggio CB_DELETESTRING (winuser. h)
description: Elimina una stringa nella casella di riepilogo di una casella combinata.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Controlli di Windows Message CB_DELETESTRING
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121319"
---
# <a name="cb_deletestring-message"></a>\_Messaggio DELETESTRING CB

Elimina una stringa nella casella di riepilogo di una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da eliminare.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un conteggio delle stringhe rimaste nell'elenco. Se il parametro *wParam* specifica un indice maggiore del numero di elementi nell'elenco, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo [**stile \_ HASSTRINGS CBS**](combo-box-styles.md) , il sistema invia un [**messaggio \_ WM DeleteItem**](wm-deleteitem.md) al proprietario della casella combinata in modo che l'applicazione possa liberare i dati aggiuntivi associati all'elemento.

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

[**CB \_ ResetContent**](cb-resetcontent.md)
</dt> <dt>

[**\_DeleteItem WM**](wm-deleteitem.md)
</dt> </dl>

 

 





