---
title: MCIWNDM_GET_DEST messaggio (Vfw.h)
description: Il messaggio MCIWNDM GET DEST recupera le coordinate del rettangolo di destinazione usate per lo zoom o l'estensione delle immagini di un \_ \_ file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndGetDest.
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a6326485bece572b03ceeca687ca4468b6d866c25c738c32d13763fd0931a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802905"
---
# <a name="mciwndm_get_dest-message"></a>Messaggio MCIWNDM \_ GET \_ DEST

Il **messaggio MCIWNDM \_ GET \_ DEST** recupera le coordinate del rettangolo di destinazione usate per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndGetDest.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Rpc*
</dt> <dd>

Puntatore a una [**struttura RECT**](/previous-versions//dd162897(v=vs.85)) per restituire le coordinate del rettangolo di destinazione.

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

[**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

