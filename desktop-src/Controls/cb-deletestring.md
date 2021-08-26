---
title: CB_DELETESTRING messaggio (Winuser.h)
description: Elimina una stringa nella casella di riepilogo di una casella combinata.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING del messaggio Windows controlli
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
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063581"
---
# <a name="cb_deletestring-message"></a>CB \_ DELETESTRING message

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

Il valore restituito è un conteggio delle stringhe rimanenti nell'elenco. Se il *parametro wParam* specifica un indice maggiore del numero di elementi nell'elenco, il valore restituito è CB \_ ERR.

## <a name="remarks"></a>Commenti

Se si crea la casella combinata con uno stile creato dal proprietario ma senza lo stile [**\_ HASSTRINGS di CBS,**](combo-box-styles.md) il sistema invia un messaggio [**WM \_ DELETEITEM**](wm-deleteitem.md) al proprietario della casella combinata in modo che l'applicazione possa liberare eventuali dati aggiuntivi associati all'elemento.

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

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





