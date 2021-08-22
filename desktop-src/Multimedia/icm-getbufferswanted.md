---
title: ICM_GETBUFFERSWANTED messaggio (Vfw.h)
description: Il ICM \_ GETBUFFERSWANTED esegue una query su un driver per il numero di buffer da allocare. È possibile inviare questo messaggio in modo esplicito o tramite la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED messaggio Windows Multimediali
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
ms.openlocfilehash: c4bd5fae6e9f008649366cf922ef117f5b6f7560a7764c4f8d81552a255de48a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495871"
---
# <a name="icm_getbufferswanted-message"></a>\_ICM GETBUFFERSWANTED message

Il **ICM \_ getBUFFERSWANTED** esegue una query su un driver per il numero di buffer da allocare. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**ICGetBuffersWanted.**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted)


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Indirizzo per contenere il numero di campioni di cui il driver ha bisogno per eseguire in modo efficiente il rendering dei dati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce ICERR \_ OK in caso di esito positivo o ICERR \_ UNSUPPORTED in caso contrario.

## <a name="remarks"></a>Commenti

Questo messaggio viene usato dai driver che usano hardware per il rendering dei dati e desiderano garantire un ritardo di tempo minimo causato dall'attesa dell'arrivo dei buffer. Ad esempio, se un driver controlla una scheda di decompressione video che può contenere 10 fotogrammi di video, potrebbe restituire 10 per questo messaggio. Questo indica alle applicazioni di provare a rimanere 10 fotogrammi avanti rispetto al frame attualmente necessario.

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

 

 





