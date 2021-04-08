---
title: Messaggio di ICM_GETQUALITY (VFW. h)
description: Il \_ messaggio ICM getquality esegue una query su un driver di compressione video per restituire la relativa impostazione della qualità corrente.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964989"
---
# <a name="icm_getquality-message"></a>\_Messaggio ICM GETquality

Il messaggio **ICM \_ getquality** esegue una query su un driver di compressione video per restituire la relativa impostazione della qualità corrente.


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo per contenere il valore di qualità corrente. I valori di qualità variano da 0 a 10.000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





