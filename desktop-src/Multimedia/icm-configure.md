---
title: ICM_CONFIGURE messaggio (Vfw.h)
description: Il ICM CONFIGURE invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione o esegue una query su un driver di compressione video per determinare se dispone di \_ una finestra di dialogo di configurazione.
ms.assetid: 9760788e-fa66-44d7-bda6-aa9536143774
keywords:
- ICM_CONFIGURE di messaggi Windows multimediali
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
ms.openlocfilehash: 7bc2d9176415c22a1b79a8dc08ee84db1c77fbd6665f89f615b38d3c60538d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785001"
---
# <a name="icm_configure-message"></a>\_ICM MESSAGGIO CONFIGURE

Il **ICM \_ CONFIGURE** invia una notifica a un driver di compressione video per visualizzare la finestra di dialogo di configurazione o esegue una query su un driver di compressione video per determinare se è disponibile una finestra di dialogo di configurazione. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icconfigure)


```C++
ICM_CONFIGURE 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hwnd"></span><span id="HWND"></span>*Hwnd*
</dt> <dd>

Handle per la finestra padre della finestra di dialogo visualizzata. È possibile determinare se un driver dispone di una finestra di dialogo di configurazione specificando 1 in questo parametro, come nella macro [**ICQueryConfigure.**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR OK se il driver supporta questo messaggio o \_ ICERR \_ UNSUPPORTED in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio è diverso dal messaggio [**DRV \_ CONFIGURE**](drv-configure.md) usato per la configurazione hardware. La finestra di dialogo per questo messaggio deve consentire all'utente di impostare e modificare lo stato interno a cui fanno riferimento i ICM [**\_ GETSTATE**](icm-getstate.md) [**ICM \_ SETSTATE.**](icm-setstate.md) Ad esempio, questa finestra di dialogo può consentire all'utente di modificare i parametri che influiscono sul livello di qualità e altre opzioni di compressione simili.

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

 

 





