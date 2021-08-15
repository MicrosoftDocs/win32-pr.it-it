---
title: MCIWNDM_GET_SOURCE messaggio (Vfw.h)
description: Il messaggio MCIWNDM GET SOURCE recupera le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante \_ \_ la riproduzione. È possibile inviare questo messaggio in modo esplicito o usando la macro MCIWndGetSource.
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef8bcbaf0909adeae5345448769c68e726456a4bbf4375f08d874e3502ab6a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429401"
---
# <a name="mciwndm_get_source-message"></a>Messaggio MCIWNDM \_ GET \_ SOURCE

Il **messaggio MCIWNDM \_ GET \_ SOURCE** recupera le coordinate del rettangolo di origine usato per ritagliare le immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**MCIWndGetSource.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Rpc*
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per contenere le coordinate del rettangolo di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

