---
title: TTM_HITTEST messaggio (Commctrl.h)
description: Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera informazioni sullo strumento.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105edd555a1da1ba037f7dda114e1d9f9ef53048c02a7cb11e1df1ff0c01ad2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060521"
---
# <a name="ttm_hittest-message"></a>Messaggio \_ HITTEST TTM

Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera informazioni sullo strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TTHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) Quando si invia il messaggio, il **membro hwnd** deve specificare l'handle per uno strumento e il membro **pt** deve specificare le coordinate di un punto. Se il valore restituito **è TRUE,** il **membro ti** (una [**struttura TOOLINFO)**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) riceve informazioni sullo strumento che occupa il punto. Il **membro cbSize** della **struttura ti** deve essere compilato prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se lo strumento occupa il punto specificato oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Questo messaggio deve essere inviato quando lo strumento ha il flag TRACK TTF \_ impostato. Per altre informazioni su questo flag, vedere [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). TTM HITTEST avrà esito negativo se TTF TRACK non è impostato, indipendentemente dal fatto che il punto di hit si trova o meno \_ \_ nel rettangolo degli strumenti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) e **TTM \_ HITTESTA** (ANSI)<br/>                   |



 

 





