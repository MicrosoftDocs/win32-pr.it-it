---
description: Indica che la riproduzione DVD è stata arrestata. Questo evento viene inviato quando un titolo o un capitolo viene completato e il navigatore DVD non trova altre istruzioni di branching per la riproduzione successiva. L'evento non viene inviato quando l'applicazione interrompe la riproduzione.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 2304d83aea532b764777b683c57c3bdd4d5df79a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326643"
---
# <a name="ec_dvd_playback_stopped"></a>\_riproduzione DVD \_ EC \_ arrestata

Indica che la riproduzione DVD è stata arrestata. Questo evento viene inviato quando un titolo o un capitolo viene completato e il [navigatore DVD](dvd-navigator-filter.md) non trova altre istruzioni di branching per la riproduzione successiva. L'evento non viene inviato quando l'applicazione interrompe la riproduzione.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Membro dell'enumerazione del [**DVD \_ PB \_ arrestato**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , che indica perché la riproduzione è stata arrestata.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

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

 

 




