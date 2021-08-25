---
title: CB_INITSTORAGE messaggio (Winuser.h)
description: Un'applicazione invia il messaggio CB INITSTORAGE prima di aggiungere un numero elevato di elementi alla parte casella di riepilogo \_ di una casella combinata. Questo messaggio alloca memoria per l'archiviazione degli elementi della casella di riepilogo.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be1aeccdde2c81c87956a42e72440732ff9eb2732cbd066f51308816c01f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089091"
---
# <a name="cb_initstorage-message"></a>CB \_ INITSTORAGE message

Un'applicazione invia il **messaggio \_ CB INITSTORAGE** prima di aggiungere un numero elevato di elementi alla parte casella di riepilogo di una casella combinata. Questo messaggio alloca memoria per l'archiviazione degli elementi della casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da aggiungere.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantità di memoria da allocare per le stringhe elemento, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per i quali è stata preallocazione memoria, ovvero il numero totale di elementi aggiunti da tutti i messaggi **\_ CB INITSTORAGE** riusciti.

Se il messaggio ha esito negativo, il valore restituito è CB \_ ERRSPACE.

Il messaggio alloca memoria e restituisce i valori di esito positivo ed errore descritti in precedenza.

## <a name="remarks"></a>Commenti

Il **messaggio \_ CB INITSTORAGE** consente di velocizzare l'inizializzazione delle caselle combinate con un numero elevato di elementi (oltre 100). Riserva la quantità di memoria specificata in modo che i successivi messaggi [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)e [**CB \_ DIR**](cb-dir.md) prendano il tempo più breve possibile. È possibile usare stime per i *parametri wParam* *e lParam.* Se si sovrastima, la memoria aggiuntiva viene allocata. Se si sottovaluta, la normale allocazione viene usata per gli elementi che superano la quantità richiesta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





