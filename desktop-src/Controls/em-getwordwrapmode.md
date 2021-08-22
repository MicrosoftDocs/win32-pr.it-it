---
title: EM_GETWORDWRAPMODE messaggio (Richedit.h)
description: Ottiene le opzioni di ritorno a capo automatico e interruzione di parola correnti per il controllo Rich Edit.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef3127e5ce3652e9103dfa0e030d66ec7b1b085bc4b60d0cf0bb3f03a30d3fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437951"
---
# <a name="em_getwordwrapmode-message"></a>Messaggio EM \_ GETWORDWRAPMODE

Ottiene le opzioni di ritorno a capo automatico e interruzione di parola correnti per il controllo Rich Edit.

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

Il messaggio restituisce le opzioni correnti per il ritorno a capo automatico e l'interruzione di parola.

## <a name="remarks"></a>Commenti

Questo messaggio non deve essere inviato dalla procedura di word break definita dall'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





