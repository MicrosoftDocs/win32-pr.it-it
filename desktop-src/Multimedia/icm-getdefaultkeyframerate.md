---
title: Messaggio di ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: Il \_ messaggio MCI GETDEFAULTKEYFRAMERATE esegue una query su un driver di compressione video per la spaziatura dei fotogrammi chiave predefinita o preferita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE messaggi multimediali di Windows
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
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400680"
---
# <a name="icm_getdefaultkeyframerate-message"></a>\_Messaggio GETDEFAULTKEYFRAMERATE ICM

Il messaggio **MCI \_ GETDEFAULTKEYFRAMERATE** esegue una query su un driver di compressione video per la spaziatura dei fotogrammi chiave predefinita o preferita. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Indirizzo per contenere la spaziatura dei fotogrammi chiave preferita.

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

 

 





