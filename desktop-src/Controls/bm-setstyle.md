---
title: BM_SETSTYLE messaggio (Winuser.h)
description: Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro Button SetStyle.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- BM_SETSTYLE controlli Windows messaggio
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f635a70bf806c6c26f5b236ea939bc453d27bf0fe135f8e2586aeb59021b9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674419"
---
# <a name="bm_setstyle-message"></a>Messaggio \_ SETSTYLE BM

Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ Button SetStyle.**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stile del pulsante. Questo parametro può essere una combinazione di stili del pulsante. Per una tabella degli stili dei pulsanti, vedere [Stili dei pulsanti.](button-styles.md)

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD di**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) *lParam* è un **valore BOOL** che specifica se il pulsante deve essere ridisegnato. Il valore **TRUE** ridisegna il pulsante. Il valore **FALSE** non ridisegna il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



 

