---
title: EM_STOPGROUPTYPING messaggio (Richedit.h)
description: Impedisce a un controllo Rich Edit di raccogliere altre azioni di digitazione nell'azione di annullamento corrente. Il controllo archivia l'eventuale azione di digitazione successiva in una nuova azione nella coda di annullamento.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- EM_STOPGROUPTYPING dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e62a5d652218b24240ce612851c4c08e335b31230532bc778bb44c5d7e74854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672279"
---
# <a name="em_stopgrouptyping-message"></a>MESSAGGIO EM \_ STOPGROUPTYPING

Impedisce a un controllo Rich Edit di raccogliere altre azioni di digitazione nell'azione di annullamento corrente. Il controllo archivia l'eventuale azione di digitazione successiva in una nuova azione nella coda di annullamento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito è zero. Questo messaggio non può avere esito negativo.

## <a name="remarks"></a>Commenti

Un controllo Rich Edit raggruppa le azioni di digitazione consecutive, inclusi i caratteri eliminati usando il tasto **BackSpace,** in una singola azione di annullamento fino a quando non si verifica uno degli eventi seguenti:

-   Il controllo riceve un **messaggio EM \_ STOPGROUPTYPING.**
-   Il controllo perde lo stato attivo.
-   L'utente sposta la selezione corrente, usando i tasti di direzione o facendo clic con il mouse.
-   L'utente preme **il tasto** CANC.
-   L'utente esegue qualsiasi altra azione, ad esempio un'operazione Incolla che **non comporta la** digitazione.

È possibile inviare il **messaggio EM \_ STOPGROUPTYPING** per interrompere le azioni di digitazione consecutive in gruppi di annullamento più piccoli. Ad esempio, è possibile inviare **EM \_ STOPGROUPTYPING** dopo ogni carattere o a ogni interruzione di parola.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ UNDO**](em-undo.md)
</dt> </dl>

 

 





