---
title: PSM_SETNEXTTEXT messaggio (Prsht.h)
description: Imposta il testo del pulsante Avanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- PSM_SETNEXTTEXT di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d177acb2f2c96e12f5dc4b460ee88149ad81f9b4f79cc3505f776d8f1f92551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410081"
---
# <a name="psm_setnexttext-message"></a>PSM \_ SETNEXTTEXT message

Imposta il testo del **pulsante Avanti** in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetNextText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a un buffer che contiene il testo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito significativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





