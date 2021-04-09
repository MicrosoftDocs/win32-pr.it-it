---
title: Messaggio LB_SETITEMDATA (winuser. h)
description: Imposta un valore associato all'elemento specificato in una casella di riepilogo.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Controlli di Windows Message LB_SETITEMDATA
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121006"
---
# <a name="lb_setitemdata-message"></a>\_Messaggio SETITEMDATA lb

Imposta un valore associato all'elemento specificato in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento. Se questo valore è-1, il valore *lParam* si applica a tutti gli elementi nella casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica il valore da associare all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ Err.

## <a name="remarks"></a>Commenti

Se l'elemento si trova in una casella di riepilogo creata dal proprietario creata senza lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo messaggio sostituisce il valore contenuto nel parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) che ha aggiunto l'elemento alla casella di riepilogo.

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

[**\_GETITEMDATA lb**](lb-getitemdata.md)
</dt> <dt>

[**\_INSERTSTRING lb**](lb-insertstring.md)
</dt> </dl>

 

 





