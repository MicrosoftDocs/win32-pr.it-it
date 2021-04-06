---
title: Messaggio DTM_SETRANGE (COMmctrl. h)
description: Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Controlli di Windows Message DTM_SETRANGE
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742559"
---
# <a name="dtm_setrange-message"></a>\_Messaggio SEtrange DTM

Imposta l'ora di sistema minima e massima consentita per un controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Valore che specifica quali valori di intervallo sono validi. Questo parametro può essere una combinazione dei valori seguenti:



| Valore                                                                                                                                          | Significato                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ min**</dt> </dl> | Il primo elemento nella matrice della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) è valido e verrà utilizzato per impostare l'ora di sistema minima consentita.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | Il secondo elemento della matrice della struttura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) è valido e verrà utilizzato per impostare l'ora di sistema massima consentita.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una matrice a due elementi di strutture [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Il primo elemento della matrice **SYSTEMTIME** contiene il tempo minimo consentito. Il secondo elemento della matrice **SYSTEMTIME** contiene il tempo massimo consentito. Non è necessario inserire un elemento di matrice non specificato nel parametro *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

Il selettore di data e ora Visualizza solo le date e le ore che rientrano nell'intervallo specificato, impedendo all'utente di selezionare una data e un'ora non comprese nell'intervallo. Se il [**messaggio \_ SETSYSTEMTIME di DTM**](dtm-setsystemtime.md) specifica una data e un'ora che non rientrano nell'intervallo, l'operazione avrà esito negativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

