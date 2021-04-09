---
title: Messaggio LB_DELETESTRING (winuser. h)
description: Elimina una stringa in una casella di riepilogo.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Controlli di Windows Message LB_DELETESTRING
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874265"
---
# <a name="lb_deletestring-message"></a>\_Messaggio DELETESTRING lb

Elimina una stringa in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della stringa da eliminare.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è un conteggio delle stringhe rimaste nell'elenco. Il valore restituito è LB \_ Err se il parametro *wParam* specifica un indice maggiore del numero di elementi nell'elenco.

## <a name="remarks"></a>Commenti

Se un'applicazione crea la casella di riepilogo con uno stile disegnato dal proprietario ma senza lo stile [**\_ HASSTRINGS di lbs**](list-box-styles.md) , il sistema invia un messaggio [**WM \_ DeleteItem**](wm-deleteitem.md) al proprietario della casella di riepilogo in modo che l'applicazione possa liberare i dati aggiuntivi associati all'elemento.

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

[**\_ADDSTRING lb**](lb-addstring.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> <dt>

[**\_DeleteItem WM**](wm-deleteitem.md)
</dt> </dl>

 

 





