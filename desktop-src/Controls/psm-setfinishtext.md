---
title: PSM_SETFINISHTEXT messaggio (Prsht.h)
description: Imposta il testo del pulsante Fine in una procedura guidata, visualizza e abilita il pulsante e nasconde i pulsanti Avanti e Indietro. È possibile inviare questo messaggio in modo esplicito o tramite la macro PropSheet \_ SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT di controllo Windows messaggio
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
ms.openlocfilehash: 5a08cafbeafeccb2235cb9b653f997aa8c60bd5fd21a3ccbc92e572fa5d3d0db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088561"
---
# <a name="psm_setfinishtext-message"></a>Messaggio \_ PSM SETFINISHTEXT

Imposta il testo del **pulsante Fine** in una procedura guidata, visualizza e abilita il pulsante e nasconde i **pulsanti** Avanti **e** Indietro. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**PropSheet \_ SetFinishText.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore al nuovo testo per il **pulsante** Fine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il **pulsante Fine** non dispone di un tasto di scelta rapida. È possibile creare un acceleratore di tastiera con questo messaggio includendo una e commerciale (&) nella stringa di testo assegnata a *lParam*. Ad esempio, "&fine" definisce F come tasto di scelta rapida.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) e **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





