---
title: PSM_PRESSBUTTON messaggio (Prsht.h)
description: Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro PressButton di PropSheet.
ms.assetid: 82a55a29-d916-47ee-b0a0-f685a3a386d9
keywords:
- PSM_PRESSBUTTON del messaggio Windows controlli
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
ms.openlocfilehash: 182a51e6017a6ffcfbba74229e95a9848bede371e7e7e0faa04abed0a60c210e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088671"
---
# <a name="psm_pressbutton-message"></a>Messaggio \_ PRESSBUTTON PSM

Simula la selezione di un pulsante della finestra delle proprietà. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ PressButton di PropSheet.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_pressbutton)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice del pulsante da selezionare. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                            | Significato                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PSBTN_APPLYNOW"></span><span id="psbtn_applynow"></span><dl> <dt>**PSBTN \_ APPLYNOW**</dt> </dl> | Seleziona il **pulsante** Applica. Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/> |
| <span id="PSBTN_BACK"></span><span id="psbtn_back"></span><dl> <dt>**PSBTN \_ BACK**</dt> </dl>             | Seleziona il **pulsante** Indietro.<br/>                                                                                                         |
| <span id="PSBTN_CANCEL"></span><span id="psbtn_cancel"></span><dl> <dt>**PSBTN \_ CANCEL**</dt> </dl>       | Seleziona il **pulsante** Annulla.<br/>                                                                                                       |
| <span id="PSBTN_FINISH"></span><span id="psbtn_finish"></span><dl> <dt>**FINE PSBTN \_**</dt> </dl>       | Seleziona il **pulsante** Fine.<br/>                                                                                                       |
| <span id="PSBTN_HELP"></span><span id="psbtn_help"></span><dl> <dt>**GUIDA DI \_ PSBTN**</dt> </dl>             | Seleziona il **pulsante ?** . Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>  |
| <span id="PSBTN_NEXT"></span><span id="psbtn_next"></span><dl> <dt>**PSBTN \_ NEXT**</dt> </dl>             | Seleziona il **pulsante** Avanti.<br/>                                                                                                         |
| <span id="PSBTN_OK"></span><span id="psbtn_ok"></span><dl> <dt>**PSBTN \_ OK**</dt> </dl>                   | Seleziona il **pulsante OK.** Questo valore non è valido quando si usa lo stile della procedura guidata Aero ([**PSH \_ ACROBATWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).<br/>    |



 

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





