---
title: WM_CAP_SET_SCALE messaggio (Vfw.h)
description: Il messaggio WM \_ CAP SET SCALE abilita o disabilita il \_ \_ ridimensionamento delle immagini video di anteprima.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE messaggio Windows Multimediali
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3293be6917917581957df0f5dae9456274f1d2cc3eeffff5ea971c3596209a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369395"
---
# <a name="wm_cap_set_scale-message"></a>Messaggio WM \_ CAP \_ SET \_ SCALE

Il **messaggio WM CAP SET \_ \_ \_ SCALE** abilita o disabilita il ridimensionamento delle immagini video di anteprima. Se il ridimensionamento è abilitato, il fotogramma video acquisito viene adattato alle dimensioni della finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o usando la macro [**capPreviewScale.**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale)


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*F*
</dt> <dd>

Flag di ridimensionamento di anteprima. Specificare **TRUE** per questo parametro per adattare i fotogrammi di anteprima alle dimensioni della finestra di acquisizione o **FALSE** per visualizzarli alle dimensioni naturali.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo o FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Il ridimensionamento delle immagini di anteprima controlla la presentazione immediata dei fotogrammi acquisiti all'interno della finestra di acquisizione. Non ha alcun effetto sulle dimensioni dei frame salvati nel file.

Il ridimensionamento non ha alcun effetto quando si usa la sovrimpressione per visualizzare i video nel buffer dei fotogrammi.

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

 

 





