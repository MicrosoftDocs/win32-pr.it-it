---
title: Messaggio di EM_GETCTFMODEBIAS (RichEdit. h)
description: Ottiene i valori di distorsione della modalità Framework dei servizi di testo per un controllo Microsoft Rich Edit.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Controlli di Windows Message EM_GETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120011"
---
# <a name="em_getctfmodebias-message"></a>\_Messaggio GETCTFMODEBIAS em

Ottiene i valori di distorsione della modalità Framework dei servizi di testo per un controllo Microsoft Rich Edit.

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

Valore di distorsione della modalità del Framework dei servizi di testo corrente.

## <a name="remarks"></a>Commenti

Per ottenere la distorsione della modalità IME, chiamare [**em \_ GETIMEMODEBIAS**](em-getimemodebias.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP1 \[\]<br/>                                  |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**\_SETCTFMODEBIAS em**](em-setctfmodebias.md)
</dt> <dt>

[**\_GETIMEMODEBIAS em**](em-getimemodebias.md)
</dt> </dl>

 

 





