---
title: TVM_GETISEARCHSTRING messaggio (Commctrl.h)
description: Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060241"
---
# <a name="tvm_getisearchstring-message"></a>Messaggio TVM \_ GETISEARCHSTRING

Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero. Il controllo visualizzazione albero usa la stringa di ricerca incrementale per selezionare un elemento in base ai caratteri digitati dall'utente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetISearchString di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al buffer che riceve la stringa di ricerca incrementale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il numero di caratteri nella stringa di ricerca incrementale.

## <a name="remarks"></a>Commenti

**Avviso di sicurezza:** L'uso errato di questo messaggio potrebbe compromettere la sicurezza del programma. È necessario allocare un buffer sufficientemente grande da contenere la stringa. Chiamare prima il messaggio passando **NULL** in *lParam*. Viene restituito il numero di caratteri, **escluso NULL,** necessari. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di [continuare, vedere Security Considerations: Microsoft Windows Controls](sec-comctls.md) (Considerazioni sulla sicurezza: Microsoft Windows Controls).

Se il controllo visualizzazione albero non è in modalità di ricerca incrementale, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





