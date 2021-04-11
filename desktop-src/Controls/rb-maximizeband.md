---
title: Messaggio RB_MAXIMIZEBAND (COMmctrl. h)
description: Ridimensiona una banda in un controllo Rebar alla dimensione ideale o più grande.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- Controlli di Windows Message RB_MAXIMIZEBAND
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708a8fae7c0dd8e72eea8e5acefe43ab50054592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874153"
---
# <a name="rb_maximizeband-message"></a>\_Messaggio MAXIMIZEBAND RB

Ridimensiona una banda in un controllo Rebar alla dimensione ideale o più grande.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda da ingrandire.

</dd> <dt>

*lParam* 
</dt> <dd>

Indica se la larghezza ideale della banda deve essere utilizzata quando la banda è ingrandita. Se questo valore è diverso da zero, verrà utilizzata la larghezza ideale. Se questo valore è zero, la banda verrà resa il più possibile grande.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





