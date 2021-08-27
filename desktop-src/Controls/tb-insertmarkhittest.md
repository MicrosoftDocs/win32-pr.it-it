---
title: TB_INSERTMARKHITTEST messaggio (Commctrl.h)
description: Recupera le informazioni sul segno di inserimento per un punto in una barra degli strumenti.
ms.assetid: 65c64fd0-f089-4b1a-84e5-1a3e10aa7f5e
keywords:
- TB_INSERTMARKHITTEST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TB_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc231b915d6d71cc22ee3cd98b1c6dd602451cc3c70d2153ba1bee8a0d55657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061361"
---
# <a name="tb_insertmarkhittest-message"></a>TB \_ INSERTMARKHITTEST message

Recupera le informazioni sul segno di inserimento per un punto in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Puntatore a una [**struttura POINT**](/previous-versions//dd162805(v=vs.85)) che contiene le coordinate dell'hit test rispetto all'area client della barra degli strumenti.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) che riceve le informazioni sul segno di inserimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se il punto è un segno di inserimento oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

