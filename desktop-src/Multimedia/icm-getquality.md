---
title: ICM_GETQUALITY messaggio (Vfw.h)
description: Il ICM \_ GETQUALITY esegue una query su un driver di compressione video per restituire l'impostazione di qualità corrente.
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY di Windows multimediali
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
ms.openlocfilehash: cef214fe36c713e63659fcbd4dde2021c8d410b36ea9f5525ed54c76c5c4b6a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495861"
---
# <a name="icm_getquality-message"></a>\_ICM Messaggio GETQUALITY

Il **ICM \_ GETQUALITY** esegue una query su un driver di compressione video per restituire l'impostazione di qualità corrente.


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo che deve contenere il valore di qualità corrente. I valori di qualità sono da 0 a 10.000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR OK se il driver supporta questo messaggio o \_ ICERR \_ UNSUPPORTED in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> <dt>

[Messaggi di compressione video](video-compression-messages.md)
</dt> </dl>

 

 





