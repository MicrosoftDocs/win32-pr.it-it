---
title: Messaggio TB_SETEXTENDEDSTYLE (COMmctrl. h)
description: Imposta gli stili estesi per un controllo Toolbar.
ms.assetid: aec64bc7-74b4-4efc-9864-2c8a9fbd35c2
keywords:
- Controlli di Windows Message TB_SETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a540aaeff61bd81b649f0509e064a29282f598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120678"
---
# <a name="tb_setextendedstyle-message"></a>TB \_ SETEXTENDEDSTYLE messaggio

Imposta gli stili estesi per un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Valore che specifica i nuovi stili estesi. Questo parametro può essere una combinazione di [stili estesi](toolbar-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che rappresenta gli stili estesi precedenti. Questo valore può essere una combinazione di [stili estesi](toolbar-extended-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ GETEXTENDEDSTYLE**](tb-getextendedstyle.md)
</dt> </dl>

 

 





