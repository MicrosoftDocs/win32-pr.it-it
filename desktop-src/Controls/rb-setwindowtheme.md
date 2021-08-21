---
title: RB_SETWINDOWTHEME messaggio (Commctrl.h)
description: Imposta lo stile di visualizzazione di un controllo rebar.
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2def8b1e4e1961ab549468260760d80182e466e44841fbbb767929a8033893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078550"
---
# <a name="rb_setwindowtheme-message"></a>Messaggio RB \_ SETWINDOWTHEME

Imposta lo stile di visualizzazione di un controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una stringa Unicode che contiene lo stile di visualizzazione rebar da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene usato.

## <a name="remarks"></a>Commenti

> [!Note]  
> Per usare questo messaggio, è necessario fornire un manifesto che specifica Comclt32.dll versione 6.0. Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





