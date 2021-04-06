---
title: Messaggio TB_SETHOTITEM2 (COMmctrl. h)
description: Imposta l'elemento attivo in una barra degli strumenti.
ms.assetid: 43666b1d-1197-452f-aa79-eb0a1a23e5b7
keywords:
- Controlli di Windows Message TB_SETHOTITEM2
topic_type:
- apiref
api_name:
- TB_SETHOTITEM2
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027920e4363b46fcc0b6d9b0d87129e01843318
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742650"
---
# <a name="tb_sethotitem2-message"></a>TB \_ SETHOTITEM2 messaggio

Imposta l'elemento attivo in una barra degli strumenti.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento che verrà reso attivo. Se questo valore è-1, nessuno degli elementi sarà attivo.

</dd> <dt>

*lParam* 
</dt> <dd>Combinazione di flag HICF \_ xxx. Vedere <a href="/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem">**NMTBHOTITEM**</a>.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice dell'elemento attivo precedente oppure-1 se non è presente alcun elemento attivo.

## <a name="remarks"></a>Commenti

Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





