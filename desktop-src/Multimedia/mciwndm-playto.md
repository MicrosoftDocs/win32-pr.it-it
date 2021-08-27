---
title: MCIWNDM_PLAYTO messaggio (Vfw.h)
description: Il messaggio MCIWNDM PLAYTO riproduce il contenuto di un dispositivo MCI dalla posizione corrente alla posizione finale specificata o fino a quando un altro comando non \_ interrompe la riproduzione.
ms.assetid: ed940ee7-7b96-47da-99d3-6697f8a2e3d5
keywords:
- MCIWNDM_PLAYTO messaggio Windows Multimediali
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
ms.openlocfilehash: 61004706c8dfacb05ad47c6ddf261ac813d58f5076dfdd4e134896b3f8c646e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037941"
---
# <a name="mciwndm_playto-message"></a>Messaggio PLAYTO MCIWNDM \_

Il **messaggio \_ PLAYTO MCIWNDM** riproduce il contenuto di un dispositivo MCI dalla posizione corrente alla posizione finale specificata o fino a quando un altro comando non interrompe la riproduzione. Se la posizione finale specificata è oltre la fine del contenuto, la riproduzione si interrompe alla fine del contenuto. È possibile inviare questo messaggio in modo esplicito o tramite la macro [**MCIWndPlayTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)


```C++
MCIWNDM_PLAYTO 
wParam = 0; 
lParam = (LPARAM) (LONG) lEnd; 
```



## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lEnd"></span><span id="lend"></span><span id="LEND"></span>*Prestare*
</dt> <dd>

Posizione finale. Le unità per la posizione finale dipendono dal formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Questa macro viene definita usando le macro [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) e [**MCIWndPlayTo,**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) che a loro volta usano il comando [MCI \_ SEEK](mci-seek.md) e il **messaggio MCIWNDM \_ PLAYTO.**

È anche possibile specificare una posizione iniziale e finale per la riproduzione usando la macro [**MCIWndPlayFromTo.**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                       |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI \_ SEEK](mci-seek.md)
</dt> <dt>

[**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)
</dt> <dt>

[**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)
</dt> <dt>

[**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek)
</dt> </dl>

 

 





