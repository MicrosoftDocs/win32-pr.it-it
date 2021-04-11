---
title: Messaggio di WM_CAP_SET_SCALE (VFW. h)
description: Il \_ \_ \_ messaggio di scalabilità set di WM consente di abilitare o disabilitare il ridimensionamento delle immagini video di anteprima.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- WM_CAP_SET_SCALE messaggi multimediali di Windows
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
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121391"
---
# <a name="wm_cap_set_scale-message"></a>\_Messaggio di \_ \_ scalabilità set di WM Cap

Il messaggio di **\_ \_ \_ scalabilità set di WM** consente di abilitare o disabilitare il ridimensionamento delle immagini video di anteprima. Se il ridimensionamento è abilitato, il fotogramma video acquisito viene allungato alle dimensioni della finestra di acquisizione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="f"></span><span id="F"></span>*f*
</dt> <dd>

Flag di ridimensionamento anteprima. Specificare **true** per questo parametro per estendere i frame di anteprima alla dimensione della finestra di acquisizione o **false** per visualizzarli alla dimensione naturale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il ridimensionamento delle immagini di anteprima controlla la presentazione immediata dei frame acquisiti all'interno della finestra di acquisizione. Non ha alcun effetto sulle dimensioni dei frame salvati in un file.

La scalabilità non ha alcun effetto quando si usa la sovrimpressione per visualizzare il video nel buffer del frame.

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

 

 





