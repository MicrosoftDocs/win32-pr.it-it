---
title: Messaggio di ICM_DRAW_START_PLAY (VFW. h)
description: Il \_ messaggio di \_ inizio riproduzione del progetto ICM \_ fornisce l'ora di inizio e di fine di un'operazione di riproduzione a un driver di rendering. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICDrawStartPlay.
ms.assetid: 27c4c06e-6510-43dc-a754-fe44144796f5
keywords:
- ICM_DRAW_START_PLAY messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_DRAW_START_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefea0f6344fb598fac1f0413bba5c377c5914e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119555"
---
# <a name="icm_draw_start_play-message"></a>\_Messaggio di \_ inizio \_ riproduzione del progetto ICM

Il messaggio di **\_ \_ inizio \_ riproduzione del progetto ICM** fornisce l'ora di inizio e di fine di un'operazione di riproduzione a un driver di rendering. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICDrawStartPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstartplay) .


```C++
ICM_DRAW_START_PLAY 
wParam = (DWORD_PTR) lFrom; 
lParam = (DWORD_PTR) lTo; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lFrom"></span><span id="lfrom"></span><span id="LFROM"></span>*lFrom*
</dt> <dd>

Ora di inizio.

</dd> <dt>

<span id="lTo"></span><span id="lto"></span><span id="LTO"></span>*lTo*
</dt> <dd>

Ora di fine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo messaggio non restituisce alcun valore.

## <a name="remarks"></a>Commenti

Questo messaggio precede tutti i dati del frame inviati al driver di rendering.

Le unità per *lFrom* e *LTO* vengono specificate con il messaggio di [**\_ \_ inizio del progetto ICM**](icm-draw-begin.md) . Per i dati video si tratta in genere di un numero di frame. Per ulteriori informazioni sulla velocità di riproduzione, vedere i membri **dwRate** e **DwScale** della struttura [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) .

Se l'ora di fine è inferiore all'ora di inizio, la direzione della riproduzione viene invertita.

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

 

 





