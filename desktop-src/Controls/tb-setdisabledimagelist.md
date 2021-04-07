---
title: Messaggio TB_SETDISABLEDIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti disabilitati.
ms.assetid: 1e76b3cf-2d06-48c8-8298-ef6caf3d85c3
keywords:
- Controlli di Windows Message TB_SETDISABLEDIMAGELIST
topic_type:
- apiref
api_name:
- TB_SETDISABLEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7cc8c9ec1fdc9658413da5991fa109e7bef27a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048597"
---
# <a name="tb_setdisabledimagelist-message"></a>TB \_ SETDISABLEDIMAGELIST messaggio

Imposta l'elenco di immagini che il controllo toolbar utilizzerà per visualizzare i pulsanti disabilitati.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini che verrà impostato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente utilizzato per visualizzare i pulsanti disabilitati oppure **null** se non è stato impostato in precedenza alcun elenco di immagini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





