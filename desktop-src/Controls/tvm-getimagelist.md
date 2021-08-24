---
title: TVM_GETIMAGELIST messaggio (Commctrl.h)
description: Recupera l'handle per l'elenco di immagini normali o di stato associato a un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro TreeView \_ GetImageList.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- TVM_GETIMAGELIST di controllo Windows messaggio
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b7536f21757d5ad03446654d9eed17444e4e07570c3f4bf032b7d32f0009208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119293281"
---
# <a name="tvm_getimagelist-message"></a>Messaggio TVM \_ GETIMAGELIST

Recupera l'handle per l'elenco di immagini normali o di stato associato a un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o usando la macro [**TreeView \_ GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**STATO \_ TVSIL**</dt> </dl>    | Indica l'elenco di immagini di stato. È possibile usare immagini di stato per indicare gli stati degli elementi definiti dall'applicazione. Un'immagine di stato viene visualizzata a sinistra dell'immagine selezionata o non selezionata di un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle HIMAGELIST all'elenco di immagini specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ SETIMAGELIST**](tvm-setimagelist.md)
</dt> </dl>

 

 





