---
title: Messaggio di MCIWNDM_PUT_DEST (VFW. h)
description: Il \_ \_ messaggio dest MCIWNDM put ridefinisce le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndPutDest.
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST messaggi multimediali di Windows
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
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742951"
---
# <a name="mciwndm_put_dest-message"></a>MCIWNDM \_ put \_ messaggio dest

Il **messaggio \_ \_ dest MCIWNDM put** ridefinisce le coordinate del rettangolo di destinazione usato per lo zoom o l'estensione delle immagini di un file AVI durante la riproduzione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*PRC*
</dt> <dd>

Puntatore a una struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) contenente le coordinate del rettangolo di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

