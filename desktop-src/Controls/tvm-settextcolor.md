---
title: TVM_SETTEXTCOLOR messaggio (Commctrl.h)
description: Imposta il colore del testo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro TreeView SetTextColor.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41559abd6724ee9c8ce9f86cfcff092ad13d949a80a55d45ff996f36b284932d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503611"
---
# <a name="tvm_settextcolor-message"></a>Messaggio TVM \_ SETTEXTCOLOR

Imposta il colore del testo del controllo. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ TreeView SetTextColor.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

[**Valore COLORREF**](/windows/desktop/gdi/colorref) che contiene il nuovo colore del testo. Se questo argomento è -1, il controllo tornerà a usare il colore di sistema per il colore del testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore COLORREF** che rappresenta il colore del testo precedente. Se questo valore è -1, il controllo usava il colore di sistema per il colore del testo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

