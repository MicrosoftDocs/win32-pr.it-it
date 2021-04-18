---
description: Segnala l'inizio di qualsiasi ancora (PGC, Cell o VOBU).
ms.assetid: cf2b08c9-22fa-4559-9289-787eaec46c6c
title: EC_DVD_STILL_ON (Dvdevcode. h)
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
ms.openlocfilehash: 0e2f9fcfecc44ee6d0769e00805c0aee512b2e7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325652"
---
# <a name="ec_dvd_still_on"></a>\_DVD EC \_ ancora \_ acceso

Segnala l'inizio di qualsiasi ancora (PGC, Cell o VOBU).

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore booleano (**bool**) che indica se i pulsanti sono disponibili. Zero (0) indica che i pulsanti sono disponibili, quindi il metodo [**IDVDControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff) non funzionerà. Uno (1) indica che non è disponibile alcun pulsante, pertanto **IDVDControl2:: StillOff** funzionerà.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valore **DWORD** che indica il numero di secondi per cui durerà ancora. 0xFFFFFFFF indica ancora un infinito, ovvero attendere fino a quando l'utente preme un pulsante o fino a quando l'applicazione non chiama [**IDVDControl2:: StillOff**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-stilloff).

</dd> </dl>

## <a name="remarks"></a>Commenti

Tutte le combinazioni di pulsanti sono comunque possibili (i pulsanti accesi rimangono accesi, i pulsanti su con ancora disattivato, il pulsante disattivato con ancora acceso, il pulsante disattivato con ancora disattivato).

Questo evento viene generato in tutti i domini.

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

 

 




