---
title: Messaggio di EM_GETEVENTMASK (RichEdit. h)
description: Recupera la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- Controlli di Windows Message EM_GETEVENTMASK
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4d231bbb9d5592ff2f90da6a5096783b38c292
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964581"
---
# <a name="em_geteventmask-message"></a>\_Messaggio GETEVENTMASK em

Recupera la maschera di eventi per un controllo Rich Edit. La maschera eventi specifica i codici di notifica che il controllo Invia alla finestra padre.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilizzato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce la maschera eventi per il controllo Rich Edit.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETEVENTMASK em**](em-seteventmask.md)
</dt> <dt>

[**Flag di maschera eventi controllo Rich Edit**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





