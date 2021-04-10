---
title: Messaggio CB_INITSTORAGE (winuser. h)
description: Un'applicazione invia il \_ messaggio INITSTORAGE CB prima di aggiungere un numero elevato di elementi alla casella di riepilogo di una casella combinata. Questo messaggio alloca memoria per archiviare gli elementi della casella di riepilogo.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Controlli di Windows Message CB_INITSTORAGE
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
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119734"
---
# <a name="cb_initstorage-message"></a>\_Messaggio INITSTORAGE CB

Un'applicazione invia il **messaggio \_ INITSTORAGE CB** prima di aggiungere un numero elevato di elementi alla casella di riepilogo di una casella combinata. Questo messaggio alloca memoria per archiviare gli elementi della casella di riepilogo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Numero di elementi da aggiungere.

</dd> <dt>

*lParam* 
</dt> <dd>

Quantità di memoria da allocare per le stringhe di elemento, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è il numero totale di elementi per cui la memoria è stata pre-allocata, ovvero il numero totale di elementi aggiunti da tutti i messaggi **CB \_ INITSTORAGE** correttamente.

Se il messaggio ha esito negativo, il valore restituito è CB \_ ERRSPACE.

Il messaggio alloca memoria e restituisce i valori di esito positivo e negativo descritti in precedenza.

## <a name="remarks"></a>Commenti

Il messaggio **CB \_ INITSTORAGE** consente di velocizzare l'inizializzazione di caselle combinate con un numero elevato di elementi (oltre 100). Si riserva la quantità di memoria specificata in modo che i messaggi [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)e [**CB \_**](cb-dir.md) successivi abbiano il minor tempo possibile. È possibile utilizzare le stime per i parametri *wParam* e *lParam* . Se si esegue la sovrastima, viene allocata la memoria aggiuntiva, se si sottovaluta, per gli elementi che superano la quantità richiesta viene utilizzata l'allocazione normale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**DIR della CB \_**](cb-dir.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> </dl>

 

 





