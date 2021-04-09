---
title: Messaggio di WM_CAP_SET_PREVIEW (VFW. h)
description: Il messaggio di anteprima di WM \_ Cap \_ set \_ Abilita o Disabilita la modalità di anteprima.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- WM_CAP_SET_PREVIEW messaggi multimediali di Windows
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
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121394"
---
# <a name="wm_cap_set_preview-message"></a>\_Messaggio di \_ \_ Anteprima set di WM Cap

Il messaggio di **Anteprima di WM \_ Cap \_ set \_** Abilita o Disabilita la modalità di anteprima. In modalità di anteprima, i frame vengono trasferiti dall'hardware di acquisizione alla memoria di sistema e quindi visualizzati nella finestra di acquisizione utilizzando le funzioni GDI. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*f*
</dt> <dd>

Flag di anteprima. Specificare **true** per questo parametro per abilitare la modalità di anteprima o **false** per disabilitarlo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

La modalità di anteprima usa risorse di CPU sostanziali. Le applicazioni possono disabilitare l'anteprima o abbassare la frequenza di anteprima quando un'altra applicazione ha lo stato attivo. Il membro **fLiveWindow** della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se la modalità di anteprima è attualmente abilitata.

L'abilitazione della modalità di anteprima Disabilita automaticamente la modalità overlay.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> <dt>

[Messaggi di acquisizione video](video-capture-messages.md)
</dt> </dl>

 

 





