---
title: ICM_GETDEFAULTKEYFRAMERATE messaggio (Vfw.h)
description: Il ICM getDEFAULTKEYFRAMERATE esegue una query su un driver di compressione video per la spaziatura predefinita \_ (o preferita) dei fotogrammi chiave. È possibile inviare questo messaggio in modo esplicito o usando la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff21682f08dfdcda120f5efb5f7f8629a9e93e21faaf27ff4ee9ee59da8c762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038701"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_ICM Messaggio GETDEFAULTKEYFRAMERATE

Il **ICM \_ getDEFAULTKEYFRAMERATE** esegue una query su un driver di compressione video per la spaziatura predefinita (o preferita) dei fotogrammi chiave. È possibile inviare questo messaggio in modo esplicito o usando la macro [**ICGetDefaulteyFrameRate.**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate)


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo che deve contenere la spaziatura tra fotogrammi chiave preferita.

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

 

 





