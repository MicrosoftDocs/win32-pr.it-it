---
title: Messaggio HDM_GETIMAGELIST (COMmctrl. h)
description: Ottiene l'handle per l'elenco di immagini che è stato impostato per un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare l'intestazione \_ GetStateImageList o la macro header GetImages \_ .
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- Controlli di Windows Message HDM_GETIMAGELIST
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742279"
---
# <a name="hdm_getimagelist-message"></a>HDM \_ messaggio GETimagine

Ottiene l'handle per l'elenco di immagini che è stato impostato per un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito o usare l'intestazione [**\_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) o la macro header [**\_ GetImages**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) .

## <a name="parameters"></a>Parametri

<dl> <dt>*wParam*</dt> <dd>Uno dei valori seguenti:

| Valore                                                                                                                                                      | Significato                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normale**</dt> </dl> | Indica che si tratta di un elenco di immagini normale.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**\_stato HDSIL**</dt> </dl>    | Indica che si tratta di un elenco di immagini di stato.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un handle per il set di elenchi di immagini per il controllo intestazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





