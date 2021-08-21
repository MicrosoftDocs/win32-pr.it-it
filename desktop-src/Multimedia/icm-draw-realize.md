---
title: ICM_DRAW_REALIZE messaggio (Vfw.h)
description: Il ICM DRAW REALIZE notifica a un driver di rendering di realizzare \_ la tavolozza di disegno durante il \_ disegno. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICDrawRealize.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE messaggio Windows Multimediali
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
ms.openlocfilehash: f05e9bd21cc8185afd17ec909fcf95bf3ac6bedba7477f47191b9f3d51383914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987246"
---
# <a name="icm_draw_realize-message"></a>\_ICM Messaggio DRAW \_ REALIZE

Il **ICM \_ DRAW \_ REALIZE** notifica a un driver di rendering di realizzare la tavolozza di disegno durante il disegno. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICDrawRealize.**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize)


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="hdc"></span><span id="HDC"></span>*Hdc*
</dt> <dd>

Handle per il controller di dominio usato per realizzare il riquadro.

</dd> <dt>

<span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*
</dt> <dd>

Flag di sfondo. Specificare **TRUE** per realizzare la tavolozza come attività in background o **FALSE** per realizzare la tavolozza in primo piano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR OK se la tavolozza di disegno viene realizzata o ICERR UNSUPPORTED se viene realizzata la tavolozza associata \_ \_ ai dati decompressi.

## <a name="remarks"></a>Commenti

I driver devono rispondere a questo messaggio solo se la tavolozza di disegno è diversa dalla tavolozza decompressa.

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

 

 





