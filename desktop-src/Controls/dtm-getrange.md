---
title: Messaggio DTM_GETRANGE (COMmctrl. h)
description: Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Controlli di Windows Message DTM_GETRANGE
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
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477933"
---
# <a name="dtm_getrange-message"></a>\_Messaggio GETRANGE DTM

Ottiene l'ora di sistema corrente minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **DWORD** che corrisponde a una combinazione di GDTR \_ min o GDTR \_ max. Il primo elemento della matrice [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contiene il tempo minimo consentito se \_ è impostato GDTR min. Il secondo elemento della matrice **SYSTEMTIME** contiene il tempo massimo consentito se \_ è impostato GDTR max.

## <a name="remarks"></a>Commenti

Il selettore di data e ora Visualizza solo le date e le ore che rientrano nell'intervallo specificato, impedendo all'utente di selezionare una data e un'ora non comprese nell'intervallo. Se il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) specifica una data e un'ora che non rientrano nell'intervallo, l'operazione avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

