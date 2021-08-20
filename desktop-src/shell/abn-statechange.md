---
description: Notifica a una barra delle app che lo stato di visualizzazione automatica o sempre in alto della barra delle applicazioni è stato modificato&8212; in altri caso, l'utente ha selezionato o \# cancellato il &\# 0034; Always on top&\# 0034; or &\# 0034; Nascondi automaticamente&casella di controllo \# 0034; nella finestra delle proprietà della barra delle applicazioni.
title: ABN_STATECHANGE messaggio (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b0017930bd3cf4c8cba356206cfa2207df04ea9c203018703a5f3064d0abb11b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861583"
---
# <a name="abn_statechange-message"></a>Messaggio ABN \_ STATECHANGE

Notifica a una barra delle app che lo stato di visualizzazione automatica o sempre in alto della barra delle applicazioni è stato modificato, ad esempio l'utente ha selezionato o deselezionato la casella di controllo "Sempre in alto" o "Nascondi automaticamente" nella finestra delle proprietà della barra delle applicazioni.


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a>Parametri

Questo messaggio non ha parametri.

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Una barra delle app può usare questo messaggio di notifica per impostarne lo stato in modo che sia conforme a quello della barra delle applicazioni, se necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




