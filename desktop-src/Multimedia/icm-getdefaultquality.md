---
title: ICM_GETDEFAULTQUALITY messaggio (Vfw.h)
description: Il ICM \_ GETDEFAULTQUALITY esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY di messaggi Windows multimediali
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
ms.openlocfilehash: df9c27527cea53c4b4eca6cf75babef3a41f80732d8ecf7a18528c07d6d9311b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525911"
---
# <a name="icm_getdefaultquality-message"></a>\_ICM Messaggio GETDEFAULTQUALITY

Il **ICM \_ GETDEFAULTQUALITY** esegue una query su un driver di compressione video per fornire l'impostazione di qualità predefinita. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICGetDefaultQuality.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo che deve contenere il valore di qualità predefinito. I valori di qualità sono da 0 a 10.000.

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

 

 





