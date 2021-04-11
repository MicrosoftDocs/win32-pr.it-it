---
title: Messaggio PSM_ENABLEWIZBUTTONS (Prsht. h)
description: Abilita o Disabilita uno dei pulsanti standard in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro EnableWizButtons di PropSheet.
ms.assetid: 9e8ff2dc-c0e7-4754-8be2-2c7b65a524f4
keywords:
- Controlli di Windows Message PSM_ENABLEWIZBUTTONS
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
ms.openlocfilehash: 01fb30fa3337aed369c2cd24a1296785bd6b3a79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964470"
---
# <a name="psm_enablewizbuttons-message"></a>\_Messaggio ENABLEWIZBUTTONS di PSM

Abilita o Disabilita uno dei pulsanti standard in una procedura guidata Aero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ EnableWizButtons di PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_enablewizbuttons) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Uno o più dei valori seguenti che specificano quali pulsanti della finestra delle proprietà devono essere abilitati. Se il valore di un pulsante è incluso sia in questo parametro che in *lParam*, è abilitato.



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

Uno o più degli stessi valori utilizzati in *wParam*, che specificano quali pulsanti sono interessati da questa chiamata. Se il valore di un pulsante viene visualizzato in questo parametro ma non in *wParam*, significa che il pulsante deve essere disabilitato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





