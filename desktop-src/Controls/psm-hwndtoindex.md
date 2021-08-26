---
title: PSM_HWNDTOINDEX messaggio (Prsht.h)
description: Accetta l'handle della finestra della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro PropSheet HwndToIndex.
ms.assetid: vs|controls|~\controls\propsheet\messages\psm_hwndtoindex.htm
keywords:
- PSM_HWNDTOINDEX di controllo Windows messaggio
topic_type:
- apiref
api_name:
- PSM_HWNDTOINDEX
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ed61c958fb3a0b30ba7cf55d1040cac51caa67f460d329312fb0e798b016aec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985831"
---
# <a name="psm_hwndtoindex-message"></a>Messaggio \_ HWNDTOINDEX PSM

Accetta l'handle della finestra della pagina della finestra delle proprietà e restituisce il relativo indice in base zero. È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ PropSheet HwndToIndex.**](/windows/desktop/api/Prsht/nf-prsht-propsheet_hwndtoindex)

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Handle per la finestra della pagina.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'indice in base zero della pagina della finestra delle proprietà specificata da *wParam* in caso di esito positivo. In caso contrario, restituisce -1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Prsht.h</dt> </dl> |



 

 





