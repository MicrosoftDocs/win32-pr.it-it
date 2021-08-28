---
title: RB_MAXIMIZEBAND messaggio (Commctrl.h)
description: Ridimensiona una banda in un controllo Rebar in base alle dimensioni ideali o massime.
ms.assetid: 79fff6d0-01f2-4308-b916-38dc06dad894
keywords:
- RB_MAXIMIZEBAND dei messaggi Windows
topic_type:
- apiref
api_name:
- RB_MAXIMIZEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13ef02fbe9611c09d1932907c8218ffd169d3e18d10e0b07faa2b63d50058af1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770091"
---
# <a name="rb_maximizeband-message"></a>Messaggio RB \_ MAXIMIZEBAND

Ridimensiona una banda in un controllo Rebar in base alle dimensioni ideali o massime.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda da ingrandire.

</dd> <dt>

*lParam* 
</dt> <dd>

Indica se la larghezza ideale della banda deve essere usata quando la banda è ingrandita. Se questo valore è diverso da zero, verrà usata la larghezza ideale. Se questo valore è zero, la banda verrà resa più grande possibile.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito non viene utilizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





