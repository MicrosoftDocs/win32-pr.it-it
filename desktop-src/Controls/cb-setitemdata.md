---
title: Messaggio CB_SETITEMDATA (winuser. h)
description: Un'applicazione invia un \_ messaggio SETITEMDATA CB per impostare il valore associato all'elemento specificato in una casella combinata.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Controlli di Windows Message CB_SETITEMDATA
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874129"
---
# <a name="cb_setitemdata-message"></a>\_Messaggio SETITEMDATA CB

Un'applicazione invia un **messaggio \_ SETITEMDATA CB** per impostare il valore associato all'elemento specificato in una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica l'indice in base zero dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica il nuovo valore da associare all'elemento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se si verifica un errore, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

Se l'elemento specificato si trova in una casella combinata creata dal proprietario creata senza lo stile [**\_ HASSTRINGS CBS**](combo-box-styles.md) , questo messaggio sostituisce il valore nel parametro *lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) che ha aggiunto l'elemento alla casella combinata.

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

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





