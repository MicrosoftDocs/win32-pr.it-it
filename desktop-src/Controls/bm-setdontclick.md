---
title: Messaggio BM_SETDONTCLICK (winuser. h)
description: Imposta un flag su un pulsante di opzione che controlla la generazione di BN che hanno \_ fatto clic su messaggi quando il pulsante riceve lo stato attivo.
ms.assetid: 91d98bce-abea-4afc-a995-0f426ba7a518
keywords:
- Controlli di Windows Message BM_SETDONTCLICK
topic_type:
- apiref
api_name:
- BM_SETDONTCLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8596ec679ff07b87b3433d5b5a7805698f56f84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301185"
---
# <a name="bm_setdontclick-message"></a>\_Messaggio SETDONTCLICK BM

Imposta un flag su un pulsante di opzione che controlla la generazione di BN che hanno [ \_ fatto clic su](bn-clicked.md) messaggi quando il pulsante riceve lo stato attivo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* \[ in\]
</dt> <dd>

Valore **booleano** che specifica lo stato. **True** per impostare il flag, in caso contrario **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



 

 





