---
title: Messaggio RB_SIZETORECT (COMmctrl. h)
description: Tenta di trovare il layout migliore delle bande per il rettangolo specificato.
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- Controlli di Windows Message RB_SIZETORECT
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121486"
---
# <a name="rb_sizetorect-message"></a>\_Messaggio SIZETORECT RB

Tenta di trovare il layout migliore delle bande per il rettangolo specificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) che specifica il rettangolo in cui deve essere ridimensionato il controllo Rebar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se si è verificata una modifica del layout oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Le bande Rebar verranno disposte e incapsulate in base alle esigenze per adattarsi al rettangolo. Le bande con lo \_ stile VARIABLEHEIGHT RBBS verranno ridimensionate nel modo più uniforme possibile per adattarsi al rettangolo. L'altezza di un Rebar orizzontale o la larghezza di un Rebar verticale può variare a seconda del nuovo layout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

