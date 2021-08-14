---
title: TVM_CREATEDRAGIMAGE messaggio (Commctrl.h)
description: Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- TVM_CREATEDRAGIMAGE del messaggio Windows controlli
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
ms.openlocfilehash: a18a00b2225749b30b8dcd9a928fd73e3ffabcfd4a4f9512cd2332d98cc08a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408661"
---
# <a name="tvm_createdragimage-message"></a>Messaggio TVM \_ CREATEDRAGIMAGE

Crea una bitmap di trascinamento per l'elemento specificato in un controllo di visualizzazione albero. Il messaggio crea anche un elenco di immagini per la bitmap e aggiunge la bitmap all'elenco di immagini. Un'applicazione può visualizzare l'immagine quando si trascina l'elemento usando le funzioni dell'elenco immagini. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ CreateDragImage di TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elemento che riceve la nuova bitmap di trascinamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle all'elenco di immagini a cui è stata aggiunta la bitmap di trascinamento in caso di esito positivo oppure NULL in caso **contrario.**

## <a name="remarks"></a>Commenti

Se si crea un controllo visualizzazione albero senza un elenco di immagini associato, non è possibile usare il messaggio **TVM \_ CREATEDRAGIMAGE** per creare l'immagine da visualizzare durante un'operazione di trascinamento. È necessario implementare un metodo personalizzato per la creazione di un cursore di trascinamento.

L'applicazione è responsabile dell'eliminazione dell'elenco di immagini quando non è più necessario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





