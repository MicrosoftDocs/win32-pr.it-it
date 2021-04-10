---
title: Messaggio TVM_SETINDENT (COMmctrl. h)
description: Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegnato il controllo in modo da riflettere la nuova larghezza. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro di Sedentazione TreeView.
ms.assetid: 377da8fe-c8e6-479b-a283-f1811cbc3e58
keywords:
- Controlli di Windows Message TVM_SETINDENT
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
ms.openlocfilehash: f85263c7c4330a692dc08949870a0eaa92f2b22c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120103"
---
# <a name="tvm_setindent-message"></a>\_Messaggio di rientro TVM

Imposta la larghezza del rientro per un controllo di visualizzazione albero e ridisegnato il controllo in modo da riflettere la nuova larghezza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro di [**\_ sedentazione TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Larghezza, in pixel, del rientro. Se questo parametro è inferiore alla larghezza minima definita dal sistema, la nuova larghezza viene impostata sul valore minimo definito dal sistema.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il valore di rientro minimo definito dal sistema è in genere di cinque pixel, ma non è corretto. Per recuperare il valore esatto del rientro minimo in un particolare sistema, inviare un messaggio di **\_ sedentazione TVM** con *wParam* impostato su zero. Inviare quindi un messaggio [**TVM \_ GetIndent**](tvm-getindent.md) per recuperare il valore di rientro minimo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Sedentazione TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setindent)
</dt> </dl>

 

 





