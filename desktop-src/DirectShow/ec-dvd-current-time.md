---
description: Segnala l'inizio di ogni unità VOBU (video Object Unit), un segmento video di lunghezza compresa tra 0,4 e 1,0 secondi.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327440"
---
# <a name="ec_dvd_current_time"></a>\_ \_ ora corrente DVD \_ EC

Segnala l'inizio di ogni unità VOBU (video Object Unit), un segmento video di lunghezza compresa tra 0,4 e 1,0 secondi.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore **DWORD** che indica il codice temporale di riproduzione corrente in un formato binario codificato (BCD) di ore, minuti, secondi, frame (HH: mm: SS: FF). Membro della struttura [**del \_ timecode del DVD**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore booleano (**bool**) che indica il timecode. Zero (0) indica 25 fotogrammi al secondo, mentre 1 indica 30 fotogrammi al secondo (non eliminati). Il valore 2 indica che non è possibile determinare il tempo di riproduzione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Solo i film lineari semplici segnalano questo evento.

Questo evento viene generato nel dominio del titolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




