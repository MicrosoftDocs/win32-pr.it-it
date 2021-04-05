---
title: Messaggio CB_GETITEMHEIGHT (winuser. h)
description: Determina l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- Controlli di Windows Message CB_GETITEMHEIGHT
topic_type:
- apiref
api_name:
- CB_GETITEMHEIGHT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4aac9d8f9a430c056f8b91a9306d77c182f4c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873801"
---
# <a name="cb_getitemheight-message"></a>\_Messaggio GETITEMHEIGHT CB

Determina l'altezza degli elementi dell'elenco o il campo di selezione in una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Componente della casella combinata di cui è necessario recuperare l'altezza. Questo parametro deve essere-1 per recuperare l'altezza del campo di selezione. Deve essere zero per recuperare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) . In tal caso, il parametro *wParam* è l'indice in base zero di un elemento di elenco specifico.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'altezza, in pixel, degli elementi dell'elenco in una casella combinata. Se la casella combinata ha lo stile [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) , è l'altezza dell'elemento specificato dal parametro *wParam* . Se *wParam* è-1, il valore restituito è l'altezza della parte del controllo di modifica (o del testo statico) della casella combinata. Se si verifica un errore, il valore restituito è CB \_ Err.

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

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**\_MeasureItem WM**](wm-measureitem.md)
</dt> </dl>

 

 





