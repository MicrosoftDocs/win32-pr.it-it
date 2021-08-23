---
title: TVM_SETEXTENDEDSTYLE messaggio (Commctrl.h)
description: Indica al controllo di visualizzazione albero di impostare stili estesi. Inviare questo messaggio o usare la macro TreeView \_ SetExtendedStyle.
ms.assetid: 35cb6ac8-1c1e-4ecd-88b2-878d3f6ccaa5
keywords:
- TVM_SETEXTENDEDSTYLE di controllo Windows messaggio
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
ms.openlocfilehash: d13d99a2f7a27475c30867f007f45d7525118d3077ebdce235c6bd33e1f8aafe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750961"
---
# <a name="tvm_setextendedstyle-message"></a>Messaggio TVM \_ SETEXTENDEDSTYLE

Indica al controllo di visualizzazione albero di impostare stili estesi. Inviare questo messaggio o usare la macro [**TreeView \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setextendedstyle).

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Maschera usata per selezionare gli stili da impostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Valore che indica lo stile esteso. Per altre informazioni sugli stili, vedere [Stili estesi del controllo Visualizzazione struttura ad albero.](tree-view-control-window-extended-styles.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Gli stili estesi per un controllo di visualizzazione albero non hanno nulla a che fare con gli stili estesi usati con la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) o [**la funzione SetWindowLong.**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

