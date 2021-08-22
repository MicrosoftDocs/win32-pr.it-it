---
title: TVM_SETIMAGELIST messaggio (Commctrl.h)
description: Imposta l'elenco di immagini normali o di stato per un controllo di visualizzazione albero e ridisegna il controllo usando le nuove immagini. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro TreeView SetImageList.
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- TVM_SETIMAGELIST dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df79089c7a2071c6af702da9ef862178738ede3dccff312c3fbae7dbefe4de56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018679"
---
# <a name="tvm_setimagelist-message"></a>Messaggio \_ TVM SETIMAGELIST

Imposta l'elenco di immagini normali o di stato per un controllo di visualizzazione albero e ridisegna il controllo usando le nuove immagini. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ TreeView SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini da impostare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ NORMAL**</dt> </dl> | Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**STATO \_ TVSIL**</dt> </dl>    | Indica l'elenco di immagini di stato. È possibile usare immagini di stato per indicare gli stati degli elementi definiti dall'applicazione. Un'immagine di stato viene visualizzata a sinistra dell'immagine selezionata o non selezionata di un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini. Se *lParam* è **NULL,** il messaggio rimuove l'elenco di immagini specificato dal controllo visualizzazione albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini precedente, se presente, oppure NULL in caso **contrario.**

## <a name="remarks"></a>Commenti

Il controllo di visualizzazione albero non elimina l'elenco di immagini specificato con questo messaggio. L'applicazione deve eliminare l'elenco di immagini quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TVM \_ GETIMAGELIST**](tvm-getimagelist.md)
</dt> </dl>

 

 





