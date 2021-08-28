---
title: PSM_ENABLEWIZBUTTONS messaggio (Prsht.h)
description: Abilita o disabilita uno dei pulsanti standard in una procedura guidata Dio. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro EnableWizButtons di PropSheet.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- PSM_ENABLEWIZBUTTONS dei messaggi Windows
topic_type:
- apiref
api_name:
- PSM_ENABLEWIZBUTTONS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a677b596e57a55271224f5b22baac5d979e2806c20676065457aa47b8a66e527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825872"
---
# <a name="psm_enablewizbuttons-message"></a>Messaggio \_ ENABLEWIZBUTTONS PSM

Abilita o disabilita uno dei pulsanti standard in una procedura guidata Dio. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ EnableWizButtons di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più dei valori seguenti che specificano quali pulsanti della finestra delle proprietà devono essere abilitati. Se il valore di un pulsante è incluso sia in questo parametro che *in lParam,* è abilitato.



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

Uno o più degli stessi valori utilizzati in *wParam*, che specificano quali pulsanti sono interessati da questa chiamata. Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, indica che il pulsante deve essere disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





