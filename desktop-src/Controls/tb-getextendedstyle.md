---
title: Messaggio TB_GETEXTENDEDSTYLE (COMmctrl. h)
description: Recupera gli stili estesi per un controllo Toolbar.
ms.assetid: d9e31a8e-5e5a-4d2d-bc3b-65ac40e8592f
keywords:
- Controlli di Windows Message TB_GETEXTENDEDSTYLE
topic_type:
- apiref
api_name:
- TB_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80bc4f4ad45e5c1c75366e0890f3fd76ec1fa74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741210"
---
# <a name="tb_getextendedstyle-message"></a>TB \_ GETEXTENDEDSTYLE messaggio

Recupera gli stili estesi per un controllo Toolbar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che rappresenta gli stili attualmente in uso per il controllo Toolbar. Questo valore può essere una combinazione di [stili estesi](toolbar-extended-styles.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TB \_ SETEXTENDEDSTYLE**](tb-setextendedstyle.md)
</dt> </dl>

 

 





