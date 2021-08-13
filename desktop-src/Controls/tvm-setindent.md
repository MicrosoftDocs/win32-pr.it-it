---
title: TVM_SETINDENT messaggio (Commctrl.h)
description: Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegna il controllo in modo da riflettere la nuova larghezza. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetIndent.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- TVM_SETINDENT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SETINDENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538a89439909afe346ae8776d31a2104c7f6014664a33bdd3864bf43b0387e80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669666"
---
# <a name="tvm_setindent-message"></a>TvM \_ SETINDENT message

Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegna il controllo in modo da riflettere la nuova larghezza. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetIndent.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Larghezza, in pixel, del rientro. Se questo parametro è minore della larghezza minima definita dal sistema, la nuova larghezza viene impostata sul valore minimo definito dal sistema.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il valore del rientro minimo definito dal sistema è in genere di cinque pixel, ma non è fisso. Per recuperare il valore esatto del rientro minimo in un particolare sistema, inviare un messaggio **\_ SETINDENT TVM** con *wParam* impostato su zero. Inviare quindi un [**messaggio \_ TVM GETINDENT**](tvm-getindent.md) per recuperare il valore minimo del rientro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TreeView \_ SetIndent**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





