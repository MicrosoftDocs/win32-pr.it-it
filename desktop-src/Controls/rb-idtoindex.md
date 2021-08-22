---
title: RB_IDTOINDEX messaggio (Commctrl.h)
description: Converte un identificatore di banda in un indice di banda in un controllo rebar.
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b13d243498d821e64be19beebb04fab3f198442aced73ced6f424d32d7177ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642601"
---
# <a name="rb_idtoindex-message"></a>Messaggio RB \_ IDTOINDEX

Converte un identificatore di banda in un indice di banda in un controllo rebar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Identificatore definito dall'applicazione della banda in questione. Si tratta del valore passato nel **membro wID** della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) quando è stata inserita la banda.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice della banda in base zero in caso di esito positivo oppure -1 in caso contrario. Se sono presenti identificatori di banda duplicati, viene restituito il primo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





