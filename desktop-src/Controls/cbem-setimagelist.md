---
title: Messaggio CBEM_SETIMAGELIST (COMmctrl. h)
description: Imposta un elenco di immagini per un controllo ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Controlli di Windows Message CBEM_SETIMAGELIST
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964861"
---
# <a name="cbem_setimagelist-message"></a>CBEM \_ messaggio di immagine

Imposta un elenco di immagini per un controllo ComboBoxEx.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Handle per l'elenco di immagini da impostare per il controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo oppure restituisce **null** se non è stato impostato in precedenza alcun elenco di immagini.

## <a name="remarks"></a>Commenti

> [!IMPORTANT]
> L'altezza delle immagini nell'elenco immagini potrebbe modificare i requisiti di dimensioni del controllo ComboBoxEx. È consigliabile ridimensionare il controllo dopo l'invio di questo messaggio per assicurarsi che venga visualizzato correttamente.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





