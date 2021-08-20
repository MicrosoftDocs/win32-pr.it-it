---
title: WM_CAP_SET_PREVIEW messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET PREVIEW abilita o disabilita la modalità di \_ \_ anteprima.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25bf7f1ce2a61cb104c1e1764f9bca9c82d3aa40d44cc8a1eef9ce435584271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369385"
---
# <a name="wm_cap_set_preview-message"></a>Messaggio \_ DI ANTEPRIMA WM CAP \_ SET \_

Il **messaggio WM CAP SET \_ \_ \_ PREVIEW** abilita o disabilita la modalità di anteprima. In modalità di anteprima, i frame vengono trasferiti dall'hardware di acquisizione alla memoria di sistema e quindi visualizzati nella finestra di acquisizione usando le funzioni GDI. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPreview.**](/windows/desktop/api/Vfw/nf-vfw-cappreview)


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Flag di anteprima. Specificare **TRUE** per questo parametro per abilitare la modalità di anteprima o **FALSE** per disabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** l'operazione ha esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

La modalità di anteprima usa notevoli risorse della CPU. Le applicazioni possono disabilitare l'anteprima o ridurre la frequenza di anteprima quando un'altra applicazione ha lo stato attivo. Il **membro fLiveWindow** della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità di anteprima è attualmente abilitata.

L'abilitazione della modalità di anteprima disabilita automaticamente la modalità di sovrapposizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





