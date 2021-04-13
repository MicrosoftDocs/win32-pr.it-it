---
title: Messaggio di ICM_GETDEFAULTQUALITY (VFW. h)
description: Il \_ messaggio MCI GETDEFAULTQUALITY esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475700"
---
# <a name="icm_getdefaultquality-message"></a>\_Messaggio GETDEFAULTQUALITY ICM

Il messaggio **MCI \_ GETDEFAULTQUALITY** esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo per contenere il valore di qualità predefinito. I valori di qualità variano da 0 a 10.000.

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

 

 





