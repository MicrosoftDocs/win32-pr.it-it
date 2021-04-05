---
title: Messaggio PSM_SETFINISHTEXT (Prsht. h)
description: Imposta il testo del pulsante fine in una procedura guidata, Mostra e Abilita il pulsante e nasconde i pulsanti avanti e indietro. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- Controlli di Windows Message PSM_SETFINISHTEXT
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740098"
---
# <a name="psm_setfinishtext-message"></a>\_Messaggio SETFINISHTEXT di PSM

Imposta il testo del pulsante **fine** in una procedura guidata, Mostra e Abilita il pulsante e nasconde i pulsanti **Avanti** e **indietro** . È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al nuovo testo per il pulsante **fine** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il pulsante **fine** non dispone di un tasto di scelta rapida. È possibile creare un tasto di scelta rapida con questo messaggio includendo una e commerciale (&) nella stringa di testo assegnata a *lParam*. Ad esempio, "&Finish" definisce F come tasto di scelta rapida.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





