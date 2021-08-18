---
title: CB_GETITEMDATA messaggio (Winuser.h)
description: Un'applicazione invia un messaggio GETITEMDATA CB a una casella combinata per recuperare il valore fornito dall'applicazione associato all'elemento \_ specificato nella casella combinata.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- CB_GETITEMDATA di Windows di messaggi
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
ms.openlocfilehash: 8427e666668303456d16c00ae460a608a51bc31cd59e0ee6fa6851031057695b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019929"
---
# <a name="cb_getitemdata-message"></a>Messaggio \_ CB GETITEMDATA

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

Il valore restituito è il valore associato all'elemento. Se si verifica un errore, si tratta di CB \_ ERR.

Se l'elemento si trova in una casella combinata creata dal proprietario senza lo stile [**\_ CBS HASSTRINGS,**](combo-box-styles.md) il valore restituito è il valore contenuto nel *parametro lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING,**](cb-insertstring.md) che ha aggiunto l'elemento alla casella combinata. Se lo **stile \_ CBS HASSTRINGS** non è stato usato, il valore restituito è il *parametro lParam* contenuto in un [**messaggio \_ SETITEMDATA CB.**](cb-setitemdata.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



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

 

 





