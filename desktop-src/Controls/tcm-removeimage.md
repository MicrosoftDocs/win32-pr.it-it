---
title: Messaggio TCM_REMOVEIMAGE (COMmctrl. h)
description: Rimuove un'immagine dall'elenco di immagini di un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TabCtrl RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Controlli di Windows Message TCM_REMOVEIMAGE
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302515"
---
# <a name="tcm_removeimage-message"></a>\_Messaggio TCM REMOVEIMAGE

Rimuove un'immagine dall'elenco di immagini di un controllo struttura a schede. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'immagine da rimuovere.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Il controllo struttura a schede aggiorna l'indice dell'immagine di ogni scheda, in modo che ogni scheda rimanga associata alla stessa immagine precedente. Se una scheda usa l'immagine da rimuovere, la scheda verrà impostata in modo da non avere alcuna immagine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





