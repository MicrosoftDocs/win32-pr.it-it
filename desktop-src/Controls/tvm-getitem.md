---
title: Messaggio TVM_GETITEM (COMmctrl. h)
description: Recupera alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView GetItem.
ms.assetid: e26ec000-967d-46de-8f71-6ebc36fefe5e
keywords:
- Controlli di Windows Message TVM_GETITEM
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
ms.openlocfilehash: dff96f4721a3c50eda54792b2b1c003cd808bf11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121699"
---
# <a name="tvm_getitem-message"></a>\_Messaggio TVM GETitem

Recupera alcuni o tutti gli attributi di un elemento della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getitem) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che specifica le informazioni per recuperare e ricevere informazioni sull'elemento. Con la [versione 4,71](common-control-versions.md) e successive, è invece possibile usare una struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Quando il messaggio viene inviato, il membro **hitet** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) identifica l'elemento per il quale recuperare le informazioni e il membro **mask** specifica gli attributi da recuperare.

Se il \_ flag di testo TVIF è impostato nel membro **mask** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) o [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) , il membro **pszText** deve puntare a un buffer valido e il membro **cchTextMax** deve essere impostato sul numero di caratteri nel buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TVM \_ GETITEMW** (Unicode) e **TVM \_ getitema** (ANSI)<br/>                   |



 

 





