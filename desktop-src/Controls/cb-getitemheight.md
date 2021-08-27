---
title: CB_GETITEMHEIGHT messaggio (Winuser.h)
description: Determina l'altezza degli elementi dell'elenco o del campo di selezione in una casella combinata.
ms.assetid: 72fba6ca-0a51-4801-bd45-5f5a7d5ebee2
keywords:
- CB_GETITEMHEIGHT controlli Windows messaggio
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
ms.openlocfilehash: a6e3ad9636c32e40bfa95f1f3b2c209eab42023205e0a967cc91804ec314a103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089191"
---
# <a name="cb_getitemheight-message"></a>CB \_ GETITEMHEIGHT message

Determina l'altezza degli elementi dell'elenco o del campo di selezione in una casella combinata.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Componente casella combinata di cui recuperare l'altezza. Questo parametro deve essere -1 per recuperare l'altezza del campo di selezione. Deve essere zero per recuperare l'altezza degli elementi dell'elenco, a meno che la casella combinata non abbia lo stile [**CBS \_ OWNERDRAWVARIABLE.**](combo-box-styles.md) In tal caso, il *parametro wParam* è l'indice in base zero di un elemento dell'elenco specifico.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è l'altezza, in pixel, degli elementi dell'elenco in una casella combinata. Se la casella combinata ha lo stile [**CBS \_ OWNERDRAWVARIABLE,**](combo-box-styles.md) corrisponde all'altezza dell'elemento specificato dal *parametro wParam.* Se *wParam* è -1, il valore restituito è l'altezza della parte del controllo di modifica (o testo statico) della casella combinata. Se si verifica un errore, il valore restituito è CB \_ ERR.

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

[**CB \_ SETITEMHEIGHT**](cb-setitemheight.md)
</dt> <dt>

[**WM \_ MEASUREITEM**](wm-measureitem.md)
</dt> </dl>

 

 





