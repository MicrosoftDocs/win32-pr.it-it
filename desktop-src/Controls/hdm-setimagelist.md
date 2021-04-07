---
title: Messaggio HDM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito oppure usare l'intestazione \_ SetStateImageList o la \_ macro di intestazione.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Controlli di Windows Message HDM_SETIMAGELIST
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964161"
---
# <a name="hdm_setimagelist-message"></a>HDM \_ messaggio di immagine

Assegna un elenco di immagini a un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito oppure usare l'intestazione [**\_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) o la macro di intestazione. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist)

## <a name="parameters"></a>Parametri

<dl> <dt>*wParam*</dt> <dd>Uno dei valori seguenti:

| Valore                                                                                                                                                      | Significato                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normale**</dt> </dl> | Indica che si tratta di un elenco di immagini normale.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**\_stato HDSIL**</dt> </dl>    | Indica che si tratta di un elenco di immagini di stato.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle per un elenco di immagini.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo. Restituisce **null** in caso di errore o se non è stato impostato in precedenza alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





