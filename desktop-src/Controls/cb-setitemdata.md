---
title: CB_SETITEMDATA messaggio (Winuser.h)
description: Un'applicazione invia un messaggio \_ CB SETITEMDATA per impostare il valore associato all'elemento specificato in una casella combinata.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- CB_SETITEMDATA dei controlli Windows messaggio
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
ms.openlocfilehash: 7abd50db9050178bc5d8d3b8ff556bce90f340fdb8d6692a514b0348aceeeab3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089011"
---
# <a name="cb_setitemdata-message"></a>CB \_ SETITEMDATA message

Un'applicazione invia un **messaggio \_ CB SETITEMDATA** per impostare il valore associato all'elemento specificato in una casella combinata.

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

Se si verifica un errore, il valore restituito è CB \_ ERR.

## <a name="remarks"></a>Commenti

Se l'elemento specificato si trova in una casella combinata creata dal proprietario senza lo stile [**\_ HASSTRINGS di CBS,**](combo-box-styles.md) questo messaggio sostituisce il valore nel *parametro lParam* del messaggio [**CB \_ ADDSTRING**](cb-addstring.md) o [**CB \_ INSERTSTRING**](cb-insertstring.md) che ha aggiunto l'elemento alla casella combinata.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ GETITEMDATA**](cb-getitemdata.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





