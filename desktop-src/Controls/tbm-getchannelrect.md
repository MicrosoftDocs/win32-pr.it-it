---
title: Messaggio TBM_GETCHANNELRECT (COMmctrl. h)
description: Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un TrackBar.
ms.assetid: 353edae3-1a26-4e85-8a32-ba8b5a976d24
keywords:
- Controlli di Windows Message TBM_GETCHANNELRECT
topic_type:
- apiref
api_name:
- TBM_GETCHANNELRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02982e9ce417b9fcf3e16d0e14d061e3ffd97a8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963934"
---
# <a name="tbm_getchannelrect-message"></a>\_Messaggio GETCHANNELRECT TBM

Recupera le dimensioni e la posizione del rettangolo di delimitazione per il canale di un TrackBar. (Il canale è l'area in cui viene spostato il dispositivo di scorrimento. Contiene l'evidenziazione quando viene selezionato un intervallo.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) . Il messaggio compila questa struttura con il rettangolo di delimitazione del canale, in coordinate client della finestra del TrackBar.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

