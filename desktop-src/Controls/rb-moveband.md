---
title: Messaggio RB_MOVEBAND (COMmctrl. h)
description: Sposta una banda da un indice a un altro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Controlli di Windows Message RB_MOVEBAND
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475341"
---
# <a name="rb_moveband-message"></a>\_Messaggio MOVEBAND RB

Sposta una banda da un indice a un altro.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice in base zero della banda da spostare.

</dd> <dt>

*lParam* 
</dt> <dd>

Indice in base zero della nuova posizione della banda.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.

## <a name="remarks"></a>Commenti

È probabile che questo messaggio modifichi l'indice di altre bande nel controllo Rebar. Se una banda viene spostata dall'indice 6 all'indice 0, per tutte le bande comprese tra l'indice viene incrementato di uno.

*lParam* non deve mai essere maggiore del numero di bande meno uno. Il numero di bande può essere ottenuto con il messaggio [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





