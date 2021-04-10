---
title: Messaggio di EM_GETOPTIONS (RichEdit. h)
description: Recupera le opzioni di controllo Rich Edit.
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- Controlli di Windows Message EM_GETOPTIONS
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964573"
---
# <a name="em_getoptions-message"></a>\_Messaggio GEToptions em

Recupera le opzioni di controllo Rich Edit.

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

Questo messaggio restituisce una combinazione dei valori del flag di opzione correnti descritti nel [**messaggio \_ seoptions em**](em-setoptions.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Opzioni em**](em-setoptions.md)
</dt> </dl>

 

 





