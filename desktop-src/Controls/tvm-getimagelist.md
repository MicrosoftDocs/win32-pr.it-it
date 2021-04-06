---
title: Messaggio TVM_GETIMAGELIST (COMmctrl. h)
description: Recupera l'handle per l'elenco di immagini normale o di stato associato a un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView Getimagine.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Controlli di Windows Message TVM_GETIMAGELIST
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
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743391"
---
# <a name="tvm_getimagelist-message"></a>Messaggio macchina virtuale TVM \_

Recupera l'handle per l'elenco di immagini normale o di stato associato a un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini da recuperare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normale**</dt> </dl> | Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**\_stato TVSIL**</dt> </dl>    | Indica l'elenco di immagini di stato. È possibile usare le immagini di stato per indicare gli Stati degli elementi definiti dall'applicazione. Viene visualizzata un'immagine di stato a sinistra dell'immagine selezionata o non selezionata di un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle HIMAGELIST per l'elenco di immagini specificato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SEimagine TVM**](tvm-setimagelist.md)
</dt> </dl>

 

 





