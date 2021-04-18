---
title: Messaggio CB_SETITEMHEIGHT (winuser. h)
description: Un'applicazione invia un \_ messaggio CB SETITEMHEIGHT per impostare l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.
ms.assetid: 25a01170-5ffc-4d86-b696-706f5375570b
keywords:
- Controlli di Windows Message CB_SETITEMHEIGHT
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
ms.openlocfilehash: 8e46be007cdea17857e5d8ec42a12228821539d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302371"
---
# <a name="cb_setitemheight-message"></a>\_Messaggio SETITEMHEIGHT CB

Un'applicazione invia un messaggio **CB \_ SETITEMHEIGHT** per impostare l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica il componente della casella combinata per la quale impostare l'altezza.

Questo parametro deve essere 1 per impostare l'altezza del campo di selezione. Deve essere zero per impostare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) . In tal caso, il parametro *wParam* è l'indice in base zero di un elemento di elenco specifico.

</dd> <dt>

*lParam* 
</dt> <dd>

Specifica l'altezza, in pixel, del componente della casella combinata identificato da *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'indice o l'altezza non è valido, il valore restituito è CB \_ Err.

## <a name="remarks"></a>Commenti

L'altezza del campo di selezione in una casella combinata viene impostata indipendentemente dall'altezza degli elementi dell'elenco. Un'applicazione deve garantire che l'altezza del campo di selezione non sia minore dell'altezza di un particolare elemento di elenco.

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

[**CB \_ GETITEMHEIGHT**](cb-getitemheight.md)
</dt> <dt>

[**\_MeasureItem WM**](wm-measureitem.md)
</dt> </dl>

 

 





