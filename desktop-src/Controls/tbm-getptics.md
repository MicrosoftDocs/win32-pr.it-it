---
title: Messaggio TBM_GETPTICS (COMmctrl. h)
description: Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Controlli di Windows Message TBM_GETPTICS
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964253"
---
# <a name="tbm_getptics-message"></a>\_Messaggio GETPTICS TBM

Recupera l'indirizzo di una matrice che contiene le posizioni dei segni di graduazione per un TrackBar.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indirizzo di una matrice di valori **DWORD** . Gli elementi della matrice specificano le posizioni logiche dei segni di graduazione del TrackBar, escluso il primo e l'ultimo segno di graduazione creato dal TrackBar. Le posizioni logiche possono essere uno qualsiasi dei valori integer nell'intervallo compreso tra le posizioni minime e massime del dispositivo di scorrimento.

## <a name="remarks"></a>Commenti

Il numero di elementi nella matrice è inferiore a due rispetto al conteggio restituito dal messaggio [**\_ GETNUMTICS TBM**](tbm-getnumtics.md) . Si noti che i valori nella matrice possono includere posizioni duplicate e che potrebbero non essere in ordine sequenziale. Il puntatore restituito è valido fino a quando non si modificano i segni di graduazione del TrackBar.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





