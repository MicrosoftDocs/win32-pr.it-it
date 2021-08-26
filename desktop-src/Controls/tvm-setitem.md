---
title: TVM_SETITEM messaggio (Commctrl.h)
description: Il messaggio TVM SETITEM imposta alcuni o tutti gli attributi di un elemento \_ della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetItem.
ms.assetid: 28d288bf-a557-4fce-870c-ffa368ece5a9
keywords:
- TVM_SETITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SETITEM
- TVM_SETITEMA
- TVM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9521bc67766dbb503fc205e966d6ce72e674a4050b6c0d237c885dcb4a8f4b68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913941"
---
# <a name="tvm_setitem-message"></a>Messaggio \_ TVM SETITEM

Il **messaggio \_ TVM SETITEM** imposta alcuni o tutti gli attributi di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetItem.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene i nuovi attributi dell'elemento. Con [la versione 4.71 e](common-control-versions.md) successive, è invece possibile usare una struttura [**TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il **membro hItem** della [**struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento e il membro **mask** specifica gli attributi da impostare.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ SETITEMW** (Unicode) e **TVM \_ SETITEMA** (ANSI)<br/>                   |



 

 





