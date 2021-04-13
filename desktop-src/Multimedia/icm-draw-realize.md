---
title: Messaggio di ICM_DRAW_REALIZE (VFW. h)
description: Il \_ messaggio ICM Draw \_ réalisateur informa un driver di rendering di realizzare la relativa tavolozza di disegno durante il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400538"
---
# <a name="icm_draw_realize-message"></a>Messaggio di realizzazione di un \_ progetto ICM \_

Il messaggio **ICM \_ Draw \_ réalisateur** informa un driver di rendering di realizzare la relativa tavolozza di disegno durante il disegno. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*HDC*
</dt> <dd>

Handle per il controller di dominio utilizzato per realizzare la tavolozza.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Flag di sfondo. Specificare **true** per realizzare la tavolozza come attività in background o **false** per realizzare la tavolozza in primo piano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se la tavolozza di disegno è realizzata o ICERR non \_ supportata se la tavolozza associata ai dati decompressi viene realizzata.

## <a name="remarks"></a>Commenti

I driver devono rispondere a questo messaggio solo se la tavolozza di disegno è diversa dalla tavolozza decompressa.

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

 

 





