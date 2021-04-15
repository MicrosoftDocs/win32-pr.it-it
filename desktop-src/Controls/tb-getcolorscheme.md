---
title: Messaggio TB_GETCOLORSCHEME (COMmctrl. h)
description: Recupera le informazioni sulla combinazione di colori dal controllo Toolbar.
ms.assetid: af172631-309e-4181-a690-05946cd6e143
keywords:
- Controlli di Windows Message TB_GETCOLORSCHEME
topic_type:
- apiref
api_name:
- TB_GETCOLORSCHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61344439ae8bc2b3a9ecd47472174577d652aa96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477105"
---
# <a name="tb_getcolorscheme-message"></a>TB \_ GETCOLORSCHEME messaggio

Recupera le informazioni sulla combinazione di colori dal controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**ColorScheme**](/windows/win32/api/commctrl/ns-commctrl-colorscheme) che riceverà le informazioni sulla combinazione di colori. Prima di inviare questo messaggio, è necessario impostare il membro **cbSize** della struttura su **sizeof**(ColorScheme).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ SETCOLORSCHEME**](tb-setcolorscheme.md)
</dt> </dl>

 

 





