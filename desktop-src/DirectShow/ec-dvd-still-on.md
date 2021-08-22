---
description: Segnala l'inizio di qualsiasi ancora (PGC, Cella o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_ON
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 801db7f1e14002aa6333b18349e259e40928a0cd45958c0e1aa618d1d1143be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303331"
---
# <a name="ec_dvd_still_on"></a>EC \_ DVD \_ STILL \_ ON

Segnala l'inizio di qualsiasi ancora (PGC, Cella o VOBU).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore booleano (**BOOL**) che indica se i pulsanti sono disponibili. Zero (0) indica che i pulsanti sono disponibili in modo che il [**metodo IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) non funzioni. Uno (1) indica che non sono disponibili pulsanti, quindi **IDvdControl2::StillOff** funzionerà.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valore DWORD** che indica il numero di secondi di durata dell'oggetto . 0xFFFFFFFF indica un valore infinito, ovvero attendere fino a quando l'utente non preme un pulsante o fino a quando l'applicazione non chiama [**IDvdControl2::StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le combinazioni di pulsanti e sono ancora possibili (pulsanti su con ancora on, pulsanti con ancora spento, pulsante disattivato con ancora on, pulsante off con ancora disattivato).

Questo evento viene generato in tutti i domini.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode.h (includere Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




