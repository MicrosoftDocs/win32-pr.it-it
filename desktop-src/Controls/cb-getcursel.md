---
title: CB_GETCURSEL messaggio (Winuser.h)
description: Un'applicazione invia un messaggio GETCURSEL CB per recuperare l'indice dell'elemento attualmente selezionato, se presente, nella casella di riepilogo \_ di una casella combinata.
ms.assetid: 47bf87f6-637f-48e9-849e-b2acbe5a6a7b
keywords:
- CB_GETCURSEL dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- CB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bc51f43fd28563be4bc3f024bf6afd35c297648aa6c6cad677aca4582c3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089261"
---
# <a name="cb_getcursel-message"></a>Messaggio \_ GETCURSEL CB

Un'applicazione invia un **messaggio \_ GETCURSEL CB** per recuperare l'indice dell'elemento attualmente selezionato, se presente, nella casella di riepilogo di una casella combinata.

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

Il valore restituito è l'indice in base zero dell'elemento attualmente selezionato. Se non è selezionato alcun elemento, si tratta di CB \_ ERR.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> </dl>

 

 





