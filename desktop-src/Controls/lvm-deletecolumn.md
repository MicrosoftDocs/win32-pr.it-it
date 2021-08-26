---
title: LVM_DELETECOLUMN messaggio (Commctrl.h)
description: Rimuove una colonna da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro ListView DeleteColumn.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920321"
---
# <a name="lvm_deletecolumn-message"></a>Messaggio LVM \_ DELETECOLUMN

Rimuove una colonna da un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**\_ ListView DeleteColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice della colonna da eliminare.

</dd> <dt>

*lParam* 
</dt> <dd>Deve essere zero.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

L'eliminazione della colonna zero di un controllo visualizzazione elenco è supportata solo ComCtl32.dll versione 6 e successive. La versione 5 supporta anche l'eliminazione della colonna zero, ma solo dopo aver utilizzato [**CCM \_ SETVERSION**](ccm-setversion.md) per impostare la versione su 5 o versione successiva. Nelle versioni precedenti alla versione 5, se è necessario eliminare la colonna zero, inserire una colonna fittizia di lunghezza zero zero ed eliminare la colonna uno e superiore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





