---
title: TTM_ADDTOOL messaggio (Commctrl.h)
description: Registra uno strumento con un controllo descrizione comando.
ms.assetid: c974866b-20e7-45bc-914e-9dcf9af161e0
keywords:
- TTM_ADDTOOL di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TTM_ADDTOOL
- TTM_ADDTOOLA
- TTM_ADDTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb66c43033e54ce51b396ff5bb11efe3b2a99e8eb2578a2e9fe4d4bc4487ccf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769541"
---
# <a name="ttm_addtool-message"></a>TTM \_ ADDTOOL message

Registra uno strumento con un controllo descrizione comando.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) contenente le informazioni necessarie al controllo descrizione comando per visualizzare il testo per lo strumento. Il **membro cbSize** di questa struttura deve essere compilato prima di inviare questo messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ ADDTOOLW** (Unicode) e **TTM \_ ADDTOOLA** (ANSI)<br/>                   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**TTM \_ DELTOOL**](ttm-deltool.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui controlli descrizione comando](tooltip-controls.md)
</dt> </dl>

 

 





