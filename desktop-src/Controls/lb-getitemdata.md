---
title: Messaggio LB_GETITEMDATA (winuser. h)
description: Ottiene il valore definito dall'applicazione associato all'elemento della casella di riepilogo specificato.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Controlli di Windows Message LB_GETITEMDATA
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121311"
---
# <a name="lb_getitemdata-message"></a>\_Messaggio GETITEMDATA lb

Ottiene il valore definito dall'applicazione associato all'elemento della casella di riepilogo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit. Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi. Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il valore associato all'elemento, oppure LB \_ Err se si verifica un errore. Se l'elemento si trova in una casella di riepilogo creata dal proprietario ed è stato creato senza lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , questo valore era nel parametro *lParam* del messaggio [**lb \_ ADDSTRING**](lb-addstring.md) o [**lb \_ INSERTSTRING**](lb-insertstring.md) che ha aggiunto l'elemento alla casella di riepilogo. In caso contrario, è il valore nel valore *lParam* del [**messaggio \_ SETITEMDATA lb**](lb-setitemdata.md) .

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

[**\_SETITEMDATA lb**](lb-setitemdata.md)
</dt> </dl>

 

 





