---
title: Messaggio BM_SETSTYLE (winuser. h)
description: Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro di tipo Button.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Controlli di Windows Message BM_SETSTYLE
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
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963943"
---
# <a name="bm_setstyle-message"></a>\_Messaggio SESTYLE BM

Imposta lo stile di un pulsante. È possibile inviare questo messaggio in modo esplicito o usare la macro di [**\_ tipo Button**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Stile del pulsante. Questo parametro può essere una combinazione di stili dei pulsanti. Per una tabella di stili di pulsante, vedere [stili dei pulsanti](button-styles.md).

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) di *lParam* è un valore **bool** che specifica se il pulsante deve essere ridisegnato. Il valore **true** riestrae il pulsante; il valore **false** non consente di ricreare il pulsante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce sempre zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

