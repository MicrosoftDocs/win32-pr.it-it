---
title: PSM_SETBUTTONTEXT messaggio (Prsht.h)
description: Imposta il testo di un pulsante in una procedura guidata di Aero. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PropSheet SetButtonText.
ms.assetid: 30b7afd1-5094-430f-9c48-d87832d96050
keywords:
- PSM_SETBUTTONTEXT dei controlli Windows messaggio
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
ms.openlocfilehash: feac193beef3149140447a38c0be00b7f4fa0c1c1b28e10a5d7de2203ba21cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088591"
---
# <a name="psm_setbuttontext-message"></a>Messaggio \_ SETBUTTONTEXT PSM

Imposta il testo di un pulsante in una procedura guidata di Aero. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PropSheet SetButtonText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setbuttontext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno dei valori seguenti che specifica il pulsante il cui testo è impostato.



| Valore                                                                                                                                                                                 | Significato                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="PSWIZB_BACK"></span><span id="pswizb_back"></span><dl> <dt>**PSWIZB \_ BACK**</dt> </dl>                               | Pulsante  Indietro.<br/>   |
| <span id="PSWIZB_CANCEL"></span><span id="pswizb_cancel"></span><dl> <dt>**PSWIZB \_ CANCEL**</dt> </dl>                         | Pulsante  Annulla.<br/> |
| <span id="PSWIZB_DISABLEDFINISH"></span><span id="pswizb_disabledfinish"></span><dl> <dt>**PSWIZB \_ DISABLEDFINISH**</dt> </dl> | Pulsante **Fine.**<br/> |
| <span id="PSWIZB_FINISH"></span><span id="pswizb_finish"></span><dl> <dt>**PSWIZB \_ FINISH**</dt> </dl>                         | Pulsante **Fine.**<br/> |
| <span id="PSWIZB_NEXT"></span><span id="pswizb_next"></span><dl> <dt>**PSWIZB \_ NEXT**</dt> </dl>                               | Pulsante  Avanti.<br/>   |



 

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETBUTTONTEXTW** (Unicode)<br/>                                       |



 

 





