---
title: MCIWNDM_SETSPEED messaggio (Vfw.h)
description: Il messaggio MCIWNDM \_ SETSPEED imposta la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de0d78fef7723dab0ae2e2d3923f73f872e38dfd9c3e0f42443f7141f020336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782991"
---
# <a name="mciwndm_setspeed-message"></a>Messaggio DI MCIWNDM \_ SETSPEED

Il **messaggio MCIWNDM \_ SETSPEED** imposta la velocità di riproduzione di un dispositivo MCI. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndSetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*Ispeed*
</dt> <dd>

Velocità di riproduzione. Specificare 1000 per la velocità normale, valori maggiori per velocità più veloci e valori più piccoli per le velocità più lente.

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

[**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





