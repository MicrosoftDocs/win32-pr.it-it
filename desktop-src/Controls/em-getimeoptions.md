---
title: EM_GETIMEOPTIONS messaggio (Richedit.h)
description: Recupera le opzioni IME (Input Method Editor) correnti.
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS di controllo Windows messaggio
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049061"
---
# <a name="em_getimeoptions-message"></a>Messaggio \_ EM GETIMEOPTIONS

Recupera le opzioni IME (Input Method Editor) correnti.

> [!Note]  
> Questo messaggio è supportato solo nelle versioni in lingua asia di Microsoft Rich Edit 1.0. Non è supportato nelle versioni successive di Rich Edit.

 

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Non usato; deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio restituisce uno o più valori del flag di opzione IME descritti nel [**messaggio EM \_ SETIMEOPTIONS.**](em-setimeoptions.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)
</dt> </dl>

 

 





