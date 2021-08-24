---
title: LVM_SETITEMPOSITION32 messaggio (Commctrl.h)
description: Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in visualizzazione icona o icona piccola).
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 dei messaggi Windows controlli
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737b9aa78067bd4851c907da4ac51bd2645a833d8f3335c90a6e81a902d3a30a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656251"
---
# <a name="lvm_setitemposition32-message"></a>Messaggio LVM \_ SETITEMPOSITION32

Sposta un elemento in una posizione specificata in un controllo visualizzazione elenco (deve essere in visualizzazione icona o icona piccola). Questo messaggio è diverso dal [**messaggio LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) in quanto usa coordinate a 32 bit. È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ ListView SetItemPosition32.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Indice dell'elemento della visualizzazione elenco per il quale impostare la posizione.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura POINT**](/previous-versions//dd162805(v=vs.85)) che contiene la nuova posizione dell'elemento, nelle coordinate della visualizzazione elenco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

