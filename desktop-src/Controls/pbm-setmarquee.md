---
title: Messaggio PBM_SETMARQUEE (COMmctrl. h)
description: Imposta l'indicatore di stato sulla modalità marquee. Questo fa sì che l'indicatore di stato si sposti come un Marquee.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- Controlli di Windows Message PBM_SETMARQUEE
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964563"
---
# <a name="pbm_setmarquee-message"></a>\_Messaggio di RISELEZIONE PBM

Imposta l'indicatore di stato sulla modalità marquee. Questo fa sì che l'indicatore di stato si sposti come un Marquee.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se attivare o disattivare la modalità marquee.

</dd> <dt>

*lParam* 
</dt> <dd>Tempo, in millisecondi, tra gli aggiornamenti di animazione Marquee. Se questo parametro è zero, l'animazione Marquee viene aggiornata ogni 30 millisecondi.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce sempre **true**.

## <a name="remarks"></a>Commenti

Utilizzare questo messaggio quando non si conosce la quantità di avanzamento verso il completamento, ma si desidera indicare che lo stato di avanzamento è stato eseguito.

Inviare il **messaggio \_ per** l'avvio o l'arresto dell'animazione.

> [!Note]  
> È necessario impostare lo stile del controllo su [**PBS \_ Marquee**](progress-bar-control-styles.md) prima di provare ad avviare l'animazione.

 

> [!Note]  
> Per questo messaggio è necessario ComCtl32.dll versione 6,00 o successiva.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





