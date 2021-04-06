---
title: Messaggio di ICM_GETBUFFERSWANTED (VFW. h)
description: Il \_ messaggio MCI GETBUFFERSWANTED esegue una query su un driver per il numero di buffer da allocare. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963881"
---
# <a name="icm_getbufferswanted-message"></a>\_Messaggio GETBUFFERSWANTED ICM

Il messaggio **MCI \_ GETBUFFERSWANTED** esegue una query su un driver per il numero di buffer da allocare. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Indirizzo per contenere il numero di campioni necessari al driver per eseguire in modo efficiente il rendering dei dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK se ha esito positivo o ICERR non \_ supportato in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato dai driver che usano l'hardware per eseguire il rendering dei dati e vogliono garantire un ritardo di tempo minimo causato dall'attesa dell'arrivo dei buffer. Ad esempio, se un driver controlla una lavagna di decompressione video che può ospitare 10 frame di video, potrebbe restituire 10 per questo messaggio. In questo modo, le applicazioni devono provare a rimanere 10 frame prima del frame attualmente necessario.

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

 

 





