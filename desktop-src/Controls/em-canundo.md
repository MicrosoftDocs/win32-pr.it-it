---
title: Messaggio EM_CANUNDO (winuser. h)
description: Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: ae7ff372-b1f8-4ab7-9a7e-450aed3e0bc5
keywords:
- Controlli di Windows Message EM_CANUNDO
topic_type:
- apiref
api_name:
- EM_CANUNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 345367b25790051a444363bb9bbc02af3d6fb0fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120319"
---
# <a name="em_canundo-message"></a>\_Messaggio CANUNDO em

Determina se sono presenti azioni nella coda di annullamento di un controllo di modifica. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se sono presenti azioni nella coda di annullamento del controllo, il valore restituito è diverso da zero.

Se la coda di annullamento è vuota, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se la coda di annullamento non è vuota, è possibile inviare il messaggio di [**\_ annullamento em**](em-undo.md) al controllo per annullare l'operazione più recente.

**Modificare i controlli e rich edit 1,0:** La coda di annullamento contiene solo l'operazione più recente.

**Rich Edit 2,0 e versioni successive:** La coda di annullamento può contenere più operazioni.

**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive. Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Annulla**](em-undo.md)
</dt> </dl>

 

 





