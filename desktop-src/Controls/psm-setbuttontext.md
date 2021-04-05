---
title: Messaggio PSM_SETBUTTONTEXT (Prsht. h)
description: Imposta il testo su un pulsante in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- Controlli di Windows Message PSM_SETBUTTONTEXT
topic_type:
- apiref
api_name:
- PSM_SETBUTTONTEXT
- PSM_SETBUTTONTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41a0b55f73fc7084e89f54c1e741d12000b0f949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048256"
---
# <a name="psm_setbuttontext-message"></a>\_Messaggio SETBUTTONTEXT di PSM

Imposta il testo su un pulsante in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetButtonText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno dei valori seguenti che specifica il pulsante il cui testo è impostato.



| Valore                                                                                                                                                                                 | Significato                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ indietro**</dt> </dl>                               | Pulsante **indietro** .<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**\_annullamento PSWIZB**</dt> </dl>                         | Pulsante **Annulla** .<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**\_DISABLEDFINISH PSWIZB**</dt> </dl> | Pulsante **fine** .<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**\_fine PSWIZB**</dt> </dl>                         | Pulsante **fine** .<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ successivo**</dt> </dl>                               | Pulsante **Avanti** .<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Testo da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





