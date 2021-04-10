---
title: Messaggio TVM_GETINSERTMARKCOLOR (COMmctrl. h)
description: Recupera il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetInsertMarkColor di TreeView.
ms.assetid: d1fba4bb-1bdb-44e0-8083-b564cdafc055
keywords:
- Controlli di Windows Message TVM_GETINSERTMARKCOLOR
topic_type:
- apiref
api_name:
- TVM_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61416a428fed88ece8f50ca640dd9a05ec131614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964847"
---
# <a name="tvm_getinsertmarkcolor-message"></a>\_Messaggio GETINSERTMARKCOLOR TVM

Recupera il colore utilizzato per creare il segno di inserimento per la visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetInsertMarkColor di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getinsertmarkcolor) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore [**COLORREF**](/windows/desktop/gdi/colorref) che contiene il colore del segno di inserimento corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETINSERTMARKCOLOR TVM**](tvm-setinsertmarkcolor.md)
</dt> </dl>

 

