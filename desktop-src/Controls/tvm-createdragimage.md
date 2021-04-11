---
title: Messaggio TVM_CREATEDRAGIMAGE (COMmctrl. h)
description: Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Controlli di Windows Message TVM_CREATEDRAGIMAGE
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119919"
---
# <a name="tvm_createdragimage-message"></a>\_Messaggio CREATEDRAGIMAGE TVM

Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero. Il messaggio crea anche un elenco di immagini per la bitmap e aggiunge la bitmap all'elenco di immagini. Un'applicazione può visualizzare l'immagine durante il trascinamento dell'elemento utilizzando le funzioni dell'elenco immagini. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento che riceve la nuova bitmap di trascinamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini a cui è stata aggiunta la bitmap di trascinamento in caso di esito positivo; in caso contrario, **null** .

## <a name="remarks"></a>Commenti

Se si crea un controllo di visualizzazione albero senza un elenco di immagini associato, non è possibile usare il messaggio **TVM \_ CREATEDRAGIMAGE** per creare l'immagine da visualizzare durante un'operazione di trascinamento. È necessario implementare un metodo personalizzato per creare un cursore di trascinamento.

L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





