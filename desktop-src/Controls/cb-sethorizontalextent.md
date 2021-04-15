---
title: Messaggio CB_SETHORIZONTALEXTENT (winuser. h)
description: Un'applicazione invia il \_ messaggio SETHORIZONTALEXTENT CB per impostare la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole).
ms.assetid: 85e8ff4f-ad9a-451c-b791-bd442b32d716
keywords:
- Controlli di Windows Message CB_SETHORIZONTALEXTENT
topic_type:
- apiref
api_name:
- CB_SETHORIZONTALEXTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51e505f36f7cfd3fa47644a288db4a97ba89ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476630"
---
# <a name="cb_sethorizontalextent-message"></a>\_Messaggio SETHORIZONTALEXTENT CB

Un'applicazione invia il **messaggio \_ SETHORIZONTALEXTENT CB** per impostare la larghezza, in pixel, in base alla quale è possibile scorrere orizzontalmente una casella di riepilogo (larghezza scorrevole). Se la larghezza della casella di riepilogo è inferiore a questo valore, la barra di scorrimento orizzontale scorre orizzontalmente gli elementi nella casella di riepilogo. Se la larghezza della casella di riepilogo è maggiore o uguale a questo valore, la barra di scorrimento orizzontale è nascosta o, se la casella combinata ha lo stile [**CBS \_ DISABLENOSCROLL**](combo-box-styles.md) , disabilitato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specifica la larghezza scorrevole della casella di riepilogo, in pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro non viene usato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CB \_ GETHORIZONTALEXTENT**](cb-gethorizontalextent.md)
</dt> </dl>

 

 





