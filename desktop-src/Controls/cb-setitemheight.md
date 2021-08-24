---
title: CB_SETITEMHEIGHT messaggio (Winuser.h)
description: Un'applicazione invia un messaggio CB SETITEMHEIGHT per impostare l'altezza degli elementi dell'elenco o del campo \_ di selezione in una casella combinata.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- CB_SETITEMHEIGHT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_SETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b97e83d13e66d0a8252fdc1974c775188f8009958a3f286916b0e46ea4f0e88c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699441"
---
# <a name="cb_setitemheight-message"></a>CB \_ SETITEMHEIGHT message

Un'applicazione invia un **messaggio \_ CB SETITEMHEIGHT** per impostare l'altezza degli elementi dell'elenco o del campo di selezione in una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il componente della casella combinata per cui impostare l'altezza.

Questo parametro deve essere 1 per impostare l'altezza del campo di selezione. Deve essere zero per impostare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OWNERDRAWVARIABLE.**](combo-box-styles.md) In tal caso, il *parametro wParam* è l'indice in base zero di un elemento dell'elenco specifico.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'altezza, in pixel, del componente casella combinata identificato da *wParam.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'indice o l'altezza non è valida, il valore restituito è CB \_ ERR.

## <a name="remarks"></a>Commenti

L'altezza del campo di selezione in una casella combinata viene impostata indipendentemente dall'altezza degli elementi dell'elenco. Un'applicazione deve garantire che l'altezza del campo di selezione non sia inferiore all'altezza di un particolare elemento dell'elenco.

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

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





