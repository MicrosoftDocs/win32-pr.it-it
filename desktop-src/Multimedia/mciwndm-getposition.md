---
title: Messaggio di MCIWNDM_GETPOSITION (VFW. h)
description: Il \_ messaggio MCIWNDM GetPosition Recupera il valore numerico della posizione corrente all'interno del contenuto del dispositivo MCI.
ms.assetid: 6dc5d3bd-8515-4514-a2a5-c1bee07f7acf
keywords:
- MCIWNDM_GETPOSITION messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_GETPOSITION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e7468b0e3698a72d3dce82bbd1591d59940d9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873421"
---
# <a name="mciwndm_getposition-message"></a>\_Messaggio GETPOSITION MCIWNDM

Il messaggio **MCIWNDM \_ GetPosition** Recupera il valore numerico della posizione corrente all'interno del contenuto del dispositivo MCI. Questa macro fornisce anche la posizione corrente in formato stringa in un buffer definito dall'applicazione. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) o [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .


```C++
MCIWNDM_GETPOSITION 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPTSTR) lp; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*Len*
</dt> <dd>

Dimensione, in byte, del buffer. Se la stringa con terminazione null è più lunga del buffer, viene troncata. Usare zero per impedire il recupero della posizione sotto forma di stringa.

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*LP*
</dt> <dd>

Puntatore a un buffer definito dall'applicazione utilizzato per restituire la posizione. Usare zero per impedire il recupero della posizione sotto forma di stringa. Se il dispositivo supporta le tracce, le informazioni sulla posizione della stringa vengono restituite nel formato TT: MM: SS: FF, dove TT corrisponde a Tracks, MM e SS corrispondono a minuti e secondi e FF corrisponde ai frame.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un intero corrispondente alla posizione corrente. Le unità per il valore di posizione dipendono dal formato dell'ora corrente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition)
</dt> <dt>

[**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring)
</dt> </dl>

 

 





