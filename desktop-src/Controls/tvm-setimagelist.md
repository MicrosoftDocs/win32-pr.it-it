---
title: Messaggio TVM_SETIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini normale o di stato per un controllo di visualizzazione albero e ridisegnato il controllo usando le nuove immagini. È possibile inviare questo messaggio in modo esplicito o usando la macro dell'oggetto TreeView \_ .
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Controlli di Windows Message TVM_SETIMAGELIST
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
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741554"
---
# <a name="tvm_setimagelist-message"></a>\_Messaggio SEimagine TVM

Imposta l'elenco di immagini normale o di stato per un controllo di visualizzazione albero e ridisegnato il controllo usando le nuove immagini. È possibile inviare questo messaggio in modo esplicito o usando la macro dell'oggetto [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di elenco di immagini da impostare. Questo parametro può essere uno dei valori seguenti:



| Valore                                                                                                                                                      | Significato                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <dt>**TVSIL \_ normale**</dt> </dl> | Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.<br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <dt>**\_stato TVSIL**</dt> </dl>    | Indica l'elenco di immagini di stato. È possibile usare le immagini di stato per indicare gli Stati degli elementi definiti dall'applicazione. Viene visualizzata un'immagine di stato a sinistra dell'immagine selezionata o non selezionata di un elemento.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini. Se *lParam* è **null**, il messaggio rimuove l'elenco di immagini specificato dal controllo di visualizzazione albero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedente, se presente, o **null** in caso contrario.

## <a name="remarks"></a>Commenti

Il controllo di visualizzazione albero non eliminerà l'elenco di immagini specificato con questo messaggio. Quando non è più necessario, l'applicazione deve eliminare l'elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**macchina \_ virtuale TVM**](tvm-getimagelist.md)
</dt> </dl>

 

 





