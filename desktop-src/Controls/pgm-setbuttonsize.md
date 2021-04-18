---
title: Messaggio PGM_SETBUTTONSIZE (COMmctrl. h)
description: Imposta la dimensione corrente del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la \_ macro SetButtonSize del cercapersone.
ms.assetid: b31960f8-87c2-4209-8213-df75ac883e11
keywords:
- Controlli di Windows Message PGM_SETBUTTONSIZE
topic_type:
- apiref
api_name:
- PGM_SETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf8c164ed960675c1a68be36acfe0eff40f972f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517644"
---
# <a name="pgm_setbuttonsize-message"></a>\_Messaggio SETBUTTONSIZE PGM

Imposta la dimensione corrente del pulsante per il controllo pager. È possibile inviare questo messaggio in modo esplicito o utilizzare la macro [**\_ SetButtonSize del cercapersone**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbuttonsize) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore di tipo **int** che contiene le nuove dimensioni del pulsante, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **int** che contiene le dimensioni del pulsante precedenti, in pixel.

## <a name="remarks"></a>Commenti

Se il controllo pager dispone dello [**stile \_ orizzontalmente PGS**](pager-control-styles.md) , le dimensioni del pulsante determinano la larghezza dei pulsanti del cercapersone. Se il controllo pager presenta lo stile [**PGS \_ Vert**](pager-control-styles.md) , le dimensioni del pulsante determinano l'altezza dei pulsanti di spostamento. Per impostazione predefinita, il controllo pager imposta le dimensioni del pulsante su tre quarti della larghezza della barra di scorrimento.

Il pulsante del cercapersone presenta una dimensione minima, attualmente 12 pixel. Tuttavia, questo può cambiare in modo da non dipendere da questo valore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GETBUTTONSIZE PGM**](pgm-getbuttonsize.md)
</dt> </dl>

 

 





