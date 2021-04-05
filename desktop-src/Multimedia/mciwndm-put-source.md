---
title: Messaggio di MCIWNDM_PUT_SOURCE (VFW. h)
description: Il \_ messaggio di origine MCIWNDM put \_ ridefinisce le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739815"
---
# <a name="mciwndm_put_source-message"></a>\_Messaggio di \_ origine put MCIWNDM

Il messaggio di **\_ \_ origine MCIWNDM put** ridefinisce le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Puntatore a una struttura [Rect](/previous-versions//ms536136(v=vs.85)) contenente le coordinate del rettangolo di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

