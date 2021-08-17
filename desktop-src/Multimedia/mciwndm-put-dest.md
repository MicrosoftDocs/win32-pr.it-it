---
title: MCIWNDM_PUT_DEST messaggio (Vfw.h)
description: Il messaggio PUT DEST MCIWNDM ridefinisce le coordinate del rettangolo di destinazione usate per lo zoom o l'estensione delle immagini di un file AVI durante \_ \_ la riproduzione. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST di messaggi Windows multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27eb2afdcec32d43b0352af1ead0b4c89715641fd370611542e1e5c6da9efa85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373502"
---
# <a name="mciwndm_put_dest-message"></a>MESSAGGIO PUT \_ DEST MCIWNDM \_

Il **messaggio PUT \_ \_ DEST MCIWNDM** ridefinisce le coordinate del rettangolo di destinazione usate per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndPutDest.**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*Rpc*
</dt> <dd>

Puntatore a [**una struttura RECT**](/previous-versions//dd162897(v=vs.85)) contenente le coordinate del rettangolo di destinazione.

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

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

