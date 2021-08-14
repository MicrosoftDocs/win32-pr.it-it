---
title: TVM_GETITEM messaggio (Commctrl.h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro GetItem di \_ TreeView.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- TVM_GETITEM di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_GETITEM
- TVM_GETITEMA
- TVM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425b0200df62b1cfcbc18556ad12513e43cebadf6e5742b36880464fad195fb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984891"
---
# <a name="tvm_getitem-message"></a>Messaggio TVM \_ GETITEM

Recupera alcuni o tutti gli attributi di un elemento della visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ GetItem di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che specifica le informazioni da recuperare e riceve informazioni sull'elemento. Con [la versione 4.71](common-control-versions.md) e successive è invece possibile usare una [**struttura TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Quando il messaggio viene inviato, il membro **hItem** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento su cui recuperare le informazioni e il membro **mask** specifica gli attributi da recuperare.

Se il flag TVIF TEXT è impostato nel membro mask della struttura \_ [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX,**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri in tale buffer. 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) e **TVM \_ GETITEMA** (ANSI)<br/>                   |



 

 





