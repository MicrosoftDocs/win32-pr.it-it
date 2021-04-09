---
title: Messaggio TVM_GETISEARCHSTRING (COMmctrl. h)
description: Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Controlli di Windows Message TVM_GETISEARCHSTRING
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
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121290"
---
# <a name="tvm_getisearchstring-message"></a>\_Messaggio GETISEARCHSTRING TVM

Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero. Il controllo di visualizzazione albero utilizza la stringa di ricerca incrementale per selezionare un elemento in base ai caratteri digitati dall'utente. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetISearchString di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .

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

**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma. È necessario allocare un buffer sufficientemente grande per conservare la stringa. Chiamare prima il messaggio passando **null** in *lParam*. Viene restituito il numero di caratteri, esclusi i **valori null**, che sono obbligatori. Chiamare quindi il messaggio una seconda volta per recuperare la stringa. Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .

Se il controllo di visualizzazione albero non è in modalità di ricerca incrementale, il valore restituito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





