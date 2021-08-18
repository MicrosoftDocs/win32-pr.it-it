---
title: EM_GETIMEMODEBIAS messaggio (Richedit.h)
description: Recupera la distorsione della modalità Input Method Editor (IME) per un controllo Microsoft Rich Edit.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS di controllo Windows messaggio
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
ms.openlocfilehash: 49ad5504ca2e5ac1a332657c4f539c9f983292617b6e74b949598488ceb38dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019539"
---
# <a name="em_getimemodebias-message"></a>Messaggio \_ EM GETIMEMODEBIAS

Recupera la distorsione della modalità Input Method Editor (IME) per un controllo Microsoft Rich Edit.

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

Questo messaggio restituisce l'impostazione corrente di distorsione della modalità IME.

## <a name="remarks"></a>Commenti

Per ottenere la distorsione Framework servizi di testo, usare [**EM \_ GETCTFMODEBIAS.**](em-getctfmodebias.md)

L'applicazione deve [**chiamare \_ l'ISIME EM**](em-isime.md) prima di chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con \[ app desktop SP1\]<br/>                                  |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 





