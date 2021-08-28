---
title: LB_SETITEMDATA messaggio (Winuser.h)
description: Imposta un valore associato all'elemento specificato in una casella di riepilogo.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- LB_SETITEMDATA controlli Windows messaggio
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
ms.openlocfilehash: dd9a705014ef770edba5b540a7acbd2512b685d5ebf8ca913df8fa329dc6058a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085331"
---
# <a name="lb_setitemdata-message"></a>Messaggio \_ LB SETITEMDATA

Imposta un valore associato all'elemento specificato in una casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento. Se questo valore è -1, il *valore lParam* si applica a tutti gli elementi nella casella di riepilogo.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il *parametro wParam* è limitato a valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Anche se il numero di elementi è limitato, la dimensione totale in byte degli elementi in una casella di riepilogo è limitata solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica il valore da associare all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è LB \_ ERR.

## <a name="remarks"></a>Commenti

Se l'elemento si trova in una casella di riepilogo creata dal proprietario senza lo stile [**\_ HASSTRINGS di LBS,**](list-box-styles.md) questo messaggio sostituisce il valore contenuto nel *parametro lParam* del messaggio [**\_ LB ADDSTRING**](lb-addstring.md) o [**LB \_ INSERTSTRING**](lb-insertstring.md) che ha aggiunto l'elemento alla casella di riepilogo.

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

[**LB \_ ADDSTRING**](lb-addstring.md)
</dt> <dt>

[**LB \_ GETITEMDATA**](lb-getitemdata.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> </dl>

 

 





