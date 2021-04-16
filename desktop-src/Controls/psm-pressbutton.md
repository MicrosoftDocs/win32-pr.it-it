---
title: Messaggio PSM_PRESSBUTTON (Prsht. h)
description: Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet PressButton.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- Controlli di Windows Message PSM_PRESSBUTTON
topic_type:
- apiref
api_name:
- PSM_PRESSBUTTON
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b54b04dcc7b1263019f49ff8c1de0d2c21a12a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479409"
---
# <a name="psm_pressbutton-message"></a>\_Messaggio PRESSBUTTON di PSM

Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ PressButton**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del pulsante da selezionare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**\_APPLYNOW PSBTN**</dt> </dl> | Seleziona il pulsante **applica** . Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ indietro**</dt> </dl>             | Consente di selezionare il pulsante **indietro** .<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**\_annullamento PSBTN**</dt> </dl>       | Consente di selezionare il pulsante **Annulla** .<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**\_fine PSBTN**</dt> </dl>       | Consente di selezionare il pulsante **fine** .<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**Guida di PSBTN \_**</dt> </dl>             | **Consente** di selezionare il pulsante?. Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ successivo**</dt> </dl>             | Consente di selezionare il pulsante **Avanti** .<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ OK**</dt> </dl>                   | Seleziona il pulsante **OK** . Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





