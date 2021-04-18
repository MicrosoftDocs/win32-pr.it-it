---
title: Messaggio di MCIWNDM_CHANGESTYLES (VFW. h)
description: Il \_ messaggio MCIWNDM CHANGESTYLES modifica gli stili utilizzati dalla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- MCIWNDM_CHANGESTYLES messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301170"
---
# <a name="mciwndm_changestyles-message"></a>\_Messaggio MCIWNDM CHANGESTYLES

Il messaggio **MCIWNDM \_ CHANGESTYLES** modifica gli stili utilizzati dalla finestra MCIWnd. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="mask"></span><span id="MASK"></span>*maschera*
</dt> <dd>

Maschera che identifica gli stili che possono cambiare. Questa maschera rappresenta l'operatore OR bit per bit di tutti gli stili che saranno consentiti per la modifica.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valore*
</dt> <dd>

Nuove impostazioni di stile per la finestra. Specificare zero per questo parametro per disattivare tutti gli stili identificati nella maschera. Per un elenco degli stili disponibili, vedere la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





