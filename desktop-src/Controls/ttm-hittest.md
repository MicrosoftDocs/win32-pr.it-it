---
title: Messaggio TTM_HITTEST (COMmctrl. h)
description: Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera le informazioni sullo strumento.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Controlli di Windows Message TTM_HITTEST
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
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476781"
---
# <a name="ttm_hittest-message"></a>\_Messaggio TTM HITTEST

Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera le informazioni sullo strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) . Quando si invia il messaggio, il membro **HWND** deve specificare l'handle per uno strumento e il membro **PT** deve specificare le coordinate di un punto. Se il valore restituito è **true**, il membro **ti** (una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) riceve informazioni sullo strumento che occupa il punto. Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura **ti** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se lo strumento occupa il punto specificato o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio deve essere inviato quando per lo strumento è \_ impostato il flag di traccia ttf. Per ulteriori informazioni su questo flag, vedere [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa). Il TTM \_ HITTEST avrà esito negativo se \_ non è impostata la traccia ttf, indipendentemente dal fatto che il punto di hit si trovi nel rettangolo Tools.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ HITTESTW** (Unicode) e **TTM \_ HITTESTA** (ANSI)<br/>                   |



 

 





