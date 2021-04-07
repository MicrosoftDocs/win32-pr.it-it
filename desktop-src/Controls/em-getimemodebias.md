---
title: Messaggio di EM_GETIMEMODEBIAS (RichEdit. h)
description: Recupera la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit di Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Controlli di Windows Message EM_GETIMEMODEBIAS
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048560"
---
# <a name="em_getimemodebias-message"></a>\_Messaggio GETIMEMODEBIAS em

Recupera la distorsione della modalità IME (Input Method Editor) per un controllo Rich Edit di Microsoft.

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

Questo messaggio restituisce l'impostazione di distorsione della modalità IME corrente.

## <a name="remarks"></a>Commenti

Per ottenere la distorsione della modalità del Framework dei servizi di testo, usare [**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md).

Prima di chiamare questa funzione, l'applicazione deve chiamare [**em \_ ISIME**](em-isime.md) .

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

[**\_ISIME em**](em-isime.md)
</dt> <dt>

[**\_GETCTFMODEBIAS em**](em-getctfmodebias.md)
</dt> </dl>

 

 





