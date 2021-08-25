---
title: DTM_GETRANGE messaggio (Commctrl.h)
description: Ottiene le ore di sistema minime e massime consentite correnti per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE di controllo Windows messaggio
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877951"
---
# <a name="dtm_getrange-message"></a>Messaggio DTM \_ GETRANGE

Ottiene le ore di sistema minime e massime consentite correnti per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ DateTime GetRange.**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di [**strutture SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore DWORD** che è una combinazione di GDTR \_ MIN o GDTR \_ MAX. Il primo elemento della matrice [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene il tempo minimo consentito se è impostato GDTR \_ MIN. Il secondo elemento della matrice **SYSTEMTIME** contiene il tempo massimo consentito se è impostato GDTR \_ MAX.

## <a name="remarks"></a>Commenti

Il selettore di data e ora visualizza solo le date/ore che rientrano nell'intervallo specificato, impedendo all'utente di selezionare una data e un'ora che non rientrano nell'intervallo. Se il [**messaggio DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) specifica una data e un'ora che non rientrano nell'intervallo, avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

