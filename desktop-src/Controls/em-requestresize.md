---
title: EM_REQUESTRESIZE messaggio (Richedit.h)
description: Impone a un controllo Rich Edit di inviare un codice di notifica EN \_ REQUESTRESIZE alla relativa finestra padre.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7113f52e2fa3a293549443f779ba937bf20b85736c6751cd9ab77bdbecd45c3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440161"
---
# <a name="em_requestresize-message"></a>Messaggio EM \_ REQUESTRESIZE

Impone a un controllo Rich Edit di inviare un codice di notifica [**EN \_ REQUESTRESIZE**](en-requestresize.md) alla relativa finestra padre.

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

Questo messaggio non restituisce un valore.

## <a name="remarks"></a>Commenti

Questo messaggio è utile durante [**l'elaborazione \_ di WM SIZE**](/windows/desktop/winmsg/wm-size) per l'elemento padre di un controllo rich edit senza fondo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**DIMENSIONI \_ WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

