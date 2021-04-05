---
title: Messaggio CB_GETITEMDATA (winuser. h)
description: Un'applicazione invia un \_ messaggio GETITEMDATA CB a una casella combinata per recuperare il valore fornito dall'applicazione associato all'elemento specificato nella casella combinata.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Controlli di Windows Message CB_GETITEMDATA
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741455"
---
# <a name="cb_getitemdata-message"></a>\_Messaggio GETITEMDATA CB

Un'applicazione invia un **messaggio \_ GETITEMDATA CB** a una casella combinata per recuperare il valore fornito dall'applicazione associato all'elemento specificato nella casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero di un elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è il valore associato all'elemento. Se si verifica un errore, è CB \_ Err.

Se l'elemento si trova in una casella combinata creata dal proprietario creata senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il valore restituito è il valore contenuto nel parametro *lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) , che ha aggiunto l'elemento alla casella combinata. Se non è stato usato lo stile **CBS \_ HASSTRINGS** , il valore restituito è il parametro *lParam* contenuto in un messaggio [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**CB \_ SETITEMDATA**](cb-setitemdata.md)
</dt> </dl>

 

 





