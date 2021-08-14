---
title: RB_GETBANDBORDERS messaggio (Commctrl.h)
description: Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile in una banda.
ms.assetid: 45f2ae7e-636e-474b-a0d0-5235c6401e6a
keywords:
- RB_GETBANDBORDERS dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- RB_GETBANDBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6b07303c10ef6f466907b11cf0e100927f63480690e77ac3dcbe80df80af97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409713"
---
# <a name="rb_getbandborders-message"></a>Messaggio RB \_ GETBANDBORDERS

Recupera i bordi di una banda. Il risultato di questo messaggio può essere utilizzato per calcolare l'area utilizzabile in una banda.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda per la quale verranno recuperati i bordi.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) che riceverà i bordi della banda. Se il controllo Rebar ha lo stile [**RBS \_ BANDBORDERS,**](rebar-control-styles.md) ogni membro di questa struttura riceverà il numero di pixel, sul lato corrispondente della banda, che costituiscono il bordo. Se il controllo Rebar non ha lo **stile RBS \_ BANDBORDERS,** solo il membro **sinistro** di questa struttura riceve informazioni valide.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

