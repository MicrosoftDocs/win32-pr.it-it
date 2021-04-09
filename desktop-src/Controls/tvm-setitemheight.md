---
title: Messaggio TVM_SETITEMHEIGHT (COMmctrl. h)
description: Imposta l'altezza degli elementi della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetItemHeight di TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- Controlli di Windows Message TVM_SETITEMHEIGHT
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964382"
---
# <a name="tvm_setitemheight-message"></a>\_Messaggio SETITEMHEIGHT TVM

Imposta l'altezza degli elementi della visualizzazione struttura ad albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetItemHeight di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Nuova altezza di ogni elemento nella visualizzazione albero, in pixel. L'altezza minore di 1 verrà impostata su 1. Se questo argomento non è pari e il controllo di visualizzazione albero non ha lo stile [**\_ NONEVENHEIGHT TVS**](tree-view-control-window-styles.md) , questo valore verrà arrotondato per difetto al valore pari più vicino. Se questo argomento è-1, il controllo verrà ripristinato utilizzando l'altezza predefinita dell'elemento.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'altezza precedente, in pixel, degli elementi.

## <a name="remarks"></a>Commenti

Il controllo di visualizzazione albero utilizza questo valore per l'altezza di tutti gli elementi. Per modificare l'altezza dei singoli elementi, vedere la descrizione del membro **iIntegral** della struttura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETITEMHEIGHT TVM**](tvm-getitemheight.md)
</dt> </dl>

 

 





