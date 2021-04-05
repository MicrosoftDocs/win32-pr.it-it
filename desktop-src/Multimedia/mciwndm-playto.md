---
title: Messaggio di MCIWNDM_PLAYTO (VFW. h)
description: Il \_ messaggio MCIWNDM PlayToSpazio riproduce il contenuto di un dispositivo MCI dalla posizione corrente fino al percorso finale specificato oppure fino a quando un altro comando non interrompe la riproduzione.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYTO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf0104204dc0306615ead91be036459cdf3c11d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120938"
---
# <a name="mciwndm_playto-message"></a>\_Messaggio MCIWNDM PlayToSpazio

Il messaggio **MCIWNDM \_ PlayToSpazio** riproduce il contenuto di un dispositivo MCI dalla posizione corrente fino al percorso finale specificato oppure fino a quando un altro comando non interrompe la riproduzione. Se il percorso finale specificato si trova oltre la fine del contenuto, la riproduzione si interrompe alla fine del contenuto. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) .


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prestare*
</dt> <dd>

Posizione finale. Le unità per la posizione finale dipendono dal formato dell'ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Questa macro viene definita mediante le macro [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) , che a loro volta utilizzano il comando [MCI \_ Seek](mci-seek.md) e il messaggio **MCIWNDM \_ PlayToSpazio** .

È anche possibile specificare una posizione iniziale e finale per la riproduzione usando la macro [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_ricerca MCI](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





