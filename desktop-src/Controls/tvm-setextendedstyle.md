---
title: Messaggio TVM_SETEXTENDEDSTYLE (COMmctrl. h)
description: Informa il controllo di visualizzazione albero per impostare gli stili estesi. Inviare questo messaggio o usare la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- Controlli di Windows Message TVM_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TVM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c450f72f85e40514c35f08284428feec4f7caf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517956"
---
# <a name="tvm_setextendedstyle-message"></a>\_Messaggio SETEXTENDEDSTYLE TVM

Informa il controllo di visualizzazione albero per impostare gli stili estesi. Inviare questo messaggio o usare la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Maschera utilizzata per selezionare gli stili da impostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che indica lo stile esteso. Per altre informazioni sugli stili, vedere [stili estesi del controllo di visualizzazione albero](tree-view-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di visualizzazione albero non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

