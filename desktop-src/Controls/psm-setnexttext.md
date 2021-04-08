---
title: Messaggio PSM_SETNEXTTEXT (Prsht. h)
description: Imposta il testo del pulsante avanti in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Controlli di Windows Message PSM_SETNEXTTEXT
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
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740095"
---
# <a name="psm_setnexttext-message"></a>\_Messaggio SETNEXTTEXT di PSM

Imposta il testo del pulsante **Avanti** in una procedura guidata. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETNEXTTEXTW** (Unicode)<br/>                                         |



 

 





