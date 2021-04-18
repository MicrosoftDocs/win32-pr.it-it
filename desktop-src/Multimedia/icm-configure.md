---
title: Messaggio di ICM_CONFIGURE (VFW. h)
description: Il \_ messaggio ICM Configure invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione oppure esegue una query su un driver di compressione video per determinare se dispone di una finestra di dialogo di configurazione.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_CONFIGURE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9faae26fcf132abfa424b0db7a88670735d30727
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302271"
---
# <a name="icm_configure-message"></a>\_Messaggio di configurazione ICM

Il messaggio **ICM \_ Configure** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione oppure esegue una query su un driver di compressione video per determinare se dispone di una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICConfigure**](/windows/desktop/api/Vfw/nf-vfw-icconfigure) .


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*HWND*
</dt> <dd>

Handle per la finestra padre della finestra di dialogo visualizzata. È possibile determinare se un driver dispone di una finestra di dialogo di configurazione specificando 1 in questo parametro, come nella macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se il driver supporta questo messaggio o ICERR non \_ supportato in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è diverso dal messaggio [**di \_ configurazione di DRV**](drv-configure.md) usato per la configurazione hardware. La finestra di dialogo per questo messaggio deve consentire all'utente di impostare e modificare lo stato interno a cui fanno riferimento i messaggi di stato [**MCI \_**](icm-getstate.md) GetState e [**ICM \_**](icm-setstate.md) . Questa finestra di dialogo, ad esempio, può consentire all'utente di modificare i parametri che interessano il livello di qualità e altre opzioni di compressione simili.

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

 

 





