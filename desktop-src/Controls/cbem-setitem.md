---
title: CBEM_SETITEM messaggio (Commctrl.h)
description: Imposta gli attributi per un elemento in un controllo ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- CBEM_SETITEM dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b1010c090283a47404ee93ef5f3bc1cf2d5ffe71a646d6d734cb443152bdd64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527931"
---
# <a name="cbem_setitem-message"></a>Messaggio \_ CBEM SETITEM

Imposta gli attributi per un elemento in un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che contiene le informazioni sull'elemento da impostare. Quando il messaggio viene inviato, il membro **mask** della struttura deve essere impostato per indicare quali attributi sono validi e il membro **iItem** deve specificare l'indice in base zero dell'elemento da modificare. **L'impostazione del membro iItem** su -1 modificherà l'elemento visualizzato nel controllo di modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero in caso di esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **CBEM \_ SETITEMW** (Unicode) e **CBEM \_ SETITEMA** (ANSI)<br/>                 |



 

 





